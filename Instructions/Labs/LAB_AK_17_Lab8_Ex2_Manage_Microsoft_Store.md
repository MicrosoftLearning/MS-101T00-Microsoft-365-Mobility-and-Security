# Module 17 - Lab 8 - Exercise 2 - Manage the Microsoft Store for Business


In this exercise, you will add apps to the company store, and then verify how those apps appear in the store to an Adatum employee.

### Task 1: Add apps to your private store 

1. On your Client 1 VM (LON-CL1), you should still have the **Microsoft Store for Business** tab open in your Edge browser. If so, select it now; otherwise, navigate to **https://www.microsoft.com/business-store** and sign in as **admin@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider).

2. In the **Microsoft Store for Business**, on the menu bar at the top of the page, select **Shop for my group**. 

3. Scroll down to the **Made by Microsoft** section and select **Translator.**

4. On the **Translator** window, leave the **License type** on **Online** and select **Get the app**. 

5. On the **Thanks for your order** page, select **Close**. 

6. This returns you to the **Translator** page. Notice that **License type** is set to **Online,** but if you select the drop-down arrow in the **License type** field, the **Offline licensing** type also is available. Select the **ellipsis (…)** button that appears to the right of the **Install** button. Notice that only the **Manage** option is available. 

7. Select **Shop for my group**, then scroll down to the **Made by Microsoft** section and select **Show all**.

8. In the **Made by Microsoft** window, select **Fresh Paint.**

9. On the **Fresh Paint** window, leave the **License type** on **Online** and select **Get the app.**

10. On the **Thanks for your order** page, select **Close**. 

11. Select **Shop for my group**, then scroll down to the **Made by Microsoft** section and select **Show all.**

12. In the **Made by Microsoft** window, select **Reader**. 

13. On the **Reader** page, the **License type:** field currently displays **Online**. Select the drop-down arrow in the **License type** field and select **Offline**, and then select **Get the app.**

14. On the **Thanks for your order** page, select **Close**. 

15. In the **Microsoft Store for Business**, on the menu bar at the top of the page, select **Manage.**

16. On the **Overview** page, in the **Products and Services** tile, select **Manage apps.**

17. On the **Products and Services** page, as you scroll down through the apps, note how they all have an **Install** button. However, when you get to **Reader,** there is no **Install** button. In the **Reader** section, under **Settings and Actions**, select **More actions available on details page.**  <br/>

	‎**Note:** The **More actions available on details page** option may not immediately appear at this time. Because you selected this app for Offline use, it may take some time for this button to appear. If this **More actions available on details** option does not appear, simply proceed to the next step; otherwise, select this option, and on the **Reader** detail page, note the **Download package for offline use** message and that a **Download** button is available.

18. In the **Microsoft Store for Business**, on the menu bar at the top of the page, select **Adatum private store.** 

19. On the **Adatum private store** page, select **+Add collection.**

20. In the **Add a collection** window, under **Give this collection a name**, enter **Collection1** in the **Enter a collection name** text box. 

21. Scroll down and select the **Add** button below each of the following products: 

	- **Fresh Paint**

	- **Microsoft Remote Desktop**

	- **Translator** 

22. At the bottom of the page, select **Done**. 

23. By default, new apps are only visible to admins; as a result, they must be assigned visibility permissions to be seen by non-admins. So at this point in time, **Collection1** is only visible to admins.   <br/>

	Perform the following steps to assign visibility permissions to **Fresh Paint**, **Microsoft Remote Desktop,** and **Translator**:

	- In the **Microsoft Store for Business**, on the menu bar at the top of the page, select **Manage.**

	- On the **Overview** page, in the **Products and Services** tile, select **Manage apps**.

	- On the **Products and Services** page, scroll down through the apps and select **Fresh Paint.**

	- On the **Fresh Paint** window, select **Private store availability**. Under **Choose groups of people who can see this app**, select **Everyone** if it’s not already selected.

	- If you had to select **Everyone** in the prior step, you can see a **Your changes have been saved.** message at the top of the window.

	- Repeat these steps for **Microsoft Remote Desktop** and **Translator**.

24. Leave the **Microsoft Store for Business** tab open in your Edge browser. You will use this in the next task. 


### Task 2: View your private store as a company employee 

In this task, you are going to sign into the Microsoft Store for Business as one of Adatum’s employees, Joni Sherman. You’ll then verify that when Joni navigates to Adatum’s private store, she can see the 5 apps that were automatically added to the private store, as well as the collection of apps that was created in the prior task. 

1. Switch to the Client 2 VM (LON-CL2) where you should be logged in as the **lon-cl1\\admin** account, and into Microsoft 365 as Joni Sherman (**jonis@M365xZZZZZZ.onmicrosoft.com)** with a password of **Pa55w.rd**.

2. If you are still logged into Microsoft 365 as another user, select the circle in the upper right, select **Sign out,** and then close the other tabs in the browser. 

3. In your **Edge** browser, enter the following URL in the address bar: **https://www.microsoft.com/business-store**

4. On the **Microsoft Store for Business** page, in the upper-right corner of the page, select **Sign in.** 

5. If you are not signed in automatically, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) in the **Sign in** page, and then select **Next**.

6. In the **Enter password** page, enter **Pa55w.rd** and then select **Sign in**.

7. In the **Microsoft Store for Business**, on the menu bar at the top of the page, select **Adatum private store.**

8. In the Adatum private store, verify that Joni can see the following: 

	- The five apps that were automatically added to the private store: Sway, OneNote, PowerPoint Mobile, Excel Mobile, and Word Mobile.

	- The Collection1 app that you created in the prior task that includes: Fresh Paint, Microsoft Remote Desktop, and Translator.


# End of Lab 8