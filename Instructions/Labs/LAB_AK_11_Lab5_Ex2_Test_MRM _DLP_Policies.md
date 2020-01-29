# Module 11 - Lab 5 - Exercise 2 - Test MRM and DLP Policies


You are now at the point in your pilot project where you want to test policies. You have decided to test an MRM policy that affects how email messages are archived, and then you want to test a DLP policy related to emails that contain sensitive information. 

### Task 1 – Test an MRM Policy to Archive Email Messages

In this exercise, you will send an email from Holly Dickson to one of your test users, Lynne Robbins. You will then log into Microsoft 365 as Lynne on the Client 2 VM, locate the email in her Inbox, and then assign the email a custom retention tag that you created. This personal retention tag will override the parent folder tag for this specific message, which will be moved to Lynne’s In-Place archive mailbox after 3 years rather than 2 years.

1. You should still be logged into your Client 1 VM as the **lon-cl1\\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In **Microsoft Edge**, If you have an **Outlook on the web** tab open for Holly, then select it now; otherwise, navigate to **https://outlook.office.com** and sign in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) using a password of **Pa55w.rd.** 

3. If **Outlook** **on the web** was already open, then verify that you are logged in as **Holly** by checking the user icon in the upper right corner (the **HD** circle). If you enter **Outlook on the web** as **MOD Administrator**, repeat the steps from lab 1 by logging out as the MOD Administrator, closing all **Edge** windows, and then logging back in as Holly.

4. In **Outlook on the web**, in the upper left corner of the screen, select **+New message**. 

5. In the message pane that appears on the right-side of the screen, enter the following information:

	- To: start typing **Lynne** and a drop-down menu displays with users whose name begins with that. Select **Lynne Robbins**.

	- Add a subject: **Archive Test**

	- Message area: type **Use this email to test archiving.**

6. Send the message by selecting either **Send** at the top of the message pane or the **Send** button at the bottom of the pane.

7. Switch to the Client 2 VM (LON-CL2) in the **Virtual machine** field at the top of the VM.

8. In the **Edge** browser, if there are still signed in sessions, sign out of the current user account and close all **Edge** browser tabs.

9. Open your **Edge** browser, maximize the window and enter the following URL in the address bar: **https://outlook.office365.com**

10. You want to sign into **Outlook on the web** as **Lynne Robbins.** If the **Pick an account** window appears, Lynne’s account won’t appear since she hasn’t signed in before. Therefore, select **Use another account**. 

11. In the **Sign in** window, enter **LynneR@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and then select **Next.**

12. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.

13. In the **Stay signed in?** window, select **Don’t show this again** and then select **Yes**.

14. If you approach the site for the first time, you will be asked for your language setting and your time zone:

	- From the **Language** dropdown select **English (United States).**

	- From the **Time zone** dropdown select your preferred time zone.

15. Select **Save**.

16. If a window is displayed asking whether you want to try the new outlook, select **Try the new Outlook.**

17. If a **Welcome** window appears, then close it now.

18. In **Outlook on the web**, in Lynne’s **Inbox**, you should see the email message that Holly just sent to Lynne.

19. Back in Lab 3, you changed the assigned retention policy for Lynne’s mailbox to **Office Retention Policy**. This policy contains the **3 Year Move – Archive after three years** personal retention tag that you created in Lab 3. <br/>

	‎Upon receiving this email from Holly, Lynne has decided to tag Holly’s email to automatically archive it after three years instead of two years, which is the default policy.  <br/>
	
	‎To accomplish this, begin by selecting the **Settings** icon in the upper right corner of the toolbar (the gear-shaped icon).

20. In the drop-down menu that appears, scroll to the bottom of the menu and select **View all Outlook settings**. 

21. In the **Settings** window that appears, the **Mail** option is already selected by default in the left-hand pane. In the center pane, select **Retention policies**. 

22. In the **Retention policies** pane that appears on the right side of the screen, select **+Add new policy**. 

23. In the **Retention policies** pane, select the **3 Years Move - Archive after three years** retention tag and select the **Save** button at the top of the pane.

24. Close the **Settings** window by selecting the **X** in the upper right corner. This returns you to Lynne’s mailbox.

25. In the **Inbox**, right-click the message that she received from Holly with the subject: **Archive Test**. 

26. In the menu that appears, scroll to the bottom and select **Assign Policy**. In the **Assign Policy** menu that appears, under **Archive Policy**, select **3 Years Move - Archive after three years.**  <br/>

	‎**Note:** This personal retention policy will now override the parent folder policy for this specific message, which will be moved to Lynne’s In-Place archive mailbox after 3 years.

27. Leave Outlook open in the Client 2 VM as you will return there as Lynne in the next task after receiving another email from Holly.


### Task 2 – Test a DLP Policy for Sensitive Emails

In the previous exercise, you created a custom DLP policy that searches emails for sensitive information related to IP addresses in your Adatum tenant. In this exercise, you will send an email with an IP address from Holly Dickson to Lynne Robbins.

1. Switch to the Client 1 VM (LON-CL1), in which you should still be logged into Microsoft 365 as Holly Dickson (**holly@M365xZZZZZZ.onmicrosoft.com)** with a password of **Pa55w.rd**. 

2. You will now send an email from Holly to Lynne; the email will contain an IP address. In **Microsoft Edge**, the **Outlook on the web** tab should still be open for Holly. Select the **Outlook on the web** tab.

3. In the upper left corner of the screen, select **+New message**. 

4. In the message pane that appears on the right-side of the screen, enter the following information:

	- To: start typing **Lynne** and a drop-down menu displays with users whose name begins with that. Select **Lynne Robbins**.

	- Add a subject: **DLP Policy Test**

	- Message area: type **I will configure this IP address: 192.168.0.1.**

5. Wait a moment until the message is saved as a draft, at which point a policy tip is displayed above your message fields in the right-hand pane.

6. Select **Send.**

7. You will now send a second message from Holly to Lynne that contains multiple IP addresses.   <br/>

	‎In **Outlook**, in the upper left corner of the screen, select **+New message**. 

8. In the message pane that appears on the right-side of the screen, enter the following information:

	- To: start typing **Lynne** and a drop-down menu displays with users whose name begins with that. Select **Lynne Robbins**.

	- Add a subject: **Second** **DLP Policy Test**

	- Message area: **Test the IP address 192.168.0.1 and then the IP address 172.16.0.1.**

9. Wait a moment until the message is saved as a draft. You will see a different policy tip displayed above your message fields. Select **Show details**.

10. Select **Override** to bypass the policy tip and send the message. Note the new Policy Tip message. 

11. Select **Send.**

12. Switch to the Client 2 VM (LON-CL2) in the **Virtual machine** field at the top of the VM. 

13. If you need to sign into the VM, the **Admin** account should appear by default, so enter **Pa55w.rd** in the **Password** field to log in. 

14. You should still be logged into Outlook in the LON-CL2 VM as Lynne Robbins. In your **Edge** browser, Lynne’s mailbox should still be open in **Outlook on the web** from when you last used it in the previous task.

15. In Lynne’s **Inbox**, you should see both messages that were just sent by Holly.

16. Delete both messages from Lynne’s Inbox as the last operation in this exercise. You have now successfully tested your custom DLP policy.

17. Leave both client VMs open for the next lab. Do not close any of the browser tabs.


# End of Lab 5