# pp-srm-tool
### Security Role Management Tool for Power Platform

The Security Role Management (SRM) tool contains predefined security roles to easily manage the assoication of a Dataverse secruity role to an end User’s roles and responsibilities to the capabilities of the Power Platform.

One of the key objective of the SRM tool is to enable administrators to assign RPA related security roles to User. The tool provides easy access to predefined security roles with functionality to modify and/or add new roles to best fit different Organization requirements.

### Constraints, Assumptions, and Dependencies
•	The solution is constraint to the environment it is imported.
 
•	Need System Administrator role to import solution.

•	After importing the solution, data for RPA Task List and RPA Roles Mapped to Task table needs to be imported using CSV files provided along the solution.

•	Canvas App is used to assign and modify tasks for predefined RPA security role. 

•	The new security role cannot be created within canvas app, but the portal has a functionality to navigate to the existing role creation screen.

•	Any new role created by admin for RPA should start with “RPA” to access it within the RPA security role management portal.


### Data Source
The application uses Microsoft Dataverse as the data source.

### Master Data Lists
The master data lists are to be maintained by admins. 

<b>•	RPA Task List:</b> Data table contains predefined Task an RPA security role can perform.

<b>•	RPA Roles Mapped to Task:</b>  Data table contains Security roles and task mapped to those roles. 

<b>•	RPA Audit Log:</b> Data table contains Audit history related to RPA security role.

### Pre-defined Security Roles

<b> RPA_Reviewer_Org </b>

 Designed for use in Development and Production environments, the RPA_Reviewer_Org role is assigned to a user responsible for monitoring all run log history of the flows.  

  This Security Role enables them to: 

  •	Monitor Automation Run Logs (Organization)


<b> RPA_Reviewer_User </b>

Designed for use in Development and Production environments, the RPA_Reviewer_User role is assigned to a user responsible for monitoring their run log history of the flow. 
This Security Role enables them to:

•	Monitor Automation Run Logs (User)

<b>RPA_Developer </b>

Designed for use in Development environments, the RPA_Developer role is assigned to Users developing Robotic Process Automations. 
This Security Role enables them to:

•	Monitor Automation Run Logs (User)

•	Create Automation

•	Read (Execute) Automation

•	Update/Edit Automation

•	Share Desktop Automation

•	Create Connection

•	Update/Delete Connection

•	Manage Machine Group

•	Import Solution

•	Export Solution

•	Update/Upgrade Solution


