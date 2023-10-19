---
title : "Triển khai Wordpress"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

1. Hãy nhấp vào tên instance là Workshop-PrestaShop, sau đó nhấn vào Connect bằng SSH để đăng nhập vào instance.

![Create VPC](/images/2/0008.png?featherlight=false&width=90pc)

2. Việc này đòi hỏi bạn cần nhập lệnh sau vào terminal:

```
sudo /opt/bitnami/configure_app_domain --domain <địa_chỉ_IP_tĩnh_của_bạn>
```

- Hãy thay thế <địa_chỉ_IP_tĩnh_của_bạn> bằng địa chỉ IP tĩnh mà máy chủ của bạn đã nhận được ở các bước trước đó. Sau khi thay thế đúng, nhấn Enter để thực hiện lệnh.



3. Chúng ta đã sẵn sàng để đăng nhập vào phiên bản PrestaShop lần đầu. Bây giờ sau khi chúng ta đã chạy tập lệnh cấu hình ban đầu, chúng ta cần lấy tên người dùng và mật khẩu cho PrestaShop. Bởi vì phiên bản này được triển khai bằng một Mẫu Ứng dụng, quá trình triển khai đã tự động tạo ra thông tin đăng nhập. Chúng ta sẽ đọc một tệp trên máy chủ lưu trữ thông tin này cho chúng ta.

- Trong cửa sổ điều khiển SSH, hãy gõ 'cat ~/bitnami_credentials' và nhấn Enter.

![Create VPC](/images/2/0009.png?featherlight=false&width=90pc)

4. "Điều này sẽ trả về một tên người dùng và mật khẩu mặc định. Tên người dùng mặc định sẽ là 'user@example.com' và mật khẩu sẽ là một chuỗi ngẫu nhiên. Hãy ghi lại mật khẩu của bạn.

Trong trình duyệt web của bạn, nhập 'http://địa_chỉ_ip_cố_định_của_bạn/administration' và nhập tên người dùng và mật khẩu từ bước trước."

![Create VPC](/images/2/00010.png?featherlight=false&width=90pc)

5. Chúng tôi sẽ thay đổi tên người dùng và mật khẩu mặc định thành thông tin đăng nhập mà bạn sẽ nhớ được.

- Trong bảng điều hướng bên trái, cuộn xuống và nhấp vào "Advanced Parameters", sau đó nhấp vào "Team".

- Dưới phần "Employees", nhấp vào biểu tượng "Bút chì" bên phải của Người dùng Bitnami.

![Create VPC](/images/2/00011.png?featherlight=false&width=90pc)

6. Hãy cập nhật các giá trị ở đây với tên của bạn, họ của bạn và địa chỉ email của bạn, sau đó nhấn "Đổi mật khẩu" (cập nhật mật khẩu), và sau đó nhấn "Lưu".

LƯU Ý: Nếu đây là một trang web thương mại điện tử thực sự, chúng ta sẽ cấu hình tên miền (hoặc tên miền con) để trỏ đến địa chỉ IP tĩnh của trang web này, tạo chứng chỉ SSL cho HTTPS và bật HTTPS trong PrestaShop. Tuy nhiên, chúng ta sẽ bỏ qua những bước này vì đây là một buổi làm việc thực hành và hiện tại chúng ta không có tên miền để sử dụng.

Trong phần đầu của trang quản trị, bấm chuột phải vào "Xem cửa hàng của tôi" và mở trong tab mới. Đây là giao diện cửa hàng mặc định của bạn.

![Create VPC](/images/2/00012.png?featherlight=false&width=90pc)

