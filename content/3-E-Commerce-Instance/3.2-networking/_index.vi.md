---
title : "Cấu hình Networking"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

#### Cấu hình Networking

1. Bất cứ khi nào một instance được khởi động lại, có khả năng rằng nó sẽ nhận một địa chỉ IP public mới. Điều này không phải lúc nào cũng là lựa chọn lý tưởng cho ứng dụng của chúng ta vì chúng ta muốn tính nhất quán và không muốn cập nhật bản ghi DNS nếu ta phát hiện địa chỉ IP đã thay đổi. Đó là lý do tại sao chúng ta gắn địa chỉ IP tĩnh cho các instance của mình.
   - Khi instance đã ở trạng thái 'Running', chúng ta sẽ gán cho nó một địa chỉ IP tĩnh. Nhấp vào tên của instance sau đó nhấp vào tab **Networking**.

   ![Create VPC](/images/2/0004.png?featherlight=false&width=90pc)

2. Dưới **Public IP address**, chọn **Create static IP**.

   ![Create VPC](/images/2/0005.png?featherlight=false&width=90pc)

3. Trên trang **Create Static IP Address**, cuộn xuống cuối trang và đặt tên cho địa chỉ IP tĩnh. Tương tự, tên ở đây cần phải độc nhất đối với tất cả các tài nguyên khác. Nhập PrestaShop-IP và nhấn **Create**.

   ![Create VPC](/images/2/0006.png?featherlight=false&width=90pc)

   Bạn sẽ nhận thấy rằng Lightsail không chỉ tạo địa chỉ IP tĩnh mà còn kết nối nó với tài nguyên mà không cần bạn phải nhấp vào 'attach' như chúng ta đã làm trong quy trình làm việc với WordPress.

   ![Create VPC](/images/2/0007.png?featherlight=false&width=90pc)
