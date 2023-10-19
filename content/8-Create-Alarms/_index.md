---
title: "Create Alarm"
date: "`r Sys.Date()`"
weight: 8
chapter: false
pre: "<b>8. </b>"
---

#### Create Alarm

Alerts are designed to notify administrators when a specific event occurs so that administrators can adjust the instance or gather information about what is happening. Alerts will help you detect incidents if your instance encounters issues, uses high CPU resources, demands additional instances, or moves to a larger instance, as we did in the previous section. In the following steps, you will learn about these alerts and create some alerts for your instance.

Since PrestaShop is where we theoretically make money, let's focus on that instance for now.

1. Click on the instance name Workshop-Prestashop.

- Then, click on the Metrics Banner button.
- Under 'Metric graphs', click on the CPU overview button.
- Here are all the metrics that customers can see for the version. These metrics are evaluated every 5 minutes.

![Create VPC](/images/5/0009.png?featherlight=false&width=90pc)

2. Select **CPU burst capacity (percentage)**.

![Create VPC](/images/5/00010.png?featherlight=false&width=90pc)

3. Choose **Add alarm**.
4. We will create two alarms. One when the burst capacity is below 50% and another when it's below 25%.

![Create VPC](/images/5/00011.png?featherlight=false&width=90pc)

5. In this case, you need to keep the option at "not greater than or equal to" and adjust the input value down to 50%. At the same time, you need to maintain the threshold for 2 occurrences in the last 10 minutes.

![Create VPC](/images/5/00012.png?featherlight=false&width=90pc)

6. Choose to receive notifications via Email.

- When prompted, click on **Add contact**.

![Create VPC](/images/5/00013.png?featherlight=false&width=90pc)

7. Enter a valid email address and click on **Add contact**.

![Create VPC](/images/5/00014.png?featherlight=false&width=90pc)

8. You will need to verify your email address. In this workshop, we won't send any alert notifications. However, if you set up alerts correctly, you will need to verify your email address within 24 hours.

![Create VPC](/images/5/00015.png?featherlight=false&width=90pc)

9. Click **I understand**.

- Select **Expand Advanced settings** and review the options, but keep the default values.

- Click **Create**.

![Create VPC](/images/5/00016.png?featherlight=false&width=90pc)

10. Now you will see a new alert has been created. Click on "Add alarm" again, and we will create a second alert.

![Create VPC](/images/5/00017.png?featherlight=false&width=90pc)

11. In this workshop, we will keep all the default settings. Choose "Send me a notification when the alarm state changes to OK" to receive a notification when the alert state changes to OK.

- Click the "Create" button to complete the process.

![Create VPC](/images/5/00018.png?featherlight=false&width=90pc)

12. If you scroll up on the graph, you will see two lines, each representing one of the two alerts, to display their activation thresholds.

![Create VPC](/images/5/00019.png?featherlight=false&width=90pc)

"You can use these previous steps to set up additional alarms for any versions we have deployed. Identifying issues before they impact your users is a crucial part of your business's continuous operation."
