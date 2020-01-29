# Module 20 - Lab 9 - Exercise 4 - Enroll a Windows 10 Device

One of Adatum’s goals for their Microsoft 365 deployment is to enroll their Windows 10 devices to Azure AD and Intune so that the devices can be managed by MDM. As part of her pilot project, Holly Dickson wants to enroll the LON-CL2 PC to Intune. In this exercise, you will first verify that the device is not currently enrolled, and having done that, you will enroll the device to Azure AD and Intune and then verify the enrollment. 

During her pilot project, Holly plans to use certificates with Intune to authenticate Adatum’s users to applications and corporate resources through VPN, Wi-Fi, and email profiles. By using certificates to authenticate these connections, Adatum’s end-users won't need to enter usernames and passwords, which helps to make their access seamless. 

### Task 1: Verify the device is not enrolled

1. You should still be logged into your Client 1 VM (LON-CL1) as the **lon-cl1\\admin** and into Microsoft 365 as **Holly Dickson**.
2. In the **Azure portal**, in the navigation thread at the top of the screen (**Home > Microsoft Intune > Device configuration)**, select **Microsoft Intune**.
3. In the **Microsoft Intune – Overview** page, in the middle pane under **Manage**, select **Devices**.
4. On the **Devices** pane, scroll to the bottom of the detail pane on the right and verify that no device is currently enrolled to Intune.
5. In the middle pane under **Manage**, select **All Devices** and verify that no device is listed in the details pane.
6. Switch to **LON-CL2**. If necessary, log in as the **Admin** account with a password of **Pa55w.rd**.
7. You now want to start the Certificates MMC for the local machine. In the Search field on the taskbar, enter **run**, and then on the menu, select **Run**.
8. In the **Run** window, enter **certlm.msc** in the **Open** field and then select **OK**.
9. In the **certlm – [Certificates – Local Computer]** window, in the left-hand navigation pane, select **Personal** and verify that no certificate is listed in the details pane on the right.
10. Minimize the **certlm – [Certificates – Local Computer]** window as you will use it in a later task.

### Task 2: Enroll the device to Azure AD and Intune

1. In **LON-CL2**, in the Search field on the taskbar enter **access work**, and then in the menu, select **Access work or school**.
2. In the **Settings** app, in the **Access work or school** section, select **+Connect**.
3. In the **Microsoft account** window, on the **Set up a work or school account** page, select **Join this device to Azure Active Directory**.
4. On the **Let's get you signed in** page, in the **Work or school account** text box, enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) and then select **Next**.
5. On the **Enter password** page, enter **Pa55w.rd** in the **Password** field and then select **Sign in**.
6. On the **Make sure this is your organization** dialog box, select **Join**.
7. On the **You&#39;re all set!** page, select **Done**.
8. In the **Settings** app, in the **Access work or school** section, verify that the device is connected to Azure AD and then close the **Settings** app by selecting the **X** in the upper right-hand corner.

### Task 3: Verify the device is enrolled to Azure AD and Intune

1. In **LON-CL2** , maximize the **certlm – [Certificates – Local Computer]** console on the taskbar.
2. In the **certlm – [Certificates – Local Computer]** console, in the left-hand navigation pane, the **Personal** folder should already be selected from the prior task. In the menu bar, select **Action** and then select **Refresh**.
3. In the left-hand navigation pane, under the **Personal** folder, select **Certificates**. In the details pane, verify that several certificates are listed.<br/>

    **Note** : Those certificates were added when you joined the LON-CL2 device to Azure AD and enrolled it to Intune.
4. Close the **certlm – [Certificates – Local Computer]**  console.
5. Switch to the Client 1 VM (**LON-CL1**). You should still be logged in as **lon-cl1\\admin**, and you should still be logged into the Azure portal as **Holly Dickson**.
6. In your **Edge** browser, in the **Azure portal**, the **Device configuration – Profiles** window should be displayed from the prior task.
7. In the navigation thread that appears at the top of the page (**Home > Microsoft Intune > Device configuration – Profiles**), select **Microsoft Intune.**
8. In the **Microsoft Intune – Overview** window, in the middle pane under **Manage**, select **Devices**.
9. In the details pane on the right, verify that one device is now enrolled. Select the **Enrolled devices** tile. The right-hand pane now displays the **LON-CL2** device that you just enrolled to Intune. Note that it is managed by MDM.
10. In the middle pane, under **Manage**, select **Azure AD devices** and verify that in the details pane the same device is listed.<br/>

    **Note:** This view lists devices that are joined to Azure AD. Remember that you configured integration between Azure AD and Intune, and because of that, any device that is joined to Azure AD is automatically enrolled to Intune.
11. Leave the Client 1 VM open for the next exercise.


# Proceed to Exercise 5