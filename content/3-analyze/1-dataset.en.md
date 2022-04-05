---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>3.1 </b>
title: Data Set
weight: 31
---

#### Create a data set

You retrieve data from a data store by creating a SQL dataset or a container dataset. AWS IoT Analytics can query the data to answer analytical questions.

1. Navigate to the **AWS IoT Analytics** console.
2. In the left navigation pane, navigate to **Data sets**
3. Choose **Create a data set**
4. Select **Create SQL**
    * **ID:** ``streamdataset``
    * **Select data store source:** iotastore, this datastore is associated with S3 bucket containing the transformed data created in [step 2.4](/2-streaming-workflow/4-analytics-data-store).
7. Click **Next**
8. Keep the default SQL statement, which should read ``SELECT * FROM iotastore`` and click **Next**
9. Input the folllowing:
    * **Data selection window:** Delta time
    * **Offset:** -5 Seconds - the 5 second offset is to ensure all 'in-flight' data is included into the data set at time of execution.
    * **Timestamp expression:** ``from_iso8601_timestamp(timestamp)`` - we need to convert the ISO8601 timestamp coming from the streaming data to a standard timestamp. **Next**.
10. Keep the query schedule as *Not scheduled*, which implies you will have to run the query manually later. Keep all other options as default and click **Next** until you reach 'Configure the delivery rules of your analytics results'
11. Click **Add rule**.
12. Choose **Deliver result to S3**.
    * **S3 bucket:** select the S3 bucket that ends with '-dataset'.
    * **IAM Role:** Create New role that allows IoT Analytics to put data to S3 and give your new IAM Role a name, for example ``iot-analytics-dataset-role``.
13. Click **Create data set** to finalize the creation of the data set.

The data set details should look as follows:

![Data Set Details](/static/images/dataset.png?width=800px)