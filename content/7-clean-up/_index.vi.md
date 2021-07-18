+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

Hiện tại chúng ta đang sử dụng tài nguyên theo kiến trúc sau

![Lightsail](/images/architecture/arc-lightsailrds.png?width=75pc)

Ngoài ra chúng ta cũng đã tạo thêm 1 EC2 instances.

Chúng ta sẽ tiến hành xóa các tài nguyên theo thứ tự sau 

1. Truy cập vào [Giao diện dịch vụ EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-southeast).
  + Click **Instances**.
  + Click chọn Instance EC2.
  + Click **Instance state**.
  + Click **Terminate instance**.
  + Click **Terminate**.

![Lightsail](/images/1-deploy-infra/0081.png?width=90pc)


2. Truy cập vào [Giao diện dịch vụ RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1)
  + Click vào **Database**
  + Click chọn vào RDS DB chúng ta đã tạo.
  + Click **Actions**.
  + Click **Delete**.

![Lightsail](/images/1-deploy-infra/0082.png?width=90pc)

  + Bỏ chọn **Create final snapshot?**
  + Click chọn **I acknowledge that upon instance deletion, automated backups, including system snapshots and point-in-time recovery, will no longer be available.**
  + Điền **delete me** để xác nhận.
  + Click **Delete**.

![Lightsail](/images/1-deploy-infra/0083.png?width=90pc)

3. Truy cập vào [giao diện quản trị của Lightsail](https://lightsail.aws.amazon.com/ls/webapp/home/) click **Create Instance**.
  + Click vào biểu tượng 3 dấu chấm của instance **PHP-FE-1**.
  + Click **Delete**.
  + Click **Yes, delete**.
  + Làm tương tự cho instance **PHP-FE-2** và **PHP-FE-3**.

![Lightsail](/images/1-deploy-infra/0084.png?width=90pc)

4. Click vào tab **Snapshots**.
  + Click **Delete multiple**.
  + Chọn cả 2 snapshot.
  + Click **Delete**.
  + Click **Yes**.

![Lightsail](/images/1-deploy-infra/0087.png?width=90pc)

5. Click tab **Databases**.
  + Click vào biểu tượng 3 dấu chấm của instance **Todo-DB**.
  + Click **Delete**.
  + Click **Yes, delete**.
  + Click **Yes**
![Lightsail](/images/1-deploy-infra/0085.png?width=90pc)

6. Click tab **Networking**.
+ Click vào biểu tượng 3 dấu chấm của instance **Todo-LB**.
  + Click **Delete**.
  + Click **Yes, delete**.

![Lightsail](/images/1-deploy-infra/0086.png?width=90pc)