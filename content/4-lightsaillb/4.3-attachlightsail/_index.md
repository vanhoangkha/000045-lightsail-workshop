+++
title = "Assemble instance to LB"
date = 2021
weight = 3
chapter = false
pre = "<b>4.3 </b>"
+++
#### Attach the Lightsail instance to the load balancer
In this step, after creating the Lightsail instances, we will attach the Lightsail instances to the **Todo-LB** load balancer that we created.

1. Return to the [Lightsail console] interface (https://lightsail.aws.amazon.com/ls/webapp/home/). Click on the **Networking** tab then click on the name of the load balancer **Todo-LB** we created.


![Lightsail](/images/9/0001.png?featherlight=false&width=90pc)

2. In the **Target Instances** section, click the dropdown menu, type **P** to bring up the list of Lightsail instances we have created, then select our first instance as **PHP-FE -first**.

![Lightsail](/images/9/0002.png?featherlight=false&width=90pc)

3. Click **Attach** to proceed with attaching the instance to the load balancer.

![Lightsail](/images/9/0003.png?featherlight=false&width=90pc)

4. Click **Attach another** and do the same steps 2.3 to attach the remaining 2 instances.

![Lightsail](/images/9/0004.png?featherlight=false&width=90pc)

5. After attaching 3 Lightsail instances, we will reach the following state.

![Lightsail](/images/9/0005.png?featherlight=false&width=90pc)

6. Drag the screen upwards, right click on the DNS Name of **Todo-LB** load balancer and click **Open link in new tab** to access our web application.

![Lightsail](/images/9/0006.png?featherlight=false&width=90pc)

7. Do F5 to refresh the browser a few times, we will see we connect to 2 different Lightsail instances. Congratulations on successfully scaling your web application.

![Lightsail](/images/9/0007.png?featherlight=false&width=90pc)