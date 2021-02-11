# Module 1 - Lab 1 - Exercise 1 - Set up your Microsoft 365 Tenant

In the labs for this course, you are taking on the role of Holly Dickson, Adatum Corporation's Enterprise Administrator. Adatum does NOT have legacy, on-premises servers; therefore, you will be implementing Microsoft 365 in a cloud-only deployment. You have deployed Microsoft 365 in a virtualized lab environment, and you have been tasked with completing a pilot project that tests the security, compliance, and device management features in Microsoft 365 as they relate to Adatum's business requirements.

You have just started the pilot project; therefore, in this first lab you will set up a personalized Microsoft 365 user account for Holly that will be used throughout all the labs in this course. This first exercise also requires that you perform several setup tasks that will initialize your trial tenant for the remaining labs in this course. You must configure your trial tenant, create a personalized Global Admin user account in Microsoft 365 for Holly, configure several test users and groups that will be used throughout the remaining labs, and turn on Information Rights Management (IRM) in SharePoint Online as well as audit logging.

### Task 1 - Obtain Your Office 365 Credentials

Once you launch the lab, a free trial tenant will be automatically created for you to access Microsoft 365 in the Microsoft Virtual Lab environment. Within this tenant, your lab hosting provider will create a Microsoft 365 user account for a default tenant administrator named MOD Administrator. Your lab hosting provider will assign this user account a unique username and password, and the account will be assigned the Microsoft 365 Global administrator role. You must retrieve this username and password so that you can sign into Microsoft 365 within the Microsoft Virtual Lab environment.

1. Because this course can be offered by learning partners using any one of several authorized lab hosting providers, the actual steps involved to retrieve the tenant prefix, tenant ID, and tenant password associated with your trial tenant may vary by lab hosting provider. Therefore, your instructor will provide you with the necessary instructions on how to retrieve this information for your course. The information that you should write down for later use includes:

	- **Tenant prefix.** This tenant prefix is for the Microsoft 365 user accounts that you will use to sign into Microsoft 365 throughout the labs in this course. The domain for each Microsoft 365 user account is in the format of {user alias}@xxxxxZZZZZZ.onmicrosoft.com, where xxxxxZZZZZZ is the tenant prefix. It consists of two parts - your lab hoster's prefix (xxxxx; some hosters use a generic prefix such as M365x, while others use their company initials or some other designation) and the tenant ID (ZZZZZZ; usually a 6 digit number). Record this xxxxxZZZZZZ tenant prefix value for later use. When any of the lab steps direct you to sign into Microsoft 365 as one of the user accounts (such as the MOD Administrator), you must enter the xxxxxZZZZZZ value that you obtained here as the tenant prefix portion of your .onmicrosoft.com domain.

	- **Tenant password.** This is the password provided by your lab hosting provider for the tenant admin account.


### Task 2: Set up the Organization Profile

In your role as Holly Dickson, Adatum's Enterprise Administrator, you have been tasked with setting up the company's profile for its Microsoft 365 trial tenant. In this task, you will configure the required options for Adatum's tenant. Since Holly has yet to create a personal Microsoft 365 user account (you will do this in Task 3), Holly will initially sign into Microsoft 365 as the default Microsoft 365 MOD Administrator account using the Tenant email address and password that was assigned by your lab hosting provider.

1. When you open your lab hosting provider's Virtual Machine environment, you need to begin with the Client 1 VM (LON-CL1). If your VM environment opens with one of the other machines, then switch to the LON-CL1 VM now.

2. On **LON-CL1**, you must select **Ctrl+Alt+Delete** to log in (your instructor will guide you on how to find this option in your VM environment). Log into LON-CL1 as the **Admin** (or Administrator) account with the password **Pa55w.rd**. 

3. If you receive a **Networks** warning message asking if you want this PC to be discoverable by other PCs and devices on this network, select **Yes**.

4. On the taskbar at the bottom of the page, select the **Microsoft Edge** icon. Maximize your browser window when it opens.

5. In your browser go to the **Microsoft Office Home** page by entering the following URL in the address bar: **https://portal.office.com/** 

6. In the **Sign in** dialog box, copy and paste in the **Tenant Username** provided by your lab hosting provider (**admin@xxxxxZZZZZZ.onmicrosoft.com**, where xxxxxZZZZZZ is the tenant prefix assigned by your lab hosting provider) and then select **Next**.

7. In the **Enter password** dialog box, copy and paste in the **Tenant Password** provided by your lab hosting provider and then select **Sign in**.

8. On the **Stay signed in?** dialog box, select the **Don’t show this again** check box and then select **Yes.** 

9. In the top right corner of the screen, notice the initials **MA** that appear in a circle. These are the initials of the **MOD Administrator** account, which is the tenant admin account created by your lab hosting provider. If any of the other Microsoft 365 user accounts that were created by your lab hosting provider have a picture associated with the account, that picture will be displayed when the user logs in. When a user such as the MOD Administrator has no picture assigned to it, the user's initials are displayed in place of the picture. 

10. If a **Get your work done with Office 365** window appears, then close it now. 

11. On the **Microsoft Office Home** tab, in the column of Microsoft 365 app icons that appear on the left side of the screen, scroll down and select the **Admin** icon; this opens the **Microsoft 365 admin center** in a new browser tab.
	
12. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Show all** and then select **Settings**. In the Settings group, select **Org settings**. 

13. On the **Org settings** page, the **Services** tab is displayed by default. Select the **Organization profile** tab.

14. In the **Organization profile** tab on the **Org settings** page, select **Organization information** from the list of profile data.

15. In the **Organization information** pane that appears, enter the following information:

    - Name: **Adatum Corporation** (Note: Contoso is originally displayed as the organization name; this was explained in the Introduction section at the start of this lab. In this step you will change it to Adatum Corporation.)

    - Street Address: **555 Main Street**

    - City: **Redmond**

    - State or province: **Washington**

    - ZIP or postal code: **98052**

    - Phone: do not change

    - Technical contact: do not change

    - Preferred language: **English**

16. Select **Save**.

17. Scroll to the top of the **Organization information** pane. Note the message indicating the changes have been saved. Select the **X** in the upper right-hand corner to close the pane.

18. Back on the **Organization profile** tab, in the list of organization profile data, select **Release preferences**.

19. In the **Release preferences** pane that appears, select the **Targeted release for select users** option and then select **Save**.<br/>

    **Note:** One of the benefits of Microsoft 365 is the ability to have the latest features and updates automatically applied to your environment, which can reduce maintenance costs and overhead for an organization and allow early-adopter users to test new features. By setting up your Release preferences, you can control how and when your Microsoft 365 tenant receives these updates. <br/>

    **Note:** This **Targeted release for select users** option enables you to create a control group of users who will preview updates so that you can prepare the updates for your entire organization. The **Targeted release for everyone** option is more commonly used in development environments, where you can get updates early for your entire organization. In non-development environments, such as Adatum, targeted release to a select group of users is the more typical preference as it enables an organization to control when it wants to make updates available to everyone once they've been reviewed by the control group.

20. In the **Release preferences** pane, below the list of release options, select **Select users**.

21. In the **Choose users for targeted release** pane that appears, select inside the **Who should receive targeted releases?** field. This displays the list of active users (these are the ten Microsoft 365 user accounts created for your tenant by your lab hosting provider). In this list, select each of the following users (Note: You have to select each user, one at a time; after selecting a user, you will have to select inside the field again to re-display the list so that you can display the next user): 

	- **Alex Wilber**
	- **Joni Sherman**
	- **Lynne Robbins**
	- **MOD Administrator** <br/>

    **Note:** Alex, Joni, and Lynne are administrators who are part of Holly's pilot team. Their accounts will be used throughout the labs for this course.
    
22. Select **Save**.

23. After selecting the users, scroll to the bottom of the **Release preferences** pane to verify you selected the required users. Close the **Release preferences** pane once you verified these four users were selected. 

24. Tn the list of organization profile data, select **Custom themes**.

25. In the **Custom themes** pane, scroll to the bottom of the pane and select the **Show the user's display name** check box. <br/>

	As you scroll through the pane, review the various theme and branding options that are available for you to update. For the purpose of this lab, you can change any of the options or leave the default values as is. For example, you can add the logo of your company and set the background image as the default for all your users. Along with these options you can change the colors for your navigation pane, text color, icon color, and accent color. Go ahead and explore the different options for your tenant and make any changes that you wish. <br/>

	**Tip:** Some color patterns aesthetically distract users. If you do change any of the colors, it is recommended that you avoid using high contrasting colors together, such as neon colors and high-resolution colors like bright pink and white.

26. Select **Save** when you are done and then close the **Custom themes** pane.

27. Remain logged into LON-DC1 with Microsoft Edge open to the **Microsoft 365 admin center** for the next task.



### Task 3 - Create a Microsoft 365 Global Admin account

Holly Dickson is Adatum’s Enterprise Administrator. Since a Microsoft 365 user account has not been set up for her, she initially signed into Microsoft 365 as the MOD Administrator account (the default Global admin) in the previous lab (you did this when you began your role as Holly and signed in using the tenant admin account). In this task, you will continue in your role as Holly Dickson where you should still be logged into Microsoft 365 as the MOD Administrator. In this lab, Holly will create a personal Microsoft 365 user account for herself, and she will assign her user account the Microsoft 365 Global Administrator role, which gives her the ability to perform all administrative functions within Microsoft 365. Following this task, you will perform all remaining labs using Holly's persona. 

**Important:** As a best practice in your real-world deployment, you should always write down the first Global admin account’s credentials (in this lab, the MOD Administrator account, whose username is admin@xxxxxZZZZZZ.onmicrosoft.com, where xxxxxZZZZZZ is the tenant prefix assigned by your lab hosting provider) and store it away for security reasons. **This account should be a non-personalized identity** that owns the highest privileges possible in a tenant. It should **not** be MFA activated (because it is not personalized). Because the username and password for this account are typically shared among several users, this first Global admin is a perfect target for attacks; therefore, it is always recommended that organizations create personalized service admin accounts and keep as few Global admins as possible. For those Global admins that you do create in your real-world deployment, they should each be mapped to a single identity (such as Holly Dickson), and they should each have Multi-Factor Authentication (MFA) enforced. That being said, you will not turn on MFA for Holly's account because time is limited in this training course and we do not want to take up lab time by making you log in using a second authentication method every time Holly logs in.

**Note:** While your lab hosting provider has created a custom domain for Adatum (xxxUPNxxx.xxxCustomDomainxxx.xxx), they did not finish the setup process for the domain; in a later lab exercise, you will finish provisioning the new domain. That being said, your lab hosting provider should have left your Microsoft 365 tenant's **xxxxxZZZZZ.onmicrosoft.com** domain as the default domain for Adatum. In this task, you will begin by verifying whether this domain is listed as the default domain. If your lab hosting provider set the new custom domain as the default, you will change it to the xxxxxZZZZZZ.onmicrosoft.com domain. This has implications in that when you add a new user account (such as the one for Holly Dickson that you will add in this task) or email addresses for new groups (later in this exercise), you want the xxxxxZZZZZZ.onmicrosoft.com domain to show as the default domain for the user and groups.

1. On the LON-CL1 VM, the **Microsoft 365 admin center** should still be open in your Microsoft Edge browser from the prior lab, and you should be signed into Microsoft 365 as the **MOD Administrator**. 

2. You will begin by verifying which domain is listed as the default domain for Adatum. In the **Microsoft 365 admin center**, in the left-hand navigation pane, under the **Settings** group select **Domains**.

3. On the **Domains** page, you should see the two domains created by your lab hosting provider - the **xxxxxZZZZZZ.onmicrosoft.com** domain and the **xxxUPNxxx.xxxCustomDomainxxx.xxx** domain. <br/>

	If the **xxxxxZZZZZZ.onmicrosoft.com*** domain displays **(Default)** next to the domain name, then skip to the next step as no change is needed. <br/>

	However, if the **xxxUPNxxx.xxxCustomDomainxxx.xxx** domain displays **(Default)** next to the domain name, then select the circle with the check mark to the left of the **xxxxxZZZZZZ.onmicrosoft.com** domain and then select **Set as default** on the menu bar. <br/>
	
	In the **Set this domain as default?** dialog box that appears, select **Set as default**. In the list of domains, the **xxxxxZZZZZZ.onmicrosoft.com** domain should now display **(Default)** next to the domain name.

4. You will now create a Microsoft 365 user account for Holly Dickson. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users** and then select **Active users**. 

5. In the **Active users** list, you will see the list of existing user accounts that were created for you by your lab hosting provider. In this task, you are taking on the role of the MOD Administrator, and as such, you must create a user account for Holly Dickson, who is Adatum's new Enterprise Administrator. In doing so, you will assign Holly the Microsoft 365 role of Global Administrator, which gives Holly global access to most management features and data across Microsoft online services. 

6. In the **Active Users** window, select **Add a user** that appears on the menu bar above the list of active users, then select **Single user** from the submenu. 

7. In the **Set up the basics** window, enter the following information:

	- First name: **Holly**

	- Last name: **Dickson** 

	- Display name: When you tab into this field, **Holly Dickson** will appear.

	- Username: **Holly** <br/>
	
		‎**IMPORTANT:** To the right of the **Username** field is the domain field. It should be prefilled with the **xxxxxZZZZZZ.onmicrosoft.com** cloud domain (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider). However, if your lab hosting provider set the custom **xxxUPNxxx.xxxCustomDomainxxx.xxx** domain as Adatum's default domain and you did not change the default domain to the **xxxxxZZZZZZ.onmicrosoft.com** domain earlier in this task, then the custom domain will appear here instead. If that happens, select the drop-down arrow in this domain field and select **xxxxxZZZZZZ.onmicrosoft.com**. You should also perform steps 2-3 to change **xxxxxZZZZZZ.onmicrosoft.com** to the default domain as this is needed in the next task. <br/>
	
		After configuring this field, Holly’s username should appear as:<br/>

		**Holly@xxxxxZZZZZZ.onmicrosoft.com**  
	
	- Clear (uncheck) the **Automatically create a password** checkbox which will enable a new box for entering a custom password.

	- In the new Password box enter: **Pa55w.rd** (Hint: Select the eye icon at the right side of the field to verify the password that you entered)

	- Clear (uncheck) the **Require this user to change their password when they first sign in** check box 

8. Select **Next**.

9. In the **Assign product licenses** window, enter the following information:

	- Select location: **United States**

	- Licenses: The **Assign user a product license** option should be selected by default; under this option, select **Office 365 E5** 

10. Select **Next.**

11. In the **Optional settings** window, select the drop-down arrow to the right of **Roles.** 

12. In the **Roles** section, the **User (no admin center access)** option is selected by default. Select the **Admin center access** option instead. By doing so, the most commonly used Microsoft 365 administrator roles are displayed below this option. 

	**Note:** If you scroll down past this list of the most commonly used admin roles and select **Show all by category**, the complete list of admin roles will be displayed (sorted by category). For Holly, you do not need to view all the admin roles by category, since Holly will be assigned the Global admin role that appears in the list of most commonly used roles.

13. Select the **Global admin** check box and then select **Next**.

14. On the **Review and finish** window, review your selections. If anything needs to be changed, select the appropriate **Edit** link and make the necessary changes. Otherwise, if everything is correct, select **Finish adding**. 

15. On the **Holly Dickson added to active users** page, under the **User details** section, select **Show** next to the password to verify Holly's password is **Pa55w.rd** and then select **Close.** 

	**Note:** If you accidentally entered a different password, then once you return to the **Active Users** page, you will need to select the **Reset a password** icon (the key icon that appears when you hover over Holly's account) to change her password to the correct value.

16. Remain logged into LON-CL1 with the Microsoft 365 admin center open in your browser for the next task.


### Task 4 – Set up Microsoft 365 User Accounts and Groups

After completing the previous task, you should still be signed into the **Microsoft 365 admin center** as the **MOD Administrator** account. In this task, you will begin implementing Adatum’s Microsoft 365 pilot project as Holly Dickson, Adatum’s new Enterprise Administrator. Therefore, you will begin this task by logging out of Microsoft 365 as the MOD Administrator and you will log back in as Holly.

In the prior task, you noticed that your Microsoft 365 trial tenant came equipped with a list of active users. As Holly Dickson, Adatum's Enterprise Admin, you have selected the following users to help you with your pilot project: Alex Wilber, Joni Sherman, Lynne Robbins, Patti Fernandez, as well as the system admin, whose user account is the MOD Administrator. 

Each user is a key member of your pilot project team. While their user accounts are already present in Microsoft 365, you need to configure their passwords so that they can more easily sign into Microsoft 365 when needed in the upcoming lab exercises. You also need to add a Microsoft 365 group that will be used in a later lab exercise.

1. On the LON-CL1 VM, the **Microsoft 365 admin center** should still be open in your Microsoft Edge browser from the prior task, and you should be signed into Microsoft 365 as the **MOD Administrator**. <br/>

	On the **Microsoft 365 admin center** tab, select the user icon for the **MOD Administrator** (the **MA** circle) in the upper right corner of your browser, and in the **MOD Administrator** window that appears, select **Sign out.** <br/>
	
	**Important:** When signing out of one user account and signing in as another, you should close all your browser tabs except for your current tab. This is a best practice that helps to avoid any confusion by closing the windows associated with the prior user. Take a moment now and close all other browser tabs except for the **Sign out** tab. 
	
2. In your Microsoft Edge browser, in the **Sign out** tab, enter the following URL in the address bar to sign back into Microsoft 365: **https://portal.office.com**. 

3. In the **Pick an account** window, only the tenant admin account (the admin@xxxxxZZZZZZ.onmicrosoft.com account) that you just logged out from appears. Select **Use another account**. 

4. In the **Sign in** window, enter **Holly@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider). Select **Next**.

5. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.

6. If a **Get your work done with Office 365** window appears, select the **X** to close it. 

7. On the **Microsoft Office Home** tab, in the column of Microsoft 365 app icons that appear on the left side of the screen, scroll down and select the **Admin** icon; this opens the **Microsoft 365 admin center** in a new browser tab.

8. If a survey window appears, select **Cancel**.

9. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users**, and then under it, select **Active users**.

10. In the **Active Users** window, when you hover your mouse over a user's **Display name** (or you select the check mark field to the left of the **Display name**), a **key icon** appears to the right of the user's name. By selecting the key icon, you can reset a user's password. You need to reset Alex, Joni, Lynne, and Patti's passwords to **Pa55w.rd**.<br/>

    Select the key icon for **Alex Wilber**.

11. In the **Reset password** pane for Alex, select clear (uncheck) the **Automatically create a password** checkbox, enter **Pa55w.rd** in the **Password** field, select and copy this value so that you can paste it in for Joni and Lynne's accounts, and then unselect the **Require this user to change their password when they first sign in** check box.

12. Select **Reset** and then select **Close**.

13. Repeat steps 10-12 for **Joni Sherman**, **Lynne Robbins**, and **Patti Fernandez**. For these three accounts, paste in the **Pa55w.rd** password that you copied for Alex. You do not need to change the password for the **MOD Administrator** because you must continue using the default password provided by your lab hosting provider for this tenant admin account.

14. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Groups**, and then under it, select **Active groups**.

15. In the **Active groups** window, select **Add a group** that appears on the menu bar.

16. In the **Choose a group type** pane, select **Microsoft 365 (recommended)** and then select **Next**.

17. In the **Set up the basics** pane, enter **Sales Group** in the **Name** field. You must select the **Description** field to enable the **Next** button. Leave the **Description** field blank and select **Next**. 

18. In the **Assign owners** pane, enter **Joni** in the **Owners** field. A list of users whose name starts with Joni will appear; select **Joni Sherman** and then select **Next**.

19. In the **Edit settings** pane, enter **salesgroup** in the **Group email address** field (Note: the domain should be the xxxxxZZZZZZ.onmicrosoft.com domain, which you should have verified in a prior task is the default domain for Adatum). <br/>

	Under the **Privacy** section, select the **Public – Anyone can see group content** option (even if this option is selected by default, select it again to enable the **Next** button), and leave the **Create a team for this group** check box selected. Select **Next**.

20. In the **Review and finish adding group** pane, review your selections. If anything needs to be corrected, select the corresponding **Edit** option. When everything is correct, select **Create group**.

21. Once the group is created, select the **Close** button on the **New group created** window.

22. This will return you to the **Groups** window. You may need to select the **Refresh** option on the menu bar for the **Sales Group** to appear in the list of groups. In fact, you may have to wait a few minutes for the Sales Group to appear, so you may need to select the **Refresh** option on the menu bar once or twice.

23. Once the **Sales Group** appears in the list of groups, select it.

24. In the **Sales Group** pane that appears, the **General** tab is displayed by default. Select the **Members** tab.

25. In the **Members** tab, under the **Owners** section, Joni Sherman should appear as the only group owner. Under the **Members** section, select **View all and manage members**.

26. In the **View members** window for the Sales Group, select the **+Add members** button.

27. In the list of users that appears, select **Alex Wilber, Joni Sherman**, and **Lynne Robbins**, select the **Save** button, and then select the **Close** button to finish the add process. <br/>

	**Note:** You will not add Patti Fernandez to this group. Patti's key role in the pilot project is to test the Privileged Identity Management functionality in the next lab exercise. 

28. The **Sales Group** window now displays the three members of the group. Select **Close**.

29. Close the **Sales Group** pane by selecting the **X** in the upper right-hand corner.

30. Leave the **Microsoft 365 admin center** tab open in your browser and proceed to the next task.


### ‎Task 5 - Enable IRM for SharePoint Online 

In this task, you will turn on Information Rights Management (IRM) for SharePoint Online. 

**Note:** While you will validate IRM for Exchange and SharePoint in Lab 4, you must enable IRM for SharePoint Online now because it can take up to 60 minutes or more for IRM to show up in SharePoint Online. By the time you get to the validation exercise in Lab 4, IRM should have finished its internal configuration and you won’t have to wait for it to be present in SharePoint Online.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In the **Microsoft 365 admin center**, select **Show all** (if necessary) in the left-hand navigation pane to see all the navigation options. Under **Admin centers,** select **SharePoint**. This will open the SharePoint admin center.

3. In the **SharePoint admin center**, in the left-hand navigation pane, select **Settings**. 

4. At the bottom of the **Settings** page is a sentence that says **Can’t find the setting you’re looking for? Go to the classic settings page.** In this sentence, select the hyperlinked text: **classic settings page**.

5. On the classic **Settings** page, scroll down to the **Information Rights Management (IRM)** section, select the **Use the IRM service specified in your configuration** option, and then select the **Refresh IRM Settings** button.

6. This will return you to the top of the **Settings** page. You must scroll to the bottom of the page to select the **OK** button. In doing so, when you get to the **Information Rights Management (IRM)** section, verify the **Use the IRM service specified in your configuration** option is selected and a **We successfully refreshed your settings** message appears below the **Refresh IRM Settings** button. Continue scrolling to the bottom of the page and select **OK**. 

7. This will return you to the top of the **Settings** page. In your browser, close the current tab (the **xxxxxZZZZZZ-admin.sharepoint.com** tab).

8. Do **NOT** close the **SharePoint admin center** tab in your Edge browser. Leave your browser open for the next task.


### Task 6 – Turn on Audit Logging to enable Alert Policies

In Lab 3, you will create Alert Policies using the Security and Compliance Center. However, before you can implement alerts, an admin must first turn on Audit Logging for the organization. Since it can take a couple of hours for audit logging to become fully enabled once you turn it on, you will turn it on in this lab so that it's fully enabled by the time you get to Lab 3.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. <br/>

	Select the **Microsoft 365 admin center** tab in your Edge browser. 

2. In the **Microsoft 365 admin center**, select **Show all** (if necessary) in the left-hand navigation pane to see all the navigation options. Under **Admin centers,** select **Security**. This will open the Office 365 Security and Compliance center.

3. In the **Office 365 Security &amp; Compliance center**, in the left-hand navigation pane, select **Search**, and then under it, select **Audit log search**.

4. In the **Audit log search** window, a warning message is displayed at the top of the page. Select the **Turn on auditing** button that appears on the right-side of this message, and then in the **Security &amp; Compliance** dialog box that appears, select **Yes** to confirm that your organization settings need to be updated. <br/>

	**Note:** It may take several minutes for the setting to be updated, at which time the **Security &amp; Compliance** dialog box will disappear.

5. Leave the Client 1 VM and the Security and Compliance Center open and proceed to the next lab.


### Task 7 – Prepare Users for Content Searches

In Module 8, you will perform a Content Search lab that requires that Joni Sherman and Holly Dickson be members of the eDiscovery Manager role. In this exercise, you will add Joni and Holly to this role. The reason you are doing this now is that it can sometimes take up to an hour or more for newly assigned permissions to successfully propagate. If you waited and assigned Holly and Joni to this role group at the time you performed the Content Search lab in Module 8, you would receive error messages involving parameter fields because their permissions would not have finished propagating. By adding them to this role group now, enough time will elapse for the propagation to complete by the time you get to the Module 8 lab. 

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, you should still have the **Office 365 Security and Compliance Center** open in a tab from the prior task. If you closed that tab, then in the **Microsoft 365 admin center**, under the **Admin centers** group, select **Security**.

3. In the **Office 365 Security and Compliance Center**, in the left-hand navigation pane, select **Permissions.**

4. In the **Home &gt; Permissions** page, select the **eDiscovery Manager** check box.

5. In the **eDiscovery Manager** pane that appears, scroll down to the **eDiscovery Manager** section and select **Edit role group**.

6. The **Editing Choose eDiscovery Manager** wizard opens. The list of users who are assigned this role should be empty. Select **Choose eDiscovery Manager**.

7. In the **Choose eDiscovery Manager window**, select **(+) Add**.

8. In the list of users that’s displayed, select **Joni Sherman** and **Holly Dickson**, select **Add**, and then select **Done**. 

9. In the **Editing Choose eDiscovery Manager** window, select **Save**.

10. In the **eDiscovery Manager** window, select **Close**.

11. Leave your browser open and do not close any of the tabs.

# End of Lab 1
