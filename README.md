# Task 1. Java backend and REST API example.
## Overview

This Spring Boot Java application offers a REST API to manage and execute "Task" objects stored in MongoDB

## Features
- Create, Retrieve, Update and Delete Tasks
- Execute tasks using system commands
- Store task data in MongoDB

## Prerequisites
- MongoDB installed and running
- Java 17+ installed
- Maven for building the project
- Postman (optional, for testing API requests)

# Setup & Usage
## Start MongoDB Service
- Open CMD as Administrator
- Run **net start MongoDB**

## Run the SpringBoot Application
- Navigate to your Project folder
- Run **mvn spring-boot:run**

## Open MongoDB Shell
- Use Command as **mongosh**
- Switch to the database **taskdb**

## Create a task using Postman
- Create a new collection in postman and set the method as *PUT*
- Base URL is **http://localhost:8080/tasks**
- Enter some data in body by navigating to *raw* and insert the data given below
- {
  "id": "123",
  "name": "Print Hello",
  "owner": "John Smith",
  "command": "echo Hello World!"
  }
- Click Send

## Verify Data in MongoDB
- Check stored data by using the command *db.tasks.find().pretty()*

## Performing CRUD Operations using CMD
- To get all tasks use **curl -X GET http://localhost:8080/tasks**
- To get task by ID use **curl -X GET http://localhost:8080/tasks/123**
- To execute task use **curl -X PUT http://localhost:8080/tasks/123/execute**
- To delete task use **curl -X DELETE http://localhost:8080/tasks/123**

### Note
- Ensure MongoDB is running before starting the application
- Use Postman for testing API endpoints
