# Chapter 2: Explore the Anonymized Report

< [Back to Chapter 1](./Exercise3_Chapter1.md)

## Open HDI Container in the SAP HANA Database Explorer

To view your deployed database objects in SAP HANA Cloud, click on **Open HDI container** next to the rocket.

![img](./Images/Exercise1_027.png)

## Database Explorer

You will be asked to enter your username. Insert the Platform Username ``platformEA1811`` and click on **Next**.

![img](./Images/Exercise1_027_1.png)

The Database Explorer opens, in which you can see all the HANA objects currently available in your HDI container. As you can see from the database's name, you are currently within your recently created HDI container. Click on **Synonyms** to see the tables you are accessing through the user-provided service (which you created in Chapter 1).

![img](./Images/IMG-002.png.png)

## Explore table data

Right-Click on the **INCIDENT_ARCHIVE_VT_SYN** object and select **Open Data** to get an overview about the incidents, that happened in 2020 and are stored in the data lake. 

![img](./Images/Exercise1_029.png)

To explore all tables, proceede in the same way with the other synonym objects.

## Preview the anonymized report

1. Switch to the **Database Explorer** and open your **HDI Container**. Select **Views** in the catalog and right-click on **V_INCIDENT_REPORT_ANONYMIZATION**. Select the **Generate SELECT Statement**. This opens a SQL Console with the statement.

   ![img](./Images/Exercise3_003.png)

2. Before you can run the select statement, you need to **refresh** your View. To do so, **paste** the following code ``REFRESH VIEW XXXXXXXXXXXXXXXXXX ANONYMIZATION;`` into the console and above the previously generated statement. Please **copy** and **paste** the highlighted name from your select statement into the XXX area of the refresh View statement. 

   ![img](./Images/Exercise3_004.png)
   
   Click on the **green** **Play button** to execute both commands.

## Explore the report and gain first Insights

Explore the anonymized report. You will see that there is no way to identify a person through the given quasi-identifiers. 

![img](./Images/Exercise3_005.png)

Maybe you can find a group of employees opening more incidents than others by setting some group by clauses. 

![img](./Images/Exercise3_006.png)

## What you achieved in this chapter:

- No individual can be identified via the remaining information, but it is still possible to set up optimization processes based on the data. 

**Congratulations! You finished the Hands-On Exercises.**

![img](./Images/Exercise3_Finish.gif)

< [Back to start](./README.md)

< [Back to Hands-On Overview](../README.md)
