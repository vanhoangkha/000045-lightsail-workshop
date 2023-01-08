+++
title = "Create EC2 Instance"
date = 2021
weight = 2
chapter = false
pre = "<b>6.2 </b>"
+++


#### Create EC2 Instance from exported snapshot


1. After clicking **Open in the Amazon EC2 console**, we will be redirected to the AMI (Amazon Machine Image) management interface. The AMI is the template for creating EC2 instances.
  + Click **Launch** to proceed to create EC2 instance.

![Lightsail](/images/14/0001.png?featherlight=false&width=90pc)


1. Click **Next: Configure Instance Details**.

![Lightsail](/images/14/0002.png?featherlight=false&width=90pc)


2. Make sure the selected VPC is VPC Default. Click **Review and Launch**.

![Lightsail](/images/14/0003.png?featherlight=false&width=90pc)

3. Click **Launch** to proceed to create the instance.
  + Click **Create a new keypair**.
  + Name the key pair arbitrarily.
  + Click **Download Key Pair**.
  + Click **Launch Instances**.

![Lightsail](/images/14/0004.png?featherlight=false&width=90pc)

{{%notice tip%}}
The key pair is used to encrypt the login information to the EC2 instance. In this lab we do not use this key pair.
{{%/notice%}}

1. Click **View Instances**, then click on instance id.

![Lightsail](/images/14/0005.png?featherlight=false&width=90pc)

2. Click on **Security** tab then click on security group.

![Lightsail](/images/14/0006.png?featherlight=false&width=90pc)

{{%notice tip%}}
Please save this security group information to prepare for the step of configuring the security group for RDS.
{{%/notice%}}

1. Click **Edit inbound rules**.

![Lightsail](/images/14/0007.png?featherlight=false&width=90pc)

2. Click **Add rule**.
  + Type section, select **HTTP**.
  + In the Source section, select **Anywhere IPv4**.
  + Click **Add rule**.
  + Type section, select **HTTPS**.
  + Click **Save rules**.

9. Click **Instances**.
  + Click on the EC2 instance we just selected.
  + Click **Open address** or open the public address of the EC2 instance in the browser.

![Lightsail](/images/14/0008.png?featherlight=false&width=90pc)

10. We will get an error like this, because the RDS security group has not allowed our EC2 instance to connect to. In the next step, we will configure the security group of the RDS instance, allowing the EC2 instance we just created to connect.

![Lightsail](/images/14/0009.png?featherlight=false&width=90pc)