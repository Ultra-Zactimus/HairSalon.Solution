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

<strong><em>Requirements for Running the Project in a Browser</em></strong>
#

Developer Note -- <em>You do not need to type in `$` into the terminal, the terminal starts with `$` on GitBash and `%` on Bash.</em>

* Visit https://github.com/Ultra-Zactimus/HairSalon.Solution
* Clone this repository to your desktop.
* Navigate to the top level directory in your terminal.
* Run "$ `touch appsettings.json`"
* Run "$ `code .`" to open the project in VS Code. If you do not have VS Code please visit their website: https://code.visualstudio.com/
* Add in this code to the `appsettings.json` file inside `VS Code`:
  `{
    "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=[YOUR_MYSQL_PROJECTNAME];uid=root;pwd=[YOUR-PASSWORD-HERE];"
    }
  }`

* Create a gitignore file. Run "$ `touch .gitignore`" on the top level of the project.
* Inside of `VS Code` type in `appsettings.json` into the gitignore file. This will keep your password safe.
* Change the password to be the same password as your mySQL Server Password. If you do not have mySQL server please visit their website: https://www.mysql.com/


Developer Note -- <em>You do not need the square brackets around your password, that is only to demonstate where your password needs to be. For further instructions please scroll down below for a more detailed setup in the SQL Setup section</em>

* Run "$ `dotnet add package Microsoft.EntityFrameworkCore -v 5.0.0`"
* Run "$ `dotnet add package Pomelo.EntityFrameworkCore.MySql -v 5.0.0-alpha.2`"
* Run "$ `dotnet add package Microsoft.EntityFrameworkCore.Proxies -v 5.0.0`"
* Run "$ `dotnet restore`" to restore the bin and obj folders.
* Next follow the steps below to create your database and password for the `appsettings.json` file.
#
<strong><em>Installation for MySQL</em></strong>
#

Developer Note -- <em>I have included images of the entire process needed to get this program set up in the `img` folder inside of `wwwroot` folder. If at any point you are not sure about where you should be clicking or adding things, please refer to those images.</em>

* Visit the website for MySQL Workbench and download it on your computer.
* When you reach the Configuration part of the installation select "<em>Use Legacy Password Encryption</em>", make sure to also set your password here to something you will remember.
* In the terminal Run "$ `echo 'export PATH="/usr/local/mysql/bin:$PATH"' >> ~/.bash_profile`"
* Run "$ `source ~/.bash_profile`" to ensure that the project is installed properly. If you see `mysql>` appear in the terminal then everything should be ready.
* Next Run "$ `mysql -u root -p`", you should be prompted to enter a password.
![Picture of My SQL Workbench Start up Page](/HairSalon/wwwroot/img/img01.png)
* Once you are in, open up MySQL Workbench click the MySQL Connections on the left hand side, you will be prompted to enter your password.
*You should now be within the main workspace of MySQL Workbench.
* In the upper left should be a list of icons, hover your mouse over them till you find the one that says `"Create a new schema in the connected server"` Click that button.
* The next page should look like this:
* Name your project and click apply and finish. This name will be used in the `appsettings.json` file in the section before the password.
* Next step, on the main menu click on this new database in the window to the left till you see list item called `Table`. right click on it and you should see an option to `Create Table`.
* You will be taken to the screen for creating the table that will represent the Class in the code.
* This is very important. Tables must match the class names plural in order for this program to work. So since the one class in this project is called `Client`, it would be `clients` as the Table name.
* Next in the middle section click on the left to add a new item to the table name this the same name as the class's perameter for Id, if you are creating the Client table item, it should be `ClientId`. In the next window select INT and then check the boxes for PK, NN, and AI. This is very important.
* Next you will create the another item in the table that will be for the ClientName set this to a `VarChar` and it must be (255), it defaults at (45).
* Lastly you will want one more item for that StylistId this one will need to also be an INT and you will need PK and NN checked. Once these are all done click Apply at the bottom right and finish.
* Next you will need to create another Table and name this one `stylists`. This table will just include the `StylistId` INT PK, NN, AI and `StylistName` VarChar(255). Once you are done click apply and finish.
* You should now be ready to run the program as intended. If you would like to see each item being added to the database click on the Table tab in Workbench until you see `clients` and `stylists`. If you look to the right of it you should see 2 icons, the one to the farthest right will bring up the table with all the items inside of the table with their ID.
* Run "$ `dotnet build`" to build the project.
* Run "$ `dotnet watch run`" to launch a LocalHost. Click on `LocalHost:5000`. You may have to hold Ctrl or Command when clicking it to get it to open in your internet broswer.

## Known Bugs

* No known bugs at this time.

## License

MIT

Copyright © 2022 Zachary Green