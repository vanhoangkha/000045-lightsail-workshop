---
title: "Deploying WordPress"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3.3 </b> "
---

1. Click on the instance named Workshop-PrestaShop, then click on Connect via SSH to log in to the instance.

![Create VPC](/images/2/0008.png?featherlight=false&width=90pc)

2. This requires you to enter the following command in the terminal:

```
sudo /opt/bitnami/configure_app_domain --domain <your_static_IP_address>
```

- Replace `<your_static_IP_address>` with the static IP address your server received in the previous steps. After replacing it correctly, press Enter to execute the command.

3. We are now ready to log in to PrestaShop for the first time. Now that we've run the initial configuration command, we need to get the username and password for PrestaShop. Because this version is deployed with an Application Template, the deployment process has automatically generated login information for us. We will read a file on the server hosting this information for us.

- In the SSH console window, type 'cat ~/bitnami_credentials' and press Enter.

![Create VPC](/images/2/0009.png?featherlight=false&width=90pc)

4. This will return a default username and password. The default username will be 'user@example.com', and the password will be a random string. Make a note of your password.

In your web browser, enter 'http://your_static_IP_address/administration' and use the username and password from the previous step.

![Create VPC](/images/2/00010.png?featherlight=false&width=90pc)

5. We will change the default username and password to login information that you will remember.

- In the left navigation panel, scroll down and click on "Advanced Parameters," then click on "Team."

- Under the "Employees" section, click on the pencil icon to the right of the Bitnami User.

![Create VPC](/images/2/00011.png?featherlight=false&width=90pc)

6. Update the values here with your name, your last name, and your email address, then click "Change Password" and then "Save."

NOTE: If this were a real e-commerce website, we would configure a domain (or subdomain) to point to the static IP address of this website, create an SSL certificate for HTTPS, and enable HTTPS in PrestaShop. However, we will skip these steps as this is a practical session, and we currently don't have a domain to use.

In the top part of the admin page, right-click on "View My Shop" and open it in a new tab. This is your default store interface.

![Create VPC](/images/2/00012.png?featherlight=false&width=90pc)
