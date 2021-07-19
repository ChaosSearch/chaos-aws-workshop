---
title: "Chaos Refinery®"
chapter: true
weight: 22
---

## Refinery

The ChaosSearch Refinery is a major component of the ChaosSearch service. It provides a variety of capabilities unique to the ChaosSearch platform and will provide a streamlined approach to transforming your data.

The Refinery offers a collection of tooling geared to cleaning, preparing, and transforming data such that users can programmatically and visually interact with information as needed.

Refinery Index Views replace Index Patterns. Index Views are logical indexes based on physical indexes.

The Refinery gives users the unique ability to do Schema Transformation on index data for cleaning, preparing, and transforming without the need to write or execute code.

ChaosSearch&#39;s query cache feature when enabled is used for caching the results of queries. After an initial query is executed, results are cached for improved search results and experience.

## Refinery Exercise

In this exercise we will create a view for the Object Group( **chaosXX-obj** ) and Index we just created. **\* Note** - If you didn&#39;t create an Object Group in the first Exercise you may use **chasoMSTR-obj**. Our view name will be **chaosXX-v** where XX is the ID provided in the workshop package.

Refinery Exercise Objectives:

- Create a View based on the Object created earlier
- Use the Transform Capabilities
- Make the View Cacheable and Case Insensitive

## Create View

**Click Create View**

![](/images/preparing/createview.jpg)

You can now select the object group we just created (chaosxx-obj). To filter the list, simply enter **chao** in the **Search** box.

![](/images/preparing/selectobjectgroup.jpg)

If you wanted to create a view that had a rolling window you could select **Index Window** and then enter the time period to view. For this exercise we will not select the Index Window.

Select **Next** at the bottom right side of the screen to proceed.

You are now presented with the Schema Transformation page where you may change data types and perform transformations in the view. For this exercise we will breakout the field cs\_uri\_stem into 3 fields, Domain, Port and Path. Either scroll down until you see the cs\_uri\_stem field or you can enter cs\_uri\_stem in the **Search Fields** box.

![](/images/preparing/selectfield.jpg)

Click on the **Gear Icon** on the right side of the screen.

  - Select **Refresh** to Preview the data
  - Select **Materialize with Regex** by **Select Transform**
  - For **Field Transform Pattern (REGEX):** Enter **(\\S+[:])(\\d+)(\\S+)**
  - Select the **+ Add Field** 3 times to add 3 new fields
  - Name the Fields:
    - Domain
    - Port
    - Path
  - Select **Refresh** to Preview the data

## Create Transformation

Your screen should now look like:

![](/images/preparing/createtransformation.jpg)

Now select **Save Transform** at the top right of the screen. Scroll through the fields and note the 3 fields you just added to the view. Select **Next** at the bottom right on the screen.

Select a **Timestamp Field,** for this exercise there is only one choice

![](/images/preparing/savetransform.jpg)

Select Create View at the bottom right on the screen.

- Enter the name **chaosXX-v**
- Select **Cacheable**
- Select **Case Insensitive**
- Select **Create**

![](/images/preparing/createviewfinal.jpg)


{{% notice note %}}
ChaosSearch Refinery Documentation [https://docs.chaossearch.io/docs/refinery](https://docs.chaossearch.io/docs/refinery)
{{% /notice %}}