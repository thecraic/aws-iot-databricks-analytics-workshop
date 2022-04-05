---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>3.2 </b>
title: Query execution
weight: 32
---

#### Query Execution and Saving the data set

Since the query was not scheduled in the data set created in the previous step, now you have to run the query manually to refresh the data set.  

1. Navigate to **Data sets** on the lefthand navigation pane of the AWS IoT Analytics console.
2. Click on 'streamdataset'
3. Click on **Actions** and in the dropdown menu choose **Run now**.
4. On the left navigation menu, choose **Content** and monitor the status of your data set creation.
5. The results will be shown in the preview pane and saved as a .csv in the '-dataset' S3 bucket.

![Data set preview](/static/images/dataset-preview.png?width=780px)