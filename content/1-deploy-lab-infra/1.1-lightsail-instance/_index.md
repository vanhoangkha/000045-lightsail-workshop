+++
title = "Create Lightsail instance"
date = 2021
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++


As a first step, we will deploy a sample application based on the LAMP stack and place the application in a Lightsail instance.
The Lightsail instance plays the same role as a virtual server in a traditional environment.
The resources in the lab should be created in the same Region, here we will use Region Singapore.

1. From [Lightsail's admin interface](https://lightsail.aws.amazon.com/ls/webapp/home/)
- Select **Let's get started**

![Lightsail](/images/1/0001.png?featherlight=false&width=90pc)

2. Click **Create Instance**.

![Lightsail](/images/1/0002.png?featherlight=false&width=90pc)

3. Click the **Linux/Unix** platform. Under Blueprint, click **LAMP (PHP7)**.

![Lightsail](/images/1/0003.png?featherlight=false&width=90pc)

4. Drag the screen down, and click **+Add Launch Script**.

![Lightsail](/images/1/0004.png?featherlight=false&width=90pc)

5. Copy and paste the code below into the **Enter your setup code here.** box. These commands will be run for the first time when the Lightsail instance is launched.
```
cd /opt/bitnami/apache2/htdocs
sudo rm -rf *
sleep 120
sudo git clone -b loft https://github.com/mikegcoleman/todo-php .
sudo echo "setting ownership on settings file"
sudo chown bitnami:daemon connectvalues.php
sudo chmod 666 connectvalues.php
sudo echo "adding db password to settings file"
sudo sed -i.bak "s/<password>/$(cat /home/bitnami/bitnami_application_password)/;" /opt/bitnami/apache2/htdocs/connectvalues.php
sudo echo "creating tasks database"
sudo cat /home/bitnami/htdocs/data/init.sql | /opt/bitnami/mysql/bin/mysql -u root -p$(cat /home/bitnami/bitnami_application_password)
```

![Lightsail](/images/1/0005.png?featherlight=false&width=90pc)

{{%notice tip%}}
**The above code does the following:** \
. Bitnami will have the site installed by default which we will need to remove. The script starts by passing the path to **/opt/bitnami/apache2/htdocs** and removing the default web page. \
. Next, the script proceeds to copy the application source code from the Github repo. \
. To ensure that the PHP application can write changes to the configuration file (**connectvalues.php**), the script changes the ownership (**chown**) on the file to match the account running Apache. web server, and also do (**chmod**) to make sure that account can write to the file. \
. Each Bitnami instance will generate a unique password for the pre-installed MySQL database, the next command in the scripts will open the configuration file and update it with this generated password.(Password) will be located at **/home/bitnami/bitnami_application_password** )\
. Finally, the script executes a set of SQL statements through the MySQL commandline tool to initialize the local database.
{{%/notice%}}

6. Scroll down, under **Identify your instance**, name our instance **PHP-FE-1**.

![Lightsail](/images/1/0006.png?featherlight=false&width=90pc)

7. Drag the screen down, click **Create Instance**.

![Lightsail](/images/1/0007.png?featherlight=false&width=90pc)

8. Wait a few minutes for the Lightsail instance to switch to the running state as shown below.

![Lightsail](/images/1/0008.png?featherlight=false&width=90pc)

9. Congratulations on creating your first Lightsail instance.

![Lightsail](/images/1/0009.png?featherlight=false&width=90pc)