# React

How to take Udemy Screen shot
-------------------------------
1)Open Google Chrome browser.
2)Click on the three vertical dots in the top-right corner to open the Chrome menu.
3)Scroll down and click on "Settings."
4)In the Settings menu, type "acceleration" in the search bar located at the top.
5)You will see an option labeled "Use hardware acceleration when available."
6)Disable this option by clicking on the toggle button next to it.
7)Once disabled, relaunch Google Chrome



<img width="839" alt="image" src="https://github.com/user-attachments/assets/6cbbfa4e-9c34-4461-92ea-3a1494a8522b" />


Create folder ReactCourse
------------------------
Open command prompt

Create a solution  (ReactCourse.sln)
-------------------
dotnet new sln 

create webapi with folder name as API and solution as app with controllers
-----------------------------------
dotnet new webapi -n API -controllers

Create a folder with Class as Domain , Application & Persistence
--------------------------------------
dotnet new classlib -n Domain
dotnet new classlib -n Application
dotnet new classlib -n Persistence


Create a solutions for API , Application & Persistence & Domain
-------------------------------------------------------
dotnet sln add API    
dotnet sln add Application    
dotnet sln add Persistence    
dotnet sln add Domain 

<img width="886" alt="image" src="https://github.com/user-attachments/assets/3f1140aa-13b1-4e13-a7cb-0a0b7dd9337f" />

Adding a reference from Application to API 
-------------------------------------------
API> dotnet add reference ../Application/Application.csproj

To run the application
--------------------
API> dotnet run

dotnet ef install for migration
-----------------
dotnet tool install --global dotnet-ef --version 9.0.1

connection string in appsetting.json
---------------
 "ConnectionStrings": {
    "DefaultConnection":"data source=React.db"
  }

Program.cs
-------------
builder.Services.AddDbContext<AppDbContext>(opt=>opt.UseSqlite(builder.Configuration.GetConnectionString("DefaultConnection")));


----------------------------------------------------------------------------------------------------------

List of solution 
---------------
> dotnet sln list
>
> install ef
> ---------
dotnet tool install --global dotnet-ef

Main solution is API bcz its having program.cs class so here we need to create a table that we are consuming model from persistance solution to API solution for create a migration we will use command that is 
----------------------

dotnet ef migrations add init -s API -p Persistence

To create a database
--------------------
dotnet ef database
