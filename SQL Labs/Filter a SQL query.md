machines, and the departments they’re in. Your team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine.

You are responsible for finding the required information by querying a database. You’ll add filters to your queries to locate the information more quickly.

Here’s how you’ll do this task: First, you’ll list all organization machines and their operating systems. Second, you’ll list all machines with the operating system OS 2. Third, you’ll list all the employees in the Finance and Sales departments. Fourth, you’ll obtain information about machines.

You’re ready to add filters to SQL queries.


## Task 1. List all organization machines

In this task, you need to get a list of all organization machines and their operating systems. The data is contained in the machines table. You’ll need to use the SELECT keyword to return specific columns.

Run a SQL query to retrieve only the device_id and operating_system columns from the machines table

![Screenshot 2024-08-15 190952](https://github.com/user-attachments/assets/85ba05f4-aea8-4eeb-a54e-5ca1a77d875a)

## How many rows were returned from the machines table? (You can view the number of rows at the bottom of the output.)

##### Answer: 200

## Task 2. Retrieve a list of the machines with OS 2
In this task, you need to obtain a list of all machines with the 'OS 2' operating system because these machines need an update. To get this information, you’ll run your first SQL query with a filter.

Select all the records from the machines table with a value of 'OS 2' in the operating_system column. Replace the value X with the correct string:

![Screenshot 2024-08-15 191649](https://github.com/user-attachments/assets/430ab02b-dc07-450b-92d1-71afcec57ada)

## How many machines in the database use the OS 2 operating system?
##### Answer:80

Task 3. List employees in specific departments
In this task, you need to retrieve a list of all the employees in the Finance and Sales departments to obtain their office numbers. A notice about handling confidential financial information will be posted to these offices.

Filter the rows returned from department column in the employees table to include only employees from the 'Finance' department. Replace X with the appropriate column name and Y with the appropriate value to complete the filter:

![Screenshot 2024-08-15 192602](https://github.com/user-attachments/assets/9e577801-9eb3-4e14-8384-ff5a3c177eb4)

## What is the employee_id of the first row returned?
##### Answer:1003

Modify the previous query so that it returns employees who are in the 'Sales' department.

![Screenshot 2024-08-15 193315](https://github.com/user-attachments/assets/9f5652e7-2072-4afe-80d9-7441c5f0a369)

## How many employees work in the Sales department?

##### Answer:33

## Task 4. Identify employee machines
Your team recently discovered that there are issues with machines in the South building. In this task, you need to obtain certain employee and computer information.

A machine in 'South-109' has an issue. You need to determine which employee uses that computer so you can send them an alert.

Write a query to identify which employee uses the office in 'South-109'. (The data must be returned from the office column in the employees table.)

![Screenshot 2024-08-15 195010](https://github.com/user-attachments/assets/6bc11e80-55be-4cc3-b7e0-203a7a89dee2)

## Which of the following employees uses the computer with the issue?

##### Answer: jlansky

Next, your team has determined that there is an issue with all the machines in the South building. Offices in the organization are named with the building name, a hyphen, and the office number in that building (for example, 'South-109').

Modify the query you used in the previous step so that it returns information on all the employees in the 'South' building. Use the LIKE operator with % in this query.

![Screenshot 2024-08-15 195626](https://github.com/user-attachments/assets/ceb72cc6-de11-4be3-adb7-bf303bede824)

## Which department does the first employee listed in the South building belong to?

##### Answer: Finance









