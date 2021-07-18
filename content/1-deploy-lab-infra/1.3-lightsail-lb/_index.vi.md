+++
title = "Tạo Lightsail Load Balancer"
date = 2021
weight = 3
chapter = false
pre = "<b>1.3 </b>"
+++

Để sẵn sàng cho việc mở rộng qui mô và tăng khả năng chịu lỗi, chúng ta sẻ triển khai phần Front End website của chúng ta sau Lightsail load balancer. Lightsail load balancers có thể đáp ứng cả HTTP và HTTPS traffic trên port 80 và 443. Đối với HTTPS bạn có thể request 1 certificate miễn phí từ dịch vụ AWS Certificate Manager. ( Trong khuôn khổ bài lab này, chúng ta sẽ sử dụng HTTP).

Các tài nguyên trong bài lab nên được tạo trong cùng 1 Region, ở đây chúng ta sẽ sử dụng Region Singapore.

1. Từ [giao diện quản trị của Lightsail](https://lightsail.aws.amazon.com/ls/webapp/home/) click **Networking** sau đó click **Create load balancer**.

![Lightsail](/images/1-deploy-infra/0015-createlb.png?width=90pc)

2. Kéo màn hình xuống dưới. Đặt tên cho load balancer của chúng ta là **Todo-LB**. Sau đó click **Create load balancer**.

![Lightsail](/images/1-deploy-infra/0016-namelb.png?width=90pc)

3. Chúng ta đã hoàn tất việc tạo Lightsail load balancer, chúng ta sẽ sử dụng Lightsail load balancer ở các bước tiếp theo của bài lab.

![Lightsail](/images/1-deploy-infra/0017-finish.png?width=90pc)
