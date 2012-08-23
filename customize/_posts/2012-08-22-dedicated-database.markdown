---
title: Dedicated Database
layout: doc-page
weight: 5
description: Extra DB juice with just a few clicks. 
---

This guide is to help you setup a dedicated database for your PHPFog apps.

#Specs
- Running MySQL 5.5
- Daily snapshots taken for instance disaster recovery
- Dedicated

#Setup a Dedicated database for your PHPFog apps

For production apps, PHPFog suggests the use of our dedicated database feature.
To enable dedicated database follow these steps

### 1.  Under "account" select "Dedicated Database".

This is where you will fill out the information to setup your new dedicated
database.

### 2.  Fill out the information requested

The CIDR is the IP range you wish to be accessible remotely to your database

# Once your database has been provisioned:

You will need to migrate your database from PHPFog to your new dedicated
database.

### 1.  Connect to PHPMyAdmin to access your shared database.

PHPMyAdmin can be found in your app's console under "database".

<img class="screenshot" src="/img/screenshots/database.png" alt="Launch PHPMyAdmin"/>

### 2. Select the synchronize Tab in PHPMyAdmin.

<img class="screenshot" src="/img/screenshots/db_sync.png" alt="Synchronizing your
Database"/>

### 2. Migrate your data.

Using the credentials provided for you new database host, synchronize the database of your app to the new RDS instance.

### 3.  Update your environmental variables in your codebase to reflect the new dedicated database host.

With your new dedicated data migrated, you can now update your environmental
variables or database credentials to make full use of your new dedicated
database.

Please note that there will be two sets of credentials, one for your existing
shared database and one for your new dedicated database server.

<img class="screenshot" src="/img/screenshots/env-vars.png" alt="Environmental Variables"/>

