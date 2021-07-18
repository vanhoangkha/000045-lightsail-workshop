+++
title = "Tạo RDS Instance"
date = 2021
weight = 4
chapter = false
pre = "<b>1.4 </b>"
+++

Ở bước này chúng ta sẽ tiến hành tạo một CSDL Amazon Relational Database Service (RDS). Amazon RDS là một dịch vụ CSDL cung cấp nhiều tính năng cao cấp hơn so với CSDL Lightsail ( đa dạng engine database, nhiều kích cỡ instance to hơn, tính năng read replicas...). Khi yêu cầu của ứng dụng thay đổi, chúng ta có thể sẽ cần chuyển CSDL Lightsail sang Amazon RDS. Trong workshop này, chúng ta cũng sẽ thực hiện việc thay đổi CSDL Lightsail hiện tại sang Amazon RDS.

1. Chuyển đến trang [Amazon RDS](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1#GettingStarted:), sau đó click **Create database**.
{{%notice tip%}}
Đường link trên sẽ chuyển đến trang Amazon RDS tại Region Singapore. Nếu bạn dùng Region khác, hãy lựa chọn lại Region cho đúng nhé.
{{%/notice%}}

![Lightsail](/images/1-deploy-infra/0018-createrds.png?width=90pc)

2. Click chọn **Standard Create**, sau đó chọn **MySQL**.

![Lightsail](/images/1-deploy-infra/0019-createdb1.png?width=90pc)


3. Kéo màn hình xuống, chọn MySQL version trùng với version của CSDL Lightsail trước đó. (5.7.34)
Click chọn **Free tier** để chạy RDS với cấu hình cơ bản miễn phí.

![Lightsail](/images/1-deploy-infra/0020-createdb2.png?width=90pc)

4. Kéo màn hình xuống mục **Credential settings** và nhập **dbmasteruser** ở mục **Master username**. Sau đó điền password và confirm password giống với password của CSDL Lightsail. ( **asg123456**)

![Lightsail](/images/1-deploy-infra/0021-dbpass.png?width=90pc)

5. Kéo màn hình xuống mục **Connectivity**, đảm bảo **Default VPC** đang được chọn. Nếu chúng ta đã xóa Default VPC thì sẽ cần phải tạo lại.

![Lightsail](/images/1-deploy-infra/0022-defaultvpc.png?width=90pc)

6. Kéo xuống dưới cùng và click **Create database**.

![Lightsail](/images/1-deploy-infra/0023-createrds.png?width=90pc)

7. Sẽ mất vài phút để hoàn tất quá trình tạo RDS instance. Bạn có thể tiếp tục làm các bước tiếp theo của bài lab.


![Lightsail](/images/1-deploy-infra/0023-creating.png?width=90pc)