---
title : "Cấu hình ubuntu"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---


#### Cấu hình ubuntu

1. Tùy chỉnh Ubuntu
- Mở Trình duyệt SSH
- Nhấp vào Trang chủ nếu bạn không được chuyển hướng đến trang 'Instances'.

![Create VPC](/images/1/00014.png?featherlight=false&width=90pc)

2. Đợi cho đến khi máy ảo (instance) chuyển sang trạng thái 'Running', sau đó nhấn vào biểu tượng SSH bên cạnh tên của máy ảo để mở một phiên SSH dựa trên trình duyệt.

![Create VPC](/images/1/00012.png?featherlight=false&width=10pc)

3. Chạy các lệnh sau để cài đặt các yêu cầu tiên quyết cũng như WordPress và WordPress CLI:

- Đôi khi Ubuntu có thể mất phần còn lại của clipboard khi dán nhiều lệnh. Những lệnh này đã được chia thành các điểm không tiếp tục tự động. Hãy sao chép và dán từng phần, nhấn Enter và tiến hành đến khối mã tiếp theo sau khi các lệnh hoàn thành.

- Thể hiện WordPress của chúng ta cần biết nơi cơ sở dữ liệu và cách đăng nhập để tệp WordPress có thể được cài đặt và tạo trong cơ sở dữ liệu MySQL.

- Chúng ta sẽ cần sao chép khối mã dưới đây vào một trình soạn thảo văn bản để cập nhật URL của cơ sở dữ liệu của chúng ta. Khi mã dưới đây đã được dán vào trình soạn thảo văn bản, quay lại tab trình duyệt của bạn trên trang Databases của Lightsail, nhấp vào Workshop-HA-Instance.


```
sudo wp config set DB_USER LightsailAdmin --allow-root
sudo wp config set DB_PASSWORD Sunny2DAY! --allow-root
sudo wp config set DB_NAME dbWordPress --allow-root

```

4. Sao chép URL endpoint từ trang Databases của Lightsail.

Thay thế 'YOUR_DATABASE_ENDPOINT_URL' bằng  URL endpoint của cơ sở dữ liệu của bạn. Nó nên trông giống như: 'ls-b29db08eb530807da32b98b49b9504986ece0030.chi6kqvuuhir.us-west-2.rds.amazonaws.com'

![Create VPC](/images/1/00013.png?featherlight=false&width=90pc)

```
sudo wp config set DB_HOST YOUR_DATABASE_ENDPOINT_URL --allow-root
```
- Hãy dán lệnh đã cập nhật vào phiên SSH của bạn và nhấn ENTER.

- Đóng cửa sổ SSH.