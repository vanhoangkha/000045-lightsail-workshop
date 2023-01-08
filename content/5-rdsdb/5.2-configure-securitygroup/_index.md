+++
title = "Security Group Configuration"
date = 2021
weight = 2
chapter = false
pre = "<b>5.2 </b>"
+++


#### Configure Amazon Relational Database Service's Security Group.

In this step, we will configure the Amazon Relational Database Service side firewall to accept incoming connections from the Lightsail instance.


1. Return to the [RDS console](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1) interface. (We still use Region Singapore throughout in the lab, if you use another Region, you will have to change the Region to suit). Under **Resources**, click **DB Instances**.

![Lightsail](/images/11/0001.png?featherlight=false&width=90pc)

2. Click on the name **database-1** RDS instance that we created in the preparation step.

![Lightsail](/images/11/0002.png?featherlight=false&width=90pc)

3. Under **Connectivity & security**, click on **default** security group.

![Lightsail](/images/11/0003.png?featherlight=false&width=90pc)

4. Click **Inbound Rules**, then click **Edit inbound rules**.

![Lightsail](/images/11/0004.png?featherlight=false&width=90pc)

5. Click **Add rule** to proceed with adding a new rule for the security group.
  + From the type drop down, select **MySQL/Aurora**.
  + In the source box, enter **172.26.0.0/16** (this is the Lightsail subnet CIDR).
  + Click **Save rules**

![Lightsail](/images/11/0005.png?featherlight=false&width=90pc)

So we have configured the firewall (security group) of the RDS instance to accept connections from the Lightsail subnet. Next we will configure our application to connect to the Amazon RDS endpoint.

![Lightsail](/images/11/0006.png?featherlight=false&width=90pc)