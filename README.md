Spring Boot 2 and Angular 10 WebShop
---------------------------------------------
[![Build Status](https://github.com/DanielMichalski/spring-boot-2-angular-10-webshop/workflows/Java%20CI%20with%20Maven/badge.svg)](https://github.com/DanielMichalski/spring-boot-2-angular-10-webshop/actions?query=workflow%3A%22Java+CI+with+Maven%22)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project aims to present how to create a Spring Boot 2 + Angular 10 Web application.

Core libraries
---------------------------------------------
- Spring Boot 2
- JPA (Hibernate)
- Liquibase
- Spring Data Repositories
- Angular 10
- Angular Material 10
- Angular Flex Layout 10
- Docker

Requirements
---------------------------------------------
- [Java JDK 8+](https://www.oracle.com/pl/java/technologies/javase-downloads.html)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) 
- [Node.js](https://nodejs.org/en/) 

How to run application in development mode
---------------------------------------------
#### On Windows
##### Backend
```bash
## Run PostgreSQL database on Docker
cd webshop-backend/.docker/dependencies
start.sh

## Build backend from base directory using Maven Wrapper
cd ../../..
mvnw.cmd clean install -pl webshop-backend

## Run backend using Maven Wrapper or simly run Application class
mvnw.cmd spring-boot:run -pl webshop-backend
```
##### Frontend
```bash
## Run Frontend Angular application using npm
cd webshop-frontend
npm i
npm run start
```

#### On MacOS / Linux
##### Backend
```bash
## Run PostgreSQL database on Docker
cd webshop-backend/.docker/dependencies
./start.sh

## Build backend from base directory using Maven Wrapper
cd ../../..
./mvnw clean install -pl webshop-backend

## Run backend using Maven Wrapper or simly run Application class
./mvnw spring-boot:run -pl webshop-backend
```

##### Frontend
```bash
## Run Frontend Angular application using npm
cd webshop-frontend
npm i
npm run start
```

How to run application using Docker Compose
---------------------------------------------
#### On Windows
```bash
## Run Backend and Frontend using Docker Compose
cd .docker
start.sh
```

#### On MacOS / Linux
```bash
## Run Backend and Frontend using Docker Compose
cd .docker
./start.sh
```

Application access
---------------------------------------------
Component             | URL                                      
---                   | ---                                      
Frontend              | http://localhost:4444                    
Backend               | http://localhost:8888                    
OpenAPI Documentation | http://localhost:8888/api/swagger-ui.html    
OpenAPI Spec          | http://localhost:8888/api/v3/api-docs        

Database access
---------------------------------------------
| URL                                          	| Username         	| Password 	|
|----------------------------------------------	|------------------	|----------	|
| jdbc:postgresql://localhost:5555/webshop 	    | webshop_user   	| secret   	|
