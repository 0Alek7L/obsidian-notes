#EntityFramework

==SCHEME:==
```
----------------------.NET Application------------------------
-         |              |                  |               |
-         |              |                  |               |
 -----DataSets------LINQ to SQL------Entity Framework-----  |
-         |              |                  |               |
-         |              |                  |               |
--------------------------ADO.NET-----------------------------
- SQL Server------ODBC------OLE DB------Custom Providers - - -
-							  |
-							  | 
---SQL-----NoSQL-----XML-----REST-----SharePoint-----Excel-..-
```

==ORM (Object-Relational Mapping==
**ORM data access model** (Entity Framework Core)
	Maps **database tables** to **classes** and **objects**
	Objects can be **automatically persisted** in the database
	Can operate in both connected and disconnected models
**``PROGRAMING LANGUAGE <--> ORM FRAMEWORK <--> DATABASE``**

==ПРИНЦИП ЗА ИЗВЛИЧАНЕ НА ДАННИ==
**RETREIVING DATA IN CONNECTED MODEL:
	-Open a connection (SqlConnection)
	-Execute command (SqlCommand)
	-Process the result set of the query by using a reader (SqlDataReader)
	-Close the reader         --|
	-Close the connection --| 
	-                                      |-OR JUST USE "using"**
```
SqlDataReader
-    |     /-------SqlParameter
 SqlCommand -----SqlParameter 
-    |     \------SqlParameter
SqlConnection
-    |
  Database
```

--**SqlConnection CLASS**--
SqlConnection con = new SqlConnection(
	@"Server=LAPTOP-FD7DC0N0\\MSSQLSERVER02;
	Database=SoftUni;
	TrustServerCertificate=True;
	Trusted_Connection=True;	
"); con.Open();

==SYNTAX==
```
using Microsoft.Data.SqlClient;

string connectionString = "Server=LAPTOP-FD7DC0N0\\MSSQLSERVER02;Database=SoftUni;TrustServerCertificate=True;Trusted_Connection=True;";
using (SqlConnection sqlConnection = new SqlConnection(connectionString))
{
    await sqlConnection.OpenAsync();

    string query = "SELECT FirstName, LastName, Salary FROM Employees WHERE Salary > @salaryParam"; //използва се параметър, който после е със стойност

    using (SqlCommand sqlCommand = new SqlCommand(query, sqlConnection))
    {
	    //ето тук му се задава стойност
        sqlCommand.Parameters.AddWithValue("@salaryParam",50000);
        SqlDataReader sqlDataReader = await sqlCommand.ExecuteReaderAsync();
        while(await sqlDataReader.ReadAsync())
        {
            string firstName = sqlDataReader["FirstName"].ToString();
            string lastName = sqlDataReader["LastName"].ToString();
            decimal salary = decimal.Parse(sqlDataReader["Salary"].ToString());

            Console.WriteLine($"{firstName} {lastName} - {salary}");
        }
    }
}


```

ВИНАГИ ИЗПОЛЗВАЙ ==await + async== => спомага работата на сървъра! (асинхронни методи)

==ExecuteScalar==() 
	Returns a single value - the value in the first column of the first row of the result set (as System.Object) 
==ExecuteReader==() 
	Returns a SqlDataReader 
	It is a cursor over the returned records (result set) 
	**CommandBehavior** – assigns some options 
==ExecuteNonQuery==() 
	Used for non-query SQL commands, e.g. INSERT, UPDATE, DELETE, CREATE 
	Returns the number of affected rows (int)