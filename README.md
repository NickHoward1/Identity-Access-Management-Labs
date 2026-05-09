<h1>Microsoft Entra ID Lab</h1>

<h2>Objective</h2>
The objective of this lab is to understand how businesses use Microsoft Entra ID for Identity & Access Management, develop familiarity with the platform, and perform common tasks typically carried out by an IAM Analyst in daily business operations.

<h2>Environment</h2>
<ul>
 <li>Microsoft Entra ID</li>
 <li>Virtual users/groups</li>
 <li>Conditional Access policies</li>
</ul>
<h2>Tasks Completed</h2>
<ul>
 <li>Create users/groups</li>
 <li>Assign roles</li>
 <li>Configure MFA</li>
 <li>Conditional Access</li>
 <li>Review sign-in logs</li>
</ul>

<h2>Tools used</h2>

<ul>
  <li></li>
</ul>

<h2>Screenshots</h2>

<h3>New User Accounts</h3> 

The screenshots below show the process of manually creating a new user account in Microsoft Entra ID by configuring the required properties and user details. The final step involves assigning roles and permissions using Role-Based Access Control (RBAC), which allows access to be granted based on the user’s responsibilities within the organisation. I can also bulk-create users by uploading a pre-filled CSV file, which automatically populates the required fields within the user properties. 

<b>Process:</b> Entra Admin Centre - Users - Create New Users - Basics - Properties - Assignments - Review + Create. 

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/d61448333210e2549d845205f6d79fbd6a6097ac/Screenshot%202026-05-08%20at%2009.48.20.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/5c96ab9393fd3f11ec42e6a631282e10cf12255f/Screenshot%202026-05-08%20at%2009.59.07.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/0a8b76748c329237a8aac19c57fbb9a59e1274df/Screenshot%202026-05-08%20at%2010.06.50.png" width="300" height="300" /> 
</p>
<br> <br />

<h3>Groups</h3> 

Below, I demonstrate the creation of new groups within Microsoft Entra ID. I created both an HR group and a Sales/Marketing group, each configured for different business purposes. The HR group was created as a traditional Security group, which is used to manage access to specific resources, permissions, and security features across the organisation. The Sales/Marketing group was configured as a Microsoft 365 group, enabling users to collaborate and access shared services such as Microsoft Outlook, Microsoft Excel, Microsoft PowerPoint, Microsoft Teams, Microsoft OneDrive, and other Microsoft 365 applications.

I also assigned roles within the HR Security group, including Global Administrator permissions, ensuring elevated privileges are only granted to users with the appropriate level of authority within the business as an example.

For the Sales/Marketing group, instead of manually assigning users, I configured the group as a Dynamic Group and created a rule that automatically adds users based on specific conditions. In this example, I configured the rule to include users located in the UK, demonstrating how dynamic groups can automate user management and improve administrative efficiency within Microsoft Entra ID.

<b>Process:</b> Groups - All Groups - New Group - Group Type - Fill in Fields with * - Assign Owner - Assign Users - Select roles if applicable 

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/b1b19239fe629e80fcf7345495fc51775ef35905/Screenshot%202026-05-08%20at%2014.59.34.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/4a87fb82ad1b8b6ed25ff0976f1c302df9ba8035/Screenshot%202026-05-08%20at%2015.30.16.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/969d6ed783c16747ea763dea7a64aff03b5316ee/Screenshot%202026-05-08%20at%2015.30.39.png" width="300" height="300" /> 
</p>
<br> <br />

<h3>Guest User</h3> 

Below, I created a guest user account for external visitors who may require temporary access to the system. I followed the setup process and assigned roles depending on the nature of the visit. For example, if someone only needed access to documents to review SOPs, I could provide read-only access. However, if a consultant was coming into the business to make internal changes, I could grant them the appropriate permissions to access certain files and make the necessary changes.

<b>Process:</b> Users - New Users - Invite External User - Properties - Assignments - Review + Create. 

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/d61448333210e2549d845205f6d79fbd6a6097ac/Screenshot%202026-05-08%20at%2009.48.20.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/5c96ab9393fd3f11ec42e6a631282e10cf12255f/Screenshot%202026-05-08%20at%2009.59.07.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/ac5ce17a932519d8e452a5169519ad0fd4458c58/Screenshot%202026-05-08%20at%2014.35.59.png" width="300" height="300" /> 
</p>
<br> <br />

<h3>Password Reset and MFA Configurations</h3> 

In the screenshot below, I navigate through the password reset settings in Microsoft Entra ID to configure self-service password reset (SSPR), allowing users to securely reset their own passwords without contacting the helpdesk. I also configure the authentication settings to control how often users must re-confirm their authentication information. In addition, I set up Multi-Factor Authentication (MFA) to enhance account security by applying the “something you know” and “something you have” authentication principle.

<b>Process:</b> Users - Password Reset - Properties -  Authentication methods - Registration - Notifications

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/4be7a5cc9272ce4dde5488c92391b99451d8fba8/Screenshot%202026-05-08%20at%2014.31.31.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/db352de6b8705887437d30f2fd780381d597b91d/Screenshot%202026-05-08%20at%2014.32.28.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/bdd3aa4def138c3e8fe44c558e1104cd7e4e1404/Screenshot%202026-05-08%20at%2013.43.23.png" width="300" height="300" /> 
</p>
<br> <br />



<h2>What I've Learnt</h2>

<p align="left">


<b></b> 
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
