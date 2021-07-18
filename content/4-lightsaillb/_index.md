+++
title = "Mở rộng quy mô ứng dụng"
date = 2021
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

#### Mở rộng quy mô giao ứng dụng web PHP

Bây giờ chúng ta đã tách biệt được giao diện người dùng và cơ sở dữ liệu, hãy xem cách chúng ta có thể tăng khả năng mở rộng và khả năng chịu lỗi cho ứng dụng web của mình.

Trong phần này, bạn sẽ thực hiện snapshot máy chủ ứng dụng  và triển khai hai Lightsail instance mới từ ảnh snapshot. Sau đó bạn sẽ thực hiện gắn 3 Lightsail instance vào Lightsail load balancer bạn đã tạo.

Khi mọi việc hoàn tất, bạn sẽ có phiên bản thu nhỏ có khả năng chịu lỗi của ứng dụng web hai tầng.


Kiến trúc của chúng ta khi thêm Lightsail instance và sử dụng thêm Lightsail load balancer như sau:

![Lightsail](/images/architecture/arc-lightsaillb.png?width=50pc)

#### Nội dung

1. [Thực hiện Snapshot](4.1-lightsailsnapshot/)
2. [Tạo thêm Lightsail instance](4.2-createlightsail/)
3. [Gắn Lightsail instance vào load balancer](4.3-attachlightsail/)