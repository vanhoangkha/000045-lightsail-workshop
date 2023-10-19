---
title : "Tạo snapshot"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---


####   Tạo Bản Snapshot

Tiếp tục với các quy tắc tốt nhất, khi chúng ta đã cấu hình ứng dụng theo ý muốn, việc tạo một bản snapshot là một ý kiến khôn ngoan. Điều này đảm bảo rằng bạn có một bản sao có thể triển khai lại nhanh chóng và dễ dàng nếu có sự cố xảy ra với instance hiện tại của bạn.

Amazon Lightsail cung cấp hai loại snapshot:

A) Snapshot thủ công: Tạo bản sao lưu của instance, ổ đĩa hệ thống và ổ đĩa được gắn kèm. Snapshot được tạo khi bạn nhấp vào **Create snapshot** hoặc gọi API 'CreateInstanceSnapshot'.

Lưu ý: Snapshot thủ công không bị xóa nếu instance bị xóa. Snapshot tự động bị xóa. Trước khi thực hiện bất kỳ thao tác nào.

B) Snapshot tự động: Snapshot được tạo tự động hàng ngày vào giờ bạn chọn. Lightsail sẽ lưu trữ 7 snapshot gần đây nhất.

Nếu bạn có một trang web có sự thay đổi/cập nhật hàng ngày hoặc nhiều lần trong một ngày, chúng tôi đề nghị bạn sử dụng snapshot tự động.


1. Nhấp vào Trang chủ và chọn Akaunting.

- Chọn Snapshots, Nhấp vào công tắc chuyển đổi **Automated Snapshots**.

- Lưu ý: Cả snapshot tự động và snapshot thủ công đều được tính phí với mức giá hàng tháng là $0.05GB/tháng. Điều này không bao gồm trong giá hàng tháng của instance.
- Đánh dấu vào ô **I understand**, sau đó nhấp vào **Yes, Enable**.

![Create VPC](/images/4/0007.png?featherlight=false&width=90pc)

2. Chọn **Change snapshot time** và chọn thời gian bạn cần 

![Create VPC](/images/4/0008.png?featherlight=false&width=90pc)
  
3. Chọn **Coordinated Universal Time**

![Create VPC](/images/4/0009.png?featherlight=false&width=90pc)

4. Chọn **Change**

5. Thực hiện các bước trên với 'Workshop-PrestaShop' instance.

- Chọn 'Workshop-Wordpress' instance. 
- Chọn Snapshots.
- Bên dưới 'Manual snapshots' chọn Create snapshot.

![Create VPC](/images/4/00010.png?featherlight=false&width=90pc)

6. Đặt tên cho snapshot 'Workshop-WordPress-Manual-Snapshot', sau đó chọn Create.


7. Chọn Home, sau đó chọn  Databases.

![Create VPC](/images/4/00011.png?featherlight=false&width=90pc)


8. Chọn ('Workshop-HA-Instance').

- Chọn Snapshots & restore.

![Create VPC](/images/4/00012.png?featherlight=false&width=90pc)

9. Click Create snapshot. Tên của snapshot 'Workshop-HA-Instance-Backup'.

10. Chọn Create


![Create VPC](/images/4/00013.png?featherlight=false&width=90pc)

11. Hoàn thành.

![Create VPC](/images/4/00014.png?featherlight=false&width=90pc)



