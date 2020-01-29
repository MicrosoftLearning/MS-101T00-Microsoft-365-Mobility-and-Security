# Module 5 - Lab 2 - Exercise 3 - Implement SharePoint Permission Alert


In this exercise you will configure and test an alert that will notify Lynne Robbins when a user is added to the site collection administrators for a SharePoint site collection.

### Task 1 – Create a SharePoint Permissions Alert

1. You should still be logged into the Client 1 VM (LON-CL1) as **lon-cl1\\admin,** and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In the **Microsoft 365 Security &amp; Compliance center**, in the **Alert policies** window, select **+New alert policy**.

3. In the **New alert policy** window, enter the following information:

	- Name: **Site collection admin permissions**

	- Description: **This alert notifies Lynne Robbins when a user is added to the site collection administrators on a SharePoint site collection..**

	- Severity: **Medium**

	- Category: **Permissions**

4. Select **Next.**

5. On the **Choose an activity, conditions and when to trigger the alert** window, enter the following information:

	- Activity is: enter **site collection** into the search box and select **Added site collection admin**

	- How do you want the alert to be triggered? **Every time an activity matches the rule**

12. Select **Next.**

13. On the **Decide if you want to notify people when this alert is triggered** window, enter the following information:

	- Email recipients: Remove **Holly Dickson** and add **LynneR@M365xZZZZZZ.onmicrosoft.com**

	- Daily notification limit: **No limit**

14. Select **Next.**

15. Review your settings. When everything is correct, verify that **Yes, turn it on right away** is active and select **Finish**.

16. Leave the Client 1 VM and the Microsoft 365 admin center and Security and Compliance Center tabs open for the next task.

You have now configured an additional alert policy that monitors when a site collection administrator is added to SharePoint Online site collections.

### Task 2 – Validate the  SharePoint Permissions Alert

In the prior task, you configured an alert that will notify Lynne Robbins when a site collection admin is added to a site collection. To test this alert, Holly Dickson will add Alex Wilber as a site collection admin to the first default site collection named Communication site. This activity should trigger the alert policy that you just created, which should send an alert notification email to Lynne Robbins’ mailbox. You will then switch to the Client 2 VM to see if Lynne received this email. 

1. You should still be logged into the Client 1 VM (LON-CL1) as **lon-cl1\\admin**, and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, open a new tab and enter the following URL in the address bar: **https://M365xZZZZZZ.sharepoint.com/_layouts/15/settings.aspx** (replace ZZZZZZ with the tenant ID provided by your lab hosting provider). This opens the **Site Settings** for the global SharePoint Communication site.

3. On the **Site Settings** window, under **Users and Permissions**, select **Site permissions**. In the list of user permissions for this site, select the **Site Collection Administrators** button from the top pane.

4. Enter **Alex** in the text box and select **Alex Wilber** from the drop-down menu.

5. Select **OK** to add Alex Wilber as site collection admin to the Communication site.

6. Since a new site collection admin has been added, an alert should automatically be sent to Lynne Robbins’ Inbox notifying her of this event.

	‎Switch to the Client 2 VM (LON-CL2) by selecting the **Virtual machine** field at the top of the screen and selecting LON-CL2. 

7. You should still be logged into the Client 2 VM as **lon-cl2\\admin** and into **Outlook on the web** as **Lynne Robbins**. 

8. After a few minutes, an email from the Alerts notification system will be sent to Lynne’s Inbox to let her know that Holly Dickson has added a new site collection admin to a SharePoint site collection. Open the email and review the contents, then close the message.

9. Leave your Client 1 and Client 2 VMs open for the remaining tasks in this lab.

You have now successfully tested the SharePoint alert to monitor site collection admin permissions on SharePoint sites. 


# Proceed to Exercise 4