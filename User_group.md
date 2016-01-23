#USER, GROUP

##1. User:
- User là người có thể truy cập đến hệ thống.
- User có username và password.
- Có hai loại user: super user và regular user.
- với tài khoản super user : root -có thể làm bất cứ điều gì muốn trên hệ thống.
- Để tạo một người dùng mới, thay đổi thuộc tính của một người dùng cũng như xóa bỏ một người dùng chỉ khi có quyền của một siêu người dùng.
- Mỗi user còn có một định danh riêng gọi là UID.
- Định danh của người dùng bình thường sử dụng giá trị bắt đầu từ 500.

###Câu lệnh quản lí user:
- Tạo user:
Cú pháp: `#useradd [option] <username>`
Một số option cơ bản:
`-c “Thông tin người dùng”
-d <Thư mục cá nhân>
-m : Tạo thư mục cá nhân nếu chưa tồn tại
-g <nhóm của người dùng>`

- Thay đổi user:
Cú pháp: `#usermod [option] <username>`
Các option tương tự như useradd
Ví dụ: `#usermod –g kinhdoanh vana` //chuyển vana từ nhóm server admin sang nhóm kinh doanh.

- Xóa user:
Cúpháp : `#userdel [option] <username>`
Vídụ :  `#userdel  –r  vana`

- Khóa/Mở khóa người dùng:
`passwd –l <username>  /  passwd –u <username>
usermod –L <username> /  usermod –U <username>`
Trong /etc/shadow có thể khóa tài khoản bằng cách thay từ khóa x bằng từ khóa *.

##2. Group:

- Group là tập hợp nhiều user lại.
- Mỗi user luôn là thành viên của một group.
- Khi tạo một user thì mặc định một group được tạo ra.
- Mỗi group còn có một định danh riêng gọi là GID.
- Định danh của group thường sử dụng giá trị bắt đầu từ 500.

###Các câu lệnh quản lí group:
- Tạo nhóm:
Cú pháp: `#groupadd <groupname>`
Ví dụ: `#groupadd exo`

- Xóa nhóm:
Cú pháp: `#groupdel <groupname>`
Ví dụ: `#groupdel <exo>`

- Xem thông tin về user và group:
Cú pháp: `#id <option> <username>`
Ví dụ: `#id -g vana //xem GroupID của user vana`
Cú pháp: `#groups <username>`
Ví dụ: `#groups vana //xem tên nhóm của user vana`

- Sửa group:
`#groupmod [-n New name] [-g new goupid]`

- Đổi pass:
`gpasswd []`

Khi sử dụng lệnh useradd hoặc groupadd, nếu chúng chúng ta không liệt kê đầy đủ các thông số cần thiết thì hệ thống sẽ lấy theo giá tri mặc nhiên đã được định nghĩa.
Chúng ta có thể thay đổi định nghĩa những giá trị này trong file sau:
/etc/login.defs : file chứa thông số mặc định khi tạo user hoặc tạo group.
/etc/skel/ : Tất cả những file là thư mục con trong này sẽ được copy sang HOME của user mới
