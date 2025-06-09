<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>🎯 Top 5 Post-Install Configuration Objectives</h2>

1. **Establish Secure and Organized System Access**
   - Differentiate access for Admins, Agents, and End Users.
   - Confirm URLs for the Admin Panel and End User Portal.
   - Ensure system access is role-appropriate and secure.

2. **Define Roles, Departments, and Teams**
   - Create custom **Roles** to control permission levels.
   - Configure **Departments** to manage ticket visibility.
   - Set up **Teams** to collaborate across departments.

3. **Enable Public Ticket Submission and Manage User Access**
   - Adjust settings to allow unregistered users to create tickets.
   - Register and manage **Users** (customers) and **Agents** (support staff).

4. **Implement Service Level Agreements (SLAs)**
   - Define SLA plans with appropriate grace periods and schedules.
   - Assign SLAs to ensure timely ticket resolution and prioritization.

5. **Create Custom Help Topics to Streamline Ticket Creation**
   - Design Help Topics that reflect common user issues.
   - Guide users through consistent and categorized ticket submissions.

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/kn4IWcA.png" height="80%" width="80%"
</p>
   
1. System Setup and Access Configuration

- **Access Points:**
  - **Admin/Analyst Panel:** `http://localhost/osTicket/scp/login.php`
  - **End User Portal:** `http://localhost/osTicket`

- **Panel Acknowledgment:**
  - **Admin Panel** – For system configuration and management.
  - **Agent Panel** – For ticket management and user interaction.
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
2. Organizational Structure and Permissions

- **Roles Setup** *(Controls agent permissions)*:
  - Created Role: `Supreme Admin`
  - Path: `Admin Panel -> Agents -> Roles`

- **Departments Setup** *(Controls ticket visibility and segmentation)*:
  - Created Department: `SysAdmins`
  - Path: `Admin Panel -> Agents -> Departments`

- **Teams Configuration** *(Group agents across departments)*:
  - Created Team: `Online Banking`
  - Path: `Admin Panel -> Agents -> Teams`

- **Agent Configuration** *(Add and assign internal staff)*:
  - `Jane` (Department: SysAdmins)
  - `John` (Department: Support)
  - Path: `Admin Panel -> Agents -> Add New`

- **User Configuration** *(Add external users/customers)*:
  - `Karen`, `Ken`
  - Path: `Agent Panel -> Users -> Add New`
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
3. Ticket Workflow and Service Parameters

- **User Ticket Permissions:**
  - Enabled ticket submission by **unchecking** the "registration required" option.
  - Path: `Admin Panel -> Settings -> User Settings`

- **SLA (Service Level Agreements):**
  - `Sev-A`: 1 hour grace period, 24/7 schedule
  - `Sev-B`: 4 hours grace period, 24/7 schedule
  - `Sev-C`: 8 hours grace period, business hours
  - Path: `Admin Panel -> Manage -> SLA`

- **Help Topics Configuration** *(Guides user ticket submissions)*:
  - Topics:
    - Business Critical Outage
    - Personal Computer Issues
    - Equipment Request
    - Password Reset
    - Other
  - Path: `Admin Panel -> Manage -> Help Topics`
<br />
