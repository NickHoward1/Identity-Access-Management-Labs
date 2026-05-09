<h1>Microsoft Entra ID Lab</h1>

<h2>Objective</h2>
The objective of this lab is to understand how businesses use Microsoft Entra ID for Identity & Access Management, develop familiarity with the platform, and perform common tasks typically carried out by an IAM Analyst in daily business operations.

<h2>Environment</h2>
<ul>
 <li>Microsoft Entra ID</li>
 
</ul>
<h2>Tasks Completed</h2>
<ul>
 <li>Create users/groups</li>
 <li>Assign roles (RBAC)</li>
 <li>Configure MFA</li>
 <li>Conditional access</li>
 <li>Review sign-in logs</li>
 <li>App Integration (SAML)</li>
</ul>

<h2>Screenshots</h2>

<h3>New User Accounts</h3> 

The screenshots below show the process of manually creating a new user account in Microsoft Entra ID by configuring the required properties and user details. The final step involves assigning roles and permissions using Role-Based Access Control (RBAC), which allows access to be granted based on the user’s responsibilities within the organisation. I can also bulk-create users by uploading a pre-filled CSV file, which automatically populates the required fields within the user properties. 

<b>Process:</b> Entra Admin Centre - Users - Create New Users - Basics - Properties - Assignments - Review + Create. 

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/d61448333210e2549d845205f6d79fbd6a6097ac/Screenshot%202026-05-08%20at%2009.48.20.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/5c96ab9393fd3f11ec42e6a631282e10cf12255f/Screenshot%202026-05-08%20at%2009.59.07.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/0a8b76748c329237a8aac19c57fbb9a59e1274df/Screenshot%202026-05-08%20at%2010.06.50.png" width="300" height="300" /> 
</p>


<h3>Groups</h3> 

Below, I demonstrate the creation of new groups within Microsoft Entra ID. I created both an HR group and a Sales/Marketing group, each configured for different business purposes. The HR group was created as a traditional Security group, which is used to manage access to specific resources, permissions, and security features across the organisation. The Sales/Marketing group was configured as a Microsoft 365 group, enabling users to collaborate and access shared services such as Microsoft Outlook, Microsoft Excel, Microsoft PowerPoint, Microsoft Teams, Microsoft OneDrive, and other Microsoft 365 applications.

I also assigned roles within the HR Security group, including Global Administrator permissions, ensuring elevated privileges are only granted to users with the appropriate level of authority within the business as an example.

For the Sales/Marketing group, instead of manually assigning users, I configured the group as a Dynamic Group and created a rule that automatically adds users based on specific conditions. In this example, I configured the rule to include users located in the UK, demonstrating how dynamic groups can automate user management and improve administrative efficiency within Microsoft Entra ID.

<b>Process:</b> Groups - All Groups - New Group - Group Type - Fill in Fields with * - Assign Owner - Assign Users - Select roles if applicable 

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/b1b19239fe629e80fcf7345495fc51775ef35905/Screenshot%202026-05-08%20at%2014.59.34.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/4a87fb82ad1b8b6ed25ff0976f1c302df9ba8035/Screenshot%202026-05-08%20at%2015.30.16.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/969d6ed783c16747ea763dea7a64aff03b5316ee/Screenshot%202026-05-08%20at%2015.30.39.png" width="300" height="300" /> 
</p>

<h3>Guest User</h3> 

Below, I created a guest user account for external visitors who may require temporary access to the system. I followed the setup process and assigned roles depending on the nature of the visit. For example, if someone only needed access to documents to review SOPs, I could provide read-only access. However, if a consultant was coming into the business to make internal changes, I could grant them the appropriate permissions to access certain files and make the necessary changes.

<b>Process:</b> Users - New Users - Invite External User - Properties - Assignments - Review + Create. 

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/d61448333210e2549d845205f6d79fbd6a6097ac/Screenshot%202026-05-08%20at%2009.48.20.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/5c96ab9393fd3f11ec42e6a631282e10cf12255f/Screenshot%202026-05-08%20at%2009.59.07.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/ac5ce17a932519d8e452a5169519ad0fd4458c58/Screenshot%202026-05-08%20at%2014.35.59.png" width="300" height="300" /> 
</p>

<h3>Password Reset and MFA Configurations</h3> 

In the screenshot below, I navigate through the password reset settings in Microsoft Entra ID to configure self-service password reset (SSPR), allowing users to securely reset their own passwords without contacting the helpdesk. I also configure the authentication settings to control how often users must re-confirm their authentication information. In addition, I set up Multi-Factor Authentication (MFA) to enhance account security by applying the “something you know” and “something you have” authentication principle.

<b>Process:</b> Users - Password Reset - Properties -  Authentication methods - Registration - Notifications

<p>
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/4be7a5cc9272ce4dde5488c92391b99451d8fba8/Screenshot%202026-05-08%20at%2014.31.31.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/db352de6b8705887437d30f2fd780381d597b91d/Screenshot%202026-05-08%20at%2014.32.28.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/bdd3aa4def138c3e8fe44c558e1104cd7e4e1404/Screenshot%202026-05-08%20at%2013.43.23.png" width="300" height="300" /> 
</p>

<h3>Audit Logs</h3> 

The screenshot below shows me accessing the Audit Logs page within Microsoft Entra ID. This is where I can monitor for unusual behaviour such as out-of-hours logins, multiple login attempts within a short period of time, unfamiliar locations, or logins from countries not associated with normal business operations. If I identify anything suspicious, I can investigate further using tools such as Microsoft Sentinel and Wireshark to determine whether a user account may have been compromised. From there, I would follow the appropriate mitigation process and escalate the incident to the Senior SOC Analyst if required.

<b>Process:</b> Users - Password Reset - Properties -  Authentication methods - Registration - Notifications

<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/6ef0a6c9a8610c68c5ae53cf8dbcb9519e3c5b60/Screenshot%202026-05-09%20at%2010.44.16.png" width="300" height="300"/>

<h3>Enterprise Application Integration</h3> 

The screenshots below show how I would integrate a new application into Microsoft Entra ID for the company I work for. In this example, I integrated AWS by following the setup process, generating the Base64 certificate, and sending it to the appropriate team to complete the configuration. Once the setup was complete, I carried out testing to ensure the application was fully working and correctly integrated with Entra ID.

After confirming the integration was successful, I could then assign users and apply Conditional Access policies where required. For example, if a user attempted to sign in to AWS outside of the business network, they would be required to authenticate using MFA. However, if they were already signed into the internal company environment, they could seamlessly access AWS through Single Sign-On (SSO) without needing to complete MFA again.

<b>Process:</b> Enterprise Apps - All Applications - New Application -  Select Application - Create - SSO - SAML - Fill in the required fields - Test.

<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/713428bc269ac77c34b538c4736320105e1f67c1/Screenshot%202026-05-09%20at%2011.18.05.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/5ff53b94d3379ed8d9ea5f71def98c1c61672a78/Screenshot%202026-05-09%20at%2011.21.40.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/7aa433727ca8477626abfcf013f9446b32d1a760/Screenshot%202026-05-09%20at%2011.39.17.png" width="300" height="300"/>

<h3>Roles & Admins (RBAC)</h3> 

The screenshot below shows me creating a user with User Administrator access to manage a smaller group of users within the business. I also created an Administrative Unit that contains one User Administrator who is responsible for managing two other users within that unit.

This shows how Administrative Units can be used to segment different areas of a business by department or location. For example, if I needed to separate a branch in Birmingham, I could create an Administrative Unit specifically for that location and assign a local administrator to manage only those users. This means they would have admin access to their own area of the business without having full administrative rights across the whole organisation.

<b>Process:</b> Create New User - Assignments - Add Roles - Create | Admin Units - Add - Properties - Assign Roles (Example: User Administrator) - Select User - Create | Click into the Unit - Add User or groups.

<img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/398562789e7af032543dbaaeb628122de7018607/Screenshot%202026-05-09%20at%2013.03.50.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src= "https://github.com/NickHoward1/Identity-Access-Management-Labs/blob/5af40b87130d384336ff5dcec00dae79982d661c/Screenshot%202026-05-09%20at%2014.42.36.png" width="300" height="300"/> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

<h2>Outcome</h2>
In this lab, I learned how to navigate my way through Microsoft Entra ID, understand why businesses use it, and recognise the benefits that come with making Identity and Access Management a seamless process. I also gained an understanding of how important Entra ID is for managing changes within an ever-evolving business environment.

Throughout the lab, I carried out a range of tasks that an IAM Analyst would typically perform as part of their day-to-day responsibilities, and I now feel comfortable completing these tasks within a real business environment.

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
