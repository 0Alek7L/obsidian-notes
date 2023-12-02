
==Scaffold-DbContext -Connection "Server=LAPTOP-FD7DC0N0\MSSQLSERVER02;	Database=SoftUni; TrustServerCertificate=True;  Integrated Security = true;	Trusted_Connection=True;" -Provider Microsoft.EntityFrameworkCore.SqlServer -OutputDir Data/Models==

==IQueryable<\T>== -> https://prnt.sc/qJ0MeBx-FGKD

==Fluent API==
One-to-zero-or-one => https://prnt.sc/lJlvAU6uHJgP
One-to-many =>
	https://prnt.sc/T2Y46O1wbvmq 
	1 - https://prnt.sc/dl7zQNZRXbZg
	2 - https://prnt.sc/OuC4BaNzNzB7
	3 - https://prnt.sc/32W890JYDx-S
Many-to-many =>
	https://prnt.sc/cs0Nax4T7-T1
	1 - 

==EXECUTING STORED PROCEDURES== => https://prnt.sc/SusyUFbsok6L
(ЕКСПЛИЦИТНО ПАРАМЕТИРИЗИРАНЕ)

attached object -> следи се от change tracker
dettached object -> не се следи от change tracker
reattaching deattached object -> https://prnt.sc/WIeh-tkXwUUY

**Когато данните се изкарват и не са нужни промени, те са detached!!**
**Когато данните трябва да се преправят, те са attached!!**

==Entity Framework Plus==
	updating and deleting ->https://prnt.sc/XDOe34oc0-wX

Ако искаме да променим employee когато е detached:
	var employee = await context.Employees
		.Where(e=>e.EmployeeId\==1)
		.AsNoTracking()
		.FirstOrDefaultAsync();
	var entry = context.Entry(employee);
	entry.State = EntityState.Modified;
	employee.FirstName = "Grigor";
	await context.SaveChanges();


==LOADING==
**Eager**
	
	Дърпа цялата информация, която ще е нужна наведнъж
**Lazy**

**Explicit**
	https://prnt.sc/E9wBGhkn1ZZt
	Всяко нещо се взима със специална заявка
	Използва се .Reference().Load() и .Collection().Load()