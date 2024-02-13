# Spring Boot Thymeleaf example: CRUD Application (Tutorials website)

A project to perform crud operations on spring data jpa entitites using spring boot,thymeleaf in MVC structure. The project is a web application aimed at displaying tutorials allowing users to create delete update and read tutorials.

Database used - MySQL Database
Tables used - tutorials

Table schema -
`tutorials` (
   `id` int NOT NULL,
   `description` varchar(256) DEFAULT NULL,
   `level` int NOT NULL,
   `published` bit(1) DEFAULT NULL,
   `title` varchar(128) NOT NULL,
   PRIMARY KEY (`id`)
 )

Functionalities -
1)Create a new tutorial
2)Retrieve all the tutorials
3)Updating publishing status of a tutorial
4)Edit a tutorial in its own page
5)Delete a tutorial

Endpoints used -
1. Get ("/tutorials")
    displays all the tutorials from the server

2. Get ("/tutorials/new")
    renders a form to create a new tutorial

3. Post ("/tutorials/save")
    saves the tutorial created in /tutorials/new to the database

4. Get ("/tutorials/{id}")
    renders the prefilled form with tutorial of id {id} to be edited

5. Get ("/tutorials/delete/{id}")
    deletes the specific tutorial with id {id}

6. Get ("/tutorials/{id}/published/{status}")
    changes the published status of the tutorial.

Dependencies used - 
1)spring-boot-starter-data-jpa
2)spring-boot-starter-thymeleaf
3)spring-boot-starter-web
4)mysql-connector-j
5)bootstrap
6)jquery
7)webjars-locator-core
8)spring-boot-devtools
9)spring-boot-starter-test