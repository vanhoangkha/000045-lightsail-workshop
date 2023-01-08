+++
title = "Update database configuration"
date = 2021
weight = 3
chapter = false
pre = "<b>5.3 </b>"
+++


#### Update the application's database configuration.

In this step, we will define the endpoint of the Amazon Relational Database Service instance we created, and then configure the application to connect to the RDS instance.

1. Return to the [RDS console](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1) interface. (We still use Region Singapore throughout in the lab, if you use another Region, you will have to change the Region to suit). Under **Resources**, click **DB Instances**.

![Lightsail](/images/12/0001.png?featherlight=false&width=90pc)

2. Click on the name **database-1** RDS instance that we created in the preparation step.

![Lightsail](/images/12/0002.png?featherlight=false&width=90pc)

3. In the **Connectivity & security** section, save the endpoint information.

![Lightsail](/images/12/0002.png?featherlight=false&width=90pc)

4. Return to the [Lightsail console] interface (https://lightsail.aws.amazon.com/ls/webapp/home/).

5. Connect to the public IP address of the Lightsail instance to access the todo app.
6. Click **Settings**, then update **DB Hostname** with RDS endpoint, click **Save Settings**.
![Lightsail](/images/1-deploy-infra/0062.png?width=90pc)
{{%notice tip%}}
Carefully check the endpoint information when you copy and paste it into the **DB Hostname** field, avoiding extra spaces at the end.
{{%/notice%}}

7. We will see that the Task list will not have the tasks we created, because we are using the new Amazon RDS database.

![Lightsail](/images/1-deploy-infra/0063.png?width=90pc)

8. Do the same for both Lightsail instances. Then we create tasks on each Lightsail instance. As a result we will see that the task is fully visible on the todo application no matter which instance we are connecting directly to.

So we have configured the firewall (security group) of the RDS instance to accept connections from the Lightsail subnet. Next we will configure our application to connect to the Amazon RDS endpoint.

{{%notice tip%}}
During the update of DB Hostname configuration for todo application, you may get below error. Since each time it connects to the DB, the todo application tries to create the tasks table.
You can ignore this error and perform Refresh (press F5 key) to continue connecting the application to the RDS Instance. \
```
Saving settings and testing connection


Connecting to the database.

There was an error connecting to the database server:
CREATE DATABASE IF NOT EXISTS tasks; use tasks; CREATE TABLE tasks ( id INT(11) UNSIGNED AUTO_INCREMENT PRIMARY KEY, summary VARCHAR(30) NOT NULL, details VARCHAR(250) NOT NULL, priority VARCHAR(20) NOT NULL, dueDate TIMESTAMP, isComplete VARCHAR(10) );
SQLSTATE[42S01]: Base table or view already exists: 1050 Table 'tasks' already exists
```
{{%/notice%}}