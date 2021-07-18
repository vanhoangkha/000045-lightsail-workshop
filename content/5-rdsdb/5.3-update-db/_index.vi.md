+++
title = "Cập nhật cấu hình CSDL"
date = 2021
weight = 3
chapter = false
pre = "<b>5.3 </b>"
+++


#### Cập nhật cấu hình CSDL của ứng dụng.

Ở bước này, chúng ta sẽ xác định endpoint của Amazon Relational Database Service instance chúng ta đã tạo, sau đó cấu hinh ứng dụng để kết nối tới RDS instance.

1. Quay trở lại giao diện [RDS console](https://ap-southeast-1.console.aws.amazon.com/rds/home?region=ap-southeast-1). ( chúng ta vẫn sử dụng Region Singapore xuyên suốt trong bài lab, nếu bạn sử dụng Region khác, bạn sẽ phải thay đổi lại Region cho phu hợp). Dưới mục **Resources**, click **DB Instances**.

![Lightsail](/images/1-deploy-infra/0056-rds.png?width=90pc)

2. Click vào tên **database-1** RDS instance mà chúng ta đã tạo ở bước chuẩn bị.
![Lightsail](/images/1-deploy-infra/0057-rds.png?width=90pc)

3. Tại mục **Connectivity & security**, lưu lại thông tin endpoint.
![Lightsail](/images/1-deploy-infra/0061.png?width=90pc)

4. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/).

5. Kết nối tới địa chỉ IP public của Lightsail instance để truy cập ứng dụng todo.
6. Click **Settings**, sau đó cập nhật **DB Hostname** bằng endpoint của RDS, click **Save Settings**.
![Lightsail](/images/1-deploy-infra/0062.png?width=90pc)
{{%notice tip%}}
Cẩn thận kiểm tra thông tin endpoint khi bạn copy paste vào mục **DB Hostname**, tránh thừa khoảng trắng cuối cùng.
{{%/notice%}}

7. Chúng ta sẽ thấy danh sách Task sẽ không có các task chúng ta đã tạo, vì chúng ta đang sử dụng CSDL Amazon RDS mới.

![Lightsail](/images/1-deploy-infra/0063.png?width=90pc)

8. Làm tương tự cho cả 3 Lightsail instance.Sau đó chúng ta tạo task trên mỗi Lightsail instance.Kết quả chúng ta sẽ thấy task hiển thị đủ trên ứng dụng todo dù ta đang kết nối trực tiếp tới instance nào.
![Lightsail](/images/1-deploy-infra/0064.png?width=90pc)

Vậy là chúng ta đã cấu hình tường lửa (security group) của RDS instance để chấp nhận kết nối từ Lightsail subnet. Tiếp theo chúng ta sẽ cấu hình ứng dụng của chúng ta kết nối tới Amazon RDS endpoint.

{{%notice tip%}}
Trong quá trình cập nhật cấu hình DB Hostname cho ứng dụng todo, bạn có thể gặp lỗi dưới đây. Do mỗi lần kết nối vào DB, ứng dụng todo sẽ thử tạo bảng tasks.
Bạn có thể bỏ qua lỗi này và thực hiện Refresh ( ấn phím F5 ) để ứng dụng kết nối tiếp tục vào RDS Instance. \
```
Saving settings and testing connection


Connecting to database.

There was an error connecting to the database server:
CREATE DATABASE IF NOT EXISTS tasks; use tasks; CREATE TABLE tasks ( id INT(11) UNSIGNED AUTO_INCREMENT PRIMARY KEY, summary VARCHAR(30) NOT NULL, details VARCHAR(250) NOT NULL, priority VARCHAR(20) NOT NULL, dueDate TIMESTAMP, isComplete VARCHAR(10) );
SQLSTATE[42S01]: Base table or view already exists: 1050 Table 'tasks' already exists
```
{{%/notice%}}
