---
layout: post
title: "MySQL Replication between RDS Aurora MySQL Clusters"
date: 2022-11-02 17:00:00 -0000
categories: Aurora MySQL Replication DR Automation Cloud
tags: [Aurora MySQL Replication DR Automation Cloud]
---

# Summary

If you ever had to look after MySQL replication either On-Prem or Self Managed Cloud VMs, you may have felt a sense of relief when you moved to a cloud managed MySQL such as AWS RDS.

However, even with RDS's more hands-off approach of DB managment there are times when you might to handle the replication yourself.  For example, if you want to replicate your MySQL data to a different AWS region or a different account or even a different cloud provider.

This article explains how to set this up and get RDS working.


# Example setup.

For this article, we are going to have one VPC with two RDS Aurora MySQL Clusters.  This is a very simple setup and very likely not representative of an environment you are likely to replicate. However, this document will concentrate on the core functionailty which is the master slave setup.  This setup is a fairly simple one and quite straightforward to expand to more complex setups which span multiple vpcs and accounts or even on prem.

These are the core components:

- AWS VPC network
- 1 x Master (Source) Database
- 1 x Slave (Destination) Database

![pond underliner](../aurora-mysql-replication-between-clusters.png)

# Setting Up

## Setup the
