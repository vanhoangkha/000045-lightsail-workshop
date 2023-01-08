+++
title = "Tạo EC2 Instance"
date = 2021
weight = 2
chapter = false
pre = "<b>6.2 </b>"
+++


#### Tạo EC2 Instance từ bản snapshot đã export


1. Sau khi click **Open in the Amazon EC2 console**, chúng ta sẽ được chuyển hướng tới giao diện quản lý AMI ( Amazon Machine Image). AMI là template để tạo nên các EC2 instance.
  + Click **Launch** để tiến hành tạo EC2 instance.

![Lightsail](/images/14/0001.png?featherlight=false&width=90pc)


1. Click **Next: Configure Instance Details**.

![Lightsail](/images/14/0002.png?featherlight=false&width=90pc)


2. Đảm bảo VPC đang được chọn là VPC Default. Click **Review and Launch**.

![Lightsail](/images/14/0003.png?featherlight=false&width=90pc)

3. Click **Launch** để tiến hành tạo instance.
  + Click chọn **Create a new keypair**.
  + Đặt tên key pair tùy ý.
  + Click **Download Key Pair**.
  + Click **Launch Instances**.

![Lightsail](/images/14/0004.png?featherlight=false&width=90pc)

{{%notice tip%}}
Key pair được dùng để mã hóa thông tin đăng nhập vào EC2 instance. Trong bài lab này chúng ta không sử dụng tới key pair này.
{{%/notice%}}
1. Click **View Instances**, sau đó click vào instance id.

![Lightsail](/images/14/0005.png?featherlight=false&width=90pc)

2. Click vào tab **Security** sau đó click vào security group.

![Lightsail](/images/14/0006.png?featherlight=false&width=90pc)

{{%notice tip%}}
Bạn hãy lưu thông tin security group này để chuẩn bị cho bước cấu hình security group cho RDS nhé.
{{%/notice%}}

1. Click **Edit inbound rules**.

![Lightsail](/images/14/0007.png?featherlight=false&width=90pc)

2. Click **Add rule**. 
  + Phần Type , chọn **HTTP**.
  + Phần Source, chọn **Anywhere IPv4**.
  + Click **Add rule**. 
  + Phần Type , chọn **HTTPS**.
  + Click **Save rules**.

9. Click **Instances**.
  + Click chọn EC2 instance chúng ta vừa chọn.
  + Click **Open address** hoặc mở địa chỉ public của EC2 instance trên trình duyệt.

![Lightsail](/images/14/0008.png?featherlight=false&width=90pc)

10. Chúng ta sẽ gặp lỗi như thế này, do security group của RDS chưa cho phép EC2 instance của chúng ta kết nối tới. Bước tiếp theo, chúng ta sẽ cấu hình security group của RDS instance, cho phép EC2 instance chúng ta vừa tạo kết nối.

![Lightsail](/images/14/0009.png?featherlight=false&width=90pc)