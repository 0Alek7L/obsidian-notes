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