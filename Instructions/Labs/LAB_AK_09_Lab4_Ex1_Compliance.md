# Module 9 - Lab 4 - Exercise 1 - Initialize Compliance 

In your role as Holly Dickson, Adatum’s Enterprise Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, your next steps are to implement archiving and retention at Adatum. You will begin by initializing compliance through the MDM auto-enrollment of new devices in your tenant. You will then configure retention tags and policies, and you will implement archiving with MRM retention tags. 

### Task 1 - Create a Group for Compliance Testing

To test archiving and retention in your Adatum pilot project, you will create a new mail-enabled security group and assign two users to the group – Joni Sherman and Lynne Robbins. These will be your two test users involved in the Windows Information Protection (WIP) pilot program. This group will then be used in the next task when you configure MDM auto-enrollment for new devices in your tenant. 

1. At the end of the prior lab, you were using the LON-CL2 VM. Switch to the LON-CL1 VM. You should still be logged into LON-CL1 as the **lon-cl1\\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In **Microsoft Edge**, select the **Microsoft 365 admin center tab** or open a new tab and go to **https://admin.microsoft.com.** 

3. the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Groups** and then select **Groups** below it.

4. Select **Add a group** to create a new group for compliance testing. 

5. In the **Add a group** window, enter the following information:

6. Fill all the fields to create the **WIP Users** group:

	- Type: **Mail-enabled security**

	- Name **WIP Users**

	- Group email address: tab into this field and **wipusers** is automatically pre-filled for you as the alias of the group email address

	- Group email address domain: to the right of the group email address alias is the email address domain. **M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) should be displayed here.

7. Select **Add**, and then select **Close**.

8. In the **Microsoft 365 admin center** tab, refresh the page to display the WIP users group in the list of Groups. You may have to wait a minute or two before you see the WIP users group.

9. Once **WIP Users** appears In the **Groups** window, select it.

10. In the **WIP Users** window, select the **Members** tab. 

11. In the **Members** tab, under the **Members** section, select **View and manage members**.

12. In the **View members** window, select **+Add members**. This displays the list of users.

13. In the list of users, select **Joni Sherman** and **Lynne Robbins**, then scroll to the bottom of the list and select **Save**, and then select **Close**.  <br/>

	‎**Note:** It may take a few minutes for both Joni and Lynne to display in the list of users. Simply refresh the list until both users appear.

14. Close the **WIP users** window.

15. Leave your browser open to the Microsoft 365 admin center and proceed to the next task.


### Task 2 – Configure Mobile Device Management Auto-enrollment

In this task you will activate MDM auto-enrollment for new devices in your Adatum Corporation tenant. The devices will belong to members of the WIP Users group that you created in Azure AD in the prior task. You will also configure Intune as your mobile device management authority. Activating MDM auto-enrollment is required so that you can implement Windows Information Protection in a later lab.

1. In **Microsoft Edge**, select a new tab and enter the following URL in the address bar: **https://portal.azure.com**.

2. On the **Welcome to Azure** page, select **Continue to Azure Portal website.**

3. If a **Welcome to Microsoft Azure** dialog box appears, select **Maybe later.**

4. In the **Microsoft Azure** portal, in the left-hand navigation pane, select **All Services**.

5. In the **All services** window, type **Azure Active Directory** in the search box, and then select **Azure Active Directory**, which will appear in the right-hand pane.

6. This returns the **Adatum Corporation – Overview** page. Under the **Manage** section in the middle of the page, scroll down and select **Mobility (MDM and MAM)**.

7. In the right-hand pane, select **Microsoft Intune**.

8. This returns the **Configure** window. For the **MDM User scope** option, select **Some.** This will display a **Groups** section. 

9. Select the **Groups** section and then select the arrow on the right-hand side of the section. 

10. In the **Select groups** pane, scroll down through the list of groups, select **WIP Users**, and then at the bottom of the pane select **Select**.

11. This returns the **Configure** window. Select **Restore default MDM URLs** to ensure the correct URLs are set.

12. Select **Save** on the menu bar at the top of the page.

13. In the left-hand navigation pane in the Azure portal, select **All Services.**

14. In the **All services** window, type **Intune** in the search box, and then select **Intune**, which will appear in the right-hand pane.

15. This returns the **Microsoft Intune – Overview** page. Under the **Manage** section in the middle of the page, select **Device enrollment.**

16. In the **Choose MDM Authority** pane in the middle of the screen, you are requested to choose whether Intune or Configuration Manager is your mobile device management authority. Scroll to the bottom of the pane, select **Intune MDM Authority,** and then select **Choose**.

17. In your Microsoft Edge browser, you can close the Azure portal tab, which should return you to the Microsoft 365 admin center tab.

You have configured automatic enrollment in Intune for devices of users in the WIP Users security group.


# Proceed to Exercise 2