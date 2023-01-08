+++
title = "Create RDS Instance"
date = 2021
weight = 4
chapter = false
pre = "<b>1.4 </b>"
+++

In this step, we will proceed to create an Amazon Relational Database Service (RDS) database. Amazon RDS is a database service that offers more advanced features than Lightsail databases (various database engines, larger instance sizes, read replicas...). As application requirements change, we may need to migrate the Lightsail database to Amazon RDS. In this workshop, we will also perform the migration of an existing Lightsail database to Amazon RDS.

1. Go to [Amazon RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1#GettingStarted:) page, then click **Create database**.
{{%notice tip%}}
The above link will redirect to the Amazon RDS page in Region Singapore. If you use another Region, please select the correct Region again.
{{%/notice%}}

![Lightsail](/images/4/0001.png?featherlight=false&width=90pc)

2. Click **Standard Create**, then select **MySQL**.

![Lightsail](/images/4/0002.png?featherlight=false&width=90pc)


3. Scroll down, and select the MySQL version that matches the version of the previous Lightsail database. (5.7.34)
Click **Free tier** to run RDS with basic configuration for free.

![Lightsail](/images/4/0003.png?featherlight=false&width=90pc)

4. Scroll down to **Credential settings** and enter **dbmasteruser** in **Master username**. Then enter the password and confirm the password is the same as the password of the Lightsail database. ( **asg123456**)

![Lightsail](/images/4/0004.png?featherlight=false&width=90pc)

5. Scroll down to **Connectivity**, make sure **Default VPC** is selected. If we deleted the Default VPC, it will need to be recreated.

![Lightsail](/images/4/0005.png?featherlight=false&width=90pc)

6. Scroll to the bottom and click **Create database**.

![Lightsail](/images/4/0006.png?featherlight=false&width=90pc)

7. It will take a few minutes to complete the creation of the RDS instance. You can continue with the next steps of the lab.

![Lightsail](/images/4/0007.png?featherlight=false&width=90pc)