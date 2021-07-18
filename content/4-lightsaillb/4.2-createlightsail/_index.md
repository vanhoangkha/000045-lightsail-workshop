+++
title = "Tạo Lightsail instance"
date = 2021
weight = 2
chapter = false
pre = "<b>4.2 </b>"
+++


#### Tạo Lightsail instance từ snapshot


1. Sau khi snapshot đã được tạo hoàn chỉnh, click vào biểu tượng 3 chấm.

![Lightsail](/images/1-deploy-infra/0040-newinstance.png?width=90pc)

2. Click **Create new instance** để tiến hành tạo Lightsail instance từ snapshot.

![Lightsail](/images/1-deploy-infra/0041-newinstance.png?width=90pc)

3. Click **Change zone** để thay đổi Availability Zone cho Lightsail instance, chúng ta sẽ tạo 2 Lightsail instance mới ở 2 Availability zone khác với Lightsail instance ban đầu.

![Lightsail](/images/1-deploy-infra/0042-newinstance.png?width=90pc)

4. Click **Zone B**.

![Lightsail](/images/1-deploy-infra/0043-newinstance.png?width=90pc)

5. Kéo màn hình xuống dưới cùng , đặt tên Lightsail instance là **PHP-FE-2** và click **Create instance**.

![Lightsail](/images/1-deploy-infra/0044-newinstance.png?width=90pc)

6. Click vào Lightsail instance **PHP-FE-1** , click vào tab **Snapshots** và làm tương tự bước 1 tới 5 để tạo thêm instance **PHP-FE-3** nhưng ở **Zone C** nhé.
Sau khi tạo xong hãy chắc chắn các instance đều ở trạng thái running trước khi thực hiện bước tiếp theo.
![Lightsail](/images/1-deploy-infra/0045-finish.png?width=90pc)