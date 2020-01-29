# Module 5 - Lab 2 - Exercise 4 - Test the Default eDiscovery Alert


In this exercise you will test a default Microsoft 365 alert policy that will notify all tenant admins, such as Holly Dickson, when an eDiscovery case has been created or exported.

**Note:** An eDiscovery alert of this nature is important because an eDiscovery search, when left unregulated, can pull sensitive content that can be exported to an unauthorized source.

### Task 1 – Review the default eDiscovery Alert

In this task, you will verify whether a default Microsoft 365 alert is triggered when somebody in your tenant creates an eDiscovery case or exports data from an existing case. Holly Dickson is a part of the Tenant Admins in your tenant and will be one of the recipients of this alert. 

1. You should still be logged into the Client 1 VM (LON-CL1) as **lon-cl1\\admin,** and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, select the **Microsoft 365 Security &amp; Compliance Center** tab.

3. In the **Microsoft 365 Security &amp; Compliance Center**, in the left-hand navigation pane, select **Alerts** and then select **Alert policies**.

4. Search for the Alert policy with the name **eDiscovery search started or exported** and then select it.

5. In the right-side pane you can now see the settings of this default alert. You should then verify the settings are configured as following:

	- Conditions: **Activity is eDiscoverySearchStartedOrExported**

	- Aggregation: **Single event**

	- Scope: **All users**

	- Email recipients: **TenantAdmins**

6. If all settings are correct, select the **Close** button to close the Window.

You have now reviewed the default Microsoft 365 eDiscovery alert that notifies tenant admins when an eDiscovery case is created or exported.

### Task 2 – Validate the default eDiscovery Alert

To test this default alert, Holly Dickson will create an eDiscovery case. This activity should trigger the alert policy, which should send an alert notification email to all tenant admins. Since Holly is a Tenant Admin, she should receive this alert. 

1. You should still be logged into the Client 1 VM (LON-CL1) as **lon-cl1\\admin,** and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, select the **Microsoft 365 Security &amp; Compliance Center** tab. 

3. In the **Microsoft 365 Security &amp; Compliance Center**, in the left-hand navigation pane, select **eDiscovery**, and then under it, select **eDiscovery**.

4. On the **eDiscovery** window, select **+Create a case**.

5. In the **New case** window, enter the following information:

	- Case Name: **Testing eDiscovery Alerts**

	- Case description: **This case will be used for testing the default Microsoft 365 eDiscovery alert.**

6. Select **Save**.

7. When an eDiscovery case is created, an alert should automatically be sent to the Inbox of all users with tenant admin permissions. 

8. Open a new tab in your browser and go to **Outlook on the web** by entering the following URL in the address pane: **https://outlook.office365.com**

9. After a few minutes, an email from the Alerts notification system will be sent to Holly’s **Inbox** to inform her that an eDiscovery case was created. Open the email and review the contents, then close the message.

10. In your **Edge** browser, switch back to the **Microsoft 365 Security &amp; Compliance Center** tab and select **Audit Log Search** in the left-side navigation pane. 

11. At the bottom of the page, select the **Search** button to display all recent activity. This will display the activity that created this alert. 

12. Leave your Client VMs open for the remaining labs in this course.  

You have now successfully tested the default Microsoft 365 eDiscovery alert that monitors the creation of an eDiscovery case or data export from an existing case.


# End of Lab 2