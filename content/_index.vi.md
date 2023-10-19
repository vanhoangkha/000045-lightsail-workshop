---
title : "AMAZON LIGHTSAIL WORKSHOP - COST OPTIMIZATION ON AWS"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# AMAZON LIGHTSAIL WORKSHOP - COST OPTIMIZATION ON AWS

Trong vòng 60-120 phút tới, buổi học này sẽ hướng dẫn bạn xây dựng 3 ứng dụng trên Lightsail: WordPress, PrestaShop và Akaunting. Để mang đến trải nghiệm đầy đủ, WordPress và Akaunting sẽ được triển khai trên Lightsail OS blueprints, trong khi Prestashop sẽ sử dụng Application Blueprint.

Sau khi mỗi ứng dụng được triển khai, chúng ta sẽ điều tra cách bảo mật ứng dụng hơn, tạo sao lưu, chuyển sang các loại máy ảo lớn hơn khi doanh nghiệp của bạn phát triển, và tạo cảnh báo để theo dõi hệ thống một cách chủ động.


#### Tổng quan

Trong bài thực hành này, chúng ta sẽ triển khai một số ứng dụng mã nguồn mở khác nhau trên Amazon Lightsail và cấu hình tài nguyên Lightsail một cách giúp bạn mở rộng ứng dụng khi doanh nghiệp của bạn phát triển, đồng thời bảo vệ các ứng dụng khỏi trạng thái mặc định của chúng. Mỗi bước sẽ bao gồm một số best practices để giúp bạn trở thành một chuyên gia sử dụng Amazon Lightsail.

#### Các ứng dụng cần triển khai
Chúng ta sẽ triển khai WordPress như trang blog/website, Prestashop như trang web thương mại điện tử và Akaunting như ứng dụng tài chính. Cả ba ứng dụng này đều là sản phẩm mã nguồn mở mà bạn có thể tự tổ chức. Những bài học trong bài thực hành này cũng áp dụng cho tất cả các ứng dụng khác mà bạn có thể triển khai trên Lightsail.

#### Chi phí của bài thực hành và dọn dẹp

Bài thực hành này thuộc loại miễn phí hiện tại nếu bạn chưa sử dụng hết 720 giờ tài nguyên Lightsail của miễn phí. Nếu bạn đã sử dụng hết tài nguyên Lightsail miễn phí, bài thực hành này, với thời gian chạy là 2 giờ, sẽ tốn khoảng 0,085 đô la. Nếu bạn bắt đầu bài thực hành này, ngay cả khi bạn không hoàn thành bài thực hành, bạn cần gỡ bỏ các tài nguyên bạn triển khai để không bị tính phí sau khi tài nguyên miễn phí đã được sử dụng hết.