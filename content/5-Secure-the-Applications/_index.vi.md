---
title : "Bảo mật ứng dụng"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---



1. Một trong những trụ cột của AWS Well-Architected Framework là 'Bảo mật'. Điều quan trọng là chúng ta phải đảm bảo rằng các máy ảo, cơ sở dữ liệu và ứng dụng của chúng ta luôn được bảo vệ tối đa. Chúng ta đã sử dụng các mật khẩu khác nhau cho các ứng dụng và cơ sở dữ liệu khác nhau, ngoài ra, chúng ta muốn thu nhỏ bề mặt tấn công của ứng dụng của mình càng nhỏ càng tốt.

- Bề mặt tấn công là những điểm có thể trở thành cửa vào hoặc vị trí có thể bị kẻ tấn công thử vào. Đối với mỗi máy ảo Lightsail, chúng ta muốn đóng càng nhiều cổng càng tốt mà không làm gián đoạn tính khả dụng, để giảm thiểu các vị trí mà kẻ tấn công có thể tiếp cận.

- Chúng ta cần hiểu cách làm việc với các máy ảo Lightsail của chúng ta. Để truyền thông với các máy ảo của chúng ta, entê hoặc Putty SSH thông qua Terminal hoặc sử dụng bảng điều khiển SSH trong trình duyệt, chúng ta cần cổng 22 đang mở. Tuy nhiên, sau khi chúng ta hoàn tất cấu hình các ứng dụng của chúng ta, chúng ta nên tắt cổng 22 để tăng cường bảo mật cho máy ảo của chúng ta. Cho đến khi chúng ta cần đăng nhập và thực hiện thêm cấu hình cho máy ảo, lúc đó chúng ta có thể mở Cổng 22.

- Chúng ta sẽ bắt đầu với WordPress trước.

- Trên tab **Instance**, nhấp vào Workshop-WordPress.
- Nhấp vào **Networking**.

![Create VPC](/images/4/0001.png?featherlight=false&width=90pc)

2. Cuộn xuống phần 'IPv4 Firewall' và nhấp vào biểu tượng 'Modify' trên dòng 'SSH'.

![Create VPC](/images/4/0002.png?featherlight=false&width=10pc)

3. Dưới đây, bạn sẽ thấy rằng bạn có thể hạn chế truy cập vào Cổng 22 thông qua một số cách khác nhau:

- [Tốt] Hạn chế truy cập từ giao diện SSH của Lightsail (người dùng vẫn có thể truy cập SSH thông qua các công cụ khác).

- [Tốt hơn] Hạn chế chỉ từ địa chỉ IP, cho phép bạn truy cập cổng từ các địa chỉ IP cụ thể (ví dụ: nhà, văn phòng).

- [Tốt nhất] Chúng ta có thể loại bỏ mọi truy cập vào cổng 22 (nhấn Hủy sau đó nhấn biểu tượng Thùng rác).

![Create VPC](/images/4/0003.png?featherlight=false&width=90pc)

4. Vì chúng ta không cần đăng nhập vào phiên bản của mình nữa, chúng ta sẽ gỡ bỏ tất cả quyền truy cập vào cổng 22.

- Nhấp vào **Cancel**.
- Nhấp vào biểu tượng **Trashcan** trên dòng SSH.
- Cuộn xuống phần **IPv6 firewall**.

![Create VPC](/images/4/0004.png?featherlight=false&width=90pc)

5. Làm lại bước trên.
- Cuộn lên đầu trang và nhấp vào tab **Connect**.
- Bạn sẽ thấy rằng SSH Trình duyệt hiện đã bị vô hiệu hóa (cùng với bất kỳ SSH khác nào).

![Create VPC](/images/4/0005.png?featherlight=false&width=90pc)

6. Chúng ta sẽ lặp lại các bước tương tự cho PrestaShop và Akaunting.

- Lặp lại các bước cho cả hai phiên bản 'PrestaShop' và 'Akaunting'.
- Lưu ý: Trong môi trường thực tế, chúng ta sẽ kích hoạt chứng chỉ SSL (HTTPS) và đẩy toàn bộ lưu lượng về HTTPS. Chúng ta cũng sẽ kích hoạt HTTPS (TCP 443) trên mỗi phiên bản để cho phép kết nối qua cổng đó.
- Nhấp vào **Next** trong hướng dẫn này sau khi SSH đã bị tắt cho cả IPv4 và IPv6 trên cả 3 phiên bản.

![Create VPC](/images/4/0006.png?featherlight=false&width=90pc)

