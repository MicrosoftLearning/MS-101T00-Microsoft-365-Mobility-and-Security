# Module 2 - Lab 2 - Exercise 2 - Implement a Safe Links Policy

Now that you have created a Safe Attachments policy for Adatum, you want to create a Safe Links policy and then validate the policy to ensure that it works properly.

**IMPORTANT:** This lab exercise consists of two tasks. The first task creates a Safe Links policy, and then the second task validates the policy. The problem with this lab is that when you create a safe links policy, it takes at least 30 minutes for the policy to propagate through the system. **This means that you can perform the first task, but then you must wait at least 30 minutes before you can perform the final task.** You should continue with the training class and your instructor will provide guidance on when you can perform Task 2 depending on the next break that occurs in the class schedule. 

### Task 1 – Create a Safe Links Policy

In this task, you will create a Safe Links policy that applies to all users in your tenant. You will then add the **http://tailspintoys.com** URL to the company-wide list of blocked URLs that you will define in the Safe Links global settings. The blocked URLs and other options defined in the Safe Links global settings are only applied to users who are included in active Safe Links policies. There is no built-in or default Safe Links policy, so you must create at least one Safe Links policy for these global settings to be active.  

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Admin** account, and you should still be logged into Microsoft 365 as **Holly Dickson**.

2. After finishing the previous task, you should still be in the **Microsoft 365 Security and Compliance center**. If not, in your browser, enter **https://protection.office.com.**

3. In the **Security &amp; Compliance center**, in the left-hand navigation pane, the **Threat Management** group should still be expanded from the prior task; if not, expand it now. Under this group, select **Policy**.

4. In the **Policy** window, select the **Safe Links** tile. 

5. On the **Safe links** page, select **+Create** on the menu bar. This initiates the **Create Safe Links Policy** wizard.

5. On the **Name your policy** page, enter **LinkPolicy1** in the **Name** field and then select **Next**.

6. On the **Settings** page, enter the following settings and then select **Next**: 

    - Select the action for unknown or potentially malicious URLs in messages - **On**
    - Select the action for unknown or potentially malicious URLs within Microsoft Teams - **Off**
    - Apply real-time URL scanning for suspicious links and links that point to files - select this check box
    - Wait for URL scanning to complete before delivering the message - select this check box
    - Apply safe links to email messages sent within the organization - select this check box
    - Do not track user clicks - select this check box
    - Do not allow users to click through to original URL - select this check box
   
7. On the **Applied to** page, select **+Add a condition**. In the drop-down menu that appears, under the **Applied if...** section, select **The recipient domain is**

8. In **The recipient domain is** section, select the **Choose** link to choose a domain. 

9. In **The recipient domain is** window, select the **+Add** button. In the list of domains that appear, select the check box for the **xxxxxZZZZZZ.onmicrosoft.com** domain (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider), select **Add**, and then select **Done**.

10. On the **Applied to** page, select **Next**.

11. On the **Review your settings** page, review the options that you selected. If any need to be corrected, select the appropriate **Edit** option and make the correction. If they all appear correct, select **Finish**. Once the **LinkPolicy1** policy is created, it will appear in the Safe links list. 

12. On the **Safe links** page, select **Global settings** on the menu bar.

13. In the **Safe Links policy for organization** pane that appears, enter **http://tailspintoys.com** in the **Block the following URLs** field, do NOT change the default settings for any of the other options, and then select **Save**.

14. Leave the Office 365 Security &amp; Compliance tab open for the next task.

**STOP!!** As mentioned at the start of this lab exercise, now that you have created a Safe Links policy, you must wait at least 30 minutes for the policy to propagate through the system before you can perform the next task in this exercise. 

**Do NOT proceed to the next task!** You can continue with the training course and perform the next task when your instructor feels it's appropriate given the class training schedule. 

### Task 2 – Validate the Safe Links Policy

In this task, you will test the Safe Links Policy that you just created that blocks links to the http://tailspintoys.com URL.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.

2. In your **Microsoft Edge** browser, select the **Microsoft Office Home** tab and then in the column of app icons on the left side of the screen, select the **Outlook** icon.

3. **Outlook** will open in a new tab in your browser, and Holly's **Inbox** will be displayed.

4. Select the **New Message** button in the upper left part of the screen.

5. In the email form that appears in the right-hand pane, enter the following information:

    - To: You will be sending an email to the MOD Administrator, so enter **mod** in the **To** field and then select the **MOD Administrator** email address from the user list.

    - Add a subject: **Free stuff for Adatum users**

    - body of the message: **Please click on me for free toys from TailSpin Toys.**

6. Select the text that you added in the body of the message.

7. Below the body of the message is a long row of formatting icons. Select the **Insert link** icon, which depicts two overlapping circles.

8. In the **Insert link** window, the text that you highlighted in the body of the message should be displayed in the **Display as** field. In the **Web address (URL)** field, enter the following URL: **http://tailspintoys.com/aboutus/freetoys**.

9. Select **OK**.

10. In the body of the email, the message should still be selected. Click anywhere in the body of the message to remove the highlighting. The color of the text should now be blue, and it should be underlined, indicating that this message is hyperlinked to a URL.

11. Select either **Send** button (top or bottom of the form).

12. You now want to go the MOD Administrator's Inbox in Outlook and validate whether the Safe Links policy you created in the prior task worked on the email that you just sent from Holly to the MOD Administrator.<br/>

    To do this, you must first switch the Client 2 VM (**LON-CL2**). 

13. Log into the LON-CL2 VM as the **Admin** account by entering **Pa55w.rd** in the **Password** field.

14. Select the **Microsoft Edge** icon in the taskbar, maximize the window and then enter the following URL in the address bar: **https://outlook.office365.com**

15. In the **Sign-in** window, enter **admin@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider) and then select **Next**.

16. In the **Enter password** window, enter the tenant password provided by your lab hosting provider and select **Sign in**.

17. Close the **Let Microsoft Edge save and fill your password for this site next time?** banner by selecting **Never**.

18. On the **Stay signed in?** dialog box, select the **Don't show this again** check box and then select **Yes.**

19. In the **Welcome** windows, select the X in the upper right corner to close the window.

20. In the MOD Administrator's **Inbox**, open the email that was sent by Holly.

21. Select the hyperlink in the body of the message to open it. 

22. If a window opens indicating the new browser recommended by Microsoft is here, select **No thanks**. 

23. A new tab should open in your **Edge** browser that takes you to the URL you just saw in the prior step. This site should display the following warning message: **This website has been blocked per your organization's URL policy.** This not only indicates that opening this website might not be safe, but it also verifies that the Safe Links policy you just created is working properly.

24. In LON-CL2, leave the Edge browser and all its tabs open for the next lab. 


# End of Lab 2

