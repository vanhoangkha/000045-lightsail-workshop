+++
title = "Use RDS"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Using Amazon Relational Database Service in conjunction with Lightsail

There may be times when you find that one of Lightsail's services isn't right for your needs and you'll want to use another AWS service instead.

In this lab, you will replace the Lightsail database with the RDS database. You will need to enable VPC Peering in Lightsail, add the Lightsail subnet to the RDS Security group, and then update the application to use the RDS database.


Our architecture using Amazon Relational Database Service instead of Lightsail Database is as follows:

![Lightsail](/images/architecture/arc-lightsailrds.png?width=75pc)

#### Content

1. [Enable VPC Peering](5.1-enable-vpcpeering/)
2. [Security Group Configuration](5.2-configure-securitygroup/)
3. [Update Database Configuration](5.3-update-db/)