#CẤU HÌNH NETWORK TRÊN UBUNTU

##Thông tin cơ bản:
Xem máy có bao nhiêu card mạng, gõ câu lệnh:
 `# ifconfig -a| grep eth`
 
Để kiểm tra xem các card mạng đã được cấu hình hay chưa:
 `# ifconfig `
 Lệnh này cung cấp địa chỉ  MAC, địa chỉ IP, gateway... của tất cả các card mạng.

 Để xem các định tuyến đi qua các mạng như thế nào gõ lệnh:
 `# route -n`
 
 ##Gán địa chỉ Ip tức thời cho card mạng:
 `# ifconfig ethX IP-address netmask subnet-mask`
 VD: # ifconfig eth0 192.168.1.2 netmask 255.255.255.0
 
 ##Gán địa chỉ IP cố định cho card mạng và lưu cấu hình trong file:
 Muốn card mạng được khai báo IP cố định, chúng ta đặt các lệnh cấu hình card mạng trong file cấu hình có đường dẫn là /etc/network/interface. Có thể dùng lệnh vi hoặc gedit để tạo file cấu hình card mạng này và chỉnh sửa nó

`#sudo gedit /etc/network/interfaces`

Nội dung file như sau:

`auto lo
iface lo inet loopback
auto eth0
iface eth0 inet static
address 192.168.1.2
netmask 255.255.255.1.0
gateway 192.168.1.1`
Sau khi khai báo cấu hình trong file interfaces nói trên, cần khởi động lại máy hoặc dùng lệnh sau để khởi động lại dịch vụ mạng để lấy cấu hình mới. Lưu ý 2 dòng đầu tiên là dành cho card loopback, không nên thay đổi.

`# sudo reboot
 # sudo /etc/init.d/networking restart`
 
 