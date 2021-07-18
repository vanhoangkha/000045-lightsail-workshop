+++
title = "Tạo Lightsail snapshot"
date = 2021
weight = 1
chapter = false
pre = "<b>4.1 </b>"
+++


#### Tạo Lightsail snapshot

Lightsail giúp việc tạo các instance snapshot của bạn trở nên cực kỳ đơn giản chỉ với một cú nhấp chuột. Các snapshot này có thể được sử dụng để sao lưu và khôi phục các instance, tăng hoặc giảm kích thước instance hoặc tạo instance mới.


1. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/). Click vào tên Lightsail instance của chúng ta.

![Lightsail](/images/1-deploy-infra/0037-snapshot.png?width=90pc)

2. Click tab **Snapshot**, sau đó click **Create snapshot**.

![Lightsail](/images/1-deploy-infra/0038-snapshot.png?width=90pc)

3. Click **Create** để tiến hành tạo snapshot.

![Lightsail](/images/1-deploy-infra/0039-snapshot.png?width=90pc)

{{%notice tip%}}
Trạng thái sẽ chuyển sang snapshotting, thời gian tạo snapshot khoảng hơn 5 phút, và bạn cần chờ snapshot hoàn tất trước khi thực hiện bước kế tiếp.
{{%/notice%}}
