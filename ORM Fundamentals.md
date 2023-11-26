==ORM - Object Relational Mapper - Automatically generates SQL==

Code-first model - create the classes and the ORM generates the SQL
SQL-first model - create the tables in SQL and the ORM generates the classes

==DbSet<\T> Class==
	Generic collection with additional features 
	Each **DbSet<\T>** corresponds to a single database table
	Inherits from **Icollection<\T>**
		**foreach**-able
		Supports LINQ operations
	Usually several **DbSet**s are part of a **DbContext**

==DbSet Features==
	Each DbSet tracks its own entities through a change tracker 
	Has every other feature of an ICollection 
		Accessing the elements (LINQ) ▪ Adding/Updating elements
		Removing an entity/a range of entities
		Checking for element existence
		Accessing the count of elements

==!!ВАЖНО!!==
**КОГАТО ИМА РЕФЕРЕНЦИЯ КЪМ ДРУГА ТАБЛИЦА СЕ ПИШЕ АТРИБУТ НАД PROPERTY-ТО В КЛАСА ЗА ТАБЛИЦАТА - \[ForeignKey(nameOf(Има на клас за друга таблица))]**

Как изглежда DbContext => https://prnt.sc/3iTwrXdbTUAX