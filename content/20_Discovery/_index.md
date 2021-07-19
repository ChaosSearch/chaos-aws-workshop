---
title: "Discovery"
chapter: true
weight: 20
---

## Storage

The Storage section of the **Chaos** Search platform is the entry point to ChaosSearch. We have circled the Storage tab in red. From here, you will be able to start solving some of the more common challenges are Customers face around Live Long-Term Log &amp; Event Storage, Historical Log &amp; Event Analytics, Log &amp; Event Data Management.

The S3 buckets will be listed on the left hand side of the page. We will work with the _ **chaosdemo-datasets** _ bucket, also circled in red.

![](/images/storage/storage.jpg)


## Bucket Discovery

Use the Data Discovery feature to quickly catalog and report on a variety of data sources in your buckets.

Select **&#39;** _ **chaosdemo-datasets&#39;** _ and highlight the _ **&#39;Bucket Content&#39;** _ tab that is circled. The Discovery process should start automatically. If it doesn&#39;t you can select _ **&#39;Discover Bucket&#39;** _ to start the discovery.

![](/images/storage/bucketdiscovery.jpg)


## Storage Exercise

For this exercise we will group ELB Logs together in a virtual bucket called an Object Group. We will filter for ELB logs and then create an index.

Storage Exercise Objectives:

- Create an Object Group
- Use the Filter Capabilities to group logs
- Format and Preview Data
- Validate the Data
- Create and Start an Index

To get started with object groups click **Create Object Group**.

![](/images/storage/createobjectgroup.jpg)


## Filtering Data

It is very common to have a single S3 bucket to store logs from multiple sources. In this case, the </chaosdemo-dataset/> bucket available also contains multiple datasets. In order to filter on just the ELB Logs that we are interested for this exercice, let's do the following:

1. Select the chaosdemo-datasets bucket from the left hand menu
2. Applying filters can be done a few different ways, we will use the **Prefix**

  - Prefix – enter **elb**

![](/images/storage/filteringdata.jpg)

1. Click **Next**

## Format and Preview

The system will be able to identify what file format ChaosSearch will index. Our System can index LOG, JSON, and CSV. ChaosSearch will identify if files are compressed, if so what type of compression. In log format the system will be able to write a regex to identify all available capture groups. It&#39;s possible to change or edit the capture groups by clicking on the pencil icon.

For our exercise ChaosSearch recognizes the **Format** to be Log and there is no **Compression,** additionally a regex is injected to format the content. Click **Validate** to show the formatted data.

![](/images/storage/formatandpreview.jpg)

You should now see a Formatted Preview of the data. Now select **&#39;Create Object Group&#39;** in the lower right hand side of the screen.

![](/images/storage/validateandcreate.jpg)