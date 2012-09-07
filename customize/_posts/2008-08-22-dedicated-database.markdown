---
title: Dedicated Database
layout: doc-page
weight: 5
description: Extra DB juice with just a few clicks. 
---

For the most reliable service, we recommend using a dedicated database for your production apps. Dedicated database on PHP Fog features:
 
* Amazon RDS
* MySQL 5.5.23
* Daily snapshots for disaster recovery (perform your own direct backups)

### Small Dedicated Database

* $150 per month
* 1.7 GB Memory
* 26 GB Storage Volume
* Moderate I/O Capacity

### Large Dedicated Database

* $500 per month
* 7.5 GB Memory
* 50 GB Storage Volume
* High I/O Capacity

### X-Large Dedicated Database

* $800 per month
* 15 GB Memory
* 100 GB Storage Volume
* High I/O Capacity

# Installation

### 1. In your app console, under "account" click on "Dedicated Database".

### 2.  Fill out the requested information.

The CIDR is the IP range you want to give direct database access to.

### 3. Migrate your database.

Once your new dedicated database is provisioned, you'll need to migrate your data from the PHP Fog shared database. You can do this easily from phpMyAdmin which you can access from your app console under the "Database" tab.

<img class="screenshot" src="/img/screenshots/database.png" alt="Launch PHPMyAdmin"/>

Select the "Synchronize" tab in phpMyAdmin.

<img class="screenshot" src="/img/screenshots/db_sync.png" alt="Synchronizing your
Database"/>

Using the credentials provided for you new database host, synchronize the database of your app to the new RDS instance.

### 3.  Update your environment variables in your code to reflect the new dedicated database host.

Once you change the database connection information in your app to connect to the new dedicated database, commit, and push your code, your new dedicated database will be live! 

Please note that there will be two sets of credentials, one for the PHP Fog shared database and one for your new dedicated database.

<img class="screenshot" src="/img/screenshots/env-vars.png" alt="Environment Variables"/>
