# Module 13 - Lab 6 - Exercise 2 - Implement Windows Information Protection  

Now that you have implemented Azure Information Protection as part of your pilot project at Adatum, you’re now ready to implement Windows Information Protection. In this exercise, in your role as Holly Dickson, you will create a WIP policy (Client App protection policy for Windows) that is applied to any member of the WIP Users group who has an MDM enrolled device in Intune.

### Task 1 – Configure Windows Information Protection

In this lesson you will create a WIP policy and assign it to the WIP Users group that you created in an earlier lab. 

1. Switch to the Client 1 VM (LON-CL1). You should still be logged into your Client 1 VM as the **lon-cl1\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson.** 

2. In **Microsoft Edge**, if you have the Azure portal open in a tab, then select it now; otherwise, enter **https://portal.azure.com/** and, if necessary, sign in as **holly@M365xZZZZZZ.onmicrosoft.com.**

3. In the **Azure portal**, if a window displays indicating **You have free Azure Advisor recommendations**, then close the window now.

4. In the **Azure portal**, in the left-hand navigation bar, select **All services.**

5. In the **All services** window, enter **client** in the **Search** box at the top of the window, and then in the right-hand pane, select **Client apps.**

6. In the **Client apps** window, in the middle pane under **Manage**, select **App protection policies**.

7. In the **Client apps – App protection policies** window, in the right-hand pane, select **+Create a policy** from the top menu bar. **Select Windows 10**

8. On **Basics** tab enter name **WIP Client Protection**, under **enrollement state** click **drop down** and choose  **wiht enrollement** and then select **Next**.

9. on **Targeted apps** tab, under Protected apps select **+Add**, scroll to the bottom and select **Office-365-ProPlus-1810-Allowed.xml** click **Ok** and select **Next**.

10. On the **Required settings** tab, select **Block** for **Windows information protection mode**.

11. In the **Corporate identity field**, verify that it says **M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID.) and click **Next**

12.  On the **Assignments tab** under **Included groups** click **+Select groups to include**, choose **WIP Users** click **Select** and click **Next**.  

13. On the **Review settings** tab click **Create**.

14. In the **App protection policies** list observer the **WIP Client Protection** policy status under deployed should indicate **Yes**
If the status under deployed indicates **NO**, wait a few minutes and refresh the page till the deplyed status changes to **Yes**.

15. Leave your Client 1 VM and browser open for the next lab.

You have now created an **App protection policy** (which is a Windows Information Protection policy) that protects files in Office 365 ProPlus for users with enrolled devices in the **WIP Users** group.


### Task 2 – Use Windows Information Protection

In this exercise you will enroll the Client 2 VM (LON-CL2) to Azure AD and test the Windows Information Protection policy that you created in the prior task by creating a work document and then copy and pasting from it to a personal location. This will test the WIP protection feature that prevents copy and pasting between a protected Word document and an untrusted website in your Edge browser Since the WIP policy that you created was assigned to the WIP Users group, you must switch to the Client 2 VM and create the document while signed in as Joni, who is one of the members of the WIP Users group.

1. Switch to your Client 2 VM (LON-CL2) as the **lon-cl2\admin** account, and you should be logged into Microsoft 365 as **Joni Sherman**. 

2. In the **Search** box on the taskbar at the bottom of the window, type **Work**. In the menu that appears, select **Access work or school**.

3. Below **Access work or school**, select **Connect**.

4. Enter **JoniS@M365xZZZZZZ.onmicrosoft.com** to the **Email address** field and select **Next**.

5. On the **Enter password** window, enter **Pa55w.rd** and select **Sign in**.

6. A **More information required** window appears. Select **Next**.

7. Leave the first dropdown on **Authentication phone** and select your country from the dropdown below.

8. Enter your mobile phone number to the text field right to your country and select **Next**.  <br/>

	‎**Note**: To continue enrolling the LON-CL2 VM and to test WIP in this lab, you need to enter your real mobile phone number and confirm the authentication SMS code.

9. When you receive the code for Microsoft verification on your mobile phone, enter it in the **Additional security verification** window. If the verification is successful, select **Done**.

10. If a **Sorry, your sign-in timed out. Please sign in again.** message appears, enter **Pa55w.rd** and select **Sign in**. If an additional SMS verification window appears, retry the SMS verification.

11. In the **Enter PIN** window select the **X** to close it.

12. Open **Microsoft Word**. 

13. Select **Blank document**.

14. If a **What’s New** window opens, close it.

15. In the document, type **Protected business content**.

16. Select **File** from the menu bar above the ribbon, select **Save As** on the left menu, and then select **Browse** from the **Save As** menu.

17. In the **File Explorer** window, you should see a **lock symbol** that appears to the left of the **File name** field. Next to this lock symbol is a drop-down arrow. Select this arrow, and in the menu that appears, select **Work (m365xZZZZZZ.onmicrosoft.com).**

18. Accept the default file name **Protected business content.docx**, change the file path to your **Documents** folder and select **Save**.

19. In the Word document, select the sentence that you typed back in step 5, then right-click on the selected text and select **Copy**.

20. In your **Edge** browser, open a new tab and enter the following URL in the address bar: **https://www.bing.com**.

21. On the **Bing** page, right-click into the search field and select **Paste**.

22. A pop-up window should appear with the following message: **Can’t use work content here.** Select **OK**.

23. Leave your Client 2 VM and browser open for the next lab.

You have just enrolled the Client 2 VM to your tenant, so the Client app protection policy **WIP Client Protection** that you configured in the last task could be applied to protect the content of a Word document.


# End of Lab 6
