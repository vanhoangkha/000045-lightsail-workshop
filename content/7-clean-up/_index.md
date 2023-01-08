+++
title = "Clean up resources"
date = 2021
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

Currently we are using resources according to the following architecture

![Lightsail](/images/architecture/arc-lightsailrds.png?width=75pc)

In addition, we have also created 1 more EC2 instances.

We will proceed to delete the resources in the following order

1. Go to [EC2 Service Interface](https://ap-southeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-southeast).
  + Click **Instances**.
  + Click on Instance EC2.
  + Click **Instance state**.
  + Click **Terminate instance**.
  + Click **Terminate**.

![Lightsail](/images/1-deploy-infra/0081.png?width=90pc)


2. Go to [RDS Service Interface](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1)
  + Click on **Database**
  + Click on the RDS DB we created.
  + Click **Actions**.
  + Click **Delete**.

![Lightsail](/images/1-deploy-infra/0082.png?width=90pc)

  + Uncheck **Create final snapshot?**
  + Click **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available.**
  + Enter **delete me** to confirm.
  + Click **Delete**.

![Lightsail](/images/1-deploy-infra/0083.png?width=90pc)

3. Go to [Lightsail's admin interface](https://lightsail.aws.amazon.com/ls/webapp/home/) click **Create Instance**.
  + Click on the 3-dot icon of the **PHP-FE-1** instance.
  + Click **Delete**.
  + Click **Yes, delete**.
  + Do the same for the **PHP-FE-2** and **PHP-FE-3** instances.

![Lightsail](/images/1-deploy-infra/0084.png?width=90pc)

4. Click the **Snapshots** tab.
  + Click **Delete multiple**.
  Select both snapshots.
  + Click **Delete**.
  + Click **Yes**.

![Lightsail](/images/1-deploy-infra/0087.png?width=90pc)

5. Click the **Databases** tab.
  + Click on the 3-dot icon of the **Todo-DB** instance.
  + Click **Delete**.
  + Click **Yes, delete**.
  + Click **Yes**
![Lightsail](/images/1-deploy-infra/0085.png?width=90pc)

6. Click the **Networking** tab.
+ Click on the 3-dot icon of the **Todo-LB** instance.
  + Click **Delete**.
  + Click **Yes, delete**.

![Lightsail](/images/1-deploy-infra/0086.png?width=90pc)