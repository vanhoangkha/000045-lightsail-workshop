+++
title = "Cấu hình Security Group"
date = 2021
weight = 2
chapter = false
pre = "<b>5.2 </b>"
+++


#### Cấu hình Security Group của Amazon Relational Database Service.

Ở bước này, chúng ta sẽ cấu hình tường lửa phía Amazon Relational Database Service để chấp nhận két nối tới từ Lightsail instance.


1. Quay trở lại giao diện [RDS console](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1). ( chúng ta vẫn sử dụng Region Singapore xuyên suốt trong bài lab, nếu bạn sử dụng Region khác, bạn sẽ phải thay đổi lại Region cho phu hợp). Dưới mục **Resources**, click **DB Instances**.

![Lightsail](/images/1-deploy-infra/0056-rds.png?width=90pc)

2. Click vào tên **database-1** RDS instance mà chúng ta đã tạo ở bước chuẩn bị.
![Lightsail](/images/1-deploy-infra/0057-rds.png?width=90pc)

3. Tại mục **Connectivity & security**, click vào **default** security group.
![Lightsail](/images/1-deploy-infra/0058-rds.png?width=90pc)

4. Click **Inbound Rules**, sau đó click **Edit inbound rules**.
![Lightsail](/images/1-deploy-infra/0059-rds.png?width=90pc)

5. Click **Add rule** để tiến hành thêm rule mới cho security group.
  + Từ mục type drop down chọn **MySQL/Aurora**.
  + Trong ô source , điền **172.26.0.0/16** ( đây là CIDR của Lightsail subnet ).
  + Click **Save rules**

![Lightsail](/images/1-deploy-infra/0060-rds.png?width=90pc)

Vậy là chúng ta đã cấu hình tường lửa (security group) của RDS instance để chấp nhận kết nối từ Lightsail subnet. Tiếp theo chúng ta sẽ cấu hình ứng dụng của chúng ta kết nối tới Amazon RDS endpoint.

