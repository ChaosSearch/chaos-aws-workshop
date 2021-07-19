---
title: "Getting Started"
chapter: true
weight: 10
---

## Introduction

ChaosSearch is a fully managed, secure service on AWS backed by S3 as a data store. With a few clicks, customers can be up and running in minutes, all at a fraction of the cost of running your own Elasticsearch cluster or ELK Stack.

Learn how ChaosSearch unlocks your Amazon S3 storage and turns it into a secure, durable, and cost-effective search platform with both Amazon S3 and Elasticsearch APIs.

## Step 1 - IAM Role and Policy Access

At ChaosSearch, we give you the ability to make more of your S3 infrastructure by turning into an elastic cluster. The first step in doing so is following the recommended set-up to start the creation of your IAM Role and Policy which will allow us to start listing out all of the S3 buckets within your AWS (Amazon Web Services) account.

## Step 2 - Discover Your Data in S3

Discovery is the first step in understanding all of the files that are stored in your S3 bucket(s). When Discovery starts you will begin to see the different fields populate and update as we continue to understand the contents of the bucket.

## Step 3 - Create an Object Group, a Virtual S3 Bucket

Object Groups are customizable filters for viewing what&#39;s in your buckets for fine-grained object analysis. These virtual buckets are our first steps in auto-discovering and indexing your data. As you move through the Object Group creation you will have the opportunity to define what filtering is needed to separate out the different files. Object Groups can be used for building filters on microservices, log type, log per application, etc.

## Step 4 - Index your Data

In order to see the platform in action, start indexing the data in one of your S3 buckets. During the indexing process, you will start to see different stats populating in the Group Details, Index Details, and Indexed Structure.

## Step 5 - Refinery

ChaosSearch Index Views are logical indexes based on the physical indexes created in the Storage section of the ChaosSearch Platform. The refinery allows users the unique ability to clean, prepare, and transform the index data. Schema Transformation can be applied to one or many fields and the changing of Types between a String, Number, or TimeVal without the need to re-index data.

## Step 6 - Visualization

Now that your data has been indexed, it is available to Elasticsearch and Kibana. Navigate to the Visualization tab to get started. In order to visualize and explore data in Kibana, you&#39;ll need to create an index pattern to retrieve data from Elasticsearch.


{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be architected to build a solution while demonstrating best practices along the way. These examples are not intended for use in production environments.
</p>
{{% /notice %}}