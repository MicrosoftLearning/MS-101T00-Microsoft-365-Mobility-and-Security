# Module 3 - Lab 1 - Exercise 2 - Set up your Microsoft 365 Tenant

In the labs for this course, you are taking on the role of Holly Dickson, Adatum Corporation&#39;s Enterprise Administrator. Adatum does NOT have legacy, on-premises servers; therefore, you will be implementing Microsoft 365 in a cloud-only deployment. You have deployed Microsoft 365 in a virtualized lab environment, and you have been tasked with completing a pilot project that tests Microsoft 365&#39;s security, compliance, and device management features as they relate to Adatum&#39;s business requirements.

You have just started the pilot project; therefore, in this first lab you will set up a personalized Global Admin tenant account for Holly that will be used throughout all the labs in this course. In addition, as part of managing your Microsoft 365 security services, you will edit an ATP Safe Links policy and create a Safe Attachment policy to protect your environment against malware.

This first exercise requires that you perform some setup tasks that will initialize your trial tenant for the remaining labs in this course. You must configure your trial tenant, create a personalized Global Admin account in Microsoft 365, and configure several test users that will be used throughout the remaining labs.

### Task 1 - Obtain Your Office 365 Credentials

Once you launch the lab, a free trial tenant will be automatically created for you to access Microsoft 365 in the Microsoft Virtual Lab environment. This tenant will be automatically assigned a unique username and password. You must retrieve this username and password so that you can sign into Microsoft 365 within the Microsoft Virtual Lab environment.

1. Because this course can be offered by learning partners using any one of several authorized lab hosting providers, the actual steps involved to retrieve the UPN name, network IP address, and tenant ID associated with your tenant may vary by lab hosting provider. Therefore, your instructor will provide you with the necessary instructions on how to retrieve this information for your course. The information that you should write down for later use includes:

	- **Tenant suffix ID.** This ID is for the onmicrosoft.com accounts that you will use to sign into Microsoft 365 throughout the labs. This is in the format of **{username}@M365xZZZZZZ.onmicrosoft.com**, where ZZZZZZ is your unique tenant suffix ID provided by your lab hosting provider. Record this ZZZZZZ value for later use. When any of the lab steps direct you to sign into the Office 365 or Microsoft 365 portals, you must enter the ZZZZZZ value that you obtained here.
	- **Tenant password.** This is the password for the admin account provided by your lab hosting provider.
	- **UPN name (in the format XXYYZZa) and the network IP address.** Write down the **IP Address** value (this is the IP Address of your parent domain; for example, 64.64.206.13), as well as your **UPN name** (for example, AVEAH2a).

### Task 2: Set up the Organization Profile

In your role as Holly Dickson, Adatum&#39;s Enterprise Administrator, you have been tasked with setting up the company&#39;s profile for its Microsoft 365 trial tenant. In this task, you will configure the required options for Adatum&#39;s tenant. Since Holly has yet to create a personal Microsoft 365 user account (you will do this in Task 3), Holly will initially sign into Microsoft 365 as the default Microsoft 365 MOD Administrator account using the Tenant email address and password that was assigned by your lab hosting provider.

1. When the Virtual Machine opens, it opens with the Client 1 VM (LON-CL1). You should sign into the VM as the **Admin** with a password of **Pa55w.rd**.
2. On the taskbar at the bottom of the page, select the **Microsoft Edge** icon. Maximize your browser window when it opens.
3. In your browser go to the **Microsoft Office Home** page by entering the following URL in the address bar: **https://portal.office.com/**
4. In the **Sign in** dialog box, copy and paste in the **Tenant Email** account provided by your lab hosting provider and then select **Next**.
5. In the **Enter password** dialog box, copy and paste in the **Tenant Password** provided by your lab hosting provider and then select **Sign in**.
6. Close the **Let Microsoft Edge save and fill your password for this site next time?** banner by selecting **Never**.
7. On the **Stay signed in?** dialog box, select the **Don't show this again** check box and then select **Yes.**
8. Close the **Get your work done with Office 365** pop-up window.
9. In the **Microsoft Office Home** page, select the **Admin** app. This opens the **Microsoft 365 admin center.**
10. If a feedback window appears, select **Cancel**.
11. If the **Good morning/afternoon/evening, MOD Administrator** pop-up window appears, select **Get started**.

    **Important:** Your Microsoft 365 tenant came with a default system administrator account already created. The name of this user account is **MOD Administrator**, which is the name that was displayed in this pop-up window. The username for this MOD Administrator account is **admin@M365xZZZZZZ.onmicrosoft.com**, which is the username provided by your lab hosting provider. When you sign into Office 365 with this **admin@M365xZZZZZZ.onmicrosoft.com** username, the user initials of **MA** (for MOD Administrator) will display in a circle as the user icon in the upper right corner of the Office 365 screens.

12. If you receive a **Networks** warning message asking if you want this PC to be discoverable by other PCs and devices on this network, select **No.**
13. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select the **Show All** ellipsis … icon to display all the navigation menu options.
14. In the left-hand navigation pane, select **Settings** and then under it, select **Organization profile**.
15. In the **Settings** window, select the **Organization profile** tab and select **Organization information**.
16. In the **Organization information** window, it displays Contoso as the organization name. 

    **Note:** The Contoso organization name was explained in the Introduction section at the start of this lab. In the following steps, you will change it to Adatum Corporation.

17. In the **Organization information** window, enter the following information:

    - Name: **Adatum Corporation**

    - Address: **555 Main Street**

    - City: **Redmond**

    - State: **Washington**

    - Postal Code: **98052**

    - Phone:   **425-555-1234**

    - Technical contact: do not change

    - Preferred language: **English**

18. Select **Save**.
19. Select **Close.**
20. Select **Release preferences**.
21. In the **Release preferences** window, select **targeted release for selected users** and then select **Save changes**.<br/>

    **Note:** One of the benefits of Microsoft 365 is the ability to have the latest features and updates applied to your environment automatically, which can reduce maintenance costs and overhead for an organization and allow early-adopter users to test new features. By setting up your Release preferences, you can control how and when your Office 365 tenant receives these updates.

22. In the **Are you sure you want to change to Targeted release for select people** window, select **Yes**.

    **Note:** This option enables you to create a control group of users who will preview updates so that you can prepare the updates for your entire organization. The **Targeted release for everyone** option is more commonly used in development environments, where you can get updates early for your entire organization. In non-development environments, such as Adatum, targeted release to select people is the more typical preference as it enables an organization to control when it wants to make updates available to everyone once they've been reviewed by the control group.

23. In the **Release preferences** window, select **Select users.**
24. In the **Choose users for targeted release** window, search for **Alex Wilber**, **Joni Sherman**, **Lynne Robbins**, and **MOD Administrator**, select the users and then select **Save changes**.<br/>

    **Note:** Alex, Joni, and Lynne are administrators who are part of your pilot team. Their accounts will be used throughout the labs for this course.

25. Select **Close**. This returns you to the **Organization Profile** window.
26. Select **Custom themes**.
27. In the **Custom themes** window, you can add the logo of your company and set the background image as the default for all your users. Along with these options you can change the colors for your navigation pane, text color, icon color, and accent color.Go ahead and explore some different options for your tenant. Make any changes that you wish.<br/>

    **NOTE:** Some colors patterns aesthetically distract users. Avoid using high contrasting colors together, such as neon colors and high-resolution colors like white and bright pink.

28. Once you're done exploring and making any further changes, select **Save changes** and then **Close**.
29. Remain logged into the Client 1 VM with Microsoft Edge open to the Microsoft 365 admin center for the next task.


### Task 3 - Create a Microsoft 365 Global Admin account

Holly Dickson is Adatum&#39;s Enterprise Administrator. Since she doesn&#39;t have a personal Microsoft 365 user account set up for herself, Holly initially signed into Microsoft 365 as the default Microsoft 365 MOD Administrator account in the prior task. In this task, she will create a Microsoft 365 user account for herself, and she will assign her user account the Microsoft 365 Global Administrator role, which gives her the ability to perform all administrative functions within Microsoft 365 for the company&#39;s Microsoft 365 pilot project.

**Important:** As a best practice in your real-world deployments, you should always write down the first global admin account&#39;s credentials (in this lab, the MOD Administrator) and store it away for security reasons. This account is a non-personalized identity that owns the highest privileges possible in a tenant. It is **not** MFA activated (because it is not personalized) and the password for this account is typically shared among several users. Therefore, this first global admin is a perfect target for attacks, so it&#39;s always recommended to create personalized service admins and keep as few global admins as possible. For those global admins that you do create, they should each be mapped to a single identity, and they should each have MFA enforced.

1. In your Client 1 VM (LON-CL1), in the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users**, and then under it select **Active users**.<br/>

    **Note:** In the **Active users** list, you will see that a list of predefined users has already been created in Microsoft 365. Since you&#39;re taking on the role of Holly Dickson in this lab scenario, you will create a user account for yourself, and you will assign yourself the Microsoft 365 role of Global Administrator.

2. In the **Active Users** window, select **Add a user**.
3. In the **Set up the basics** window, enter the following information:

    - First name: **Holly**

    - Last name: **Dickson**

    - Display name: When you tab into this field, **Holly Dickson** will appear.

    - Username: When you tab into this field, **Holly** will appear; leave this as the username

    - Domain: To the right of the **Username** field is the domain field. This should be prefilled with Adatum&#39;s **M365xZZZZZZ.onmicrosoft.com** cloud domain.

    - Password settings: select the **Let me create the password** option

    - Password: **Pa55w.rd**

    - Uncheck the **Make this user change their password when they first sign in** checkbox

4. Select **Next**.
5. In the **Assign product licenses** window, enter the following information:

    - Select location: **United States**

    - Licenses: Under **Assign user a product license**, select **Office 365 E5**

6. Select **Next.**
7. In the **Optional settings** window, select the drop-down arrow to the right of **Roles.**
8. In the **Roles** section, uncheck **User (no administrator access).** By doing so, all the Microsoft 365 administrator roles are available to be assigned. Select **Global Administrator** and then select **Next**.
9. On the **You&#39;re almost done – review and finish adding** window, review your selections. If anything needs to be changed, select the appropriate **Edit** link and make the necessary changes. Otherwise, if everything looks good, select **Finish adding**.
10. On the **Holly Dickson has been added** page, select **Close.**
11. If a screen appears that asks you to provide feedback on your experience, select **Cancel** to close it.
12. In the **Active Users** list, you should now see Holly&#39;s Microsoft 365 account, with her username of **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).
13. You will now sign out of Microsoft 365 as the MOD Administrator account and log back in as Holly Dickson using her new Microsoft 365 user account.<br/>

    At the top right of the **Microsoft 365 admin center**, select the user icon for the **MOD Administrator** (the **MA** circle), and in the **My account** pane, select **Sign out.**<br/>

    **Important:** When signing out of one account and signing in as another, you should close all your browser tabs except for your current tab. This is a best practice that helps to avoid any confusion by closing the windows associated with the prior user. Please close all other browser tabs now.

14. Once the **You signed out of your account** window appears, enter the following URL in the address bar: **https://portal.office.com.**
15. In the **Pick an account** window, only the admin account that you just logged out from appears. Select **Use another account**.
16. In the **Sign in** window, enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider). Select **Next**.
17. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.
18. Close the **Get your work done with Office 365** pop-up window.
19. If a **Set your time zone** window appears, enter the following:

    - From the **Language** dropdown select **English (United States)** as your language

    - From the **Time zone** dropdown select your preferred time zone.

    - Select **Save**.

    - Go back to the **Microsoft Office Home** page by entering the following URL in the address bar: **https://portal.office.com**. You will be automatically logged in as **Holly Dickson** with your updated time zone.

20. In the **Microsoft Office Home** page, select the **Admin** tile to open the Microsoft 365 Admin Center.
21. In the **Good morning/afternoon, Holly Dickson** pop-up window, select **Get started**.
22. Leave the Microsoft 365 admin center tab open and proceed to the next task.

### Task 4 – Set up Microsoft 365 User Accounts and Groups

In the prior task, you noticed that your Microsoft 365 trial tenant came equipped with a list of active users. As Holly Dickson, Adatum&#39;s Enterprise Admin, you have selected several of these user accounts to help you with your pilot project – Alex Wilber, Joni Sherman, Lynne Robbins, as well as the system admin, whose user account is MOD Administrator. Each is an administrator at Adatum, and they&#39;re key members of your pilot project team. While their user accounts are already present in Microsoft 365, you need to configure their passwords so that they can more easily sign into Microsoft 365 when needed in the upcoming lab exercises. You also need to add an Office 365 group that will be used in a later lab exercise.

1. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users**, and then under it, select **Active users**.
2. In the **Active Users** window, when you select a user account (by selecting the checkmark field to the left of the user's name), a **key icon** appears to the right of the user&#39;s name. By selecting the key icon, you can reset a user&#39;s password. You need to reset Alex, Joni, and Lynne&#39;s passwords to Pa55w.rd.<br/>

    Select the user account for Alex Wilber, then select the key icon that appears to the right of his name.

3. In the **Reset password** window for Alex, select **Let me create the password**, enter **Pa55w.rd** in the **Password** field, and then unselect the **Require this user to change their password when they first sign in** check box.
4. Select **Reset** and then select **Close**.
5. Repeat steps 2-4 for **Joni Sherman** and **Lynne Robbins**. You do not need to do this for the **MOD Administrator** account because you will continue using the default password provided by your lab hosting provider for this first global admin account that was assigned with the test tenant.
6. In the left-hand navigation pane, select **Groups**, and then under it, select **Groups**.
7. In the **Groups** window, select **Add a group**.
8. In the **New Group** window, enter the following information:

    - Type: **Office 365**

    - Name: **Sales Group**

    - Group email address: **salesgroup** (leave the domain as M365xZZZZZZ.onmicrosoft.com)

    - Privacy: **Public – Anyone can see group content**

    - Owner: select **+Select owner**, and in the **Sales group** window, in the **Owner** field, select **Joni Sherman** from the user list

9. Select **Add**, and then once the group is added, select **Close**.
10. This will return you to the **Groups** window. You may need to refresh the page to see the **Sales group** appear in the list of groups.
11. Select the **Sales group**.
12. In the **Sales group** window, select the **Members** tab.
13. Under the **Members** section, select **View all and manage members**.
14. In the **View members** window, select **+Add members**.
15. In the list of users that appears, select **Alex Wilber, Joni Sherman**, and **Lynne Robbins**, select the **Save** button that appears at the top of the page, select **Close**, and then select **Close** again.
16. The **Sales group** window now displays the three members of the group. Close this window.
17. Leave the Microsoft 365 admin center tab open and proceed to the next task.

### ‎Task 5 - Enable IRM for SharePoint Online 

In this task, you will turn on Information Rights Management (IRM) for SharePoint Online. 

**Note:** While you will validate IRM in Exchange and SharePoint in Lab 3, you must enable IRM for SharePoint Online now because it can take up to 60 minutes or more for IRM to show up in SharePoint Online. By the time you get to the validation exercise in Lab 3, IRM should have finished its internal configuration and you won’t have to wait for it to be present in SharePoint Online.

1. You should still be logged into your Client 1 VM as the **lon-cl1\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In the **Microsoft 365 admin center**, scroll down through left-hand navigation pane and under **Admin centers,** select **SharePoint**. This will open the SharePoint admin center.

3. If a **One place for SharePoint administration** pop-up window appears, select **Got it** to close the window.

4. In the **SharePoint admin center**, in the left-hand navigation pane, select **Settings**. 

5. At the bottom of the page is a sentence that says **“Can’t find the setting you’re looking for? Go to the classic settings page.”** In this sentence, select the hyperlinked text: **classic settings page**.

6. On the **Settings** page, scroll down to the **Information Rights Management (IRM)** section, select the **Use the IRM service specified in your configuration**, select the **Refresh IRM Settings** button, and then scroll down to the bottom of the page and select **OK**. 

7. Do NOT close the SharePoint admin center tab in your Edge browser. Leave your browser open for the next task.

### Task 6 – Turn on Audit Logging to enable Alert Policies

In Lab2, you will create Alert Policies using the Security and Compliance Center. However, before you can implement alerts, an admin must first turn on Audit Logging for the organization. Since it can take a couple of hours for audit logging to be fully enabled once you turn it on in the Security and Compliance Center, you will turn it on in this lab so that it&#39;s fully enabled by the time you get to Lab 2.

1. You should still be logged into your Client 1 VM as the **lon-cl1\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.
2. In your **Edge** browser, enter the following URL in the address bar: **https://protection.office.com.**
3. In the **Office 365 Security &amp; Compliance center**, in the left-hand navigation pane, select **Search**, and then under it, select **Audit log search**.
4. In the **Audit log search** window, select **Turn on auditing,** and then confirm the **Your organization settings need to be updated. Do you want to continue?** question by selecting **Yes**.
5. Leave the Client 1 VM and the Security and Compliance Center open and proceed to the next task.


# Proceed to Exercise 3
