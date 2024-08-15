In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.

The information you need is located in the machines and login_attempts tables in the organization database.

Here’s how you’ll do this task: First, you’ll obtain information on the employee devices that must be updated. Next, you’ll examine the login attempts for unusual activity. Finally, you’ll use the ORDER BY keyword to sort the data returned by your SQL queries.

## Task 1. Retrieve employee device data
In this task, you need to obtain information on employee devices because your team needs to update them. The information you need is in the machines table in the organization database.

First, you need to retrieve all the information about the employee devices.

Run the following query to select all device information from the machines table:

##### SELECT * FROM machines;
![Screenshot 2024-08-15 181955](https://github.com/user-attachments/assets/35d68775-0229-47d3-9ddc-68c7cbc082f6)

Run the following query to select only the device_id and email_client columns from the machines table. Replace X with device_id and Y with email_client:

![Screenshot 2024-08-15 182334](https://github.com/user-attachments/assets/fafedf9a-61d0-4e62-91d9-dbf72d42099f)

## What email client is returned in the third row?

##### Answer: Email Client 2

Complete the query to return only the device_id, operating_system, and OS_patch_date columns from the machines table. Replace X, Y, and Z with the columns that you need to return:

![Screenshot 2024-08-15 182748](https://github.com/user-attachments/assets/d859a5a2-32bd-45b4-9510-a4073993e99b)

## What is the patch date of the first entry?

##### Answer: 2021-09-11

## Task 2. Investigate login activity
In this task, you need to analyze the information from the log_in_attempts table to determine if any unusual activity has occurred.

Write a SQL query to select the event_id and country columns from the log_in_attempts table.

![Screenshot 2024-08-15 183234](https://github.com/user-attachments/assets/18ce9813-b076-4902-8e3b-91e1ce56657f)

## Were any login attempts made from Australia?
##### Answer: NO

## Write a SQL query that selects the username, login_date, and login_time columns from the log_in_attempts table.

![Screenshot 2024-08-15 184039](https://github.com/user-attachments/assets/ef82c06d-ecb5-429d-beab-acc7b6f2017d)

## What username is returned in the fifth row?
##### Answer: jrafael

Write a SQL query that selects all columns from the log_in_attempts table, using a single symbol after the SELECT keyword.

![Screenshot 2024-08-15 184458](https://github.com/user-attachments/assets/06dbcf4e-8236-48c0-85b1-de2bfec3093e)

## Task 3. Order login attempts data
In this task, you need to use the ORDER BY keyword. You'll sequence the data that your query returns according to the login date and time.

First, you need to sort the information by date.

Run the following query, which orders log_in_attempts data by login_date:

![Screenshot 2024-08-15 185327](https://github.com/user-attachments/assets/f1ffa675-7cd0-4a50-9c06-71b69a4c2783)

## What are the username and login date of the first record returned?

##### Answer: ivelasco on 2022-05-08

Modify the query from the previous step by adding the login time to the ORDER BY clause. You must replace X with the appropriate column name:

![Screenshot 2024-08-15 185713](https://github.com/user-attachments/assets/536d2355-2898-455f-ab4b-bf108322c05f)

## What are the username and login time of the first record returned by the above query?

##### Answer: bsand at 00:19:11
