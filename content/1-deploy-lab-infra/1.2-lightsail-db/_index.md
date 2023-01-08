+++
title = "Create Lightsail DB Instance"
date = 2021
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

In this step we will create a database (CSDL) / Database (DB) Lightsail. Lightsail Database is an AWS-managed database service that allows us to reduce the complexity of database deployment and management.

Lightsail will manage the underlying infrastructure and also the database engine, we will only need to take care of creating, deploying and setting up the database tables that run in the Lightsail database.
The resources in the lab should be created in the same Region, here we will use Region Singapore.


1. From [Lightsail's admin interface](https://lightsail.aws.amazon.com/ls/webapp/home/) click **Databases** then click **Create Database**.

![Lightsail](/images/2/0001.png?featherlight=false&width=90pc)

2. From the MySQL dropdown menu, select version 5.7.xx.

![Lightsail](/images/2/0002.png?featherlight=false&width=90pc)

{{%notice tip%}}
By default, Lightsail will create a complex password for you, but this password will contain complex characters that make copying and pasting difficult. In the framework of this lab we will specify the password.
{{%/notice%}}

3. Click **Specify login credentials**.

![Lightsail](/images/2/0003.png?featherlight=false&width=90pc)

4. Uncheck **Create a strong password for me**, then set a password for your Lightsail database and make a note. Here we will set the password as **asg123456**.

![Lightsail](/images/2/0004.png?featherlight=false&width=90pc)

5. Scroll down, in this lab we will implement a high availability database model. Click **High Availability** under **Choose your database plan**.

![Lightsail](/images/2/0005.png?featherlight=false&width=90pc)

6. Drag the screen downwards. Name our database **Todo-DB**. Then click **Create database**.

![Lightsail](/images/2/0006.png?featherlight=false&width=90pc)

7. It will take more than 10 minutes for the Lightsail database to switch to the running state as shown below, congratulations on creating your first Lightsail database.
You can continue with the next steps while you wait for the Lightsail database to be created.

![Lightsail](/images/2/0007.png?featherlight=false&width=90pc)