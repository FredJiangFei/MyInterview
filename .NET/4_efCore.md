# What is Entity Framework Core?
an ORM (Object-Relational Mapper) Framework for data access, which:
1. Enables .NET developers to work with a database using .NET objects.
2. Eliminates the need for most of the data-access code that typically needs to be written.

# Why do we need to use an ORM?
help operate Database


# EF Core Development Approaches:
1. Code-First Approach
2. Database-First Approach

# EF Core does not have the following features:
1. Spatial Type
2. Complex/value types
3. EDMX Model format
4. Lazy loading
5. Stored Procedures

# Reasons to use EF Core:
1. Simple to get started
2. It supports NoSQL Databases along with relational databases
3. It fits nicely in ASP.NET MVC Core setup
4. Integrates well with LINQ
5. Possible to use on Linux and Mac since it is based on .NET Core along with Windows.


# Entity states in EF Core
* Added: The entity is marked as added.
* Deleted: The entity is marked as deleted.
* Modified: The entity has been modified.
* Unchanged: The entity hasn't been modified
* Detached: The entity isn't tracked.

# How to add new table in database using EF Core Code First approach?
1. dotnet ef migrations add
2. dotnet ef database update
3. dotnet ef migrations remove

# other ORMs
* Dapper
* NHibernate
* Entity Framework 6.x

# DbContext and DbSet
DbSet: An entity set is represented by a DbSet class that can be used for creating, reading, updating, and deleting operations on it. Those DbSet type properties, which map to database tables and views, must be included in the context class (derived from DbContext).   

DbContext: It is considered an essential class in EF API that bridges the gap between an entity or domain class and the database. Communication with the database is its primary responsibility.

# virtual
All navigation properties must be marked as virtual
The virtual keyword allows EF to override the property and fetch the data when called. 

# 