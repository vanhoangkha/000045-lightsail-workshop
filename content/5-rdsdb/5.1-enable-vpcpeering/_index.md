+++
title = "Activate VPC Peering"
date = 2021
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++


#### Activate VPC Peering

In this step, we will enable VPC Peering feature to create connection from Lightsail network to AWS Default VPC
Lightsail network is only capable of peering with AWS Default VPC.

![Lightsail](/images/architecture/arc-lightsailrds.png?width=75pc)

1. Return to the [Lightsail console] interface (https://lightsail.aws.amazon.com/ls/webapp/home/). Click on **Account** in the upper right corner menu.

![Lightsail](/images/10/0001.png?featherlight=false&width=90pc)

2. Click on **Account**, then click on **Advance** tab.

![Lightsail](/images/10/0002.png?featherlight=false&width=90pc)

3. Click **Enable VPC Peering**.

![Lightsail](/images/10/0003.png?featherlight=false&width=90pc)

The next step is to configure the Amazon Relational Database Service side firewall to accept incoming connections from the Lightsail instance.