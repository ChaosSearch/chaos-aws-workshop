---
title: "Alerting"
chapter: true
weight: 33
---

## Alerting

ChaosSearch alerts page is the list of all alerts that are visible within the platform. This guide will walk through the creation of a _Monitor_, a _Trigger_, and the specific _Destination_ that alerts should be sent to.

Alerts are part of the Open Distro of Kibana and allows you to create a monitor, a trigger for the monitor and a destination to send the alert. In Kibana, Alerts are accessed by selecting the Alert Icon as pictured below:

![](/images/analytics/kibanaalerting.jpg)

Create Monitor - Creating a monitor in ChaosSearch will allow you to specify a particular value that should be monitored when defining the monitor by utilizing the extraction query or visual graph.

Create Trigger - To create a trigger, you specify the threshold value for the field that is being monitored. If the value of the field exceeds the threshold, the Monitor enters the Active state.

Create Destination - Choose between a Slack channel, AWS Chime, or you can set up a custom webhook to receive messages. If you choose a custom webhook, you will set up headers and a message body, and the plugin will POST its message to the destination URL.

## Alerting Exercise

For this exercise we will monitor ELB logs for backend\_status\_codes \&gt; 200. The alert will be sent to a Slack workspace that has already been defined.

Alerts Exercise Objectives:

- Use the Alert Icon in Kibana to create a monitor
- Create a Trigger for the monitor
- Choose the predefined destination **Slack Workshop** to send the Alerts to.

From Kibana, select the Alert Icon as pictured above. The initial Alert pages is a dashboard of all existing monitors. In the picture below, we have no monitors defined.

![](/images/analytics/viewmonitors.jpg)

Select **Create Monitor** in the middle of the screen. In the **Configure Monitor** screen enter the following:

- **Monitor Name** : Enter **chaosXX-mon**
- **Monitor State: leave unchecked - t** his will enable the monitor on creation

## Define Monitor

- **How do you want to define the monitor:** Enter **Define using visual graph**
- **Index:** From the drop down select the **view** you created in the **Refinery exercise.**  
**Note:** If you didn&#39;t create a view in the Refinery Exercise you may use **chasoMSTR-v**.
- **Timefield:** From the **drop down, select timestamp**

At this point your screen should look like:

![](/images/analytics/definemonitor.jpg)

Scroll down to view the remainder of the screen. The first thing you will see is the graph, this is a result from our choice for **How do you want to define the monitor:** Enter **Define using visual graph.**

Since we are looking for `backend_status_codes IS NOT 200` we will define **Create Monitor For** and the **timeframe** of the **last 30 days.**

- Use the drop down list for **FOR THE LAST** and select **30 day(s)**
- **For the where clause select**
  - **Field: backend\_status\_code**
  - **Operator: is not**
  - **Value: 200**

  ![](/images/analytics/monitorfilter.jpg)

Scroll down to **Monitor Schedule** and select

- **Frequency: by interval**
- **Every 1 Minutes**

Select the **Create** button on the bottom right of the screen. This will create the **Monitor** and bring you to a **Create Trigger** screen for the monitor.

## Define Trigger

To **Define** the **Trigger** enter the following:

- **Trigger Name chaosXX-trg**
- **Security Level** Choose the level from the drop down list. **Choose 1**
- **Trigger Condition** choose the number of occurrences to trigger the alert. **Choose 10**

![](/images/analytics/definetrigger.jpg)

Now we need to **Configure Actions -** what to do when the Alert has triggered. Enter the following:

- **Action Name: chaosXX-act**
- **Destination: From the pull down Select SlackDemo -(Slack)**
- **Message Subject: chaosXX Alert**

Scroll down and look at the **Message Preview** then Select **Create** at the bottom right of the screen. You are brought to the screen for the Alert you just created.

![](/images/analytics/alertdashboard.jpg)


{{% notice note %}}
ChaosSearch Alerting Documentation [https://docs.chaossearch.io/docs/alerting-overview](https://docs.chaossearch.io/docs/alerting-overview)
{{% /notice %}}


