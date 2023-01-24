# Security Role Management Tool

The Security Role Management (SRM) tool contains predefined security roles to easily manage the assoication of a Dataverse secruity role to an end User’s roles and responsibilities to the capabilities of the Power Platform.

One of the key objective of the SRM tool is to enable administrators to assign RPA related security roles to User. The tool provides easy access to predefined security roles with functionality to modify and/or add new roles to best fit different Organization requirements.

### Constraints, Assumptions, and Dependencies

* The solution is constraint to the environment it is imported.

* Need System Administrator role to import solution.

* After importing the solution, data for RPA Task List and RPA Roles Mapped to Task table needs to be imported using CSV files provided along the solution.

* Canvas App is used to assign and modify tasks for predefined RPA security role.

* The new security role cannot be created within canvas app, but the portal has a functionality to navigate to the existing role creation screen.

* Any new role created by admin for RPA should start with “RPA” to access it within the RPA security role management portal.

### Data Source

The application uses Microsoft Dataverse as the data source.

### Master Data Lists

The master data lists are to be maintained by admins.

* <b>RPA Task List:</b> Data table contains predefined Task an RPA security role can perform.

* <b>RPA Roles Mapped to Task:</b>  Data table contains Security roles and task mapped to those roles.

* <b>RPA Audit Log:</b> Data table contains Audit history related to RPA security role.

### Pre-defined Security Roles

* <b> RPA_Reviewer_Org </b>

     Designed for use in Development and Production environments, the RPA_Reviewer_Org role is assigned to a user responsible for monitoring all run log history of the flows.

     This Security Role enables them to:

     • Monitor Automation Run Logs (Organization)
  
* <b> RPA_Reviewer_User </b>

    Designed for use in Development and Production environments, the RPA_Reviewer_User role is assigned to a user responsible for monitoring their run log history of the flow.

    This Security Role enables them to:

    • Monitor Automation Run Logs (User)

* <b>RPA_Developer </b>

    Designed for use in Development environments, the RPA_Developer role is assigned to Users developing Robotic Process Automations.
    This Security Role enables them to:

    • Monitor Automation Run Logs (User)

    • Create Automation

    • Read (Execute) Automation

    • Update/Edit Automation

    • Share Desktop Automation

    • Create Connection

    • Update/Delete Connection

    • Manage Machine Group

    • Import Solution

    • Export Solution

    • Update/Upgrade Solution

* <b> RPA_Deployer </b>
  
    Designed for use in all Development, Testing and Production environments, the RPA_Deployer role is assigned to a user responsible for the migrating solutions between environments.

    This Security Role enables them to:

    • Create Connection

    • Update/Delete Connection

    • Manage Machine Group

    • Import Solution

    • Export Solution

    • Update/Upgrade Solution

* <b> RPA_Tester </b>
    Designed for use in Testing in environments, the RPA_TEST-Tester role is assigned to a user responsible for testing Automations before release into Production environments.

    This Security Role enables them to:

    • Create Automation

    • Read (Execute) Automation

    • Update/Edit Automation

    • Monitor Automation Run Logs (Organization)

    • Create Connection

    • Update/Delete Connection

### Installation

1. Download the solution zip file
2. Go to make.powerapps.com (<http://make.powerapps.com>)
3. Navigate to solutions page
3. Import the zip file downloaded
4. Select the solution zip file from the downloaded location
5. Select the Dataverse connection during import

### Import Master Data

* <b> RPA Task List </b>
1. Go to make.powerapps.com (<http://make.powerapps.com>)
2. Navigate to Dataverse and click on Tables
3. Select *All*  under the tables 
4. Search for *RPA Task List*
5. For the listed table, **RPA Task List**, select the option *import data from the Excel*
6. Upload the file [*ff_rpatasklists.csv*](/ff_rpatasklists.csv)
7. Map the data as below - 
![RPA Task List import data mapping](/assets/images/md-map-1.jpg)
1. Make sure the data import successfully imported the data rows in the table

* <b> RPA Role Task List </b>
1. Go to make.powerapps.com (<http://make.powerapps.com>)
2. Navigate to Dataverse and click on Tables
3. Select *All*  under the tables 
4. Search for *RPA Roles Mapped to Task*
5. For the listed table, **RPA Roles Mapped To Task**, select the option *import data from the Excel*
6. Upload the file [*ff_rparoletasklists.csv*](/ff_rparoletasklists.csv)
7. Map the data as below - 
![RPA Task List import data mapping](/assets/images/md-map-1.jpg)
1. Make sure the data import successfully imported the data rows in the table

### Walk through of RPA_Reviewer_Role
![](/assets/videos/reviewer-demo.gif)

## Microsoft Open Source Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).

Resources:

- [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)
- [Microsoft Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)
- Contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with questions or concerns

## Trademarks 
This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow Microsoft's Trademark & Brand Guidelines. Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos are subject to those third-party's policies.

## Security

Microsoft takes the security of our software products and services seriously, which includes all source code repositories managed through our GitHub organizations, which include [Microsoft](https://github.com/Microsoft), [Azure](https://github.com/Azure), [DotNet](https://github.com/dotnet), [AspNet](https://github.com/aspnet), [Xamarin](https://github.com/xamarin), and [our GitHub organizations](https://opensource.microsoft.com/).

If you believe you have found a security vulnerability in any Microsoft-owned repository that meets Microsoft's [Microsoft's definition of a security vulnerability](https://docs.microsoft.com/en-us/previous-versions/tn-archive/cc751383(v=technet.10)), please report it to us as described below.

## Reporting Security Issues

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them to the Microsoft Security Response Center (MSRC) at [https://msrc.microsoft.com/create-report](https://msrc.microsoft.com/create-report).

If you prefer to submit without logging in, send email to [secure@microsoft.com](mailto:secure@microsoft.com).  If possible, encrypt your message with our PGP key; please download it from the the [Microsoft Security Response Center PGP Key page](https://www.microsoft.com/en-us/msrc/pgp-key-msrc).

You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Additional information can be found at [microsoft.com/msrc](https://www.microsoft.com/msrc).

Please include the requested information listed below (as much as you can provide) to help us better understand the nature and scope of the possible issue:

  * Type of issue (e.g. buffer overflow, SQL injection, cross-site scripting, etc.)
  * Full paths of source file(s) related to the manifestation of the issue
  * The location of the affected source code (tag/branch/commit or direct URL)
  * Any special configuration required to reproduce the issue
  * Step-by-step instructions to reproduce the issue
  * Proof-of-concept or exploit code (if possible)
  * Impact of the issue, including how an attacker might exploit the issue

This information will help us triage your report more quickly.

If you are reporting for a bug bounty, more complete reports can contribute to a higher bounty award. Please visit our [Microsoft Bug Bounty Program](https://microsoft.com/msrc/bounty) page for more details about our active programs.

## Preferred Languages

We prefer all communications to be in English.

## Policy

Microsoft follows the principle of [Coordinated Vulnerability Disclosure](https://www.microsoft.com/en-us/msrc/cvd).