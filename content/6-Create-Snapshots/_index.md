---
title: "Create Snapshot"
date: "`r Sys.Date()`"
weight: 6
chapter: false
pre: "<b>6.</b>"
---

#### Create a Snapshot

Continuing with best practices, once you have configured your application as desired, creating a snapshot is a wise idea. This ensures that you have a copy that can be quickly and easily deployed if any issues occur with your current instance.

Amazon Lightsail offers two types of snapshots:

A) Manual Snapshot: Create a backup of the instance, system disk, and attached disks. Snapshots are created when you click **Create snapshot** or call the 'CreateInstanceSnapshot' API.

Note: Manual snapshots are not deleted when the instance is deleted. They are deleted automatically. Proceed with caution.

B) Automated Snapshot: Snapshots are automatically created daily at the time you choose. Lightsail will retain the 7 most recent snapshots.

If you have a website with daily or frequent updates, we recommend using automated snapshots.

1. Click on Home and select Akaunting.

- Choose Snapshots, then click the **Automated Snapshots** toggle.

- Note: Both automated and manual snapshots incur a monthly charge of $0.05 per GB. This is not included in the monthly instance cost.
- Check the box **I understand**, then click **Yes, Enable**.

![Create VPC](/images/4/0007.png?featherlight=false&width=90pc)

2. Choose **Change snapshot time** and select the time you need.

![Create VPC](/images/4/0008.png?featherlight=false&width=90pc)

3. Choose **Coordinated Universal Time**

![Create VPC](/images/4/0009.png?featherlight=false&width=90pc)

4. Choose **Change**

5. Follow the steps above with the 'Workshop-PrestaShop' instance.

- Select the 'Workshop-Wordpress' instance.
- Choose Snapshots.
- Under 'Manual snapshots', select Create snapshot.

![Create VPC](/images/4/00010.png?featherlight=false&width=90pc)

6. Name the snapshot 'Workshop-WordPress-Manual-Snapshot', then click Create.

7. Go to Home, then select Databases.

![Create VPC](/images/4/00011.png?featherlight=false&width=90pc)

8. Select ('Workshop-HA-Instance').

- Choose Snapshots & restore.

![Create VPC](/images/4/00012.png?featherlight=false&width=90pc)

9. Click Create snapshot. Name the snapshot 'Workshop-HA-Instance-Backup'.

10. Click Create.

![Create VPC](/images/4/00013.png?featherlight=false&width=90pc)

11. Complete.

![Create VPC](/images/4/00014.png?featherlight=false&width=90pc)
