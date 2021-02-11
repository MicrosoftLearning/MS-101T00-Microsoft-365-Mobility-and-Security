# Module 3 - Lab 3 - Exercise 1 - Conduct a Spear Phishing attack using the Attack Simulator

Holly Dickson is concerned that some users at Adatum may require education about phishing attacks. As part of her pilot project, Holly has decided to use the Microsoft 365 Attack Simulator to determine her users' susceptibility to phishing attacks.


### Task 1: Enable Multi-factor Authentication for the Global Admin
To use Microsoft's Attack Simulator to simulate a phishing attack, you must first enable Multi-Factor Authentication (MFA) for either your entire organization or for just the Global admin who will run the simulator. For her pilot project, Holly does not want to set up MFA for all the Adatum users at this point in time; therefore, she will enable MFA for her user account only, and then after she finishes running the Attack Simulator, she will turn MFA back off. 

**Important:** To implement MFA, you will need to use your mobile phone to receive a verification code so that you can enter it into your tenant as a second form of authentication. If you do not have a phone, you will have to skip this lab. If this is the case, notify your instructor, who can potentially partner you with another student to follow along through this lab.

1. Switch to the **LON-CL1** VM, where you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of **Pa55w.rd**. 

2. In your **Edge** browser, you should still be logged into Microsoft 365 as Holly Dickson. Select the tab containing the **Office 365 Security and Compliance** center, which should still be open from the Safe Links lab that you just completed. 

3. In the **Office 365 Security and Compliance** center, in the left-hand navigation pane under **Threat management**, select **Attack simulator**. 

4. On the **Attack Simulator** page, scroll down to see the four types of attacks that you can simulate. Also note the warning message that indicates you must enable multi-factor authentication (MFA) to schedule or terminate attacks. This is required because the system wants to confirm your credentials before you conduct a simulated attack. In the upcoming steps, you will enable MFA for Holly and then perform a phishing attack.

5. To enable MFA for Holly Dickson's user account, select the **Microsoft 365 admin center** tab in your browser, and then in the left hand-navigation pane, select **Users** and then select **Active users**.

6. In the **Active users** window, on the menu bar at the top of the user list, select the select **Multi-factor authentication**. If it does not appear, select the **ellipsis (More actions)** icon. Then, in the drop-down menu that appears, select  **Multi-factor authentication**.

7. In the **multi-factor authentication** window, the **users** tab is displayed by default. Note the MFA status for all existing user accounts, which is **Disabled**. Select the check box for **Holly Dickson**, and in Holly's properties pane that appears on the right, select **Enable**.

8. On the **About enabling multi-factor auth** dialog box, select **enable multi-factor auth**. 

9. When the **Updates successful** dialog box appears, select **close**. In the **multi-factor authentication** window, verify Holly's MFA Status has changed to **Enabled**. 

10. You must now sign out of Microsoft 365 as Holly, close your browser session (to clear cache), open a new session, and then log back in as Holly using MFA. The first time you sign back in after having MFA enabled for your user account, you will be asked for the authentication information needed for MFA, such as your phone number and authentication options. You will then be texted a verification code to validate the authentication process works. You will perform these steps in the remaining portion of this task.<br/>

	You must begin by signing out of Microsoft 365 as Holly, so select the **HD** user icon in the upper right corner of the browser and in the **Holly Dickson** window that appears, select **Sign out**. 

11. Once you are signed out, close the browser session and all the browser tabs.

12. Select the **Edge** icon on your taskbar to open a new browser session, and then navigate directly to the **Office 365 Security and Compliance** center by entering the following URL in the address bar: **https://protection.office.com**

13. In the **Sign in** window, enter **Holly@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider) and then select **Next**. In the **Enter password** window, enter **Pa55w.rd** and select **Sign in**.

14. Because MFA is enabled for Holly, a **More information required** window appears. Select **Next**.

15. On the **Microsoft Authenticator** page, you can download this mobile app or use a different method for MFA verification. For the purposes of this lab, we recommend you use your mobile phone so that you do not have to take time installing the Microsoft Authenticator app that you may not use again after this training class. Select the **I want to set up a different method** option at the bottom of the page. 

16. On the **Choose a different method** dialog box that appears, select the drop-down arrow in the **Which method would you like to use?** field, select **Phone**, and then select **Confirm**. 

17. In the **Phone** window that appears, under **What phone number would you like to use?** field, select your country or region, and then in the field next to it, enter your phone number (in the format **nnn-nnn-nnnn**). Verify the **Text me a code** option is selected and then select **Next**.

18. Retrieve the verification code from the text message that is sent to your phone.

19. In the **Phone** window, enter the 6 digit verification code in the **Enter code** field and then select **Next**.

20. This takes you back to the **Microsoft Authenticator**, Select the **I want to set up a different method** option at the bottom of the page. 

21. On the **Choose a different method** dialog box that appears, select the drop-down arrow in the **Which method would you like to use?** field, select **Email**, and then select **Confirm**. 

22. Enter your personal email address.

23. Open your personal email address and the email from Adatum corporation.  Note the verification code.

24. Enter the verification code from the Adatum email to your personal email address then select **Next**.

25. On the **Success!** page, select **Done**.

26. If you receive a dialog box indicating your sign in has timed out, you will have to enter Patti's password of **Pa55w.rd** and then you will be sent another verification code to your phone. On the **Enter code** window, enter this new code and then select **Verify**. 

27. If you take too long to complete this process, the **Enter password** window will appear with a message indicating you took too long to complete the sign in process, so you will be timed-out. If this occurs, you must sign in again with Holly's password of **Pa55w.rd**. Another verification code will be texted to your phone, so enter it in the **Enter code** screen that appears and select **Verify**.

28. The **Office 365 Security and Compliance** center should now be displayed in your browser. You will resume from here in the next task when you launch a spear phishing attack using the Attack Simulator. Leave this tab open in your browser. 

29. You have now configured MFA, you have signed into the **Office 365Security and Compliance** center using MFA, and you are ready to run the Attack Simulator. Leave everything as is in your VM and proceed to the next task.


### Task 2: Configure and launch a Spear Phishing attack

Now that Holly has turned on MFA, she is ready to run the Attack Simulator and launch a simulated spear phishing attack. This will provide visibility into how well Adatum is prepared to handle such a security attack. 

1. You should still be on **LON-CL1**, and you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of **Pa55w.rd**.

2. You should still have the **Office 365 Security and Compliance** center open in in your **Edge** browser from the prior task. If not, enter **https://protection.office.com** in the address bar, and then when you receive the dialog box asking for a second form of authentication, proceed through the verification process. 

3. In the **Office 365 Security and Compliance** center, select **Threat management** in the left-hand navigation pane and then select **Attack simulator**. 

4. On the **Attack Simulator** page, you reviewed the four types of simulated attacks that are available in the prior task. For this simulation, Holly has decided to conduct an account breach in which she will use a URL to try and obtain usernames and passwords. This is referred to in the Attack Simulator as a **Spear Phishing (Credentials Harvest)** attack. <br/>

	You can launch this attack either from this page or the **Attack Details** page. Since the **Attack Details** page has additional information on what this attack will do, it is recommended that you launch it from there so that you can learn about the specifics of this type of attack. <br/>
	
	To the right of the **Spear Phishing (Credentials Harvest)** section, select **Attack Details**.

5. On the **Attack details** page, review the specific information related to the **Spear Phishing (Credentials Harvest)** attack type.

6. In the **Launch attack** section for the **Spear Phishing (Credentials Harvest)** attack type, select **Launch attack**. This initiates the **Configure Phishing Attack** wizard.

7. In the **Configure Phishing Attack** wizard, the steps involved in the simulation are displayed in the left-hand pane. While you can manually create a phishing campaign, it is recommended that you take advantage of the available templates that will prefill most of the information for you. The key to a successful phishing attack is to create a very intriguing, real-world looking email, and the templates provide very creative solutions. <br/>.  

8. Select **Launch a simulation**.

9. **Credential Harvest** should be select be default, if not choose it, then select **Next**.

10. Enter a name for the simulation and select **Next**.

11. On the **Select Payload** screen, choose a payload you would like to simulate, then select **Next**.

12. In the next step, you will select the users that will receive the phishing email. You can select users from the company address book (the Active Users), or for large-scale attacks, you can import users from a .csv file. For this simple simulation, you will only send the email to one user, so select **Add Users**. <br/>

	Enter **Lynne** in the **Search for users or groups** field and select **Enter**. In the list of users that appears, select **Lynne Robbins** and select **Add 1 User(s)**. Lynne's user account record will display in the list of **Recipients**. Select **Next**. 

13. In the **Assign Training** page, accept the defaults you.  and elect **Next**.

14. On the **Training landing page** page, accept the defaults and select **Next**.

11. On the **Launch Details** page, review the options available, the select **Next**

12. On the **Review Simulation** page, confirm all of the settings are correct and select **Submit**. This will launch the phishing attack!

13. Leave your browser and the Security and Compliance Center open for the next task.


### Task 3: Review the attack simulation results

In this task, you will verify whether Lynne Robbins received the email that you configured in the Attack Simulator, and then you will review the report associated with the Spear Phishing attack that you simulated.

1. Switch to the **LON-CL2** VM and log in as the **Admin** with a password of **Pa55w.rd**.

2. In the Edge browser, in the **Outlook** tab in which you are signed in as the MOD Administrator, select the **MA** initials in the upper right hand corner of the screen. In the **MOD Administrator** window that appears, select **Sign out**.

3. Close all browser tabs except for the **Sign out** tab. In the **Sign out** tab, enter the following URL in the address bar to navigate directly to Outlook on the web: **https://outlook.office365.com**.
 
4. In the **Pick an account** window, select **Use another account**. 

5. In the **Sign in** window, enter **LynneR@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix ID provided by your lab hosting provider), and then in the **Enter password** window, enter **Pa55w.rd** and select **Sign in**. 

6. Close the **Welcome** window.

7. In Lynne's Outlook Inbox, you should see the spear phishing email that was sent by the Attack Simulator. Select the email to open it and review the details in the body of the message. 

**NOTE!** It can take up to 15 minutes for the email to arrive.  Wait for the email before proceeding.

8. Select the link that is included in the email. Even though you know this is a spear phishing attack, this will enable you to see the effect of doing so in the Attack Simulator report that tracks the results of the spear phishing campaign.

9. In the **Sign in** dialog box that appears, enter **LynneR@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix ID provided by your lab hosting provider), and then in the **Enter password** window, enter **Pa55w.rd** and select **Sign in**. 

10. This displays a web page that explains how you have redirected to it as part of a Phishing awareness test being run by your organization. Read through the contents of this page. 

11. Switch back to LON-CL1.

12. In your browser session where you are logged in as Holly Dickson, if you are still on the **Attack details** page, then scroll down to the **Attack History** section under **Spear Phishing (Credential Harvest)** section and select the **Refresh** button. It should display details on your phishing attack. Select the right arrow to view the report on the phishing attack. <br/>

	 **Note:** If you were instead back on the **Attack simulator** page, then in the **Spear Phishing (Credential Harvest)** section, below the **Attack Completed** message, select **View Report**.

13. On the **Report** page, review the report for the phishing campaign that you completed. Note the date and time of the report. If you had run a previous simulation, it sometimes takes a few minutes to update this report information with the details from the current simulation that you just ran. If this occurs, refresh the page after a few minutes. Review the information on the page and note the results after having selected the spear phishing URL in the email that was sent to Lynne Robbins earlier in this task.

14. Leave your browser open in LON-CL1 and do not close any of the tabs.
    

# Proceed to Lab 3 - Exercise 2
