---
title: Dedicated Database
layout: doc-page
weight: 5
description: Extra DB juice with just a few clicks. 
---

For the most reliable service, we recommend using a dedicated database for your production apps. Luckily, PHP Fog makes gives you the ability to upgrade in a matter of a few clicks to dedicated database with the following configuration:
 
* Amazon RDS
* MySQL 5.5
* Daily snapshots for disaster recovery

### 1. In your app console, under "account" click on "Dedicated Database".

### 2.  Fill out the requested information.

The CIDR is the IP range you want to give remote database access to. 

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
