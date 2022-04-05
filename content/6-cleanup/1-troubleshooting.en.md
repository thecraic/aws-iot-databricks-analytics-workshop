---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>6.1 </b>
title: Troubleshooting
weight: 61
---


### Troubleshooting
To aide in troubleshooting, you can enable logs for IoT Core and IoT Analytics that can be viewed in **AWS CloudWatch**.

#### AWS IoT Core

1. Navigate to the **AWS IoT Core** console
2. Click on **Settings** in the left-hand pane
3. Under **Logs**, click on **Edit**
   * **Level of verbosity**: Debug (most verbose)
   * **Set role**: Click **Create New**
   * **Name:** iotcoreloggingrole
   
The log files from AWS IoT are send to **Amazon CloudWatch**. The AWS console can be used to look at these logs.

For additional troubleshooting, refer to here [IoT Core Troubleshooting](https://docs.aws.amazon.com/iot/latest/developerguide/iot_troubleshooting.html)


#### AWS IoT Analytics

1. Navigate to the **AWS IoT Analytics** console
2. Click on **Settings** in the left-hand pane
3. Under **Logs**, click on **Edit**
   * **Level of verbosity**: Debug (most verbose)
   * **Set role**: Click **Create New**
   * **Name:** iotanalyticsloggingrole
   * **Create role**
4. Click on **Update**

The log files from AWS IoT Analytics will be send to **Amazon CloudWatch**. The AWS console can be used to look at these logs.

For additional troubleshooting, refer to here [IoT Analytics Troubleshooting](https://docs.aws.amazon.com/iotanalytics/latest/userguide/troubleshoot.html)