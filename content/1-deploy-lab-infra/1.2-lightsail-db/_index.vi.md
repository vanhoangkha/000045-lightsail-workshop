+++
title = "Tạo Lightsail DB Instance"
date = 2021
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

Trong bước này chúng ta sẽ tạo một cơ sở dữ liệu (CSDL) / Database (DB) Lightsail. CSDL Lightsail là một dịch vụ CSDL được quản lý bởi AWS, cho phép chúng ta giảm bớt sự phức tạp khi triển khai và quản lý CSDL.

Lightsail sẽ quản lý hạ tầng bên dưới và cả engine của CSDL, chúng ta sẽ chỉ cần quan tâm tới việc tạo, triển khai và lập nên các bảng CSDL chạy trong CSDL Lightsail.
Các tài nguyên trong bài lab nên được tạo trong cùng 1 Region, ở đây chúng ta sẽ sử dụng Region Singapore.


1. Từ [giao diện quản trị của Lightsail](https://lightsail.aws.amazon.com/ls/webapp/home/) click **Databases** sau đó click **Create Database**.

![Lightsail](/images/2/0001.png?featherlight=false&width=90pc)

2. Từ menu dropdown của MySQL , chọn version 5.7.xx.

![Lightsail](/images/2/0002.png?featherlight=false&width=90pc)

{{%notice tip%}}
Mặc định thì Lightsail sẽ tạo một password phức tạp cho bạn, tuy nhiên password này sẽ chứa các kí tự phức tạp khiến việc copy và paste khó khăn. Trong khuôn khổ bài lab này chúng ta sẽ chỉ định password.
{{%/notice%}}

3. Click **Specify login credentials**.

![Lightsail](/images/2/0003.png?featherlight=false&width=90pc)

4. Bỏ chọn **Create a strong password for me**, sau đó đặt password cho CSDL Lightsail của bạn và ghi chú lại. Ở đây chúng ta sẽ đặt password là **asg123456**.

![Lightsail](/images/2/0004.png?featherlight=false&width=90pc)


5. Kéo màn hình xuống dưới, trong bài lab này chúng ta sẽ triển khai mô hình CSDL mang tính sẵn sàng cao. Click chọn **High Availability** ở dưới mục **Choose your database plan**.

![Lightsail](/images/2/0005.png?featherlight=false&width=90pc)

6. Kéo màn hình xuống dưới. Đặt tên cho CSDL của chúng ta là **Todo-DB**. Sau đó click **Create database**.

![Lightsail](/images/2/0006.png?featherlight=false&width=90pc)

7. Sẽ mất hơn 10 phút để CSDL Lightsail  chuyển sang trạng thái running như bên dưới, chúc mừng bạn đã tạo được CSDL Lightsail đầu tiên.
Bạn có thể tiếp tục làm các bước tiếp theo trong lúc đợi CSDL Lightsail được tạo.

![Lightsail](/images/2/0007.png?featherlight=false&width=90pc)


