+++
title = "Update Security group"
date = 2021
weight = 3
chapter = false
pre = "<b>6.3 </b>"
+++


#### Update the Amazon Relational Database Service Security group.

In this step, we will update the Amazon Relational Database Service side firewall configuration to accept incoming connections from EC2 instances.


1. Return to the [RDS console](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1) interface. (We still use Region Singapore throughout in the lab, if you use another Region, you will have to change the Region to suit). Under **Resources**, click **DB Instances**.

![Lightsail](/images/1-deploy-infra/0056-rds.png?width=90pc)

2. Click on the name **database-1** RDS instance that we created in the preparation step.
![Lightsail](/images/1-deploy-infra/0057-rds.png?width=90pc)

3. Under **Connectivity & security**, click on **default** security group.
![Lightsail](/images/1-deploy-infra/0058-rds.png?width=90pc)

4. Click **Inbound Rules**, then click **Edit inbound rules**.

5. Click **Add rule** to proceed with adding a new rule for the security group.
  + From the type drop down, select **MySQL/Aurora**.
  + In the source box, enter **name of the security group for EC2 you saved**.
  + Click **Save rules**

![Lightsail](/images/1-deploy-infra/0078.png?width=90pc)

So we have configured the firewall (security group) of the RDS instance to accept connections from the EC2 instance.