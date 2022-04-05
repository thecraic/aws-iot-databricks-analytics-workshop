---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>4.2 </b>
title: Visualise your data set with AWS Quicksight
weight: 42
---

#### Visualise your data set with AWS Quicksight

1. Navige to the **AWS Quicksight** console.
2. Click on **New analysis**
3. Click on **New data set**
    ![New Data set Quicksight](/static/images/new-dataset-quicksight.png?width=780px)
4. Choose **AWS IoT Analytics** under FROM NEW DATA SOURCES.
5. Configure your AWS IoT Analytics data source.
    * **Data source name**: streamdataset
    * **Select an AWS IoT Analytics data set to import**: streamdataset
    ![Data source Quicksight](/static/images/datasource-quicksight.png?width=780px)
6. Click on **Create data source** to finalise the Quicksight dashboard data source configuration. You should see the data has also been imported into SPICE, which is the analytics engine driving AWS Quicksight.
7. Click on **Visualize** and wait a few moments until you see 'Import complete' in the upper right hand of the console. You should see the data have been imported into SPICE.
8. Under **Fields list**, select 'timestamp' to set the X axis for the graph.
9. Click on **sub_metering_1**, **sub_metering_2** and **sub_metering_3** to add them to the **Value** column. 
10. In the Field wells, for each **sub_metering**, choose the drop-down menu and set **Aggregate** to **Average**.
11. For **timestamp**, choose the drop-down menu and set **Aggregate** to **Minute**.

The graphs will look similar to below. 

![Quicksight Dashboard](/static/images/quicksight-dashboard.png)

You can use different fields or visual types for visualizing other smart home related information. 


:::alert{type="info"}
<p style='text-align: left;'>
You have a dashboard to analyze your smart home data</p>
:::