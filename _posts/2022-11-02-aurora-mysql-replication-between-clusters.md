---
layout: post
title: "MySQL Replication between RDS Aurora MySQL Clusters"
date: 2022-11-02 17:00:00 -0000
categories: Aurora MySQL Replication DR Automation Cloud
tags: [Aurora MySQL Replication DR Automation Clou]
---

# Summary

If you ever had to look after MySQL replication either On-Prem or Self Managed Cloud VMs, you may have felt a sense of relief when you moved to a cloud managed MySQL such as AWS RDS.

However, even with RDS's more hands-off approach of DB managment there are times when you might to handle the replication yourself.  For example, if you want to replicate your MySQL data to a different AWS region or a different account or even a different cloud provider.

