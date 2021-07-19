---
title: "Chaos Index®"
chapter: true
weight: 21
---


## Indexing Types

Enter the **Name** for the Object Group as **chaosXX-obj** where the **XX** is your ID provided in the workshop package

![](/images/preparing/objectgroupname.jpg)


In ChaosSearch you may define Live Indexing which uses SQS to notify ChaosSearch when a new file lands in the S3. We also have the option of Realtime which also uses SQS but indexes in near realtime. Since our data is &#39;Historical&#39; we will not be using SQS.

For Retention you may define the period the index is retained for. We will designate the retention as unlimited.

For this exercise uncheck all the boxes. Click _&#39;__ **Create&#39;** _ at the bottom center of the screen.


## Indexing

Our system will auto-build the mappings for the index structure. So for any fields that are present within the log files, the system will add them into the index itself, it will assign the appropriate type to that index and will dynamically add new fields as they become present.

We can redefine the retention policy if you want to make any specific changes. You can also change the target active index count at point. Meaning how much compute you want focused on this specific object group as work is being done on it. For any insight about the amount of data that has been indexed, it is all available in the index detail section.

## Start Indexing

Your screen should now look like the following, you can begin indexing by clicking &#39;_ **Start Indexing&#39;** _ 

![](/images/preparing/indexing.jpg)

When the indexing has completed your screen should look like the following:

![](/images/preparing/indexingdone.jpg)

{{% notice note %}}
ChaosSearch Object Group/Indexing Documentation [https://docs.chaossearch.io/docs/chaossearch-ui-user-guide](https://docs.chaossearch.io/docs/chaossearch-ui-user-guide)
{{% /notice %}}