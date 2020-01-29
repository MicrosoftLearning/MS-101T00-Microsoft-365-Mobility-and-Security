# Module 5 - Lab 2 - Exercise 2 - Implement Mailbox Permission Alert


In this exercise you will configure and test an alert that will notify Lynne Robbins when FullAccess permissions are granted to any mailbox within Adatum.

### Task 1 – Create a Mailbox Permission Alert

1. You should still be logged into your Client 1 VM (LON-CL1) as the **lon-cl1\\admin** and into Microsoft 365 as Holly Dickson (**holly@M365xZZZZZZ.onmicrosoft.com)** with a password of **Pa55w.rd**. 

2. In the **Microsoft 365 Security &amp; Compliance center**, in the left-hand navigation pane, select **Alerts,** and then under it, select **Alert policies**.

3. In the **Alert policies** window, select **+New alert policy**.

4. In the **New alert policy** window, enter the following information:

	- Name: **Mailbox permission change**

	- Description: **This alert notifies Lynne Robbins when FullAccess permissions are granted to any mailbox in Adatum.**

	- Severity: **Medium**

	- Category: **Permissions**

5. Select **Next.**

6. On the **Choose an activity, conditions and when to trigger the alert** window, enter the following information:

	- Activity is: enter **mail** into the search box and select **Granted mailbox permission**

	- How do you want the alert to be triggered? **Every time an activity matches the rule**

7. Select **Next.**

8. On the **Decide if you want to notify people when this alert is triggered** window, enter the following information:

	- Email recipients: Remove **Holly Dickson** and add **LynneR@M365xZZZZZZ.onmicrosoft.com**

	- Daily notification limit: **No limit**

9. Select **Next.**

10. Review your settings. When everything is correct, verify that **Yes, turn it on right away** is active and select **Finish**.

11. Leave the Client 1 VM and the Microsoft 365 admin center and Security and Compliance Center tabs open for the next task.

You have now created an activity alert in the Security & Compliance Center that is triggered when FullAccess permissions are granted to any mailboxes.


### Task 2 – Validate the Mailbox Permission Alert

In the prior task, you configured an alert that will notify Lynne Robbins when FullAccess permissions are granted to any mailbox within Adatum. To test this alert, Holly Dickson will change the FullAccess permission on Alex Wilber’s mailbox by granting Joni Sherman FullAccess to his mailbox. This activity should trigger the alert policy that you just created, which should send an alert notification email to Lynne Robbins’ mailbox. You will then log into the Client 2 VM as Lynne Robbins and see if she received this email. 

1. You should still be logged into the Client 1 VM (LON-CL1) as **lon-cl1\\admin**, and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In **Microsoft Edge**, open a new tab and enter the following URL in the address bar: **https://outlook.office365.com/ecp/** . This opens the **Exchange admin center**.

3. Select **recipients** from the left-hand navigation pane.

4. Select **Alex Wilber** from the list and edit his mailbox settings by selecting the pencil icon from the top pane.

5. In the **Edit User Mailbox** window, select **mailbox delegation** from the left-side menu and wait until all settings are loaded.

6. Scroll down to **Full Access** and select the **(+) plus** icon.

7. In the **Select Full Access** window, select **Joni Sherman**, select **add -&gt;**, and then select **OK**.

8. In the **Edit User Mailbox** window, select **Save**.

9. Since **Holly Dickson** has changed the mailbox permissions for Alex Wilbur, an alert should automatically be sent to Lynne Robbins’ Inbox that notifies her of this event.

	‎Switch to the Client 2 VM (LON-CL2) by selecting the **Virtual machine** field at the top of the screen and selecting **LON-CL2**. 

10. In Lab 1, you had signed into the Client 2 VM as **lon-cl2\\admin**, and you logged into Outlook as the MOD Administrator. You should sign out of the MOD Administrator account by selecting the **MA** user icon in the upper-right corner of the screen, and then in the **My Account** pane, select **Sign out**. 

11.  Once you’re signed out, enter the following URL in the address bar: **https://outlook.office365.com**

12. In the **Sign in** window, enter **LynneR@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant ID provided by your lab hosting provider) and then select **Next**.

13. In the **Enter Password** window, enter **Pa55w.rd** as the password and select **Sign in**. 

14. In the **Stay signed in** window, select **Yes** and if a feedback window appears, close the window.

15. In the notification bar at the bottom of the page asking if you want to **Let Microsoft Edge save and prefill your password for this site next time**, select **Never**. 

16. In the **Welcome** window, select the **X** to close it.

17. In **Outlook on the web**, in Lynne Robbins’ **Inbox**, an email should be received from the Alerts notification system (**Office365Alerts@microsoft.com**) to let her know that Holly Dickson has made a Mailbox permission change. Open the email and review the contents, then close the message.

18. Leave your Client 1 and Client 2 VMs open for the remaining tasks in this lab.

You have just successfully tested a mailbox permission alert that sent an alarm message on granting FullAccess to a user mailbox.

# Proceed to Exercise 3