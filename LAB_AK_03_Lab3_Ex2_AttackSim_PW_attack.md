# Module 3 - Lab 3 - Exercise 2 - Conduct Password attacks using the Attack Simulator

Holly Dickson is concerned that some users at Adatum may require education about secure password strategies. In this lab she will use the Microsoft 365 Attack Simulator to determine her users' susceptibility to password attacks.

**Note:** At the end of this exercise, you will disable MFA for Holly's account. This will save you from having to enter the second form of authentication when signing in as Holly in any of the remaining labs in this course.

### Task 1: Configure and launch a Brute Force attack 

Password cracking techniques are used to guess a user's password by trying many variations with a computer. Once an attacker has the user name and password for a user, the attacker will generally be able to sign in to Microsoft 365 and gain access to additional information, such as other user accounts and sensitive information. Brute-force attacks work by calculating every possible combination that could make up a password and testing to see if it is the correct password.

Two types of brute-force password attacks exist: a dictionary attack using a well-known list of passwords, and an exhaustive attack, where combinations are tried sequentially. The Attack Simulator uses a dictionary list attack, allowing modifications of frequency between attacks and the number of attempts. If a password is discovered, the password itself is not shown; only an indication that a password was discovered will be shown.

For this lab, you will not include a file of passwords; you will instead enter a short list of passwords. For her pilot project, Holly is once again going to use Lynne Robbins as her test case. 

1. You should still be in LON-CL1 and signed in as the **Admin** with a password of **Pa55w.rd**; if not, then sign in now.  

2. After the previous lab exercise, you should still be in the **Office 365 Security and Compliance** center, and you should still be logged in as Holly Dickson; if not, then do so now.

3. After the previous lab exercise, you should also be in the **Attack Simulator**; if not, then in the left-hand navigation pane, under **Threat Management**, select **Attack simulator**. In the list of 4 attacks, scroll down to the **Brute Force Password (Dictionary Attack)** section and select the **Launch Attack** button. 

**NOTE!  The rest of the exercise cannot be performed.  The interface has changed so that after you select Launch Attack, there is not a choice for Password Attacks, either Brute Force or Spray attacks.  No information available online for implementing the types of campaigns.**


4. In the **Provide a name for the password attack** page, enter **Brute Force Test** in the **Name** field and select **Next**.

5. In the **Select user accounts which to attempt the password attack** page, select the **Address Book** button, enter **Lynne** in the **Search** field, select **Lynne Robbins** from the resulting list of users, and then select **Next**.

6. In the **Choose attack settings** page, enter the following list of passwords. You MUST hit Enter after entering each password:

	- P@ssw0rd
	- Pa$$w0rd
	- PA$$WORD
	- P@55w0rd
	- Pa55w.rd
	
	**Note:** You will enter Lynne's actual password on purpose to check the results when a password match occurs. Once you have added all the passwords, select **Next**. <br/>

	**Note**: Ordinarily you would have a file that contains a list of commonly used passwords for your organization.  You would upload that file using the **Upload** button. 

7. In the **Confirmation** page, select **Finish** to run the simulation.

8. Once the attack is complete, you will be returned to the **Attack simulator** page. 

9. Leave your browser and the Security and Compliance Center open for the next task.   


### Task 2: Review the Brute Force results

You will now review the results of the Brute Force Password attack.

1. In your browser session where you are logged in as Holly Dickson, you should still be on the **Attack simulator** page. In the **Brute Force Password Dictionary Attack)** section, it will display **Attack Completed** once the attack is done. Select the **Refresh** icon on the address bar to refresh the results. This may take several minutes to complete, so you may need to refresh your screen several times. Once the attack is complete, select **View Report**.

2. On the **Attack details** page, view the report for the **Brute force test** that you completed. Review the information on the page and note the results after having entered Lynne's actual password among the list of passwords that were entered for the simulation. 

3. In the **Attack details** page, select **Attack simulator** in the navigation thread at the top of the page (**Home > Attack simulator > Report**).

4. Leave your browser open in LON-CL1 and do not close any of the tabs.
   

### Task 3: Configure and launch a Password Spray attack 

A password spray attack against an organization is typically done by running a list of commonly used passwords against a list of valid Microsoft 365 user accounts. Typically, the attacker crafts one password to try against all the known user accounts. If the attack is not successful, the attacker will try again using another carefully crafted password, usually with a waiting period between attempts to avoid policy-based account lockout triggers. For her pilot project, Holly is once again going to use Lynne Robbins as her test case. 

1. You should still be in LON-CL1 and signed in as the **Admin** with a password of **Pa55w.rd**; if not, then sign in now.  

2. In your browser session where you are logged in as Holly Dickson, you should be on the **Attack simulator** page. 

3. In the list of 4 attacks, scroll down to the **Password Spray Attack** section and select the **Launch Attack** button.

4. In the **Provide a name for the password attack** page, enter **Password Spray Test** in the **Name** field and select **Next**.

5. In the **Select user accounts which to attempt the password attack** page, select the **Address Book** button, enter **Lynne** in the **Search** field, select **Lynne Robbins** from the resulting list of users, and then select **Next**.

6. In the **Choose attack settings** page, enter the following list of passwords. Unlike the Brute Force password test, this Spray test allows you to enter all passwords in the field at one time; simply include a space in between each one. Enter the following passwords in the **Password** field: **P@ssw0rd Pa$$w0rd Pa55w.rd**
	
	**Note:** You will enter Lynne's actual password on purpose to check the results when a password match occurs. Once you have added all the passwords, select **Next**.

7. In the **Confirmation** page, select **Finish** to run the simulation.

8. Once the attack is complete, you will be returned to the **Attack simulator** page. 

9. Leave your browser and the Security and Compliance Center open for the next task.   



### Task 4: Review the Password Spray results

You will now review the results of the Password Spray attack.

1. In your browser session where you are logged in as Holly Dickson, you should still be on the **Attack simulator** page. In the **Password Spray Attack** section, it should display **Attack Completed** once the attack is done. Select the **Refresh** icon on the address bar to refresh the results. This may take several minutes to complete, so you may need to refresh your screen several times. Once the attack is complete, select **View Report**.

2. On the **Attack details** page, view the report for the **Password spray test** that you completed. Review the information on the page and note the results after having entered Lynne's actual password among the list of passwords that were entered for the simulation. 

3. In the **Attack details** page, select **Attack simulator** in the navigation thread at the top of the page (**Home > Attack simulator > Report**).

4. Leave your browser open in LON-CL1 and do not close any of the tabs.


### Task 5: Disable Multi-factor Authentication for the Global Admin

To use Microsoft's Attack Simulator to simulate phishing and password attacks, Holly enabled Multi-Factor Authentication (MFA) for her user account. Now that she has completed the Attack Simulator tests, she wants to disable MFA for her account so that she doesn't have to deal with MFA for the remainder of the pilot project.

1. You should still be logged into **LON-CL1** as the **Admin** account and into Microsoft 365 as Holly Dickson.

2. To disable MFA for Holly Dickson's user account, you must first access the **Active users** list in the Microsoft 365 admin center. If you have the **Microsoft 365 admin center** open in a browser tab, then select that now; otherwise, open a new browser tab, enter **https://portal.office.com** in the address bar, and then on the **Office 365 home** page, select **Admin**. 

3. On the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users** and then select **Active users**.

4. In the **Active users** window, on the menu bar at the top of the user list, select **Multi-factor authentication**.

5. In the **multi-factor authentication** window, the **users** tab is displayed by default. Select the check box for **Holly Dickson**, and in Holly's properties pane on the right, select **Disable**.

6. On the **Disable multi-factor authentication?** dialog box, select **yes**. 

7. When the **Updates successful** dialog box appears, select **close**. In the **multi-factor authentication** window, verify Holly's MFA Status has changed to **Disabled**. 

8. You must now sign out of Microsoft 365 as Holly and then sign back in as Holly (without MFA). To do so, perform the following steps: <br/>

	- Close your browser session and all browser tabs (to clear your cache)
	- Open a new Edge browser session
	- Enter the **https://portal.office.com** URL
	- Sign in as **Holly@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider) with a password of **Pa55w.rd**
	- From the **Microsoft Office Home** page, select the **Admin** icon to navigate to the **Microsoft 365 admin center**
	
	You are now ready to proceed to the next lab exercise.

# Proceed to Lab 3 - Exercise 3
 
