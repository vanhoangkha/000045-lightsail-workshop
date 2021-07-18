+++
title = "Sử dụng RDS"
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

#### Sử dụng Amazon Relational Database Service kết hợp với Lightsail

Có thể có lúc bạn thấy rằng một trong các dịch vụ của Lightsail không phù hợp với nhu cầu của bạn và bạn sẽ muốn sử dụng một dịch vụ AWS khác thay thế.

Trong lab này, bạn sẽ thay thế cơ sở dữ liệu Lightsail bằng cơ sở dữ liệu RDS. Bạn sẽ cần bật tính năng VPC Peering trong Lightsail, thêm  Lightsail subnet vào  RDS Security group, sau đó cập nhật ứng dụng để sử dụng cơ sở dữ liệu RDS.


Kiến trúc của chúng ta khi sử dụng Amazon Relational Database Service thay vì CSDL Lightsail như sau:

![Lightsail](/images/architecture/arc-lightsailrds.png?width=75pc)

#### Nội dung

1. [Kích hoạt VPC Peering](5.1-enable-vpcpeering/)
2. [Cấu hình Security Group](5.2-configure-securitygroup/)
3. [Cập nhật cấu hình CSDL](5.3-update-db/)