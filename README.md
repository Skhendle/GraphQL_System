[![Build Status](https://travis-ci.org/Skhendle/Blogger-Block.svg?branch=main)](https://travis-ci.org/Skhendle/Blogger-Block)
[![codecov](https://codecov.io/gh/Skhendle/Blogger-Block/branch/main/graph/badge.svg?token=rSx7WWHUb9)](https://codecov.io/gh/Skhendle/Blogger-Block)
<br>
# **Blogger-Block**
This is a learning webserver application for a user blogging platform. It will be built with fastApi, SQL-Alchemeny(SQLlite), Redis and graphene. It will have three layers. The storage layer that will store\cache all the platform data, service layer that will allow us to implement the system requirements\logic, and API layer that will allow external programs to commincate with the system.


## **Getting Started** <br>
```python
# Python version: 3.9.0
"MINGW64 - bash terminal"
# Run command in directory you will be working from.
$ : git clone https://github.com/Skhendle/Blogger-Block.git
$ : cd Blogger-Block

To create virtual environment.
$ Blogger-Block : python -m venv env

# To activate virtual environment
# Windows 
$ Blogger-Block : source ".\env\Scripts\activate"
# Ubuntu 
$ Blogger-Block : source ./env/bin/activate

# To install the requirements run
$ Blogger-Block : pip  install -r requirements.txt

# To update requirements.txt after installing new package
$ Blogger-Block\app : pip freeze > requirements.txt

# To run the application use the following command
$ Blogger-Block : uvicorn app.main:app --reload

# To run a service of the application use the following command
$ Blogger-Block : uvicorn app.'service name'.main:app --reload
# E.g
$ Blogger-Block : uvicorn app.b_register.main:app --reload

# To deactivate virtual enviroment
$ Blogger-Block : deactivate
```

## **Accessing API Documentation** <br>
- {server url}/docs
- {server url}/redoc

## </br> **API Routes Documentation Format**
* Describes how to setup a package that implements a system requirement  for the application. Specifies the file name, what the file contains and how it is used</br>

### **Package Layout | For Each System requirements**
<blockquote>

[x] __input.py__ - *Contains pyndatic classes, that are used as parameters for API functions and services class.*
</br>

[x] __route.py__ - *Contains the API function with the url describing its service path, states its Protocol( POST, GET, DELETE or UPDATE) and calls for the service to be executed*
</br>

[x] __service.py__ - *Where the logic for a system requirement is executed*
</br>

[x] __main.py__ - *Allows us to run a service independently independently*</br>
</blockquote>

## **Layered Package Architecture**
![Layed package description diagram](/images/Architecture.png)

<br>

## **Class Diagrams**
![Layed package description diagram](/images/ClassDiagram.png)
