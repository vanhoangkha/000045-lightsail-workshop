---
title: "Networking Configuration"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b>3.2</b>"
---

## Networking Configuration

1. Whenever an instance is restarted, there's a possibility that it will receive a new public IP address. This may not always be the ideal choice for our applications because we want consistency and don't want to update DNS records if we find the IP address has changed. That's why we assign static IP addresses to our instances.
   - When the instance is in the 'Running' state, we will assign it a static IP address. Click on the instance name, then go to the **Networking** tab.

   ![Create VPC](/images/2/0004.png?featherlight=false&width=90pc)

2. Under **Public IP address**, select **Create static IP**.

   ![Create VPC](/images/2/0005.png?featherlight=false&width=90pc)

3. On the **Create Static IP Address** page, scroll to the bottom and give a name to the static IP address. Similarly, the name here should be unique for all resources. Enter PrestaShop-IP and click **Create**.

   ![Create VPC](/images/2/0006.png?featherlight=false&width=90pc)

   You will notice that Lightsail not only creates the static IP address but also associates it with the resource without requiring you to click 'attach' as we did in the WordPress workflow.

   ![Create VPC](/images/2/0007.png?featherlight=false&width=90pc)
