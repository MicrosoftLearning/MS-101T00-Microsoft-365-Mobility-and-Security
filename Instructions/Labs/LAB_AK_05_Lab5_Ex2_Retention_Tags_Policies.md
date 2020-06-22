# Module 5 - Lab 5 - Exercise 2 - Configure Retention Tags and Policies  

In this exercise, you will implement archiving with MRM retention tags. You will then configure retention tags and policies through two different ways - first, through the Exchange Admin Center, and second, through the Security and Compliance Center. 

### Task 1 – Activate In-Place Archiving

In this next phase of your Adatum pilot project, you will access the Security & Compliance Center to activate Holly Dickson’s archive mailbox.   

1. You should still be logged into LON-CL1 as the **Admin** and into **Microsoft 365** as Holly Dickson.

2. In Microsoft Edge, select the **Office 365 Security & Compliance** tab; if you closed this tab earlier, then open a new tab and go to https://protection.office.com.

3. In the **Office 365 Security & Compliance**, in the left-hand navigation pane, select **Information governance**, and then under it select **Archive**.

4. On the **Archive** window, note that the archive mailboxes for all users other than Holly Dickson are **enabled**. These archive mailboxes were enabled when the VM lab environment was built for this training course and these users were preconfigured in the tenant. However, since Holly's user account was added in Lab 1, her archive mailbox is **disabled** by default.

5. To enable Holly’s archive mailbox, select **Holly Dickson** in the user list. 

6. In the details pane on the right, Holly’s archive mailbox is currently listed as **disabled**. Select **Enable**, and then in the **Warning** dialog box that appears, select **Yes** to confirm this action.

7. In your Microsoft Edge browser, leave the Office 365 Security & Compliance Center tab open as you will use it in a later task in this lab. 
 

### Task 2 – Create an MRM retention tag and policy in the Exchange Admin Center

As part of your pilot project for Adatum, you will configure MRM retention through the Exchange Admin Center by creating an MRM retention tag and then adding it to a new MRM retention policy. You will also assign several default tags to the policy as well. You will then assign this retention policy to Joni Sherman and Lynne Robbins’ mailboxes.

1. In **Microsoft Edge**, select the **Microsoft 365 admin center** tab.

2. In the **Microsoft 365 admin center**, in the left-hand navigation pane under the **Admin centers** group, select **Exchange**. This will open the Exchange admin center.

3. In the **Exchange admin center**, in the left-hand navigation pane, select **compliance management**.

4. In the **compliance management** window, select the **retention tags** tab that appears at the top of the page.

5. You want to create a retention tag, so select the **plus (+)** **sign** in the toolbar that appears across the list of existing retention tags. In the drop-down menu that appears, select **applied by users to items and folders (personal)**.

6. In **new tag applied by users to items and folders (personal)** window, under **Name**, enter **3 Years Move – Archive after three years**.

7. Under **Retention Action**, select the **Move to Archive** option.

8. Under **Retention period**, select the **When the item reaches the following age (in days)** option and enter **1095** in the retention period field that appears below this option (1095 days = 3 years).

9. In the **Comment** field, enter **Personal tag to archive email three years after being received**.

10. Select **Save** to save the retention tag, and then select **OK** once the tag is successfully saved.

11. On the menu bar on the top of the page, select the **retention policies** tab.

12. In the **retention policies page**, note that there is one default retention policy. Since this policy is selected by default, its corresponding properties are displayed in the detail pane on the right-side of the screen. This information indicates that all the default retention tags that have been assigned to this policy. <br/>

	You want to create a custom retention policy, so select the **plus (+) sign** icon in the toolbar that appears across the list of existing retention policies. 

13. In **new retention policy** window, enter **Office Retention Policy** in the **Name** field.

14. You now want to assign one or more retention tags to this new policy. Below **Retention tags**, select the **plus (+) sign** icon.

15. In the **select retention tags** window, select the **3 Years Move** tag that you just created, select the **add -&gt;** button, and then select **OK**.

16. In addition to the personal retention tag that you just added to the retention policy, you also want to add the following default tags as well:

	- Default 2 year move to archive

	- Deleted Items

	- Junk Email

	- Recoverable Items 14 days move to archive

	Repeat the prior two steps to add these tags to this policy. **Hint:** Hold down the **Ctrl** key as you select each tag in the list; this will enable you to select all four default tags at one time before selecting the **add-&gt;** button.

17. On the **new retention policy** window, select **Save** and then select **OK**.

18. You are now going to apply this retention policy to the mailboxes for your two test users, Joni Sherman and Lynne Robbins. In the **Exchange Admin Center**, in the left-hand navigation pane, select **recipients**. In the **recipients** page, the **mailboxes** tab is displayed by default. 

19. In the list of recipient mailboxes, select **Joni Sherman** and then select the **pencil (edit) icon** in the toolbar to edit the properties of Joni’s mailbox.

20. In the **Edit User Mailbox** for Joni Sherman, select **mailbox features** in the left-hand navigation pane.

21. If a **Warning** dialog box appears, select **OK**.

22. Select the drop-down arrow in the **Retention policy** field and select **Office Retention Policy**.

23. Select **Save** and then select **OK**.

24. Repeat steps 19-23 for **Lynne Robbins**.

25. Leave your web browser open and proceed to the next task.

You have created a new retention policy through the Exchange Admin Center. You assigned several retention tags to this policy, including a custom retention tag, and you assigned the retention policy to Lynne and Joni’s mailboxes.


### Task 3 – Create a Retention Policy in the Security and Compliance Center

Now that Holly has created a retention policy through the Exchange Admin Center, she wants to do the same in the Security & Compliance Center. For this policy, Holly wants to preserve the content of all Exchange Online mailboxes from deletion for 7 years after the last modification. 

1. In **Microsoft Edge**, select the **Security &amp; Compliance Center** tab if it's still open; otherwise, open a new browser tab and enter the following URL in the address bar: **https://protection.office.com**

2. In the **Security &amp; Compliance Center**, in the left-hand navigation pane, select **Information governance** and then select **Retention**.

3. In the **Retention** window, select the **+Create** button to start the wizard that’s used to create a new retention policy.

4. On the **Name your policy** page, enter **Exchange preservation** in the **Name** field and select **Next**.

5. On the **Decide if you want to retain content, delete it, or both** page, leave the **Yes, I want to retain it** option selected, as well as the **For this long** and **7 years**. Do not change these fields.<br/>

	However, in the **Retain the content based on** field, it currently indicates **when it was created**. Select the drop-down arrow for this field and select **when it was last modified**. <br/>
	
	In the **Do you want us to delete it after this time?** option, select **Yes**.

6. Select **Next**.

7. In the **Choose locations** page, select **Let me choose specific locations.** 

8. As you scroll down the page, note that the **Status** of the **Exchange email** location is turned on. Leave this set to On. However, for all the other locations that are turned on, select their toggle switches to turn them off. As you scroll through the locations, **Exchange email** should be the only location turned on.

9. Select **Next**.

10. On the **Review your settings** page, review all the settings. If any need to be corrected, select the **Edit** option and make the appropriate correction. Select **Create this policy** to finish the wizard.

11. Do not close your Client 1 VM or Microsoft Edge. Leave your web browser open as well as all tabs for the next lab.

You have now created a new retention policy in the Security & Compliance Center that retains all Exchange emails from all mailboxes for 7 years after the last modification.

 # End of Lab 5
 
