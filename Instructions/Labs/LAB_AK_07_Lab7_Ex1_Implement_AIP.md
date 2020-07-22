# Module 7 - Lab 7 - Exercise 1 - Implement Azure Information Protection  


In your role as Holly Dickson, Adatum’s Enterprise Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, your next steps are to implement Azure Information Protection (AIP) and Windows Information Protection (WIP) at Adatum. You will begin by configuring AIP and then using AIP on a client and verifying an AIP policy. You will then perform similar steps for WIP by configuring it for Adatum and then implementing WIP.

### Task 1 – Install the Azure Information Protection client

To implement Azure Information Protection as part of your pilot project at Adatum, you must first install the AIP client from the Microsoft Download Center.

1. You should still be logged into LON-CL1 as the **lon-cl1\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson** with a password of **Pa55w.rd**. 

2. In **Microsoft Edge**, open a new tab and enter the following URL in the address bar: **https://portal.azurerms.com**

3. On the **Microsoft Azure Information Protection** page, scroll to the bottom of the page to view the 3 boxes. In box #1, select **Install the Azure Information Protection application**.

4. On the **Microsoft Azure Information Protection** page, under the **Azure Information Protection client** section, select the **Windows icon** to download the client to a Windows computer.

5. On the **Download Center** page, scroll down to the **Microsoft Azure Information Protection** section and select **Download**.

6. In the **Choose the download you want** window, select **AzInfoProtection.exe** and then select **Next.**

7. In the taskbar that appears at the bottom of the page, select **Save**.

8. Once the download has successfully completed, in the taskbar that appears at the bottom of the page, select **Run.**

9. If the first page of the **Microsoft Azure Information Protection installation wizard** does not display, select the icon for it on the taskbar to display the wizard.

10. On the license and terms page, uncheck the **Help improve Azure Information Protection by sending usage statistics to Microsoft** option and then select **I agree**.

11. On the **Completed Successfully** window, select **Close**. 

12. Leave your VM and browser open and proceed to the next task.


You have successfully installed the AIP client on Client 1 VM.


### Task 2 – Configure Azure Information Protection

In this exercise you will create an AIP label and add it to the default policy so that it’s valid for all users of the Adatum tenant.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.

2. In **Microsoft Edge**, open a new tab and enter the following URL in the address bar: **https://portal.azure.com/**

3. On the **Welcome to Azure** window, scroll down to the **Azure services** section and select **More services**.

4. In the **All services** window, in the **Search** box at the top of the page, enter **Azure Information**, and then in the list of services, select **Azure Information Protection**. 

5. In the **Azure Information Protection | Quick start** window (which may take a minute or so to load), in the navigation pane on the left, under the **Classifications** section select **Labels**.

6. In the **Azure Information Protection | Labels** window, select **Add a new label**.

7. In the **Label** window, enter the following information:

	- Enabled: select **On**

	- Label display name: **PII**

	- Description **Documents, files, and emails with PII**

	- Color: **Black** is selected by default; you can use black or select **Custom** and then enter the Hex code for the color of your choice (you can locate a color and its corresponding Hex code [from this website](https://www.w3schools.com/colors/colors_names.asp).

	- Set permissions for documents and emails containing this label: select **Protect** (Note: If you selected a Custom color option in the prior setting, the color of the options for this setting will reflect the code code that you entered). 

		- In the Protection pane that appears on the right, under **Select the protection action type** option, select **Set user-defined permissions (Preview)**. Note the options that are selected be default; do NOT change them. Select **OK**.

	- Set visual marking (such as header or footer):

		- Documents with this label have a header: **Off**

		- Documents with this label have a footer: **Off**

		- Documents with this label have a watermark: **On**

			- Watermark text: **Personal Identifiable Information (PII)**

			- Watermark font size: **Auto**

			- Watermark font name: **Custom**, and then enter **Segoe UI** in the font name field

			- Watermark color: **Custom**, and then enter **#B22222** in the color field (Fire Brick red)

			- Watermark layout: **Diagonal**

8. Select **Save** in the upper left corner.

9. In the **Save settings** pop-up window that appears asking if you’re sure about saving and publishing the changes, select **OK.**

1. In Microsoft Edge, open a new tab and enter the following URL in the address bar: https://security.microsoft.com/

10. In the **Microsoft 365 security** window, under **Classifications** in the left-hand navigation pane, select **Sensitivity labels** and click the **Publish labels** button

11. In the **Choose sentivity labels to publish** window, click the **Choose sensitivity labels to publish**, select **Select all** and click **Add** and **next**

12. In the **Publish to users and groups** window, click **Next**.

1. In the **Policy settings** window, select **Users must provide justification to remove a label or classification label** and click **next**

1. In the **name your policy** Window type **Global - Unified** in the name fiald and click **Next**

1. In the **Review and finish** window, click **Submit** and click **Done** to close the window

15. Leave your browser's tabs open as you will use the Azure information protection one in the next exercise when you configure Windows Information Protection. 

You have now configured a new custom AIP label named PII and added published it to all users.


### Task 3 – Assign an AIP label to a document

In this exercise you will use the AIP label that you created in the previous task to classify a document. For this task, you will sign into Microsoft Azure Information Protection as Alex Wilber, who is a regular user without any elevated privileges.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.

2. In the **Search** box on the taskbar at the bottom of the window, type **Word**. In the menu that appears, select **Word.** 

3. After **Microsoft Word** opens, a **Microsoft Azure Information Protection Sign-in** window appears. In the **Pick an account** window, select **Use another account**, then sign in as **AlexW@M365xZZZZZZ.onmicrosoft** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and then select **Next**.

4. On the **Enter password** window, enter **Pa55w.rd** and select **Sign in**.

5. In **Word,** select **Blank document**.

6. If the **What’s New** pane appears on the right, close it.

7. In the **Word** document, type **Testing personally identifiable information (PII).**

8. There are two new additions to Word that appear as a result of having installed AIP at the start of this exercise: <br/>

	- In the **Home** ribbon, locate the **Protection** group. 
	
	- Below the **Home** ribbon, locate the **Azure Information Protection** bar. Since you created a label titled **PII** in the prior task, **PII** will appear in the middle of the AIP bar. 
	
	Select the **PII** button on the **Azure Information Protection** bar.

9. In the **Microsoft Azure Information Protection** window that appears, select the following options:

	- Select permissions: **Viewer – View Only**

	- Select users, groups, or organizations: Since Outlook is not running on the client, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider). Note: If Outlook was running, you could select the **address book** icon and then select **Joni Sherman**. <br/>

	- Expire access: Select the **Calendar** icon and then select tomorrow's date

10. Select **Apply** to finish the protection process.

11. Scroll down through the document and note the watermark that was applied. This is based on the PII label that you created in the prior task that you then applied to this document. The watermark should appear in Fire Brick red, and it should appear diagonally across the page.

12. Select **File** from the top menu bar.

13. Select **Save As** on the left menu.

14. Under the **Save As** pane, select **Browse**. 

15. In the **File Explorer** window, you should see the **Documents** folder by default; if not, navigate to **Documents** folder. Enter **ProtectedDocument** as the name of the file and then select **Save**.

16. In the **Word** doc, note how the **RESTRICTED ACCESS bar** now displays below the ribbon at the top of the page. This is a result of the **Protect** option you set for the **Permissions** parameter in the **PII label** that you created earlier. In this bar, select **Change Permission…**

17. In the **Permissions** window that appears, note how Joni Sherman (**JoniS@M365xZZZZZZ.onmicrosoft.com**) has been assigned **Read-only** permissions, but no one has been assigned the ability to change the document. In the next task, you will test out this policy. Select **OK** to close the Permissions window. 

18. Close Word.

19. Leave the Client 1 VM and your browser open and proceed to the next task.

You have just successfully created an AIP protected Word document that expires the next day, is read-only protected, and is accessible only by its creator, Alex Wilber, and Joni Sherman (with Read-only permission).


### Task 4 – Verify AIP policy

In the prior task, you created a Word document and protected it with Azure Information Protection by inserting a watermark and restricted permissions. To verify whether the protection that you assigned to the document works, you will first email the document to Joni Sherman and to your own personal email address. You will then test what functionality is possible for both Joni and yourself.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. If you have **Outlook on the web** open in a tab in your **Edge** browser, then select it now and proceed to the next step; otherwise, if you have a tab with the **Microsoft Office Home** page, then select the tab, select **Outlook**, and then proceed to the next step. If you have neither tab open, then in a new tab enter **https://outlook.office365.com** and sign in as **holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).

3. In **Outlook on the web**, select **+New Message** in the upper left part of the screen.

4. In the right-hand pane, enter the following email information:

	- To: Enter **Joni** and then select **Joni Sherman** from the user list. 

	- CC: Enter your own personal email address (not Holly's; in this case, enter your own email address)

	- Add a subject: **Protected Document Test**

	- Add a message or drop a file here: **If you can open the protected and restricted document attached to this email, then try to change it.**

	- Select **Attach** from the top menu and select **Browse this computer**. In the **File Explorer** window, select the **Documents** folder, select the **ProtectedDocument.docx** file that you created in the prior task, and then select **Open.**

5. Select **Send**.

6. Switch to LON-CL2. 

7. In LON-CL2, you should be logged into **Outlook on the Web** as **Lynne Robbins** from a previous lab exercise. Sign out as Lynne and then navigate to **https://outlook.office365.com** and sign back in as Joni Sherman (**JoniS@M365xZZZZZZ.onmicrosoft.com**, where ZZZZZZ is the tenant suffix ID provided by your lab hosting provider) with a password of **Pa55w.rd**.

8. In Joni’s **Inbox** in **Outlook on the web**, select the email that Holly just sent her, and then select the attached **ProtectedDocument.docx** file to open it. 

9. You should receive an error message indicating that the file is protected by Information Rights Management (IRM); therefore, you must use Microsoft Word to open it. Select the **X** in the upper right-hand corner of the larger window to close it.

10. This will return you to **Outlook on the web** with the email still displayed in the right-hand pane. In the body of the email, the document appears in a tile, with a drop-down arrow in the lower right corner of the tile. Select the drop-down arrow, and in the menu, select **Download**.

11. In the notification bar that appears at the bottom of the screen, select **Save.** 

12. Once the file has finished downloading, in the notification bar, select **Open.**

13. **Microsoft Word** should open along with a **Sign in** window (it may open behind the Outlook window, in which case select the **Word** icon on the taskbar to bring it forward). 

14. Because the file is RMS protected and no AIP client is installed on LON-CL2, you need to use the native RMS features of Word ProPlus and register this installation to Joni’s account. <br/>

	‎In the **Sign in** window, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** and then select **Next.** 

15. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in.**

16. In the **Use this account everywhere on your device** window that appears, select **This app only** to register this Office 365 ProPlus installation to **Joni Sherman’s** Microsoft 365 account.

17. The file should open in Word, since you assigned Joni with Read-only permission. Review the three notification bars that appear above the document. 

18. Try to change the file. Word should not recognize any keystrokes, and it should display the following message above the taskbar: **This modification is not allowed because the document is open for viewing only.** <br/>  

	‎**Note:** You have just verified that the permissions assigned to the file are working properly. Joni can read the file (since she was assigned Read-only permission), but she is unable to change it (no one was assigned Edit permission).

19. Close Word.

20. You will now test what happens when you attempt to open the document that was sent to your personal email address. Use your phone or classroom PC to access your personal email address. Open the email that you (in the role of Holly) just sent to your personal email address, and then attempt to open the attached file. 

21. You should receive a messaging indicating that you are not signed into Office with an account that has permission to access the document. You can optionally sign in with an account that has permission to access the file, or request access from the **AlexW@M365xZZZZZZ.onmicrosoft.com** account, or Cancel out of the operation. Select **Cancel**.  <br/>

	‎Since only Joni was assigned permission to read the document, you just verified that Azure Information Protection protected the document based on the PII policy parameters that you configured.

22. Remain signed into LON-CL2 and signed into Outlook on the Web as Joni. Do not close your browser.


# Proceed to Lab 7 - Exercise 2
