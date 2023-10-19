---
title : "Triển khai Prestashop E-Commerce Instance"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

#### Triển khai Prestashop E-Commerce 

1. Đôi khi, việc sao chép/dán giữa máy tính cá nhân và trình duyệt SSH có thể làm hỏng định dạng dữ liệu trong bộ nhớ tạm. Nếu bạn muốn SSH từ máy tính xách tay của bạn, hãy mở rộng các bước tương ứng cho Mac hoặc Windows bên dưới và sử dụng địa chỉ IP tĩnh của máy ảo thay vì thực hiện theo Bước 1 ở dưới.


- Nhấp vào tên instance, Akaunting, để quay lại trang instance. Sau đó, nhấp vào Kết nối bằng SSH.

- Sao chép và dán các lệnh sau vào cửa sổ SSH và nhấn Enter.

:::alert{Thay 'NEW_STATIC_IP_HERE' bằng địa chỉ IP tĩnh của instance này.}


```
# Paste the following
sudo sed -i 's/replace_here/NEW_STATIC_IP_HERE/g' /etc/apache2/sites-available/akaunting.conf

# Enable Apache2 virtualhost configuration for Akaunting
sudo a2ensite akaunting

# Enable specified module in apache configuration
sudo a2enmod rewrite

# Restart the apache service to make changes live.
sudo systemctl restart apache2

```

#### Tạo một cơ sở dữ liệu mới trên Lightsail Database Instance cho Akaunting. 
1. Trước khi chúng ta cài đặt Akaunting, chúng ta cần một cơ sở dữ liệu để lưu trữ dữ liệu. Hãy nhớ rằng, trong bài thực hành này, chúng ta đã triển khai một thể hiện cơ sở dữ liệu MySQL Lightsail từ xa và một cơ sở dữ liệu WordPress. Chúng ta sẽ tạo một cơ sở dữ liệu thứ hai trên cùng một thể hiện cơ sở dữ liệu như cơ sở dữ liệu WordPress để tận dụng tài nguyên hiện có.

Dán lệnh sau vào cửa sổ SSH của bạn (chỉnh sửa URL điểm cuối cơ sở dữ liệu để phù hợp với URL điểm cuối của cơ sở dữ liệu của bạn), và nhấn Enter.

```
mysql -u LightsailAdmin -pSunny2DAY! -h YOUR_DATABASE_ENDPOINT
```

2. Lệnh này đang ghi lại bạn vào trường hợp cơ sở dữ liệu Lightsail từ xa:

```
-u = MySQL Username
-p = Password (note there is no space between the -p and the beginning of the password)
-h = Host URL. If we used a different port other than the default, we'd have additional parameters to specify.
```

3. Bây giờ chúng ta đã kết nối với phiên bản cơ sở dữ liệu từ xa, chúng ta sẽ tạo một cơ sở dữ liệu mới cho ứng dụng Akaunting của chúng ta. Hãy gõ 'CREATE DATABASE akaunting;' và nhấn Enter.

- Chúng ta sẽ tạo một người dùng cơ sở dữ liệu mới cho cơ sở dữ liệu akaunting và gán cho nó tất cả các quyền. Chạy các lệnh sau trong phiên SSH:

```
create user 'accountant'@'localhost' identified by 'Exnte3x!';

grant all privileges on akaunting.* to 'accountant'@'localhost';

flush privileges;

exit;

```

![Create VPC](/images/3/0007.png?featherlight=false&width=90pc)

4. Chúng ta đã sẵn sàng để thực hiện việc cài đặt ứng dụng Akaunting.

- Trong trình duyệt của bạn, hãy điều hướng đến địa chỉ IP tĩnh của phiên bản Akaunting của bạn.
- Bây giờ bạn sẽ được chuyển hướng đến trang cài đặt của Akaunting. Nếu nó không tự động chuyển hướng bạn, hãy thử dán địa chỉ IP tĩnh vào trình duyệt, sau đó thêm '/install/language' và nhấn Enter.
- Chọn ngôn ngữ mà bạn muốn và nhấn **Next**.

![Create VPC](/images/3/0008.png?featherlight=false&width=90pc)

5. Hãy nhập thông tin xác thực cơ sở dữ liệu mà chúng ta đã tạo vào các ô văn bản tương ứng:

```
Hostname: your_lightsail_database_endpoint
Username: LightsailAdmin
Password: Exnte3x!
Database: akaunting
```

- Chọn **Next**

![Create VPC](/images/3/0009.png?featherlight=false&width=90pc)

6. Nếu mọi thứ đã được nhập đúng, nút 'Tiếp theo' sẽ hiện ra và nhấp nháy như những chấm trắng, giống như đang tải. Chúng ta sẽ để nó chạy trong vài phút.

- Trên trang tiếp theo, sử dụng các giá trị sau cho các thông tin quản trị viên (Admin):

```
Company Name: Example Co.
Company email: admin@example.com
Admin Email: admin@example.com
Admin Password: S@ndyBeach3s!
```

- Chọn **Next**

![Create VPC](/images/3/00010.png?featherlight=false&width=90pc)

7. Bây giờ bạn có thể đăng nhập và nhập các chi tiết cụ thể cho doanh nghiệp của bạn.
Hãy nhập tên người dùng và mật khẩu mới vào các lời nhắc và nhấp vào "Login".

8. Trong 'Company' page, click Skip this step.

![Create VPC](/images/3/00011.png?featherlight=false&width=90pc)

9. Chọn **Next**

![Create VPC](/images/3/00012.png?featherlight=false&width=90pc)

10.  Chọn **Next**

![Create VPC](/images/3/00013.png?featherlight=false&width=90pc)

11. Chọn **Create your first iinvoice*

![Create VPC](/images/3/00014.png?featherlight=false&width=90pc)

12. Chọn **Dashboard**

![Create VPC](/images/3/00015.png?featherlight=false&width=90pc)

13. Trong giao diện của Lightsail, hãy nhấp vào mục Databases.

- Tiếp theo, bạn nhấp vào tên của trường hợp cơ sở dữ liệu, sau đó chọn Tags.
- Click Edit key-only tags và nhập 'Akaunting'. Click Save.

![Create VPC](/images/3/00016.png?featherlight=false&width=90pc)


