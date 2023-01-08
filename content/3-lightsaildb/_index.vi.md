+++
title = "Kết nối CSDL Lightsail"
date = 2021
weight = 3
chapter = false
pre = "<b>3. </b>"
+++


#### Kết nối với Cơ sở dữ liệu Lightsail


Hiện tại ứng dụng web của chúng ta không có khả năng mở rộng vì cơ sở dữ liệu và ứng dụng web nằm trên cùng một máy. Sẽ khó để chúng ta có thể nâng cấp hệ thống cơ sở dữ liệu để đáp ứng yêu cầu của ứng dụng.

Để cải tiến kiến trúc hiện tại, ứng dụng và cơ sở dữ liệu cần phải được tách biệt. Trong bước này, bạn sẽ điều chỉnh cấu hình cho ứng dụng PHP để trỏ đến Cơ sở dữ liệu Lightsail đã triển khai trước đó.

Kiến trúc của chúng ta khi kết nối thêm CSDL Lightsail sẽ như sau:

![Lightsail](/images/architecture/arc-lightsaildb.png?width=50pc)

Về mặt ứng dụng, Front end PHP được cài đặt trên Lightsail instance và MySQL chạy trên CSDL Lightsail.

![Lightsail](/images/architecture/arc-lightsaildbapp.png?width=45pc)

1. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/). Click **Databases** , sau đó click vào biểu tượng 3 dấu chấm.

![Lightsail](/images/6/0001.png?featherlight=false&width=90pc)

2. Click **Manage**. 

![Lightsail](/images/6/0002.png?featherlight=false&width=90pc)

3. Tại trang quản trị **Todo-DB** , copy lại thông tin endpoint của CSDL Lightsail.
Ví dụ thông tin endpoint hiện tại là : **ls-689449b809a4e45abdcfb8c46e6c0e67ee990e9d.cqczsvxxcufs.ap-southeast-1.rds.amazonaws.com**

![Lightsail](/images/6/0003.png?featherlight=false&width=90pc)

4. Quay lại trang ứng dụng todo của chúng ta. Click **Settings**.

![Lightsail](/images/6/0004.png?featherlight=false&width=90pc)

5. Tại mục **DB Hostname**, điền thông tin endpoint của **Todo-DB**.
  + Tại mục **DB Username** điền **dbmasteruser**.
  + Tại mục **DB Password** điền **asg123456**.
  + Click **Save Settings**.

![Lightsail](/images/6/0005.png?featherlight=false&width=90pc)

6. Ứng dụng sẽ tiến hành kiểm tra kết nối tới CSDL Lightsail.

![Lightsail](/images/6/0006.png?featherlight=false&width=90pc)

7. Click **Add Task** và thêm task tùy ý. Các task tiếp theo bạn tạo sẽ được lưu vào trong CSDL Lightsail.

![Lightsail](/images/6/0007.png?featherlight=false&width=90pc)