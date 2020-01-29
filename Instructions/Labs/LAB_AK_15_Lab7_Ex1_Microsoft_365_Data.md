# Module 15 - Lab 7 - Exercise 1 - Investigate Your Microsoft 365 Data


In your role as Holly Dickson, Adatum’s Enterprise Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, you now want to test how Adatum can investigate its Microsoft 365 data. You have decided to focus on performing a content search for deleted emails, which is a common request at Adatum, and then you want to analyze eDiscovery functionality by creating an eDiscovery case. You’ll conclude this portion of the pilot project by creating a GDPR data subject request.

### Task 1 – Perform a content search for deleted emails

In this exercise, you will add Joni Sherman and Holly Dickson as members of the eDiscovery Manger role, and then you’ll log into the Client VM as Joni and perform a content search that looks for emails with the keyword IP address.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **lon-cl1\\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, if you have the **Security and Compliance Center** open in a tab, then select it; otherwise, open a new tab and enter the following URL in the address bar: **https://protection.office.com**.

3. In the **Office 365 Security and Compliance Center**, in the left-hand navigation pane, select **Permissions.**

4. In the **Home &gt; Permissions** page, select the **eDiscovery Manager** check box.

5. In the **eDiscovery Manager** role group window, scroll down to the **eDiscovery Manager** section and select **Edit**.

6. The **Editing Choose eDiscovery Manager** wizard opens. The list should be empty. Select **Choose eDiscovery Manager**.

7. In the **Choose eDiscovery Manager window**, select **(+) Add**.

8. In the list of users that’s displayed, select **Joni Sherman** and **Holly Dickson**, and then select **Add**.  <br/>

    ‎**Note:** You are adding Joni to the eDiscovery Manager role group for later use in this exercise, and you assigning Holly to the role group for use in the next exercise.

9. You should see a banner with the message **2 members added**. Select **Done** and then **Save**.

10. Switch to the Client 2 VM (LON-CL2). You should still be logged into LON-CL2 as the **lon-cl2\\admin** account, and you should be logged into Microsoft 365 as **Joni Sherman** from the prior lab. 

11. If you have a tab open in your **Edge** browser for the **Microsoft 365 Security and Compliance Center**, then select it now. Otherwise, select a new tab and enter the following URL in the address bar: **https://protection.office.com**.

12. In the **Security and Compliance Center**, in the left-hand navigation pane, select **Search**, and then under it select **Content search**.  <br/>

    ‎**Note**: If you cannot see **Search** in the navigation pane yet, you need to reload the browser tab with the **Security and Compliance Center.**

13. On the **Content search** window, in the **Searches** tab, select **(+) Guided search** on the top menu. This will initiate the **New search** wizard.

14. On the Name your search page, enter **Content Search Test** into the **Name** field and then select **Next**.

15. On the Locations page, select **All locations** and then select **Next**.

16. On the Condition card page, enter **IP address** into the Keywords box and then select **Finish**.

17. Back on the Searches tab, the Search query will run. The Status field in the bottom-left corner of the screen will indicate when the query is complete. It may take a couple of minutes for the query to run and the data to be displayed in the right-hand pane. When the content search finishes, you will see all mailbox items that you have created for the sensitive information test of your custom DLP policy. 

18. Leave the Client 2 VM open as well as all browser tabs and continue with the next task.

You have successfully assigned an eDiscovery role to Joni and performed a content search for a specific key word across all locations of your tenant.

 

### Task 2 – Create an eDiscovery case

In this task, you will create an eDiscovery case with a configured hold and content search for any violations regarding IP addresses. You will continue using Joni Sherman’s user account. Having been assigned the eDiscovery Managers role in the prior task, Joni has the permissions necessary to create an eDiscovery case.

1. You should still be logged into your Client 2 VM (LON-CL2) as the **lon-cl2\\admin** account and signed into Microsoft 365 as Joni Sherman. However, if you have been signed out of Microsoft 365, then on the Microsoft 365 sign-in page, sign into Joni’s **JoniS@M365xZZZZZZ.onmicrosoft.com** account using a password of **Pa55w.rd**.

2. The **Security and Compliance Center** should still be open in a tab in Microsoft Edge. If so, select that tab now. If not, then enter the following URL in the address bar: **https://protection.office.com.** 

3. In the **Security and Compliance Center**, in the left-hand navigation pane, select **eDiscovery**, and then under it, select **eDiscovery**.

4. On the **eDiscovery** window, select **(+) Create a case** on the top menu.

5. In the **New case** window, enter **IP Address Violation** into the **Case name** field and select **Save**.

6. Back on the **eDiscovery** page, select **Open** that appears to the left of the **IP Address Violation** case.

7. On the **IP Address Violation** window, select the **Holds** tab from the top menu.

8. Select **(+) Create** to create a new hold. This initiates the **Create a new hold** wizard.

9. On the **Name your hold** page, enter **IP Address Violation - Content** into the **Name** field and then select **Next**.

10. On the **Choose locations** page, For the location **Exchange email**, select the **Choose users, groups or teams** field.

11. On the **Edit locations** page, select **Choose users, groups or teams** again.

12. On the **Exchange email** page, Enter **Lynne** into the search field select the Search icon on the right side of the field. 

13. Scroll down on the page, and under **Users, groups, or teams**, select **Lynne Robbins** from the search results.

14. Select **Choose** and then select **Done**.

15. On the **Choose locations** page, **1 user, group, or team** is displayed to the right of **Exchange email**. Select **Next**.

16. On the **Query conditions** page, enter **IP address** into the **Keywords** box and then select **Next**.

17. On the **Review you settings** page, review the values and select **Edit** next to any that need to be modified. When you are satisfied with the settings, select **Create this hold.**

18. Back on the **eDiscovery Case overview**, on the **IP Address Violation &gt; Core ED** page, select the **Searches** tab from the top menu.

19. Select **(+) New search.** 

20. In the **New search** window, in the **Search query** pane on the left, enter **IP Address** in the **Keywords** field and then under **Locations**, select **Locations on hold**.

21. Select **Save &amp; run**.

22. In the **Save search** window, enter **IP Address Violation - Search** into the **Name** field and then select **Save**.

23. This will initiate a search query that looks for the keywords **IP Address**. Once the query is finished, wait for the preview results to be displayed. 

You have now created an eDiscovery case, added an In-Place Hold to preserve mailbox content, and created a search to discover data from the hold.


# Proceed to Exercise 2