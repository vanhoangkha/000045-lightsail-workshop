+++
title = "Cập nhật Security group"
date = 2021
weight = 3
chapter = false
pre = "<b>6.3 </b>"
+++


#### Cập nhật Security group của Amazon Relational Database Service.

Ở bước này, chúng ta sẽ cập nhật cấu hình tường lửa phía Amazon Relational Database Service để chấp nhận két nối tới từ EC2 instance.


1. Quay trở lại giao diện [RDS console](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1). ( chúng ta vẫn sử dụng Region Singapore xuyên suốt trong bài lab, nếu bạn sử dụng Region khác, bạn sẽ phải thay đổi lại Region cho phu hợp). Dưới mục **Resources**, click **DB Instances**.

![Lightsail](/images/1-deploy-infra/0056-rds.png?width=90pc)

2. Click vào tên **database-1** RDS instance mà chúng ta đã tạo ở bước chuẩn bị.
![Lightsail](/images/1-deploy-infra/0057-rds.png?width=90pc)

3. Tại mục **Connectivity & security**, click vào **default** security group.
![Lightsail](/images/1-deploy-infra/0058-rds.png?width=90pc)

4. Click **Inbound Rules**, sau đó click **Edit inbound rules**.

5. Click **Add rule** để tiến hành thêm rule mới cho security group.
  + Từ mục type drop down chọn **MySQL/Aurora**.
  + Trong ô source , điền **tên của security group cho EC2 bạn đã lưu lại**.
  + Click **Save rules**

![Lightsail](/images/1-deploy-infra/0078-rds.png?width=90pc)

Vậy là chúng ta đã cấu hình tường lửa (security group) của RDS instance để chấp nhận kết nối từ EC2 instance. 
