+++
title = "Amazon Lightsail Workshop"
date = 2021
weight = 1
chapter = false
+++
# Amazon Lightsail Workshop - Cost Optimization on AWS

#### Overview

Amazon Lightsail is the easiest way to get started with AWS. Lightsail offers compute, storage, and networking services at low, flat rates. Not stopping there, your Lightsail instances can take advantage of the rest of the services that AWS has to offer.

Deploy and scale LAMP stack applications on Amazon Lightsail

In these labs, you will deploy a scalable and fault-tolerant LAMP stack application. To start we will use the PHP front-end in a single Lightsail instance based on the Bitnami LAMP blueprint. Next, you'll implement the highly available Lightsail-managed database and redirect the web UI to use it. You will then use Lightsail's snapshot feature to scale out your PHP web application and put your servers behind the load balancer.

![Lightsail](/images/intro.jpeg?width=40pc)

#### Content

1. [Preparation](1-deploy-lab-infra/)
2. [App Test ](2-access-app/)
3. [Using Lightsail Database ](3-lightsaildb/)
4. [Using Lightsail LB](4-lightsaillb/)
5. [Using RDS](5-rdsdb/)
6. [Teleport to EC2](6-migrate-ec2/)
7. [Resource Cleanup](7-clean-up/)