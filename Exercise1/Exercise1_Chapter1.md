# Chapter 1: Access SAP Business Application Studio and create a project

< [Back to Exercise 1](./README.md)

## Access Business Application Studio

1) Click [here](https://xaea1811-cf-eu10.eu10cf.applicationstudio.cloud.sap/index.html) to open the Business Application Studio (BAS for short). 

2) Please use the P-User with the initial password  `Initial1` that was included in the email to log in to BAS. You will be prompted to change your initial password.

   ![img](./Images/IMG-000.png)

## Create Development Space

1) Click on **Create Dev Space** to create a new development environment for your project. 

   ![img](./Images/Exercise1_001.png)

2) Give your Development Space the Name **HCX** and make sure to select **SAP HANA Native Application** as application. You do not need to add any Additional SAP Extension. Click on **Create Dev Space**.

   ![img](./Images/Exercise1_002.png)

3) Your HXC Dev Space is being created right now. It takes roughly 2-3 minutes to switch from **STARTING** to **RUNNING**. Now that your space is running click on the Name **HXC** to open it. Your BAS Development Editor opens, in which you create your projects.

   ![img](./Images/Exercise1_003.png)

## Set Cloud Foundry Endpoint

1) To start developing, you need to tell BAS where you want to deploy your project. Click on **View** and then on **Find Command...**.

   ![img](./Images/Exercise1_003_1.png)

2) Type in ``cf login``. Select the given option.

   ![img](./Images/Exercise1_004.png)

3) The text box at the top opens up, and you need to **confirm** the already given **Cloud Foundry Endpoint** `https://api.cf.eu10.hana.ondemand.com` by pressing **Enter**.

   ![img](./Images/Exercise1_005.png)

4) Paste the given Platform Username from the Landing Page: ``platformEA1811``

   ![img](./Images/Exercise1_006.png)

5) Paste the given Platform User Password from the Landing Page: ``Welcomek9cG0``

   ![img](./Images/Exercise1_007.png)

6) Select the given organization

   ![img](./Images/Exercise1_008.png)

7) Set the Space to the dev

   ![img](./Images/Exercise1_009.png)

8) You set your Cloud Foundry space successfully.

   ![img](./Images/Exercise1_010.png)

## Import the project

1) Now it is time to import your project. You have multiple options to do so. In our case, we import the project from Git. Click on **Clone from Git**.

   ![img](./Images/Exercise1_011.png)

2) Insert the following link in the text box at the top: ```https://github.com/SchneiderKarl/HCX_INCIDENTREPORT_DF.git```

   ![img](./Images/Exercise1_012.png)

3) After you pressed enter, the cloning process starts.  When it is done you will receive a notification at the bottom right.

## Open the project

1) To open the cloned project, click on **Open**.

   ![img](./Images/Exercise1_014_1.png)

2) On the left, you should now see the imported project. In this area, you design your database objects. Click on the **arrow** next to the project name to expand the folder structure.

   ![img](./Images/Exercise1_017.png)

## Expand SAP HANA Projects tab

To bind your project to an HDI Container, you will need to use the runtime area. Take the **SAP HANA Projects** tab, located at the bottom of your screen, **expand**, and **pull it up to the middle of the screen**. For a better overview, **expand the folders**. 

![img](./Images/Exercise1_018_1.gif)

## Bind User-Provided Service

To access data that resides outside of the HDI Container, we will need to use a user-provided service. 
1) Click on the **Plug-Symbol** on the **cross-container-service-1** in the bottom part to bind this service (if you do not see the Plug-Symbol, hover over it).

   ![img](./Images/Exercise1_019.png)

2) Select the first binding option: **Bind to the 'HCX_SCHEMA_UPS' service**

   ![img](./Images/Exercise1_020.png)

3) If successful, you should see the following message:

   ![img](./Images/Exercise1_021.png)

## Bind HDI Container

1) Click on the plug symbol next to the **hdi_hcx-db** to create an HDI Container.

   ![img](./Images/Exercise1_022.png)

2) The command line at the top should pop up. Click on **+ Create a new service** **instance**.

   ![img](./Images/Exercise1_023.png)

3) Behind the given name add a **-YOURNAME** and hit enter.

   ![img](./Images/Exercise1_024.png)

4) Building your HDI container initially takes around one and a half minutes.

   ![img](./Images/Exercise1_025.png)

5) If this message pops up please press **Enable**.

   ![img](./Images/IMG-001.png)

## Deploy the project to HANA Cloud

Click on the rocket symbol to **deploy** the design-time objects to the HANA runtime. The terminal opens and lets you know if the deployment was successful.

![img](./Images/Exercise1_026.png)

## What you achieved in this chapter:

- You successfully connected your BAS with the Business Technology Platform, imported a project, and  deployed it.
- You connect your HDI Container to the User Provided  Service **HCX_SCHEMA_UPS** allowing you to access database objects outside your  HDI Contianer.
- You created an HDI Container Instance in HANA  Cloud, which you can also find in the BTP Service Instance area.

[Go to Chapter 2](./Exercise1_Chapter2.md) >

