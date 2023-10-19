---
title : "Dịch chuyển sang instance lớn hơn"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

#### Dịch chuyển sang instance lớn hơn

1. Khi trang web hoặc ứng dụng của bạn thu hút nhiều người sử dụng hơn, lượng tài nguyên cần thiết để đáp ứng lưu lượng truy cập sẽ tiếp tục tăng lên. Lightsail giúp bạn mở rộng trang web hoặc ứng dụng của mình một cách dễ dàng chỉ với vài cú nhấp chuột đơn giản. Trong phần này, chúng tôi sẽ tăng cường tài nguyên cho trang web WordPress của chúng ta để xử lý nhiều kết nối đồng thời hơn.

- Để có thể chuyển đổi sang một  instance lớn hơn, chúng ta cần tạo một bản snapshot thủ công của  instance hiện tại (điều này nên đã được thực hiện trong phần trước). Nếu bạn chưa ở trong trang snapshot, hãy di chuyển đến 'Home' > 'Workshop-WordPress' > Snapshots.

- Nhấp chuột vào 3 dấu chấm dọc ở phía bên phải của hàng snapshot.

![Create VPC](/images/5/0001.png?featherlight=false&width=90pc)

2. Chọn **Create new  instance**. Trong bài viết này, bạn sẽ thấy nguồn snapshot và vị trí của  instance. Chúng ta sẽ giữ nguyên tất cả các cài đặt này. 

![Create VPC](/images/5/0002.png?featherlight=false&width=90pc)

3. Chúng ta sẽ kích hoạt tính năng snapshot. Bạn hãy chọn ô kiểm "Enabled Automatic Snapshots".

![Create VPC](/images/5/0003.png?featherlight=false&width=90pc)

4. Dưới phần 'Choose a new  instance plan' chúng tôi sẽ nâng kích thước máy ảo từ 1GB/1vCPU lên máy 4GB/2vCPU với giá 20 đô la Mỹ. Bấm vào $20 USD.

![Create VPC](/images/5/0004.png?featherlight=false&width=90pc)

5. Trong trường hợp này, để đặt tên mới cho instance của chúng ta trong mục 'Identify your  instance', hãy nhập 'Workshop-WordPress-Medium' để chỉ rõ sự khác biệt giữa kích thước ban đầu và kích thước mới.
6. Chọn **Create  instance.**

7. Một máy ảo mới sẽ được triển khai. Bây giờ chúng ta cần gắn địa chỉ IP tĩnh từ trang web WordPress ban đầu vào trang web mới.

- Bấm vào máy ảo Workshop-WordPress.

- Chọn tab **Networking**.

- Dưới mục **PUBLIC IP**, chọn **Detach**. Sau đó, chọn **Yes, detach**.


![Create VPC](/images/5/0005.png?featherlight=false&width=90pc)


8. Hãy nhấp vào nút **Home** ở đầu trang và chọn trường hợp WordPress mới 'Workshop-WordPress-Medium'.

- Nhấp vào tab **Networking**.

- Dưới mục 'PUBLIC IP', hãy nhấp vào **Attach static IP**. Chọn trong danh sách thả xuống 'Workshop-WordPress-IP', sau đó nhấp vào **Attach**


![Create VPC](/images/5/0006.png?featherlight=false&width=90pc)


9. Bây giờ, bạn có thể sao chép địa chỉ IP tĩnh vào trình duyệt và thử truy cập trang web.

- Nhấn nút **Home** và nhấp vào 3 dấu chấm dọc ở bên phải của tên 'Workshop-WordPress'.
- Nhấp vào **Delete**.
- Điều này sẽ loại bỏ máy ảo, nhưng sẽ không xóa bản snapshot thủ công mà chúng ta đã tạo. Chúng ta sẽ giữ lại nó tạm thời như một bản sao lưu trong trường hợp cần thiết. Nhấp vào **Yes, delete**
- Bây giờ bạn sẽ có lại 3 máy ảo.

![Create VPC](/images/5/0007.png?featherlight=false&width=90pc)

![Create VPC](/images/5/0008.png?featherlight=false&width=90pc)