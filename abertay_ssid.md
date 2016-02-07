
# Week 5

1 . Assessment walkthrough.
<br> 2 . [Countermeasuers Presentation](https://drive.google.com/file/d/0B-CFaefA1v4RTFg2eXRmWjVPN28/view?usp=docslist_api)
<br> 3 . [PDP Presentation](https://drive.google.com/file/d/0B-CFaefA1v4RWWozWjlwSWU2QTQ/view?usp=docslist_api)

## Exercises
1 . Complete the following [Lab Exercises](https://docs.google.com/document/d/1V3dd-qx6fLKC1HlnkGhOMnUpibRhKz7c6fu05GPA8ks/edit?usp=docslist_api).

# Week 4

1 . [Security Presentation](https://drive.google.com/file/d/0B-CFaefA1v4RTFg2eXRmWjVPN28/view?usp=docslist_api)

## Exercises

1 . Send me an email with the following [message](https://docs.google.com/document/d/1B-ztaNF94ToirsNu_SIeT7LGtaPnOG0EWJOU5xzPkbU/edit?usp=docslist_api).
<br> 2 . Use the instructions in Week 3 Exercises to copy and run the following PHP project: 
```
/home/share/dvwa
```
You will need to change the database name in the following file (once you have copied it):
````
DWA-1.9/config/config.inc.php
````
Use Chrome rather than the web browser in Eclipse (you will need JavaScript). Run the following command from the terminal:
````
google-chrome
````
<br> 3 . [SQL Injection Exercises](https://docs.google.com/document/d/19xmxzBD-6jzDeqOUDhtQ7Yt3bws0-YAZL3DfN2xZv9I/edit?usp=docslist_api)
<br> 4 . [XSS Exercises](https://docs.google.com/document/d/1C3DhOaoUeo-tUU4v3I7xR39xtYOKZmRIe2P00hc4Rew/edit?usp=docslist_api)
<br> 5 . Create a file called ````exploits.txt```` in your home drive on Ygritte and document other SQL Injection and XSS exploits that you can identify. 



# Week 3


## Exercises

1 . Copy the example eclipse PHP project to your worksapce using the following commands:

```
cd workspace
mkdir example
cp -r /home/share/ssid/. example
```
<br> 2 . Run a PHP server in the example directory:

```
cd example/
php -S localhost:8???
```
<br> 3 . Point the browser in eclipse to the following PHP file:
```
http://localhost:8???/login.php 
```
<br> 4 . Import the example project into eclipse.
<br> 5 . Using your knowledge of PHP and MySQL identify improvements to the code.
<br> 6 . Create a "gardeners" project in eclipse on Ygritte and start to implement the [Gardeners Portal](https://docs.google.com/document/d/19rUg3pTqK1nwnDRaE1AgclOs9Y9GMu2bJpdSQIOg_Vg/edit?usp=docslist_api). For ease of identification (for me!) call the first page of your site "index.html" and include in it links to the login page and public advertisements page. You are required to add CSS to your site.   

# Week 2

1 . [Book: Learning PHP, MySQL and JavaScript](http://www.amazon.co.uk/Learning-MySQL-JavaScript-Robin-Nixon/dp/0596157134)
<br> 2 . [SQL Create Table](http://www.w3schools.com/sql/sql_create_table.asp)
<br> 3 . [SQL Insert](http://www.w3schools.com/sql/sql_insert.asp)
<br> 4 . [SQL Join](http://www.w3schools.com/sql/sql_join_inner.asp)
<br> 5 . [PHP Sessions](http://www.w3schools.com/php/php_sessions.asp)

## Exercises

1 . Complete Week 1 exercises using [week1exercises.php](https://gist.github.com/GedMullen/fa29fe3338a7582dbf77) and [surname.php](https://gist.github.com/GedMullen/140f12537a67b8e657fa). Make sure you do this in your "week1exercises" project on Ygritte. 
<br> 2 . Create a separate a table "users" in your own database using [users.sql](https://gist.github.com/GedMullen/11312ef28b66bf70eedf). Execute the SQL script using the following command:
```
mysql -t -u student < users.sql
```
<br> 3 . Create a "working_example" project on Ygritte and create a form that allows the user to enter in a user id and password. The page should then check the user id and password against the data that is stored in the users table and indicate to the user if the login attempt was successful.
<br> 4 . Add functionality to your site by allowing the user to register. This will involve capturing the name of the user and user password and inserting the information into the users table.
<br> 5 . Create a profile page that allows the user to see the information that they entered when they registered.
<br> 6 . Allow the users to change their profile information.
<br> 7 . Look at [PHP Sessions](http://www.w3schools.com/php/php_sessions.asp). Add session management to your site. 
<!--
users.sql
https://gist.github.com/GedMullen/11312ef28b66bf70eedf

week1exercises.php
https://gist.github.com/GedMullen/fa29fe3338a7582dbf77

surname.php
https://gist.github.com/GedMullen/140f12537a67b8e657fa
-->
# Week 1

<br> 1 . [Dynamically Generated Content Review](https://docs.google.com/presentation/d/1bWMd9ypXXUJGt-jDpjpRSfh6_2zHMRKjjBcldO0OMeM/pub?start=false&loop=false&delayms=60000&slide=id.p3)
<br> 2 . [X2GO Client](https://drive.google.com/file/d/0B-CFaefA1v4RVWN5eFRlSV9YbVU/view?usp=sharing)
<br> 3 . [Connecting To Ygritte](https://docs.google.com/document/d/1wV6XGhOPlpwCMElZAqlH83YYXo_PpdNNdVMN6Toh3mw/pub)
<br> 4 . [mysqlexample.php](https://gist.github.com/GedMullen/f58ea879c98ada9ca055)
<br> 5 . If you are unfamiliar with the Linux command line then this will help - [Learning the Command Line on Codecademy](https://www.codecademy.com/learn/learn-the-command-line)
<br> 6 . See [w3schools](http://www.w3schools.com) to brush up on your PHP, SQL, HTML and CSS. 
<br> 7 . ERD of the database used in exercises - [MySQL Example Employee Database](https://dev.mysql.com/doc/employee/en/sakila-structure.html)
<br> 8 . You can start a PHP server on Ygritte by issuing the following command (replace ??? with your unique port number):
```
php -S localhost:8??? 
```
<br> 9 . You can run an SQL script Ygritte by issuing the following command:
```
mysql -t -u student < myscript.sql
```

## Exercises

The following exercises are designed to help you refamiliarise yourself with PHP, MySQL, HTML and CSS. You should use [mysqlexample.php](https://gist.github.com/GedMullen/f58ea879c98ada9ca055) and the tutorials above as a starting point.

1 . Create an eclipse project on Ygritte called "week1exercises" and include the answers to the following exercises in this project. 
<br> 2 . Create a PHP file that generates a HTML table that details the top 10 salaries in the employees database (hint - use ORDER BY and LIMIT 10). You will need to join the EMPLOYEES and SALARIES tables.
<br> 3 . Add styling to the page generated by exercise 2.
<br> 4 . Create a form that allows the user to enter in a surname and submit it to the server. The server must then return the first 10 occurrences of the given surname in the employees database.
<br> 5 . Add more complexity to the exercises above if you have time.

