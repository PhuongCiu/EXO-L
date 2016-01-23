#CÁC CÂU LỆNH VỚI FILE VÀ FOLDER

##Liệt kê file, thư mục:
`ls [options]`
Lệnh ls liệt kê toàn bộ các tập tin và thư mục có trong thư mục hiện tại mà bạn đang ở.
`ls -a`   để hiển thị thêm các tập tin và thư mục bị ẩn
`ls -al`  để hiện chi chi tiết ngày giờ tập tin được tạo, user đang nắm quyền. thông tin chmod.
`cd <đường dẫn tới thư mục>` mở một thư mục, di chuyển đến một thư mục nào đó.
VD: `cd exo` mở thư mục exo

##Tạo file, thư mục:

`touch <newfile.txt>` tạo file mới
`mkdir <newfolder>` tạo thư mục mới

![](http://i.imgur.com/YszkXeQ.png)

##Xóa file, folder:
`rmdir <tên thư mục>` – Xoá thư mục
`rm <tên tập tin>` – Xoá bỏ tập tin
`rm -r <thư mục>` – Xoá thư mục
`rm -rf <thư mục>`  – Xoá cả các file có bên trong thư mục

![](http://i.imgur.com/FB5rxP6.png)

##Di chuyển và sao chép:
`cp <nguồn> <đích>` – Sao chép một tập tin/thư mục từ vị tri này sang vị trí khác
Bạn có thể sử dụng `cp -r <thư mục nguồn> <thư mục đích>`  để sao chép luôn tất cả các tập tin có bên trong thư mục

`mv <source> <destination>` Di chuyển tập tin/thư mục từ vị trí này sang vị trí khác. Câu lệnh này cũng có thể dùng để đổi tên tập tin/thư mục khi thư mục nguồn và đích trùng nhau

![](https://www.crazytut.com/static/images/cau-lenh-linux-cp-mv.png)

##Xem nội dung tập tin:
`cat <tập tin>`

![](http://i.imgur.com/QFnKjJ6.png)

`tail` – In ra nội dung của một tập tin với số dòng cụ thể 
`tail <tên tập tin>`  – Mặc định sẽ in ra 10 dòng của tập tin đó (10 dòng mới nhất)
`tail -n N <tên tập tin>` , thay N bằng số dòng mà bạn muốn in ra, thường lệnh này thích hợp cho việc xem log (nhật ký của tập tin)

![](https://www.crazytut.com/static/images/cau-lenh-linux-tail.png)
