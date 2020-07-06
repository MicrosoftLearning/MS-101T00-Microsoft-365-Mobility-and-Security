# Module 1 - Lab 1 - Exercise 1 - Set up your Microsoft 365 Tenant

In the labs for this course, you are taking on the role of Holly Dickson, Adatum Corporation&#39;s Enterprise Administrator. Adatum does NOT have legacy, on-premises servers; therefore, you will be implementing Microsoft 365 in a cloud-only deployment. You have deployed Microsoft 365 in a virtualized lab environment, and you have been tasked with completing a pilot project that tests Microsoft 365&#39;s security, compliance, and device management features as they relate to Adatum&#39;s business requirements.

You have just started the pilot project; therefore, in this first lab you will set up a personalized Global Admin tenant account for Holly that will be used throughout all the labs in this course. This first exercise also requires that you perform several setup tasks that will initialize your trial tenant for the remaining labs in this course. You must configure your trial tenant, create a personalized Global Admin account in Microsoft 365, configure several test users and groups that will be used throughout the remaining labs, and turn on Information Rights Management (IRM) in SharePoint Online as well as audit logging.

### Task 1 - Obtain Your Office 365 Credentials

Once you launch the lab, a free trial tenant will be automatically created for you to access Microsoft 365 in the Microsoft Virtual Lab environment. This tenant will be automatically assigned a unique username and password. You must retrieve this username and password so that you can sign into Microsoft 365 within the Microsoft Virtual Lab environment.

1. Because this course can be offered by learning partners using any one of several authorized lab hosting providers, the actual steps involved to retrieve the UPN name, network IP address, and tenant ID associated with your tenant may vary by lab hosting provider. Therefore, your instructor will provide you with the necessary instructions on how to retrieve this information for your course. The information that you should write down for later use includes:

	- **Tenant suffix ID.** This ID is for the onmicrosoft.com accounts that you will use to sign into Microsoft 365 throughout the labs. This is in the format of **{username}@M365xZZZZZZ.onmicrosoft.com**, where ZZZZZZ is your unique tenant suffix ID provided by your lab hosting provider. Record this ZZZZZZ value for later use. When any of the lab steps direct you to sign into the Office 365 or Microsoft 365 portals, you must enter the ZZZZZZ value that you obtained here.
	- **Tenant password.** This is the password for the admin account provided by your lab hosting provider.


### Task 2: Set up the Organization Profile

In your role as Holly Dickson, Adatum&#39;s Enterprise Administrator, you have been tasked with setting up the company&#39;s profile for its Microsoft 365 trial tenant. In this task, you will configure the required options for Adatum&#39;s tenant. Since Holly has yet to create a personal Microsoft 365 user account (you will do this in Task 3), Holly will initially sign into Microsoft 365 as the default Microsoft 365 MOD Administrator account using the Tenant email address and password that was assigned by your lab hosting provider.

1. When the Virtual Machine opens, it opens with the LON-CL1 VM. You should sign into the VM as the **Admin** with a password of **Pa55w.rd**. <br/>

	**Note:** At some point in this task, a blue **Networks** pane may appear on the right side of your screen asking if you want your PC to be discoverable by other PCs and devices on this network. If this pane appears, select **Yes**. During testing, this pane has appeared at various points in the task; sometimes after logging in, other times after logging into Office 365, and even after Office 365 has been used for some time. So please make note that whenever this pane appears, simply select **Yes**.
2. On the taskbar at the bottom of the page, select the **Microsoft Edge** icon. Maximize your browser window when it opens.
3. In your browser go to the **Microsoft Office Home** page by entering the following URL in the address bar: **https://portal.office.com/**
4. In the **Sign in** dialog box, enter **admin@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant suffice ID username provided by your lab hosting provider) and then select **Next**. <br/>

    **Important:** Your Microsoft 365 tenant came with a default system administrator account already created. The name of this user account is **MOD Administrator**. The user name that you just entered, **admin@M365xZZZZZZ.onmicrosoft.com**, is the user name for the MOD Administrator. 
5. In the **Enter password** dialog box, copy and paste in the **Tenant Password** provided by your lab hosting provider for the **admin@M365xZZZZZZ.onmicrosoft.com** account and then select **Sign in**.
6. Close the **Let Microsoft Edge save and fill your password for this site next time?** notification bar at the bottom of the screen by selecting **Never**.
7. On the **Stay signed in?** dialog box, select the **Don't show this again** check box and then select **Yes.**
8. Close the **Get your work done with Office 365** pop-up window.
9. In the **Microsoft Office Home** page, if a pop-up notification for **Office 365 apps** appears, close it by selecting the **Got it!** button.  <br/>

	**Note:** In the top right corner of the screen, notice the initials **MA** that appear in a circle. This is the initials for the MOD Administrator account. If a user has a picture associated with his or her account, that picture will be displayed when the user logs in. Since the MOD Administrator has no picture assigned, the user name initials are displayed instead. <br/>

	In the list of Office 365 apps on the home page, select **Admin**; this opens the **Microsoft 365 admin center.**
10. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select the **Show All** ellipsis … icon to display all the navigation menu options.
11. In the left-hand navigation pane, select **Settings** and then under it, select **Org Settings**. 
12. In the **Org Settings** page, select the **Organization profile** tab.
13. In the **Organization Profile** tab on the **Settings** page, select **Organization information** from the list organization settings.
14. In the **Organization information** pane that appears, enter the following information:

    - Name: **Adatum Corporation** (Note: Contoso is originally displayed as the organization name; this was explained in the Introduction section at the start of this lab. In this step you will change it to Adatum Corporation.)

    - Address: **555 Main Street**

    - City: **Redmond**

    - State: **Washington**

    - Postal Code: **98052**

    - Phone:   **425-555-1234**

    - Technical contact: do not change

    - Preferred language: **English**

15. Select **Save changes**.
16. Scroll to the top of the **Organization information** pane. Note the message indicating the changes have been saved. Select the **X** in the upper right hand corner to close the pane.
17. In the list of organization settings, select **Release preferences**.
18. In the **Release preferences** pane that appears, select the **Targeted release for selected users** option and then select **Save changes**.<br/>

    **Note:** One of the benefits of Microsoft 365 is the ability to have the latest features and updates applied to your environment automatically, which can reduce maintenance costs and overhead for an organization and allow early-adopter users to test new features. By setting up your Release preferences, you can control how and when your Office 365 tenant receives these updates. <br/>

    **Note:** This **Targeted release for selected users** option enables you to create a control group of users who will preview updates so that you can prepare the updates for your entire organization. The **Targeted release for everyone** option is more commonly used in development environments, where you can get updates early for your entire organization. In non-development environments, such as Adatum, targeted release to select people is the more typical preference as it enables an organization to control when it wants to make updates available to everyone once they've been reviewed by the control group.

19. In the **Release preferences** pane, scroll down and select **Select users**.
20. In the **Choose users for targeted release** pane that appears, select inside the **Who should receive targeted releases?** field. This displays the list of active users. In this list, select each of the following users (after selecting the user, you will have to select inside the field again to re-display the list): 

	- **Alex Wilber**
	- **Joni Sherman**
	- **Lynne Robbins**
	- **MOD Administrator** <br/>

    **Note:** Alex, Joni, and Lynne are administrators who are part of Holly's pilot team. Their accounts will be used throughout the labs for this course.
21. Select **Save changes**.
22. Close the **Release preferences** pane. 
23. Tn the list of organization settings, select **Custom themes**.
24. In the **Custom themes** pane, scroll to the bottom of the pane and select the **Show the user's display name** check box. <br/>

	As you scroll through the pane, review the various theme and branding options that are available for you to update. For the purpose of this lab, you can change any of the options or leave the default values as is. For example, you can add the logo of your company and set the background image as the default for all your users. Along with these options you can change the colors for your navigation pane, text color, icon color, and accent color. Go ahead and explore the different options for your tenant and make any changes that you wish. <br/>

	**Note:** Some color patterns aesthetically distract users. If you do change any of the colors, it is recommended that you avoid using high contrasting colors together, such as neon colors and high-resolution colors like bright pink and white.

25. Select **Save changes** when you are done and then close the **Custom themes** pane.
26. Remain logged into the Client 1 VM with Microsoft Edge open to the **Microsoft 365 admin center** for the next task.


### Task 3 - Create a Microsoft 365 Global Admin account

Holly Dickson is Adatum's Enterprise Administrator. Since she doesn't have a personal Microsoft 365 user account set up for herself, Holly initially signed into Microsoft 365 as the company's default MOD Administrator account in the prior task. In this task, she will create a Microsoft 365 user account for herself, and she will assign her user account the Microsoft 365 Global Administrator role, which gives her the ability to perform all administrative functions within Microsoft 365 for the company's Microsoft 365 pilot project. 

**Important:** As a best practice in your real-world deployments, you should always write down the first Global admin account's credentials (in this lab, the MOD Administrator) and store it away for security reasons. This account is a non-personalized identity that owns the highest privileges possible in a tenant. It is **not** MFA activated (because it is not personalized) and the password for this account is typically shared among several users. Therefore, this first Global admin is a perfect target for attacks, so it's always recommended to create personalized service admins and keep as few Global admins as possible. For those Global admins that you do create, they should each be mapped to a single identity, and they should each have MFA enforced.

1. In LON-CL1, in the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users**, and then under it select **Active users**.<br/>

    **Note:** In the **Active users** list, you will see that a list of predefined users has already been created in Microsoft 365. Since you&#39;re taking on the role of Holly Dickson in this lab scenario, you will create a user account for yourself, and you will assign yourself the Microsoft 365 role of Global Administrator.

2. In the **Active Users** window, select **Add a user** on the menu bar.
3. In the **Set up the basics** window, enter the following information:

    - First name: **Holly**

    - Last name: **Dickson**

    - Display name: When you tab into this field, **Holly Dickson** will appear.

    - Username: **Holly**

    - Domain: To the right of the **Username** field is the domain field. This should be prefilled with Adatum&#39;s **M365xZZZZZZ.onmicrosoft.com** cloud domain (where ZZZZZZ is the tenant suffix ID provided by your lab hosting provider).

    - Password settings: select the **Let me create the password** option

    - Password: **Pa55w.rd**

    - Uncheck the **Require this user to change their password when they first sign in** check box

4. Select **Next**.
5. In the **Assign product licenses** window, enter the following information:

    - Select location: **United States**

    - Licenses: Select the **Assign user a product license** option, and then select the **Office 365 E5** check box

6. Select **Next.**
7. In the **Optional settings** window, select the drop-down arrow to the right of **Roles.**
8. In the **Roles** section, select **Admin center access**. By doing so, the most commonly used Microsoft 365 administrator roles are enabled below this option. 

	**Note:** All the admin roles will be displayed if you select **Show all by category**. For Holly, you do not need to view all the admin roles by category, since Holly will be assigned the Global admin role that appears in the list of most commonly used roles.

9. Select **Global admin** and then select **Next**.

10. On the **Review and finish** window, review your selections. If anything needs to be changed, select the appropriate **Edit** link and make the necessary changes. Otherwise, if everything is correct, select **Finish adding**. 

11. On the **Holly Dickson added to active users** page, under the **User details** section, verify Holly's password is **Pa55w.rd** and then select **Close.** 

	**Note:** If you accidentally entered a different password, then once you return to the **Active Users** page, you will need to select the **Reset a password** icon (the key icon that appears when you hover over Holly's account) to change her password to the correct value.

12. If a window appears asking whether you want to respond to a survey on your experience, select **Cancel**.
13. In the **Active Users** list, you should now see Holly&#39;s Microsoft 365 account, with her username of **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).
14. You will now sign out of Microsoft 365 as the MOD Administrator account and log back in as Holly Dickson using her new Microsoft 365 user account.<br/>

    At the top right of the **Microsoft 365 admin center**, select the user icon for the **MOD Administrator** (the **MA** circle), and in the **My account** pane, select **Sign out.**<br/>

    **Important:** When signing out of one user account and signing in as another, you should close all your browser tabs except for your current tab. This is a best practice that helps to avoid any confusion by closing the windows associated with the prior user. Please close all other browser tabs now.

15. Once the **You signed out of your account** window appears, enter the following URL in the address bar: **https://portal.office.com.**
16. In the **Pick an account** window, only the admin account that you just logged out from appears. Select **Use another account**.
17. In the **Sign in** window, enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider). Select **Next**.
18. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.
19. Close the **Get your work done with Office 365** pop-up window.
20. If a **Set your time zone** window appears, enter the following:

    - From the **Language** dropdown select **English (United States)** as your language

    - From the **Time zone** dropdown select your preferred time zone.

    - Select **Save**.

    - Go back to the **Microsoft Office Home** page by entering the following URL in the address bar: **https://portal.office.com**. You will be automatically logged in as **Holly Dickson** with your updated time zone.

21. In the **Microsoft Office Home** page, if a pop-up notification for **Office 365 apps** appears, close it by selecting the **Got it!** button. In the list of Office 365 apps on the home page, select **Admin**; this opens the **Microsoft 365 admin center.**
22. Leave the **Microsoft 365 admin center** tab open and proceed to the next task.


### Task 4 – Set up Microsoft 365 User Accounts and Groups

In the prior task, you noticed that your Microsoft 365 trial tenant came equipped with a list of active users. As Holly Dickson, Adatum&#39;s Enterprise Admin, you have selected the following users to help you with your pilot project: Alex Wilber, Joni Sherman, Lynne Robbins, Patti Fernandez, as well as the system admin, whose user account is the MOD Administrator. 

Each user is a key member of your pilot project team. While their user accounts are already present in Microsoft 365, you need to configure their passwords so that they can more easily sign into Microsoft 365 when needed in the upcoming lab exercises. You also need to add an Office 365 group that will be used in a later lab exercise.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.
2. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users**, and then under it, select **Active users**.
3. In the **Active Users** window, when you hover your mouse over a user's **Display name** (or you select the check mark field to the left of the **Display name**), a **key icon** appears to the right of the user&#39;s name. By selecting the key icon, you can reset a user&#39;s password. You need to reset Alex, Joni, Lynne, adn Patti's passwords to **Pa55w.rd**.<br/>

    Select the key icon for **Alex Wilber**.

4. In the **Reset password** pane for Alex, select **Let me create the password**, enter **Pa55w.rd** in the **Password** field, select and copy this value so that you can paste it in for Joni and Lynne's accounts, and then unselect the **Require this user to change their password when they first sign in** check box.
5. Select **Reset** and then select **Close**.
6. Repeat steps 3-5 for **Joni Sherman**, **Lynne Robbins**, and **Patti Fernandez**. For these three accounts, paste in the **Pa55w.rd** password that you copied for Alex. You do not need to change the password for the **MOD Administrator** because you will continue using the default password provided by your lab hosting provider for this first global admin account that was assigned with the test tenant.
7. In the left-hand navigation pane, select **Groups**, and then under it, select **Groups**.
8. In the **Groups** window, select **Add a group** that appears on the menu bar.
9. In the **Choose a group type** pane, select **Office 365 (recommended)** and then select **Next**.
10. In the **Set up the basics** pane, enter **Sales Group** in the **Name** field. You must select into the **Description** field to enable the **Next** button. Leave the **Description** field blank and select **Next**. 
11. In the **Assign owners** pane, enter **Joni** in the **Owners** field. A list of users whose name starts with Joni will appear; select **Joni Sherman** and then select **Next**.
12. In the **Edit settings** pane, enter **salesgroup** in the **Group email address** field (leave the domain as M365xZZZZZZ.onmicrosoft.com). Under the **Privacy** section, select the **Public – Anyone can see group content** option (even if this option is selected by default, select it again to enable the **Next** button), and leave the **Create a team for this group** check box selected. 
13. In the **Review and finish adding group** pane, review your selections. If anything needs to be corrected, select the corresponding **Edit** option. Select **Create group**.
14. Select the **Close** button on the **New group created** window.
15. This will return you to the **Groups** window. You may need to select the **Refresh** option on the menu bar the page to see the **Sales Group** appear in the list of groups. In fact, you may have to wait a few minutes for the Sales Group to appear, so you may need to select the **Refresh** option on the menu bar once or twice.
12. Once the **Sales Group** appears in the list of groups, select it.
13. In the **Sales Group** pane, select the **Members** tab.
14. Under the **Members** section, select **View all and manage members**.
15. In the **View members** window for the Sales Group, select the **+Add members** button.
16. In the list of users that appears, select **Alex Wilber, Joni Sherman**, and **Lynne Robbins**, select the **Save** button, and then select the **Close** button to finish the add process. <br/>

	**Note:** You will not add Patti Fernandez to this group. Patti's key role in the pilot project is to test the Privileged Identity Management functionality in the next lab exercise. 
17. The **Sales Group** window now displays the three members of the group. Select **Close**.
18. In the **Sales Group** pane, scroll down and verify the three members appear. Select the **X** in the upper right-hand corner to close the window.
19. Leave the **Microsoft 365 admin center** tab open in your browser and proceed to the next task.

### ‎Task 5 - Enable IRM for SharePoint Online 

In this task, you will turn on Information Rights Management (IRM) for SharePoint Online. 

**Note:** While you will validate IRM for Exchange and SharePoint in Lab 4, you must enable IRM for SharePoint Online now because it can take up to 60 minutes or more for IRM to show up in SharePoint Online. By the time you get to the validation exercise in Lab 4, IRM should have finished its internal configuration and you won’t have to wait for it to be present in SharePoint Online.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In the **Microsoft 365 admin center**, select **Show all** (if necessary) in the left-hand navigation pane to see all the navigation options. Under **Admin centers,** select **SharePoint**. This will open the SharePoint admin center.

3. In the **SharePoint admin center**, in the left-hand navigation pane, select **Settings**. 

4. At the bottom of the page is a sentence that says **Can’t find the setting you’re looking for? Go to the classic settings page.** In this sentence, select the hyperlinked text: **classic settings page**.

5. On the **Settings** page, scroll down to the **Information Rights Management (IRM)** section, select the **Use the IRM service specified in your configuration** option, and then select the **Refresh IRM Settings** button.

6. This will return you to the top of the **Settings** page. You must scroll to the bottom of the page to select the **OK** button. In doing so, when you get to the **Information Rights Management (IRM)** section, verify the **Use the IRM service specified in your configuration** option is selected and a **We successfully refreshed your settings** message appears below the **Refresh IRM Settings** button. Continue scrolling to the bottom of the page and select **OK**. 

7. This will return you to the top of the **Settings** page. In your browser, close the current tab (the **m365xZZZZZZ-admin.sharepoint.com** tab).

8. Do **NOT** close the **SharePoint admin center** tab in your Edge browser. Leave your browser open for the next task.


### Task 6 – Turn on Audit Logging to enable Alert Policies

In Lab 3, you will create Alert Policies using the Security and Compliance Center. However, before you can implement alerts, an admin must first turn on Audit Logging for the organization. Since it can take a couple of hours for audit logging to become fully enabled once you turn it on, you will turn it on in this lab so that it&#39;s fully enabled by the time you get to Lab 3.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.
2. In your **Edge** browser, open a new tab and enter the following URL in the address bar: **https://protection.office.com.**
3. In the **Office 365 Security &amp; Compliance center**, in the left-hand navigation pane, select **Search**, and then under it, select **Audit log search**.
4. In the **Audit log search** window, a warning message is eventually displayed at the top of the page. Select the **Turn on auditing** button that appears on the right-side of this message, and then in the **Security &amp; Compliance** dialog box that appears, select **Yes** to confirm that your organization settings need to be updated. <br/>

	**Note:** It may take a couple of minutes for the setting to be updated, at which time the **Security &amp; Compliance** dialog box will disappear.
5. Leave the Client 1 VM and the Security and Compliance Center open and proceed to the next lab.


### Task 7 – Prepare Users for Content Searches

In this exercise, you will add Joni Sherman and Holly Dickson as members of the eDiscovery Manger role. The reason you are doing this now is that it can take a while for newly assigned permissions to successfully propagate. If you waited and assigned Holly and Joni to this role group at the time you performed the Content Search lab in Module 8, you would have received error messages involving parameter fields because their permissions would not have finished propagating. By adding them to this role group now, enough time will elapse for the propagation to complete by the time you get to the Module 8 lab. 

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, if you have the **Security and Compliance Center** open in a tab, then select it; otherwise, open a new tab and enter the following URL in the address bar: **https://protection.office.com**.

3. In the **Office 365 Security and Compliance Center**, in the left-hand navigation pane, select **Permissions.**

4. In the **Home &gt; Permissions** page, select the **eDiscovery Manager** check box.

5. In the **eDiscovery Manager** role group window, scroll down to the **eDiscovery Manager** section and select **Edit**.

6. The **Editing Choose eDiscovery Manager** wizard opens. The list should be empty. Select **Choose eDiscovery Manager**.

7. In the **Choose eDiscovery Manager window**, select **(+) Add**.

8. In the list of users that’s displayed, select **Joni Sherman** and **Holly Dickson**, select **Add**, and then select **Done**. 

9. In the **Editing Choose eDiscovery Manager** window, select **Save**.

10. In the **eDiscovery Manager** window, select **Close**.

11. Leave your browser open and do not close any of the tabs.

# End of Lab 1
