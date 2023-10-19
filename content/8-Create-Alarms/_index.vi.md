---
title : "Tạo cảnh báo"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

#### Tạo cảnh báo


Các cảnh báo được thiết kế để thông báo cho quản trị viên nếu một sự kiện cụ thể xảy ra, để quản trị viên có thể điều chỉnh instance hoặc nắm bắt thông tin về điều gì đang xảy ra. Các cảnh báo sẽ giúp bạn nắm bắt sự cố nếu instance của bạn gặp sự cố, sử dụng tài nguyên CPU tăng cao, đòi hỏi thêm instance hoặc di chuyển sang một instance lớn hơn như chúng ta đã thực hiện trong phần trước đó. Trong các bước tiếp theo, bạn sẽ tìm hiểu về những cảnh báo này và tạo một số cảnh báo cho instance của bạn.

Vì PrestaShop là nơi chúng ta lý thuyết sẽ kiếm tiền, hãy tập trung vào instance đó vào lúc này.

1. Nhấn vào tên  instance Workshop-Prestashop.

- Sau đó, nhấn vào nút Metrics Banner.
- Dưới 'Metric graphs', nhấn vào nút CPU overview 
- Dưới đây là tất cả các chỉ số mà khách hàng có thể thấy cho phiên bản. Các chỉ số này được đánh giá mỗi 5 phút.

![Create VPC](/images/5/0009.png?featherlight=false&width=90pc)

2. Chọn **CPU burst capacity (percentage)**

![Create VPC](/images/5/00010.png?featherlight=false&width=90pc)

3. Chọn **Add alarm**
4. Chúng ta sẽ tạo hai báo động. Một khi khả năng tăng tốc dưới 50% và một khác khi nó dưới 25%.

![Create VPC](/images/5/00011.png?featherlight=false&width=90pc)

5. Trong trường hợp này, bạn cần giữ tùy chọn ở mức "không lớn hơn hoặc bằng" và điều chỉnh giá trị đầu vào xuống 50%. Đồng thời, bạn cần duy trì ngưỡng cho 2 lần xảy ra trong vòng 10 phút gần nhất.

![Create VPC](/images/5/00012.png?featherlight=false&width=90pc)

6. Lựa chọn để nhận thông báo qua Email.

- Khi được yêu cầu, nhấn vào **Add contact**

![Create VPC](/images/5/00013.png?featherlight=false&width=90pc)

7. Hãy nhập một địa chỉ email hợp lệ và nhấn vào **Add contact**

![Create VPC](/images/5/00014.png?featherlight=false&width=90pc)

8. Bạn sẽ cần xác minh địa chỉ email của bạn. Trong workshop này, chúng tôi sẽ không gửi bất kỳ thông báo cảnh báo nào. Tuy nhiên, nếu bạn thiết lập cảnh báo một cách đúng đắn, bạn sẽ cần xác minh địa chỉ email của mình trong vòng 24 giờ.

![Create VPC](/images/5/00015.png?featherlight=false&width=90pc)

9. Click **I understand**.

- Chọn **Expand Advanced settings** và đọc qua các tùy chọn, nhưng giữ giá trị mặc định.

- Click **Create**

![Create VPC](/images/5/00016.png?featherlight=false&width=90pc)

10. Bây giờ bạn sẽ thấy cảnh báo mới được tạo. Hãy nhấn vào "Add alarm" một lần nữa và chúng ta sẽ tạo ra cảnh báo thứ hai.

![Create VPC](/images/5/00017.png?featherlight=false&width=90pc)

11. Trong workshop này, chúng ta sẽ giữ tất cả các cài đặt mặc định. Hãy chọn "Send me a notification when the alarm state changes to OK" để nhận thông báo khi trạng thái cảnh báo chuyển sang trạng thái OK.

- Nhấn vào nút "Create" để hoàn tất quá trình.

![Create VPC](/images/5/00018.png?featherlight=false&width=90pc)

12. Nếu bạn cuộn lên trên đồ thị, bạn sẽ thấy hai đường, mỗi đường biểu thị một trong hai cảnh báo, để hiển thị ngưỡng kích hoạt của chúng.

![Create VPC](/images/5/00019.png?featherlight=false&width=90pc)

"Bạn có thể sử dụng các bước trước đó này để thiết lập thêm các báo động cho bất kỳ phiên bản nào mà chúng tôi đã triển khai. Khả năng xác định vấn đề trước khi nó ảnh hưởng đến người dùng của bạn là một phần quan trọng của hoạt động liên tục của doanh nghiệp của bạn."
