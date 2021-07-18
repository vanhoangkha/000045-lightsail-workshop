+++
title = "Kích hoạt VPC Peering"
date = 2021
weight = 1
chapter = false
pre = "<b>5.1 </b>"
+++


#### Kích hoạt VPC Peering

Ở bước này, chúng ta sẽ kích hoạt tính năng VPC Peering để tạo kết nối từ Lightsail network tới AWS Default VPC
Lightsail network chỉ có khả năng peering với AWS Default VPC.

![Lightsail](/images/architecture/arc-lightsailrds.png?width=75pc)

1. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/). Click vào **Account** ở menu góc trên bên phải.

![Lightsail](/images/1-deploy-infra/0053-rds.png?width=90pc)

2. Click vào **Account**, sau đó click vào tab **Advance**.
![Lightsail](/images/1-deploy-infra/0054-rds.png?width=90pc)

3. Click chọn **Enable VPC Peering**.
![Lightsail](/images/1-deploy-infra/0055-rds.png?width=90pc)

Bước tiếp theo chúng ta sẽ cấu hình tường lửa phía Amazon Relational Database Service để cháp nhận két nối tới từ Lightsail instance.

