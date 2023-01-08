+++
title = "Create Lightsail Load Balancer"
date = 2021
weight = 3
chapter = false
pre = "<b>1.3 </b>"
+++

To be ready for scalability and fault tolerance, we will deploy the Front End of our website after the Lightsail load balancer. Lightsail load balancers can handle both HTTP and HTTPS traffic on ports 80 and 443. For HTTPS you can request a free certificate from the AWS Certificate Manager service. (In the framework of this lab, we will use HTTP.)

The resources in the lab should be created in the same Region, here we will use Region Singapore.

1. From [Lightsail's admin interface](https://lightsail.aws.amazon.com/ls/webapp/home/) click **Networking** then click **Create load balancer**.

![Lightsail](/images/3/0001.png?featherlight=false&width=90pc)

2. Drag the screen down. Name our load balancer **Todo-LB**. Then click **Create load balancer**.

![Lightsail](/images/3/0002.png?featherlight=false&width=90pc)

![Lightsail](/images/3/0003.png?featherlight=false&width=90pc)

3. We have finished creating the Lightsail load balancer, we will use the Lightsail load balancer in the next steps of the lab.

![Lightsail](/images/3/0004.png?featherlight=false&width=90pc)