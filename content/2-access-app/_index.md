+++
title = "App Access"
date = 2021
weight = 2
chapter = false
pre = "<b>2. </b>"
+++


#### Access the application

In this step, we will access the application we installed in the Lightsail instance.

Our current architecture is very simple, we will connect directly to the Lightsail instance over the internet.

![Lightsail](/images/architecture/arc-lightsailinstance.png?width=50pc)

On the application side, our Front end PHP and MySQL database are currently installed on a single Lightsail instance.

![Lightsail](/images/architecture/arc-lightsailinstanceapp.png?width=45pc)

1. Return to the [Lightsail console] interface (https://lightsail.aws.amazon.com/ls/webapp/home/).
We will see the public IP address of the Lightsail instance.

![Lightsail](/images/4/4.1/0001.png?featherlight=false&width=90pc)

2. Proceed to connect to the public IP address, we will access the todo application as shown below.

![Lightsail](/images/4/4.1/0002.png?featherlight=false&width=90pc)