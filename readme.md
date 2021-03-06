#  Employee Tracker (With total budget)

A CLI application for managing a company's employees using node, inquirer, and MySQL.

## Table of Contents

1. [About](#about)
1. [Business Context](#business-context)
1. [Minimum Requirements](#minimum-requirements)
1. [Bonus](#bonus)
1. [Development Strategy](#development-strategy)
1. [Built With](#built-with)
1. [Demo](#demo)
1. [Getting Started](#getting-started)
1. [Submission](#submission)

## About

Developers are often tasked with creating interfaces that make it easy for non-developers to view and interact with information stored in databases. Often these interfaces are known as **C**ontent **M**anagement **S**ystems. This Node.js CLI application is developed to be a solution for managing a company's employees using node, inquirer, and MySQL.

## Business Context

Following the common templates for user stories, this challenge can be framed as follows for various stakeholders:

As a Business Owner, Manager and/or HR Personnel:

```
I want to be able to view and manage the departments, roles, and employees in my company

So that I can organize and plan my business.
```

```
I want to tbe able to:

  Add departments, roles, employees

  View departments, roles, employees

  Update employee roles

and also:

  Update employee managers

  View employees by manager

  Delete departments, roles, and employees

  View the total utilized budget of a department -- ie the combined salaries of all employees in that department
```

## Minimum Requirements

- Functional application.

- GitHub repository with a unique name and a README describing the project.

- The command-line application should allow users to:

  - Add departments, roles, employees

  - View departments, roles, employees

  - Update employee roles

## Bonus

- The command-line application should allow users to:

  - Update employee managers

  - View employees by manager

  - Delete departments, roles, and employees

  - View the total utilized budget of a department -- ie the combined salaries of all employees in that department

## Development Strategy

1. Design the following database schema containing three tables:

- **department**:

  - **id** - INT PRIMARY KEY
  - **name** - VARCHAR(30) to hold department name

- **role**:

  - **id** - INT PRIMARY KEY
  - **title** - VARCHAR(30) to hold role title
  - **salary** - DECIMAL to hold role salary
  - **department_id** - INT to hold reference to department role belongs to

- **employee**:

  - **id** - INT PRIMARY KEY
  - **first_name** - VARCHAR(30) to hold employee first name
  - **last_name** - VARCHAR(30) to hold employee last name
  - **role_id** - INT to hold reference to role employee has
  - **manager_id** - INT to hold reference to another employee that manager of the current employee. This field may be null if the employee has no manager

2. Include a `seed.js` file to pre-populate database.

3. Use the [MySQL](https://www.npmjs.com/package/mysql) NPM package to connect to your MySQL database and perform queries.

4. Use [InquirerJs](https://www.npmjs.com/package/inquirer/v/0.2.3) NPM package to interact with the user via the command-line.

5. Use [console.table](https://www.npmjs.com/package/console.table) to print MySQL rows to the console. There is a built-in version of `console.table`, but the NPM package formats the data a little better.

6. Final application should look like the example below:


## Getting Started



```
This application utilised the advanges of node environment and inquirer helped to make the choices working. Created a database called employee_db and inserted values to it by making seed.sql. Here the "CRUD"functionality helped me to meet the requirement as well as the bonus activity too. Added dependancies include mysql, inquirer, console.table, promise.mysql to package.json. I switch cases, promises etc. 
```

The application can be with the following command:

```
using 👌
npm init
npm i (all the dependencies)
node filename
```



## Built With

- [Node.js](https://nodejs.org/en/docs/) -- JavaScript runtime
- [Inquirer](https://www.npmjs.com/package/inquirer) -- Interactive CLI

## Demo
![](animated.gif)

![](/2020-07-27%20(1).png)

## The recorded in the following link

https://drive.google.com/file/d/19QIP65-EB-_eHLzY022t3MW8JmdZv3O-/view

## Submission

You are required to submit the following:

- An animated GIF demonstrating the app functionality
https://drive.google.com/file/d/19QIP65-EB-_eHLzY022t3MW8JmdZv3O-/view

- The URL of the GitHub repository
https://github.com/Dhanya-krishnan2/Budgettracker--with-Employee/blob/master/readme.md
