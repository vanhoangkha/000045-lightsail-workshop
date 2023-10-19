---
title : "Triển khai Lightsail Database"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 1. </b> "
---

Để đăng nhập vào bảng điều khiển AWS, hãy thực hiện các bước sau:

- Bên cạnh hướng dẫn này, nhấp vào bảng điều khiển Amazon Lightsail.

- Đăng nhập bằng thông tin đăng nhập AWS của bạn.

- Bây giờ bạn nên thấy bảng điều khiển Lightsail.

### Triển khai một Cơ sở dữ liệu trên Lightsail

Hai trong số các ứng dụng của chúng tôi (WordPress và Akaunting) sẽ sử dụng cơ sở dữ liệu MySQL. Trong phần này, chúng ta sẽ triển khai một cơ sở dữ liệu có tính sẵn sàng cao, điều này có nghĩa là có một cơ sở dữ liệu hoạt động và một cơ sở dữ liệu thụ động được triển khai. Cả hai đều nhận tất cả các ghi/chỉnh sửa. Nếu cơ sở dữ liệu hoạt động gặp bất kỳ vấn đề gì, cơ sở dữ liệu thụ động sẽ tự động được thăng cấp tự động sang trạng thái 'Active', giúp đảm bảo tính liên tục và khả dụng. Chúng ta sẽ triển khai cơ sở dữ liệu trước vì quá trình triển khai này mất 10-15 phút và bạn có thể tiến hành các bước khác thay vì phải đợi nó sẵn sàng trước khi tiếp tục.

1. Dành một ít thời gian để làm quen với giao diện điều khiển Lightsail. Khi bạn sẵn sàng, hãy nhấp vào tab **Databases**, sau đó nhấp vào **Create database**.

![Create VPC](/images/1/0001.png?featherlight=false&width=90pc)

2. Chúng ta sẽ sử dụng phiên bản MySQL mặc định. Cuộn xuống và nhấp vào **Specify login credentials**.

   - Cho trường **User name** gõ 'LightsailAdmin' (chú ý đến việc viết hoa chữ cái).
   
   - Bỏ chọn mục **Create a strong password for me** và gõ 'Sunny2DAY!' làm mật khẩu mới của bạn.
   
   - Cho trường "Master database name" gõ 'WordPress' (một lần nữa, hãy chú ý đến việc viết hoa chữ cái).

![Create VPC](/images/1/0003.png?featherlight=false&width=90pc)

3. Chọn database plan.

![Create VPC](/images/1/0004.png?featherlight=false&width=90pc)

4. Chúng ta sẽ lựa chọn một kế hoạch cơ sở dữ liệu **STANDARD** để tiết kiệm thời gian và tiền bạc. Nếu bạn muốn sử dụng cơ sở dữ liệu 'High-Availability', nó sẽ tự động chuyển đổi trong trường hợp có sự cố xảy ra với cơ sở dữ liệu chính.

   - Chọn kế hoạch cơ sở dữ liệu $15 với 1GB Bộ nhớ và 2 vCPU.

5. Chúng ta cần đặt tên xác định cho tài nguyên/đối tượng của cơ sở dữ liệu của chúng tôi. Trong trường hợp này, tài nguyên này sẽ chạy nhiều cơ sở dữ liệu, vì vậy chúng ta cũng sẽ thêm các thẻ xác định

   - Hãy đặt tên cho đối tượng cơ sở dữ liệu là 'Workshop-DB-Instance'.

6. Vì chúng ta không thể xem tên của các cơ sở dữ liệu đang chạy bên trong trường hợp cơ sở dữ liệu mà không đăng nhập vào trường hợp đó, chúng tôi sẽ thêm một thẻ có tên của cơ sở dữ liệu. Mặc dù chúng ta đã gõ 'WordPress' cho tên cơ sở dữ liệu, Lightsail thêm một tiền tố 'db' nên cơ sở dữ liệu mà chúng ta đang tạo thực sự là 'dbWordPress'.
   
   Dưới 'Key-value tags', nhấn vào **Add key-value tag**, thêm:

```
Key = dbname
Value = dbWordPress
```

![Create VPC](/images/1/0005.png?featherlight=false&width=90pc)

7. Chọn **Create database**

![Create VPC](/images/1/0006.png?featherlight=false&width=90pc)

8. Sẽ mất khoảng 15 phút để tạo cơ sở dữ liệu.

- Trong thời gian chúng ta đợi cơ sở dữ liệu được khởi tạo, chúng ta sẽ tiến hành bước tiếp theo 'Triển khai một phiên bản WordPress'

![Create VPC](/images/1/0007.png?featherlight=false&width=90pc)

![Create VPC](/images/1/00010.png?featherlight=false&width=90pc)

9. Nhấp chuột phải vào Instances và chọn 'Open in a new tab' vì chúng ta sẽ cần quay lại trang này sau để lấy database instance Endpoint URL.

![Create VPC](/images/1/00011.png?featherlight=false&width=90pc)

Chúng ta đã thực hiện bước đầu tiên trong việc tạo một cơ sở dữ liệu từ xa để tất cả các ứng dụng của chúng ta có thể sử dụng. Nếu xảy ra sự cố với phiên bản cơ sở dữ liệu chính, sẽ có một phiên bản thứ hai đang chạy (ẩn đi với bạn), sẽ tiếp quản nếu cần thiết, đảm bảo tính sẵn sàng cao hơn cho hồ sơ cơ sở dữ liệu.

![Create VPC](/images/1/00013.png?featherlight=false&width=90pc)
