+++
title = "Tạo Lightsail instance"
date = 2021
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++


Bước đầu tiên chúng ta sẽ triển khai một ứng dụng mẫu dựa trên LAMP stack và đặt ứng dụng trong 1 Lightsail instance.
Lightsail instance đóng vai trò tương tự một máy chủ ảo ở môi trường truyền thống.
Các tài nguyên trong bài lab nên được tạo trong cùng 1 Region, ở đây chúng ta sẽ sử dụng Region Singapore.

1. Từ [giao diện quản trị của Lightsail](https://lightsail.aws.amazon.com/ls/webapp/home/)

   -  Chọn **Let's get started**

![Lightsail](/images/1/0001.png?featherlight=false&width=90pc)

2.  Click **Create Instance**.

![Lightsail](/images/1/0002.png?featherlight=false&width=90pc)

3. Click chọn nền tảng **Linux/Unix**. Dưới mục Blueprint, click chọn **LAMP (PHP7)**.

![Lightsail](/images/1/0003.png?featherlight=false&width=90pc)

4. Kéo màn hình xuống dưới , click chọn **+Add Launch Script**.

![Lightsail](/images/1/0004.png?featherlight=false&width=90pc)

5. Copy và dán đoạn mã dưới đây vào ô **Enter your setup code here.**. Các câu lệnh này sẽ được chạy lần đầu tiên khi Lightsail instance khởi chạy.
```
cd /opt/bitnami/apache2/htdocs
sudo rm -rf *
sleep 120
sudo git clone -b loft https://github.com/mikegcoleman/todo-php .
sudo echo "setting ownership on settings file"
sudo chown bitnami:daemon connectvalues.php
sudo chmod 666 connectvalues.php
sudo echo "adding db password to settings file"
sudo sed -i.bak "s/<password>/$(cat /home/bitnami/bitnami_application_password)/;" /opt/bitnami/apache2/htdocs/connectvalues.php
sudo echo "creating tasks database"
sudo cat /home/bitnami/htdocs/data/init.sql | /opt/bitnami/mysql/bin/mysql -u root -p$(cat /home/bitnami/bitnami_application_password)
```

![Lightsail](/images/1/0005.png?featherlight=false&width=90pc)


{{%notice tip%}}
**Đoạn mã trên làm các việc sau:** \
. Bitnami sẽ có trang web được cài mặc định mà chúng ta sẽ cần xóa đi. Đoạn script bắt đầu bằng việc chuyển đường dẫn tới **/opt/bitnami/apache2/htdocs** và xóa trang web mặc định. \
. Tiếp theo đoạn script tiến hành copy mã nguồn ứng dụng từ Github repo. \
. Để đảm bảo ứng dụng PHP có thể viết thay đổi vào file cấu hình (**connectvalues.php**), đoạn script tiến hành thay đổi quyền sở hữu (**chown**) trên file để đúng với với account chạy Apache web server, đồng thời thực hiện (**chmod**) để đảm bảo account đó có thể viết vào file. \
. Mỗi Bitnami instance sẽ sinh ra một password duy nhất cho cơ sở dữ liệu (CSDL) MySQL đã được cài đặt sẵn, câu lệnh tiếp theo trong đoạn scripts sẽ mở file cấu hình và cập nhật nó với password được sinh ra này.(Password sẽ nằm ở **/home/bitnami/bitnami_application_password** ) \
. Cuối cùng đoạn script thực hiện 1 tập câu lệnh SQL thông qua công cụ commandline của MySQL để khởi tạo cơ sở dữ liệu local. 
{{%/notice%}}

6. Kéo màn hình xuống dưới, ở mục **Identify your instance**, đặt tên instance của chúng ta là **PHP-FE-1**.

![Lightsail](/images/1/0006.png?featherlight=false&width=90pc)

7. Kéo màn hình xuống dưới, click **Create Instance**.

![Lightsail](/images/1/0007.png?featherlight=false&width=90pc)

8. Chờ vài phút để Lightsail instance chuyển sang trạng thái running như bên dưới.

![Lightsail](/images/1/0008.png?featherlight=false&width=90pc)

9. Chúc mừng bạn đã tạo được Lightsail instance đầu tiên.

![Lightsail](/images/1/0009.png?featherlight=false&width=90pc)