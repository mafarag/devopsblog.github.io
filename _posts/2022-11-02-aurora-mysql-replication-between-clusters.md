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


# Requirements

- Access to an AWS Account

# Set-Up

For this example we are going to have one VPC with two RDS Clusters.  This might not be the setup you will be setting up since it is a fairly simople one. However, this document will concentrate on the core functionailty which is the master slave setup.  This setup is fairly simple to expand to more complex setups with multiple vpcs and accounts.

### Create your Master RDS Server
