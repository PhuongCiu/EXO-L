#LINUX: PHÂN QUYỀN FILE, USER

##1. Phân quyền trong Linux:

Trong Linux có 3 dạng đối tượng :
- Owner (người sở hữu).
- Group owner (nhóm sở hữu).
- Other users (những người khác).
Các quyền hạn :
- Read – r – 4  : cho phép đọc nội dung.
- Write – w – 2  : dùng để tạo, thay đổi hay xóa.
- Execute – x – 1  : thực thi chương trình.
Ngoài ra, chúng ta có thể dùng số.
Vídụ : quyền r, w, x : 4+2+1 = 7
Tổ hợp 3 quyền trên có giá trị từ 0 đến 7.

##2. Thay đổi phân quyền cho file và folder:

Để phân lại quyền cho cả file/folder trên Linux thì bạn sẽ sử dụng lệnh tên là chmod. Cấu trúc sử dụng lệnh này là:
`chmod [tùy chọn] [biểu diễn phân quyền] [tên file hoặc thư mục]`
Trong đó, mục [tùy chọn] là không bắt buộc, bao gồm các tùy chọn sau:
- -v: hiển thị báo cáo sau khi chạy lệnh. Nếu bạn chmod nhiều file/folder cùng lúc thì cứ mỗi lần nó đổi quyền của 1 file/folder xong là sẽ hiện báo cáo.
- -c: giống như trên, nhưng chỉ hiện khi nó đã làm xong tất cả.
- -f: Hiểu ngắn gọn là kiểu “kệ mẹ nó”, nếu có lỗi xảy ra nó cũng không thông báo.
- -R: nếu bạn CHMOD một folder thì kèm theo -R nghĩa là áp dụng luôn vào các file/folder nằm bên trong nó.
- -help: hiển thị thông báo trợ giúp.

Ở phần [biểu diễn phân quyền], ban có thể biểu diễn bằng 3 kiểu:
kiểu ký tự: giống như ở trên (rw-rw-x–).
kiểu ugo: kiểu này sẽ phân quyền cho từng đối tượng phân quyền.
kiểu số: cũng giống như ở trên (644).

Vídụ:
`chmod 775 testfile
chmod 400 testfolder
chmod u+s testfolder` (cho phép mọi thành viên không thuộc người sở hữu và không thuộc group sở hữu có thể execute folder)
Một vài ví dụ thêm về kiểu ugo:
o+rws: cho phép user sở hữu có full quyền
g+rw: cho phép group sở hữu có quyền đọc và ghi
u+w: cho phép các user còn lại có quyền đọc
a+rws: cho phép toàn bộ user có full quyền (777)

##3. Thay chủ sở hữu file/folder:
Mặc định các file và folder sẽ được sở hữu bởi user/group tạo ra nó.
Để đổi chủ sở hữu một thư mục cho user/group nào đó thì bạn sẽ sử dụng lệnh chown như sau:
`chown -R [tên user]:[tên group] [file/folder]`
Ví dụ:
`chown -R phuongciu:phuongciu /home/exo`

