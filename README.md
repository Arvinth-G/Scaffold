# Scaffold
Adding entities to .net core project using scaffold command

# Nuget packages to configer scaffold:
Microsoft.EntityFrameworkCore.Tools
Microsoft.EntityFrameworkCore.Tools.DotNet
Microsoft.VisualStudio.Web.CodeGeneration.Design

# Scaffold Syntax
Scaffold-DbContext "Server=<DATABASE NAME>;Database=<TABLE NAME>;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir <FOLDER NAME> -context <DB CONTEXT NAME> -force
  
# Example - Scaffolding entire database
Scaffold-DbContext "Server=TestDatabase;Database=TestTable;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Entities -context TestDBContext -force

# Example - Scaffolding specific table in a database
Scaffold-DbContext "Server=TestDatabase;Database=TestTable;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Entities -context TestDBContext -t AspNetUserClaims, AspNetUserLogins
