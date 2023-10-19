---
title : "Cấu hình Networking"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Cấu hình Networking

1. Gán địa chỉ IP tĩnh cho WordPress (Static IP)
   - Chúng ta muốn đảm bảo rằng địa chỉ IP cho WordPress không thay đổi nếu máy ảo được khởi động lại hoặc cập nhật.
   - Nhấp vào nút **Home** sau đó nhấp vào **Networking**.
   - Chọn **Create Static IP**

   ![Create VPC](/images/1/00015.png?featherlight=false&width=90pc)

2. Dưới phần 'Attach to an instance', bấm vào hộp dropdown và chọn 'Workshop-WordPress'.
3. Chúng ta cần đặt tên cho địa chỉ IP tĩnh của chúng ta. Nó không nên có cùng tên với máy ảo. Xóa tên mặc định và nhập 'Workshop-WordPress-IP'.
4. Chọn **Create**

   ![Create VPC](/images/1/00017.png?featherlight=false&width=90pc)

   - Chúng ta thường thích khi mọi thứ diễn ra nhanh chóng và dễ dàng, đúng không? Điều này là một bước đơn giản nhưng quan trọng không nên bỏ lỡ. Khi cấu hình một ứng dụng với tên miền (như ví dụ.com), bạn sẽ chỉ định các bản ghi DNS cho tên miền đó đến địa chỉ IP của máy ảo. Quá trình này có thể mất từ 1 phút đến 48 giờ để lan truyền trên Internet. Đặt các bản ghi DNS thành IP tĩnh sẽ ngăn quá trình lan truyền này phải diễn ra lại nếu bạn triển khai một máy ảo mới, ví dụ. Chỉ cần gắn lại IP tĩnh và bạn có thể truy cập trang web ngay lập tức.
