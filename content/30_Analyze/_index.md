---
title: "Analyze"
chapter: true
weight: 30
---

## Analytics

In the analytics section, it&#39;s just Kibana, but we added a few extra features where you can see the query progress bar and the ability to cancel the query. Our Kibana is from the Open Distro open source project. Not from elastic.co open source. That is how we have some different features where items might be different.

## Analytics Exercise

Analytics Exercise Objectives:

- Use the Discover Icon in Kibana and the View you created
  - View the Data
  - Filter the Data for backend\_status\_code not equal to 200
  - Create a quick Visualization from the backend\_status\_code field
- Use the Visualize Icon in Kibana to view **AWS ELB - Backend Status Codes** Pie Chart
- Use the Dashboard Icon in Kibana to view the **ELB Dashboard**

At the top of your screen, in the ChaosSearch Tabs, select **Analytics**.

In Analytics select the **Discover** Icon on the top left side of your screen

Select the **View** you just created from the drop down list. **\* Note** - If you didn&#39;t create View in the Refinery Exercise you may use **chasoMSTR-v**.

![](/images/analytics/selectview.jpg)

Now Select **Last 30 Days** from the **Show Dates** drop down

![](/images/analytics/timefilter.jpg)

This will return all ELB Status codes, but we need to focus only on the error codes. In other words not 200 ELB Status.

To do this Select + Add Filter on the top left of the screen:

- Enter **backend\_status\_code** for **Field**
- Enter **is not** for **Operator**
- Enter **200** for **Value**
- Click **Save**

![](/images/analytics/createfilter.jpg)

Now we will create a quick Visualization based on the data returned in the Discover page.

Scroll down the list of fields on the left side of the screen to **backend\_status\_code** and click on the field.

Next click on **Visualize**

![](/images/analytics/quickvisualize.jpg)

Kibana creates a quick bar chart based on the field **backend\_status\_code** and the filter **NOT backend\_status\_code: 200**

![](/images/analytics/quickvisualization.jpg)