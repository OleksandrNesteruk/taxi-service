# Simple taxi service <img src="src/images/im1.png" align="centre" height="70"/> <img src="src/images/im1.png" align="left" height="70"/>


Taxi service is a simple Web-application that implements authentication, registration, and database operations. 
Application functionality:
- Registration and Authentication like a driver.
- Create/update/remove a manufacturer.
- Create/update/remove a car.
- Crete/update/remove a driver.
- Display all cars.
- Display all manufacturers.
- Display all drivers.
- Display all current assign cars on the driver
- Assigning a driver from the database to a car from the database.
---

## This app deployed on heroku and connected to a remote database.
- You can read a boring description or try the service yourself by clicking on the icon > <a href="https://my-custom-taxi-service.herokuapp.com/login"><img src="src/images/im2.png" align="centre" height="40"/></a>
---

## This application has a three-tier architecture.
<img src="src/images/im4.png" align="centre" height="200"/>

- Dao - work with database by CRUD operation.
- Service - business logic, working with data before reading or writing to the database.
- Controllers - Presentation layer, work with commands from user and sending incoming data to service.
---

## Using technologies:
- Java 11
- Tomcat - version 9.0.50
- MySQL
- JDBC
- Servlet
- JSTL
- JSP
- HTML
- CSS
---
## How to run "taxi-service" localy

First of all, you need to install MySql and Tomcat version 9.
1. Connect Tomcat to yours IDE.
2. Clone this repository.
3. Use [init.db.sql](src/main/resources/init_db.sql) in MySQL to create tables and columns.
4. Configure **URL**, **USERNAME**, **PASSWORD**, **JDBC_DRIVER** in [ConnectionUtil](src/main/java/taxi/util/ConnectionUtil.java).
5. In file [log4j.xml](src/main/resources/log4j.xml) you need at line ```<File name="LogToFile" fileName="/logs/app.log">```<br>
   change ```/logs/app.log``` on absolute path to file ```.log```.
6. Configure ```Application context``` in Tomcat.
    * Edit configurations...
    * Deployment
    * Application context:
    * Change on ```/```
7. Run "taxi-service!

