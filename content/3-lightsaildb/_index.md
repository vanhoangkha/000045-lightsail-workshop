+++
title = "Lightsail Database Connection"
date = 2021
weight = 3
chapter = false
pre = "<b>3. </b>"
+++


#### Connect to Lightsail Database


Currently, our web application is not scalable because the database and web application are on the same machine. It will be difficult for us to upgrade the database system to meet the requirements of the application.

To improve the current architecture, the application and the database need to be separated. In this step, you will configure the PHP application to point to the previously deployed Lightsail Database.

Our architecture when connecting more Lightsail database will be as follows:

![Lightsail](/images/architecture/arc-lightsaildb.png?width=50pc)

On the application side, Front end PHP is installed on the Lightsail instance and MySQL runs on the Lightsail database.

![Lightsail](/images/architecture/arc-lightsaildbapp.png?width=45pc)

1. Return to the [Lightsail console] interface (https://lightsail.aws.amazon.com/ls/webapp/home/). Click **Databases** , then click the 3 dots icon.

![Lightsail](/images/6/0001.png?featherlight=false&width=90pc)

2. Click **Manage**.

![Lightsail](/images/6/0002.png?featherlight=false&width=90pc)

3. At the **Todo-DB** admin page, copy the endpoint information of the Lightsail database.
Example current endpoint information is: **ls-689449b809a4e45abdcfb8c46e6c0e67ee990e9d.cqczsvxxcufs.ap-southeast-1.rds.amazonaws.com**

![Lightsail](/images/6/0003.png?featherlight=false&width=90pc)

4. Back to our todo app page. Click **Settings**.

![Lightsail](/images/6/0004.png?featherlight=false&width=90pc)

5. In the **DB Hostname** section, enter the endpoint information of **Todo-DB**.
  + In the **DB Username** field, enter **dbmasteruser**.
  + In the **DB Password** field, enter **asg123456**.
  + Click **Save Settings**.

![Lightsail](/images/6/0005.png?featherlight=false&width=90pc)

6. The application will check the connection to the Lightsail database.

![Lightsail](/images/6/0006.png?featherlight=false&width=90pc)

7. Click **Add Task** and add custom tasks. The next tasks you create will be saved in the Lightsail database.

![Lightsail](/images/6/0007.png?featherlight=false&width=90pc)