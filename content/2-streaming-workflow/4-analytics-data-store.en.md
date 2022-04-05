---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>2.4 </b>
title: IoT Analytics Data Store
weight: 24
---

#### Create the IoT Analytics Data Store for your pipeline

A data store receives and stores your messages. It is not a database but a scalable and queryable repository of your messages.

1. Navigate to the **AWS IoT Analytics** console.
2. In the left navigation pane, navigate to **Data stores**
3. **Create** a new data store
    * **ID:** ``iotastore``
    * **Choose the Storage Type:** Customer Managed S3 Bucket, and choose your Data Store S3 bucket created previously (ending in '-datastore').
    * **IAM Role:** Create New, and give your new IAM Role a name, for example ``iot-analytics-datastore-role``. This will give IoT Analytics the correct IAM policies to access your S3 bucket.
4. Click 'Next' and then **Create data store**

![Create DataStore](/static/images/create-datastore.png?width=780px)