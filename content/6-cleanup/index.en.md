---
chapter: true
date: "2020-10-10T18:28:43-05:00"
pre: <b>6. </b>
title: Clean Up
weight: 60
---

### Clean up resources in AWS

In order to prevent incurring additonal charges, please clean up the resources created in the workshop.

1. Navigate to the **AWS CloudFormation** console to delete the CloudFormation stacks and their associated resources.
    * Click on **IoTDeviceSimulator** and click **Delete**
    * _Note: Deleting the CloudFormation stacks can take several minutes._
2. Navigate to the **AWS Quicksight** console
    * Click on **Manage Data**
    * Click on **streamdataset** and then **Delete data set** then **Delete**
3. Navigate to the **SageMaker Management Console**:
    * Click on Notebook / Notebook Instances. Choose 'IoTAWorkshopSagemaker', click on Actions to stop, and delete.
4. Navigate to the **S3 Management Console** and delete the following:
    * The 3 buckets you created in [section 3.2](/2-streaming-workflow/2-s3-bucket) ending with '-channel', '-dataset', and '-datastore'
    * Each bucket with the prefix 'iotdevicesimulator' and 'iot-sim'.
    * Each bucket with the prefix 'sagemaker-\<your region\>'
5. Navigate to the **AWS IoT Analytics** console
   * Check that all of your pipelines, data sets, and channels have been deleted. If not, you can manually delete them from the console.