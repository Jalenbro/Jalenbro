## Activity overview
As a security analyst, you’ll often need to query numbers and dates.

For example, you may need to filter patch dates to find machines that need an update. Or you might filter login attempts made during a certain period of time to investigate a security incident.

Common operators for working with numeric or date and time data will help you accurately filter data. These are some of the operators you'll use:

= (equal)
> (greater than)
< (less than)
<> (not equal to)
>= (greater than or equal to)
<= (less than or equal to)
In this lab activity, you’ll apply these operators to accurately filter for specific numbers and dates!

## Task 1. Retrieve login attempts after a certain date
In this task, you need to investigate a recent security incident. To do this, you need to gather information about login attempts made after a certain date.

Complete the SQL query to retrieve data for login attempts made after '2022-05-09'. Replace X with the correct operator:

![Screenshot 2024-08-19 183454](https://github.com/user-attachments/assets/6e785886-79e0-42dd-b592-c525a0464c84)

I used the greater than operator to create a table with dates only after  2022-05-09

### How many login attempts were made after 2022-05-09?
#### Answer: 125

Complete the SQL query to retrieve data for login attempts that were made on or after '2022-05-09'. Replace X with the correct operator

![Screenshot 2024-08-19 185313](https://github.com/user-attachments/assets/40036868-7cf9-4ef3-9a24-b0a2c358f55f)

I used the greater than or equal too operator to get the correct table data

### How many login attempts were made on or after 2022-05-09?

#### Answer: 165

## Task 2. Retrieve logins in a date range
In this task, you need to narrow the focus of the search. Login attempts made after 2022-05-11 shouldn't be included. Use the BETWEEN and AND operators to return results between '2022-05-09' and '2022-05-11'.

![Screenshot 2024-08-19 185941](https://github.com/user-attachments/assets/c504ed6a-fde5-48e8-8b82-a366b6703ec3)

## How many login attempts were made between 2022-05-09 and 2022-05-11?

#### Answer: 123

## Task 3. Investigate logins at certain times
In this task, you need to investigate logins that were made at certain times. To do this, filter the data in the log_in_attempts table by login time (login_time).

First, your organization's typical work hours begin at 07:00:00. Retrieve all login attempts made before 07:00:00 to learn more about the users who are logging in outside of typical hours.

Write a SQL query to retrieve data for login attempts made before '07:00:00'.

![Screenshot 2024-08-19 190457](https://github.com/user-attachments/assets/86c5234b-509d-429b-85cc-21ce9cd8b3ec)
I used the lesser than operator to get the correct output on this table

### what is the username of the fifth record returned from this query?
#### Answer: eraab

Modify the query to return logins between '06:00:00' and '07:00:00'.

![Screenshot 2024-08-19 190457](https://github.com/user-attachments/assets/8ac93430-bfdf-4df8-b61c-f1c01e042f5c)

### What time was the earliest login attempt between 06:00:00 and 07:00:00?
#### Answer: 06:01:31

Task 4. Investigate logins by event ID
In this task, you need to investigate login attempts based on event ID numbers. With this query, you want to return only the event_id, username, and login_date fields from the log_in_attempts table.

Write a query to return login attempts with event_id greater than or equal to 100.

![Screenshot 2024-08-19 191849](https://github.com/user-attachments/assets/775d9622-d3d0-465b-9300-9d72b8800753)

### What is the login date of the third result returned by your query?
#### Answer: 2022-05-09

Modify the query to return only login attempts with event_id between 100 and 150.

![Screenshot 2024-08-19 192313](https://github.com/user-attachments/assets/c5e137e2-dc4a-4d1d-9251-2e71e8e40a7c)

### What is the username of the seventh result returned by your query?
#### Answer: tmitchel

