Splunk is one of the leading SIEM solutions in the market that provides the ability to collect, analyze and correlate the network and machine logs in real-time. In this room, we will explore the basics of Splunk and its functionalities and how it provides better visibility of network activities and help in speeding up the detection.

Learning Objective and Pre-requisites

If you are new to SIEM, please complete the Introduction to SIEM. This room covers the following learning objectives:

Splunk overview
Splunk components and how they work
Different ways to ingest logs
Normalization of logs
Answer the questions below
Continue with the next task.

Room Machine

Before moving forward, deploy the machine. When you deploy the machine, it will be assigned an IP. Access this room in a web browser on the AttackBox, or via the VPN at http://MACHINE_IP. The machine will take up to 3-5 minutes to start.
Answer the questions below
Connect with the lab.

![Screenshot 2024-08-11 144654](https://github.com/user-attachments/assets/8b1cef09-c6b7-43d8-8771-b853c45066db)

Splunk has three main components, namely Forwarder, Indexer, and Search Head. These components are explained below:

Splunk components



Splunk Forwarder

Splunk Forwarder is a lightweight agent installed on the endpoint intended to be monitored, and its main task is to collect the data and send it to the Splunk instance. It does not affect the endpoint's performance as it takes very few resources to process. Some of the key data sources are:

Web server generating web traffic.
Windows machine generating Windows Event Logs, PowerShell, and Sysmon data.
Linux host generating host-centric logs.
Database generating DB connection requests, responses, and errors.
Splunk Forwarder

Splunk Indexer

Splunk Indexer plays the main role in processing the data it receives from forwarders. It takes the data, normalizes it into field-value pairs, determines the datatype of the data, and stores them as events. Processed data is easy to search and analyze.

Splunk Indexer

Search Head

Splunk Search Head is the place within the Search & Reporting App where users can search the indexed logs as shown below. When the user searches for a term or uses a Search language known as Splunk Search Processing Language, the request is sent to the indexer and the relevant events are returned in the form of field-value pairs.

Image showing Splunk Search Head

Search Head also provides the ability to transform the results into presentable tables, visualizations like pie-chart, bar-chart and column-chart, as shown below:

Image showing Visualization tab



Answer the questions below
Which component is used to collect and send data over the Splunk instance?
## forwarder

﻿Splunk Bar

When you access Splunk, you will see the default home screen identical to the screenshot below.

Shows splunk Interface

Let's look at each section, or panel, that makes up the home screen. The top panel is the Splunk Bar (below image). 

Shows splunk Bar

In the Splunk Bar, you can see system-level messages (Messages), configure the Splunk instance (Settings), review the progress of jobs (Activity), miscellaneous information such as tutorials (Help), and a search feature (Find). 

The ability to switch between installed Splunk apps instead of using the Apps panel can be achieved from the Splunk Bar, like in the image below.

Shows App Bar


Apps Panel

Next is the Apps Panel.  In this panel, you can see the apps installed for the Splunk instance. 

The default app for every Splunk installation is Search & Reporting. 

App Panel

Explore Splunk

The next section is Explore Splunk. This panel contains quick links to add data to the Splunk instance, add new Splunk apps, and access the Splunk documentation. 

Shows Option to add data, access documentation, add new splunk apps

Splunk Dashboard

The last section is the Home Dashboard. By default, no dashboards are displayed. You can choose from a range of dashboards readily available within your Splunk instance. You can select a dashboard from the dropdown menu or by visiting the dashboards listing page.

Shows splunk dashboard

You can also create dashboards and add them to the Home Dashboard. The dashboards you create can be viewed isolated from the other dashboards by clicking on the Yours tab.

Please review the Splunk documentation on Navigating Splunk here.

Answer the questions below
In the Add Data tab, which option is used to collect data from files and ports?
![Screenshot 2024-08-11 145536](https://github.com/user-attachments/assets/88569381-9c17-49fe-82f7-6438d0412994)

## Monitor


Upload the data attached to this task and create an index "VPN_Logs". How many events are present in the log file?
![Screenshot 2024-08-11 150533](https://github.com/user-attachments/assets/d24e4b78-f4b1-4db0-b87e-618259e757b1)

## 2862

How many log events by the user Maleena are captured?
![Screenshot 2024-08-11 150741](https://github.com/user-attachments/assets/3787a8d7-deeb-4349-a7a5-844c49fc3e2f)

## 60

What is the name associated with IP 107.14.182.38?
![Screenshot 2024-08-11 150955](https://github.com/user-attachments/assets/dacc7177-0838-4774-a3d0-5a23958bbe61)

## smith

What is the number of events that originated from all countries except France?
![Screenshot 2024-08-11 151206](https://github.com/user-attachments/assets/a0e553e6-93d1-42cf-a265-7748b645820d)
Subtracted by total events

## 2814

How many VPN Events were observed by the IP 107.3.206.58?

![Screenshot 2024-08-11 151316](https://github.com/user-attachments/assets/f268c82d-1de1-46a6-8ca4-188705f15468)

## 14
