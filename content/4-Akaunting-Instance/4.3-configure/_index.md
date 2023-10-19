---
title: "Deploying Prestashop E-Commerce Instance"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b>4.3</b>"
---

## Deploying Prestashop E-Commerce

1. Sometimes, copying and pasting between your personal computer and an SSH browser can mess up data formatting in the clipboard. If you want to SSH from your laptop, expand the corresponding steps for Mac or Windows below and use the static IP address of the virtual machine instead of following Step 1 below.

- Click on the instance name, Akaunting, to go back to the instance page. Then, click Connect via SSH.

- Copy and paste the following commands into the SSH window and press Enter.

:::alert{Replace 'NEW_STATIC_IP_HERE' with the static IP address of this instance.}


```
# Paste the following
sudo sed -i 's/replace_here/NEW_STATIC_IP_HERE/g' /etc/apache2/sites-available/akaunting.conf

# Enable Apache2 virtualhost configuration for Akaunting
sudo a2ensite akaunting

# Enable specified module in apache configuration
sudo a2enmod rewrite

# Restart the apache service to make changes live.
sudo systemctl restart apache2

```


#### Creating a New Database on Lightsail Database Instance for Akaunting

1. Before we install Akaunting, we need a database to store data. Remember, in this practice, we deployed a remote MySQL Lightsail database instance and a WordPress database. We will create a second database on the same database instance as the WordPress database to utilize the existing resources.

Copy and paste the following command into your SSH window (edit the database endpoint URL to match your database endpoint), and press Enter.

```
mysql -u LightsailAdmin -pSunny2DAY! -h YOUR_DATABASE_ENDPOINT
```


2. This command is logging you into the remote Lightsail database:

```
-u = MySQL Username
-p = Password (note there is no space between the -p and the beginning of the password)
-h = Host URL. If we used a different port other than the default, we'd have additional parameters to specify.
```


3. Now that we're connected to the remote database instance, we will create a new database for our Akaunting application. Type 'CREATE DATABASE akaunting;' and press Enter.

- We will create a new database user for the akaunting database and grant it all privileges. Run the following commands in the SSH session:

```
create user 'accountant'@'localhost' identified by 'Exnte3x!';

grant all privileges on akaunting.* to 'accountant'@'localhost';

flush privileges;

exit;
```


4. We are ready to proceed with the Akaunting application installation.

- In your browser, navigate to the static IP address of your Akaunting instance.

- Now, you will be redirected to the Akaunting setup page. If it doesn't redirect automatically, try pasting the static IP address into the browser, then add '/install/language' and press Enter.

- Choose the language you prefer and click **Next**.

5. Enter the database authentication details we created:

```
Hostname: your_lightsail_database_endpoint
Username: LightsailAdmin
Password: Exnte3x!
Database: akaunting
```


- Click **Next**.

6. If everything is entered correctly, the 'Next' button will appear and blink like loading dots. We'll let it run for a few minutes.

- On the next page, use the following values for the admin information:

```
Company Name: Example Co.
Company email: admin@example.com
Admin Email: admin@example.com
Admin Password: S@ndyBeach3s!
```


- Click **Next**.

7. Now you can log in and input specific details for your business.

Enter a new username and password at the prompts and click "Login."

8. On the 'Company' page, click "Skip this step."

9. Click **Next**.

10. Click **Next**.

11. Click **Create your first invoice**.

12. Click **Dashboard**.

13. In the Lightsail interface, click on Databases.

- Next, click on the name of the database instance, then select Tags.
- Click Edit key-only tags and enter 'Akaunting'. Click Save.
