+++
title = "Scale Application"
date = 2021
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

#### Scaling PHP Web Application Delivery

Now that we have separated the user interface and the database, let's see how we can increase the scalability and fault tolerance of our web application.

In this section, you will take an application server snapshot and deploy two new Lightsail instances from the snapshot. You will then perform attaching 3 Lightsail instances to the Lightsail load balancer you created.

When that's done, you'll have a scaled-down, fault-tolerant version of your two-tier web application.


Our architecture when adding Lightsail instance and using additional Lightsail load balancer is as follows:

![Lightsail](/images/architecture/arc-lightsaillb.png?width=50pc)

#### Content

1. [Execute Snapshot](4.1-lightsailsnapshot/)
2. [Create more Lightsail instance](4.2-createlightsail/)
3. [Attaching Lightsail instance to load balancer](4.3-attachlightsail/)