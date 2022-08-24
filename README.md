# EmployeeManagmentSystem_react-springBoot

PROJECT: ADVANCED JAVA

Employee Management System:

The purpose of the software requirements document is to systematically capture requirements for the project and the “Employee Management System” to be developed. Both functional and non-functional requirements are captured in this document. It also serves as the input for project scoping. 
The scope of this document is limited to addressing the requirements from a user, quality, and non-functional perspective. 
Purpose	
In the current system, Admin adds new regulations and assigns them to the department manually. Department Head sends these regulations to the individual users through mail to get their consent. Users send their comments through the courier service after reading regulations. Department head has to collect the user inputs and pass them on to Admin. Since a lot of manual workflow is involved, it is time consuming for Admin to close each regulation.
So, a new system is required to automate this regulation creation and closure process.
In Scope
Employee information creation and maintenance
Department creation and maintenance
Regulation creation and maintenance
Mapping each employee to the respective department
Updating/viewing user comments on the assigned regulations
Out Scope
Loading the employee list into the application
Notifications on the status 
Current system flow 


Business Requirements
#	Rule Name	Definition
1	Mandatory Employee Fields	The system should check if the following details are being entered while adding/editing a new Employee:
•	First Name
•	Last Name
•	DOB
•	Department
Appropriate message should be thrown as an alert.
2	Business Validation	While Adding an Employee, the system should not allow the entry of Employee who is not older than 24 years into the system. 
Appropriate message should be thrown as an alert.
3	Mandatory Department  Fields	The system should check if the following details are being entered while adding a new Department:
•	Department Name
Appropriate message should be thrown as an alert.
4	Compliance of RL document	The RL document should be marked as closed only after all the employees of a department have submitted a status report.
5	Mandatory Regulation  Fields	The system should check if the following details are being entered while adding a new Regulation
•	Regulation details
•	Regulation creation date
Appropriate message should be thrown as an alert.
6	Mandatory User Comments Field	The system should check if the following details are being entered while adding a new Regulation
•	Regulation Comments.
•	Comments creation date
Appropriate message should be thrown as an alert.

High Level Business Requirements
S.No	Business Requirement ID	Short Description	Description in detail	Interacting Business Processes
1	BR001	Login with different roles User, Admin	There should be provision to login as Admin or as User.	NA
2	BR002	Add Employee	Admin should be allowed to add employee details using HTML.	NA
3	BR003	View Employees	There should be provision for Admin/User to see the entire Employee list in the organization using HTML.	NA
4	BR004	Edit Employee	Admin should be allowed to edit employee details using HTML.	NA
5	BR005	Delete Employee	Admin should be allowed to delete employee details using HTML.	NA
6	BR006	Add Department	Admin should be allowed to add department using HTML.	NA
7	BR007	View Department	Admin should be allowed to view department list using HTML.	NA
8	BR008	Create RL - Admin	Admin should be allowed to add new regulation/legislation and map it to department using HTML.	NA
9	BR009	View  RL - Admin	Admin should be allowed to view already added regulation/legislation using HTML.	NA
10	BR010	View RL  - User	The system should allow the employees to view the regulations assigned to them using HTML.	NA
11	BR011	Update  User Comments - User	Should allow the users to update the comments for the regulation assigned to them using HTML.	NA
12	BR012	View  User Comments - User	Should allow the users to view the comments updated by them using HTML.	NA

Detailed Business Requirements
S.No	Req. #	Business Requirement	Req. Type *	Priority **	Originator ***	BR Traced to Business Requirement/ Use case ID
1	BR001	Provision to login with two different roles, namely, Admin and User. 
View, Add, Edit Employee; Create RL; and Add Department operations must be permitted when logged in as Admin.
When logged in as User, View RL and Update and View Comments operations must be permitted.	F	1	Employee Management Web App	NA
2	BR002	From Web App, Admin should be allowed to enter the following details for the Employee:
•	First Name
•	Last Name
•	DOB
•	Email
•	Department	F	1	Employee Management Web App	NA
3	BR003	In Web App, the Admin can see the list of all employees in the organization. The web app must capture the following information:
•	User Id
•	First Name
•	Last Name
•	DOB
•	Email
•	Department	F	1	Employee Management Web App	NA
4	BR004	In Web App, Admin should be allowed to Edit any employee. 

Web App should allow the admin to edit the following details:
•	First Name
•	Last Name
•	DOB
•	Email
•	Department	F	1	Employee Management Web App	NA
5	BR005	From Web App, Admin should be allowed to delete the required Employee.	F	1	Employee Management Web App	NA
6	BR006	From Web App, Admin should be allowed to enter the following details for the Department
•	Department
•	Name	F	1	Employee Management Web App	NA
7	BR007	From Web App, Admin can view the department list. The web app must capture the following information:
•	Department Id
•	Department Name
	F	1	Employee Management Web App	NA
8	BR008	From Web App, Admin should be allowed to create a new Regulation/Legislation document. It should capture the following fields.
•	RL Type
•	RL Details
•	Creation Date
•	Department	F	1	Compliance Tracking	NA
9	BR009	From Web App, Admin Should be allowed to View the RL for each department. It should display the following fields.
•	RL Id
•	RL Type
•	Description
•	Creation Date
•	Department
•	Status	F	1	Compliance Tracking	NA
10	BR010	From Web App, View RL -User should allow the employees to view the regulations assigned to them. The Employees should be allowed to view the previously created status report.	F	1	Compliance Tracking	NA
11	BR011	From Web App, admin should allow the user to update the comments for each regulation assigned to them.
•	User Comments
•	Date	F	1	Compliance Tracking	NA
12	BR012	From Web App, Users should be allowed to view the Comments entered by them.	F	1	Compliance Tracking	NA

* Req. Type 
 F 	Core Functionality, 
E 	Exception, 
UI 	User Interface 
R 	Reporting

Business Objective Traceability Matrix
Business Objective	Business Requirement Number	Priority	Requirement Title	How requirement satisfies objective	Status
To maintain the employee details in an application	1	High	Employee Management Web App	Allows the Admin to  maintain the employee details effectively	Open
To track the compliance of each law to closure	2	High	Compliance Tracking	Allows the Admin to create and track the new law effectively	Open

Functional Specification  
The Employee Management Web application can be integrated by linking all the modules. EMP is basically a system that helps maintain employee information, map employees to departments, create RL documents, and track compliance and user comments. 

Important modules in the system:
a)	Employee Record Maintenance – Add, Edit, Delete, View Employees.
b)	Departments – Add, View Department
c)	Regulations/Legislation – Create, View Regulation
d)	Compliance Tracking
This document details the requirements for overall integrated application. This application can be accessed by administrators and registered users only.

Integrated application features
1. Application should have single login page. Login page should be the welcome page for the application.
2. Only registered users and administrators should be able access the application.
3. Users should not be able to access any application feature without login. 
4. There should be a logout feature. Once logged out, users should come to the welcome page or design logout page to re-login.
5. Application home page must have facility to access the following functionalities: 
a)	Admin users must be able to Add, Edit, Delete, and View Employees  
b)	Admin users must be able to Add and View Department 
c)	Admin users must be able to create regulation and View regulation status of all departments.
d)	Users must be able to View Regulations assigned to them.
e)	Users must be able to View and Update their Comments on regulation.
f)	Users must be able to track Compliance of department through status.
6. At any point of time, user should be able to go back to homepage.
7. None of the features should be accessible if session expires.
8. Logged in users should be tracked through session.
7. If user clicks the back button after logout, browser pages should not be accessible.
8. On login, user credentials should be validated against those of the registered users in the system.
9. Log in page should have username and Password fields to receive username and password and should have login button.
10. Password must be encrypted.
11. Username and password cannot be blank.
12. If the username and password do not exist in the system, application should show proper error message.

Integrated application non-functional features
1. Exceptions should not be shown on web app.
2. No debug message should appear on web app.
3. All the errors and exceptions should be logged to log file.
4. Log file path should be configurable.
5. Database connections should be configurable and should not be hard coded.

Table Structure and Relationship
 
