# React

How to take Udemy Screen shot
-------------------------------
1)Open Google Chrome browser.
2)Click on the three vertical dots in the top-right corner to open the Chrome menu.
3)Scroll down and click on "Settings."
4)In the Settings menu, type "acceleration" in the search bar located at the top.
5)You will see an option labeled "Use hardware acceleration when available."
6)Disable this option by clicking on the toggle button next to it.
7)Once disabled, relaunch Google Chrome.


<img width="839" alt="image" src="https://github.com/user-attachments/assets/6cbbfa4e-9c34-4461-92ea-3a1494a8522b" />

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
