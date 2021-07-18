+++
title = "Export Lightsail snapshot"
date = 2021
weight = 1
chapter = false
pre = "<b>6.1 </b>"
+++


#### Tạo Lightsail snapshot và export sang EC2.


1. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/). Click vào tên Lightsail instance **PHP-FE-1** của chúng ta.

2. Click tab **Snapshot**, sau đó click **Create snapshot**.
3. Đặt tên snapshot là **ec2-export**.
4. Click **Create** để tiến hành tạo snapshot.
![Lightsail](/images/1-deploy-infra/0065.png?width=90pc)

5. Sau khi snapshot được tạo hoàn tất , chúng ta sẽ click vào biểu tượng 3 chấm và click chọn **Export to EC2**.
![Lightsail](/images/1-deploy-infra/0066.png?width=90pc)

6. Click **Yes, continue**.
7. Click **Acknowledged** để bắt đầu quá trình export. Sẽ mất khoảng 15 phút để export từ Lightsail snapshot sang EC2.
8. Sau khi quá trình export hoàn tất , click **Open in the Amazon EC2 console**. Tiếp theo chúng ta sẽ tiến hành tạo EC2 instance từ bản snapshot đã export.
![Lightsail](/images/1-deploy-infra/0067.png?width=90pc)
