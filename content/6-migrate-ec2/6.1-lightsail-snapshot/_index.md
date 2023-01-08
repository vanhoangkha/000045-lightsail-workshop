+++
title = "Export Lightsail snapshot"
date = 2021
weight = 1
chapter = false
pre = "<b>6.1 </b>"
+++


#### Create Lightsail snapshot and export to EC2.


1. Return to the [Lightsail console] interface (https://lightsail.aws.amazon.com/ls/webapp/home/). Click on the name of our Lightsail instance **PHP-FE-1**.

2. Click the **Snapshot** tab, then click **Create snapshot**.

![Lightsail](/images/13/0001.png?featherlight=false&width=90pc)

3. Name the snapshot **ec2-export**.

![Lightsail](/images/13/0002.png?featherlight=false&width=90pc)

4. Click **Create** to proceed with creating snapshot.


![Lightsail](/images/13/0002.png?featherlight=false&width=90pc)


5. Once the snapshot is created, we will click on the 3-dot icon and click **Export to EC2**.


![Lightsail](/images/13/0003.png?featherlight=false&width=90pc)

6. Click **Yes, continue**.

![Lightsail](/images/13/0004.png?featherlight=false&width=90pc)

7. Click **Acknowledged** to start the export process. It will take about 15 minutes to export from Lightsail snapshot to EC2.

![Lightsail](/images/13/0005.png?featherlight=false&width=90pc)

8. Once the export is complete, click **Open in the Amazon EC2 console**. Next we will proceed to create an EC2 instance from the exported snapshot.

![Lightsail](/images/13/0006.png?featherlight=false&width=90pc)