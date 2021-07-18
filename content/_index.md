+++
title = "Amazon Lightsail Workshop"
date = 2021
weight = 1 
chapter = false
+++
# Amazon Lightsail Workshop - Tối ưu hóa chi phí trên AWS

#### Tổng quan

Amazon Lightsail là cách dễ nhất để bắt đầu tiếp cận AWS. Lightsail cung cấp dịch vụ tính toán, lưu trữ và mạng với mức giá cố định thấp. Không dừng lại ở đó, các  Lightsail instance của bạn có thể tận dụng sức mạnh của các dịch vụ còn lại mà AWS cung cấp. 

Triển khai và mở rộng ứng dụng LAMP stack trên Amazon Lightsail

Trong các bài lab này, bạn sẽ triển khai một ứng dụng LAMP stack có khả năng chịu lỗi và có thể mở rộng. Để bắt đầu chúng ta sẽ sử dụng front-end PHP trong một Lightsail instance duy nhất dựa trên bản thiết kế Bitnami LAMP. Tiếp theo, bạn sẽ triển khai cơ sở dữ liệu được quản lý Lightsail có tính khả dụng cao và chuyển hướng giao diện người dùng của web để sử dụng nó. Sau đó, bạn sẽ sử dụng tính năng ảnh chụp nhanh của Lightsail để scale out cho ứng dụng web PHP và đặt các máy chủ của bạn sau load balancer.

#### Nội dung

1. [Chuẩn bị](1-deploy-lab-infra/)
2. [Kiểm tra ứng dụng ](2-access-app/)
3. [Sử dụng CSDL Lightsail ](3-lightsaildb/) 
4. [Sử dụng Lightsail LB](4-lightsaillb/)
5. [Sử dụng RDS](5-rdsdb/)
6. [Migrate sang EC2](6-migrate-ec2/)
7. [Dọn dẹp tài nguyên](7-clean-up/)