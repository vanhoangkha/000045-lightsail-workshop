+++
title = "Gắn instance vào LB"
date = 2021
weight = 3
chapter = false
pre = "<b>4.3 </b>"
+++
#### Gắn Lightsail instance vào load balancer
Ở bước này, sau khi tạo xong các Lightsail instance, chúng ta sẽ gắn các Lightsail instance vào load balancer **Todo-LB** mà chúng ta đã tạo.

1. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/). Click vào tab **Networking** sau đó click vào tên load balancer **Todo-LB**  chúng ta đã tạo.


![Lightsail](/images/9/0001.png?featherlight=false&width=90pc)

2. Tại mục **Target Instances**, click vào dropdown menu , gõ **P** để hiện ra danh sách các Lightsail instance chúng ta đã tạo, sau đó chọn instance đầu tiên của chúng ta  là **PHP-FE-1**.

![Lightsail](/images/9/0002.png?featherlight=false&width=90pc)

3. Click **Attach** để tiến hành gắn instance vào load balancer.

![Lightsail](/images/9/0003.png?featherlight=false&width=90pc)

4. Click **Attach another** và làm tương tự bước 2,3 để gắn 2 instance còn lại.

![Lightsail](/images/9/0004.png?featherlight=false&width=90pc)

5. Sau khi gắn hoàn tất 3 Lightsail instance, chúng ta sẽ đạt trạng thái như dưới đây.

![Lightsail](/images/9/0005.png?featherlight=false&width=90pc)

6. Kéo màn hình lên trên, right click lên DNS Name của **Todo-LB** load balancer và click **Open link in new tab** để truy cập tới ứng dụng web của chúng ta.

![Lightsail](/images/9/0006.png?featherlight=false&width=90pc)

7. Thực hiện F5 để refresh trình duyệt vài lần, chúng ta sẽ thấy chúng ta kết nối tới 2 Lightsail instance khác nhau.Chúc mừng bạn đã tăng quy mô ứng dụng web của mình thành công.

![Lightsail](/images/9/0007.png?featherlight=false&width=90pc)

