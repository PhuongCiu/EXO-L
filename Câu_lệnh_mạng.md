#CÁC CÂU LỆNH VỀ MẠNG

##1. Lệnh Ping:
Lệnh ping gửi các gói ECHO_REQUEST tới địa chỉ chỉ định.
Câu lệnh nhằm kiểm tra máy tính có thể kết nối với Internet hay một địa chỉ IP cụ thể nào đó hay không.
Tuy nhiên có rất nhiều hệ thống được cấu hình để không hồi đáp với các lệnh ping.
Câu lệnh: `ping [option] <địa chỉ>`

Ví dụ: `ping –c 4 google.com`
![](http://i.imgur.com/shd4jX8.png)

##2. Lệnh Tracepath và traceroute:
Lệnh tracepath cũng tương tự như traceroute nhưng nó không đòi hỏi các quyền quản trị. Nó cũng được cài đặt mặc định trên Ubuntu còn tracerout thì không. Lệnh tracepath lần dấu đường đi trên mạng tới một đích chỉ định và báo cáo về mỗi nút mạng (hop) dọc trên đường đi. Nếu gặp phải các vấn đề về mạng, lệnh tracepath có thể chỉ ra vị trí lỗi mạng.
Câu lệnh: `tracert ip/host`

##3. Lệnh Netstat:
Câu lệnh netstat đưa ra các thống kê khác nhau cho giao diện, bao gồm các socket mở và các bảng định tuyến.
Cú pháp: `netstat [option]`
![](http://i.imgur.com/CLI2LE4.png)

Sử dụng câu lệnh `netstat –p` để xem các chương trình đi kèm với các socket mở.
Xem các thống kê chi tiết cho tất cả các cổng bằng câu lệnh `netstat –s`
![](http://i.imgur.com/f7qwzn2.png)

Kiểm tra các port đang ở trạng thái listening(lắng nghe):
netstat -l
![](http://i.imgur.com/ngDrIXu.png)

Kiểm tra các port ở trạng thái listening sử dụng giao thức TCP:
netstat -lt
![](http://i.imgur.com/siW0bd1.png)

##4. Lệnh ifconfig:
Câu lệnh ifconfig có rất nhiều tùy chọn để cấu hình, điều chỉnh và dò lỗi trên các giao diện mạng hệ thống. Đây cũng là cách để xem nhanh các địa chỉ IP và các thông tin khác của giao diện mạng. Gõ ifconfig để xem trạng thái các giao diện mạng hiện đang hoạt động bao gồm tên của chúng. Bạn cũng có thể chỉ định tên một giao diện để xem thông tin trên duy nhất giao diện đó.
`ifconfig
ifconfig eth0`

![](http://i.imgur.com/6mlyfOo.png)
##5. Lệnh ifplugstatus:
Lệnh ifplugstatus giúp kiểm tra dây cáp có được cắm vào giao diện mạng hay không. Câu lệnh này không được cài đặt mặc định trên Ubuntu. Sử dụng câu lệnh sau để cài đặt nó
`sudo apt-get install ifplugd`
Chạy các câu lệnh sau để xem trạng thái tất cả các giao diện hay chỉ xem trạng thái một giao diện cụ thể.
`ifplugstatus
ifplugstatus eth0`
![](http://i.imgur.com/v5PxlYG.png)

