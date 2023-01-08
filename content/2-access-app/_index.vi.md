+++
title = "Truy cập ứng dụng"
date = 2021
weight = 2
chapter = false
pre = "<b>2. </b>"
+++


#### Truy cập ứng dụng

Trong bước này, chúng ta sẽ truy cập ứng dụng chúng ta đã cài trong Lightsail instance.

Kiến trúc hiện tại của chúng ta rất đơn giản ,  chúng ta sẽ kết nối trực tiếp tới Lightsail instance qua internet.

![Lightsail](/images/architecture/arc-lightsailinstance.png?width=50pc)

Về mặt ứng dụng, Front end PHP và cơ sở dữ liệu MySQL của chúng ta hiện tại được cài đặt trên 1 Lightsail instance duy nhất.

![Lightsail](/images/architecture/arc-lightsailinstanceapp.png?width=45pc)

1. Quay trở lại giao diện [Lightsail console](https://lightsail.aws.amazon.com/ls/webapp/home/).
Chúng ta sẽ thấy địa chỉ IP public của Lightsail instance.

![Lightsail](/images/4/4.1/0001.png?featherlight=false&width=90pc)

2. Tiến hành kết nối tới địa chỉ public IP address, chúng ta sẽ truy cập vào ứng dụng todo như dưới đây.

![Lightsail](/images/4//4.1/0002.png?featherlight=false&width=90pc)
