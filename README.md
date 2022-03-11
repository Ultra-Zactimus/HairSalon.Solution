# _Eau Claire's Salon: My 10th Code Review at Epicodus_

#### By Zachary Green

#### _This project is a demonstation of using mySQL Server/Workbench to create a database to store and pull data into a web application for a Salon business owner. The program uses Classes and Microsoft Entity to create Objects and then push/pull them to and from a database. This project was possible under the guidance of Epicodus https://www.epicodus.com/_

## Technologies Used

* `C#`
* `Microsoft Entity`
* `ASP.NET Core MVC`
* `Bootstrap`
* `CSS`

## Description

_Hair Salon owner Eau Claire needs a website that will allow them to keep track of their Stylists and the Clients each Stylist is in charge of. They need to be able to add and remove new Stylists and add Clients to specific Stylists. This application is a simulation into adding and removing these feature._

## Setup/Installation Requirements

<em>Requirements for Running the Project in a Browser</em>

* Visit https://github.com/Ultra-Zactimus/
* Clone this repository to your desktop.
* Navigate to the top level directory in your terminal.
* Run "$ `touch appsettings.json`"
* Run "$ `code .`" to open the project in VS Code. If you do not have VS Code please visit their website: https://code.visualstudio.com/
* Add in this code to the `appsettings.json` file inside `VS Code`:
  `{
    "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=to_do_list;uid=root;pwd=[YOUR-PASSWORD-HERE];"
    }
  }`
* Change the password to be the same password as your mySQL Server Password. If you do not have mySQL server please visit their website: https://www.mysql.com/

* Developer Note -- <em>You do not need the square brackets around your password, that is only to demonstate where your password needs to be. For further instructions please scroll down below for a more detailed setup in the SQL Setup section</em>

* Run "$ `dotnet add package Microsoft.EntityFrameworkCore -v 5.0.0`"
* Run "$ `dotnet add package Pomelo.EntityFrameworkCore.MySql -v 5.0.0-alpha.2`"
* Run "$ `dotnet restore`" to restore the bin and obj folders.
* Run "$ `dotnet build`" to build the project.
* Run "$ `dotnet run`" or "$ `dotnet watch run`" to launch a LocalHost. Click on `LocalHost:5000`. You may have to hold Ctrl or Command when clicking it to get it to open in your internet broswer.

* Developer Note -- <em>You do not need to type in `$` into the terminal, the terminal starts with `$` on GitBash and `%` on Bash.</em>

<em>MySQL Setup Instructions</em>

* 

## Known Bugs

* No known bugs at this time.

## License

MIT

Copyright © 2022 Zachary Green