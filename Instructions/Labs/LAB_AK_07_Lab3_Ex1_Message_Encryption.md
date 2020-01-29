# Module 7 - Lab 3 - Exercise 1 - Configure Office 365 Message Encryption


In this lab, you will take on the persona of Holly Dickson, Adatum’s Enterprise Administrator. You have been tasked with piloting the use of Office 365 message encryption in Adatum’s Microsoft 365 deployment. Since message encryption rules can be created using both Exchange Online and Windows PowerShell, you have decided to test each method to determine which you prefer to use once you go live.

In this exercise you will set up Azure Rights Management for your tenant. You will also learn how to create a mail flow encryption rule using both the Exchange Admin Center and Windows PowerShell.

### Task 1 – Enable Azure Rights Management for Exchange Online

In this task you will use Windows PowerShell to access Exchange Online and then, through a string of commands, you will confirm that Azure RMS is active.  
1. Switch to the Client 1 VM (LON-CL1). You should still be logged into LON-CL1 as **lon-cl1\\admin**, and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. To open Windows PowerShell, select the magnifying glass (Search Windows) icon on the taskbar at the bottom of the screen and type **powershell** in the Search box that appears. 

3. In the menu that appears, right-click on **Windows PowerShell** and select **Run as administrator** in the drop-down menu. 

4. You must then initiate a connection to Azure Active Directory by running the following command: <br/>
	
	**Connect-MsolService**  ‎

5. A new window will appear requesting your credentials. Sign in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) with a password of **Pa55w.rd**.   
	
6. Running unsigned PowerShell scripts from remote computers requires changing the execution policy for PowerShell. You should run the following command that changes the Execution Policy for this PC to **unrestricted**, which sets access to the external authorization for this PC so that it can connect to Microsoft online and load all configuration files and run all scripts:   <br/>

	**Set-ExecutionPolicy unrestricted**  <br/>
	
	**Note:** If you receive a warning asking whether you want to change the execution policy, enter **A** to select **[A] Yes to All**.
	‎
7. You must then run the following command to prompt for the username and password of the user who will be running any subsequent commands: <br/>

	**&dollar;Cred = Get-Credential** <br/>
	
	A sign-in window will appear. Sign in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and a password of **Pa55w.rd**.  
	
8. You must then run the following command to create a PSSession (titled $Session) that establishes a remote connection to Exchange Online through PowerShell. When you create a PSSession, Windows PowerShell establishes a persistent connection to the remote computer. Without the -Credential parameter that invokes the $Cred macro from the prior step, this command would prompt you for the credentials of the user authorizing this command. In this case, by invoking the $Cred macro, it applies Holly’s username and password.<br/>

	**&dollar;Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $Cred -Authentication Basic -AllowRedirection**<br/>
	
	**Note:** It’s important to note that you must connect to Exchange Online PowerShell with an admin account that cannot be enabled for multi-factor authentication (MFA). In a real-world environment, if your admin account is enabled for MFA, you must install the Exchange Online Remote PowerShell Module and use the **Connect-EXOPSSession** cmdlet to connect. For more information, see the following article on how to [Connect to Exchange Online PowerShell using multi-factor authentication](https://docs.microsoft.com/en-US/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps).  
	
9. You should then run the following cmdlet to import commands, such as cmdlets, functions, and aliases, from the PSSession ($Session) created in the prior step. In this case, it imports the Exchange Online session into the PowerShell GUI. <br/>

	**Import-PSSession $Session**   <br/>
	
	‎**Note:** You can ignore the warning message that is displayed regarding unapproved verbs.  
	
10. You must then run the following command to view the Information Rights configuration for Exchange Online:  <br/>

	‎**Get-IRMConfiguration**  
	
11. To validate whether Azure Rights Management is enabled, scroll through the list of parameters that’s displayed and locate the **AzureRMSLicensingEnabled** parameter. If this value is set to **$true**, then OME is configured and you can proceed to the next step.  <br/>

	However, if **AzureRMSLicensingEnabled** is set to **$false**, then run the following command to turn on Azure RMS: <br/>

	**Set-IRMconfiguration -azureRMSLIcensingEnabled $true**

12. You then should run the **Test-IRMConfiguration** cmdlet to test Information Rights Management (IRM) configuration and functionality, including availability of an Active Directory Rights Management Services (AD RMS) server, pre-licensing, and journal report decryption.   <br/>

	‎To perform this test, run the following command to test the IRM configuration for messages sent from Holly Dickson:<br/>

	**Test-IRMConfiguration -Sender Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider)<br/>

	**Note:** The results should appear as follows:  <br/>
	
	Results : Acquiring RMS Templates ...<br/>

 	PASS: RMS Templates acquired. Templates available: Confidential \ All<br/>

	Employees, Highly Confidential \ All Employees, Encrypt, Do Not Forward.<br/>

 	Verifying encryption ...<br/>

 	PASS: Encryption verified successfully.<br/>

 	Verifying decryption ...<br/>

 	PASS: Decryption verified successfully.<br/>

 	Verifying IRM is enabled ...<br/>

 	PASS: IRM verified successfully.<br/>

	OVERALL RESULT: PASS  
	‎
13. Do not close PowerShell as you will use it in a later task; simply minimize the PowerShell window for now.
  

### Task 2 – Create a Mail Flow Encryption Rule using the Exchange admin center

In this task, you will create an encryption rule for messages inside your Exchange Online environment by using the Exchange admin center. In the next task, you will do the same thing but using PowerShell instead. 

1. On the LON-CL1 VM, you should still be logged into the Microsoft 365 admin center as Holly Dickson. If you closed your Edge browser or the Microsoft 365 admin center tab, then in Microsoft Edge navigate to **https://portal.office.com** and sign in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and **Pa55w.rd.** 

2. In the **Office 365 home page**, select **Admin**.

3. In the left-hand navigation pane, select **Show all**, which expands the list of options in the navigation pane. 

4. Scroll down in the navigation pane and under **Admin centers**, select **Exchange**. This will open the Exchange admin center.

5. In the **Exchange admin center**, in the left-hand navigation pane select **mail flow.**

6. At the top of the **mail flow** page, the **Rules** tab displays by default. In the **Rules** tab, select the plus sign (**+**) to create a new rule. This displays a drop-down menu of actions. Select **Create a new rule.**

7. In the **new rule** window, in the **Name** box, enter **Encrypt mail for guest@contoso.com** as the name of this rule.

8. Select the drop-down arrow in the **Apply this rule if**… condition box. In the drop-down menu, select **the recipient is**. 

9. For this condition, you must either select an existing name from the contact list or type a new email address in the **check names** box. In this case, enter **guest@contoso.com** in the **Check names** box and then select **OK**.

10. You need to add more conditions, so select **More options**.

11. Select **add condition**. 

12. Note how a second condition box appears below **The recipient is…** condition box. In this second condition box, select the drop-down arrow and select **The recipient**. Then in the drop-down menu select **is external/internal.**

13. In the **select recipient location** dialog box, select the drop-down arrow. In the drop-down menu, select **Outside the organization** and then select **OK.** 

14. You now need to define an action to perform when this rule is applied. In the **Do the following…** box, select the drop-down arrow. In the drop-down menu, select **Modify the message security….** In the menu that appears, select **Apply Office 365 Message Encryption and rights protection.**

15. In the **select RMS template** dialog box, select the drop-down arrow, select **Encrypt**, and then select **OK.**

16. Select **Save.** Once the rule is saved, it should appear in the list of rules in the Exchange admin center.

17. Do not navigate away from this page as you will return to it at the end of the next task. Simply minimize your Internet Explorer session for now. 
 

### Task 3 – Create a Mail Flow Encryption Rule using Windows PowerShell

In the prior task, you configured a mail flow rule encryption rule using the Exchange admin center. In this task, you will create a mail flow encryption rule using Windows PowerShell. 

1. On the LON-CL1 VM, the PowerShell session that you used in Task 1 should still be open, so maximize the PowerShell window now. If you closed the previous PowerShell session, then open an elevated session now, run the **Connect-MsolService** cmdlet, and log in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and the password **Pa55w.rd**.

2. In this step, you will create a mail flow rule by using the **New-TransportRule** cmdlet, and you’ll set the **ApplyOME** encryption parameter to $true. This rule will encrypt all outgoing mail from Adatum that is being sent to Gservices@contoso.com.  <br/>

	To create this rule, run the following command:<br/>

	**New-TransportRule -Name "Encrypt rule for Guest Services" -SentTo "Gservices@contoso.com" -SentToScope "NotinOrganization" -ApplyOME $true**  <br/>
	
	**Note:** This command will take several seconds to complete, so be patient.

3. To verify the rule exists, switch back to your Internet Explorer browser session, which should still be in the **rules** window of the **Exchange admin center**. The list of rules should only be displaying the **Encrypt mail for guest@contoso.com** rule that you created in the prior task.<br/>

	‎On the menu bar that appears above the list of rules, select the **Refresh** icon. In the refreshed list, the rule that you just created using PowerShell should appear as well.
	
4. Leave your browser session open for the next exercise.


# Proceed to Exercise 2