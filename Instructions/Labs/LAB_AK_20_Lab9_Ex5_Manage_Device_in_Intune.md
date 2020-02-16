# Module 20 - Lab 9 - Exercise 5 - Manage and Monitor a Device in Intune


Holly Dickson wants to make managing devices easier, so she has decided to implement Microsoft Intune device categories in her pilot project. Implementing device categories will enable her to automatically add devices to groups based on categories that she defines.

As part of managing devices in Intune, Holly will create dynamic groups in the Azure portal, based on the device category and device category name. After you configure device groups, users who enroll their device will be presented with a list of the categories you configured. After they choose a category and finish enrollment, their device is added to the Active Directory security group that corresponds with the category they chose.

### Task 1: Create device categories

1. In the LON-CL1 VM, you should still be logged in as **lon-cl1\admin**, and you should still be logged into the Azure portal as **Holly Dickson**.
2. In the **Azure portal**, in the navigation thread at the top of the screen (**Home > Microsoft Intune > Devices – Azure AD Devices**), select **Microsoft Intune**.
3. In the **Microsoft Intune – Overview** page, in the middle pane under **Manage,** select **Device enrollment**.
4. On the **Device enrollment** pane, in the middle pane under **Manage**, select **Device categories.**
5. In the detail pane on the right, select **+Create device category**.
6. On the **Create device category** page, under the **Basics** pane, in the **Name** text box, enter **Mobile Device** and then select **Next**.
7. On the **Scope tags** pane, select **Next**.
8. On the **Review + create** pane, select **Create**
9. On the **Device enrollment – Device categories** window, select **+Create device category**.
10. On the **Create device category**, under the **Basics** pane, in the **Name** text box, enter **Desktops** and then select **Create**.
11. On the **Scope tags** pane, select **Next**.
12. On the **Review + create** pane, select **Create**

### Task 2: Manage a device and assign it to a category

1. In the **Azure portal**, in the navigation thread at the top of the screen (**Home > Microsoft Intune > Device enrollment > Device Categories**), select **Microsoft Intune**.
2. In the **Microsoft Intune – Overview** page, in the middle pane under **Manage,** select **Devices**.
3. On the **Devices** page, in the middle pane under **Manage**, select **All devices**.
4. In the details pane, select **LON-CL2**, which is the devicethat you joined to Azure AD (and which was automatically enrolled to Intune).<br/>

    **Note:** Do not select the check box to the left of LON-CL2; select directly on LON-CL2, which opens the LON-CL2 window.
5. On the **LON-CL2** device pane on the right, review the device details. Also review the actions that you can start against the device (available on the taskbar).
6. In the middle pane, under the **Manage** section, select **Properties**. In the **Device category** field, the current value is **Unassigned**. Select the drop-down arrow for this field and in the menu, select **Mobile device** and then select **Save**.<br/>

    **Note:** For Android or iOS devices, you must select the **Device category** during enrollment.
7. In the middle pane, under the **Monitor** section, select **Hardware.**
8. In the detail pane on the right, review the hardware information that synced from the device. Also scroll down review the **Conditional access** section at the bottom of the page.
9. In the middle pane, under the **Monitor** section, select **Discovered apps** and review the list of apps that were discovered on the device.

### Task 3: Create a dynamic group for device categories

1. In the **Azure portal** , in the navigation thread at the top of the screen (**Home > Microsoft Intune > Devices – all devices > LON-CL2 – Discovered apps**), select **Microsoft Intune**.
2. In the **Microsoft Intune – Overview** page, in the middle pane under the **Manage** section, select **Groups**.
3. In the detail pane on the right, select **+New group**.
4. In the **New Group** window, enter the following information:

    - Group type: **Security**
    - Group name: **Mobile Devices**
    - Membership type: **Dynamic Device**

5. Below the **Dynamic device members** section, select **Add dynamic query**.
6. On the **Dynamic membership rules** window, hover your mouse over the row to display the rule fields, and then enter the following values:

    - Property:   **deviceCategory**
    - Operator: **Equals**
    - Value: enter **Mobile Device**

7. Select in the **Rule syntax** field to review the query syntax **(device.deviceCategory -eq "Mobile Device")**.
8. Select **Save.**
9. On the **New Group** window, select **Create.** The Mobile Device group should now appear in the list of groups.

### Task 4: Create a conditional access policy
The modern security perimeter now extends beyond an organization's network to include user and device identity. Organizations can utilize these identity signals as part of their access control decisions.

Conditional Access is the tool used by Azure Active Directory to bring signals together, to make decisions, and enforce organizational policies. Conditional Access is at the heart of the new identity driven control plane.

In this task, you will create a conditional access policy that Holly plans to implement in her pilot project. 

1. In the **Azure portal** , in the navigation thread at the top of the screen (**Home > Microsoft Intune > Groups – All groups**), select **Microsoft Intune**.
2. In the **Microsoft Intune – Overview** page, in the middle pane under the **Manage** section, select **Conditional access**.
3. In the detail pane on the right, select **+New policy**.
4. On the **New** pane, in the **Name** text box, type **Conditional1** and then select the **Users and groups** section.
5. On the **Users and groups** pane, select the **All users** radio button and then select **Done**.
6. On the **New** pane, select the **Cloud apps or actions** section.
7. On the **Cloud apps or actions** pane, select the **Select apps** radio button and then select the **Select**
8. In the **Select** pane, select **Office 365 Exchange Online**, select the **Select** button at the bottom of the page, and then select **Done**.
9. On the **New** pane, select the **Conditions** section.
10. On the **Conditions** pane, select the **Device platforms** section.
11. On the **Device platforms** pane, in the **Configure** field, select **Yes**. In the **Include** tab, select the **Select device platforms** radio button, select the **Windows** check box,and then select **Done.**
12. On the **Conditions** pane, select **Done**.
13. On the **New** pane, under **Access Controls**, select the **Grant** section.
14.  On the **Grant** pane, select the **Require device to be marked as compliant** check box, and then select **Select**.
15. On the **New** pane, scroll down and select the **Session** section.
16. In the **Session** pane, review the explanation but do not select any option. Select the **X** in the **Session** pane to close it.
17. On the **New** pane, select **Create**.The **Conditional1** policy now appears in the policy list in the right-hand pane.<br/>

    **Note:** You created a conditional access policy to get familiar with the available options; however, the policy is not effective because you didn&#39;t enable it.



# End of Lab 9
