---
chapter: false
date: "2020-10-10T18:28:43-05:00"
pre: <b>2.3 </b>
title: IoT Analytics Channel
weight: 23
---

#### Create the IoT Analytics Channel

A channel collects and archives raw, unprocessed message data before publishing this data to a pipeline. Next we will create the IoT Analytics channel that will consume data from the IoT Core broker and store the data into your S3 bucket.

1. Navigate to the **AWS IoT Analytics** console.
2. In the left navigation pane, navigate to **Channels**
3. **Create** a new channel
    * **ID:** ``streamchannel``
    * **Choose the Storage Type:** Customer Managed S3 Bucket, and choose your Channel S3 bucket (ending in '-channel'.) created in the previous step.
    * **IAM Role:** Create New, and give your new IAM Role a name, for example ``iot-analytics-role``. This will give IoT Analytics the correct IAM policies to access your S3 bucket.

    ![Create Channel](/static/images/create-channel.png?width=720px)


7. Click '**Next**' and input the following.  This step will create an IoT Rule that consumes data on the specified topic.
    * **IoT Core topic filter:** ``smarthome/house1/energy/appliances``
    * **IAM Role:** Create New, and give your new IAM Role a name, for example ``iot-core-analytics-role``. This will give IoT Analytics the correct IAM policies to access your AWS IoT Core topic.
    * Click on **See messages** to see the messages from your smartbuilding device arriving on the topic. Ensure your device is still running in Device Simulator if you do not see any messages.
8. Click **Create Channel**