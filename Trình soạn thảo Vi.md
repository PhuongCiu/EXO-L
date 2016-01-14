#TRÌNH SOẠN THẢO VI

##1. Cơ bản:
– Sử dụng vi kèm theo tên file(s) muốn edit: vi one.txt two.txt etc.txt
– Có 2 mode: command mode và insert mode. Khi bắt đầu sử dụng lệnh vi, vi mặc định ở command mode. Hoặc ấn Esc để chuyển sang command mode khi người dùng đang ở insert mode.
- Ấn phím lệnh i hoặc a từ chế độ command mode để chuyển sang insert mode. i để thêm ký tự trước con trỏ, a để thêm ký tự sau con trỏ.

##2. Nhóm lệnh di chuyển con trỏ:
h - sang trái 1 space
e - sang phải 1 space
w - sang phải 1 từ
b - sang trái 1 từ
k - lên 1 dòng
j - xuống 1 dòng
) - cuối câu
( - đầu câu
} - đầu đoạn văn
{ - cuối đoạn văn

##3. Nhóm lệnh xóa:
dw - xóa 1 từ
d^ - xóa ký tự từ con trỏ đến đầu dòng
d$ - xóa ký tự từ con trỏ đến cuối dòng
3dw - xóa 3 từ
dd - xóa dòng hiện hành
5dd - xóa 5 dòng
x - xóa 1 ký tự

##4. Nhóm lệnh thay thế:
cw - thay thế 1 từ
3cw - thay thế 3 từ
cc - dòng hiện hành
5cc - 5 dòng

##5. Nhóm lệnh tìm kiếm:
? tìm trở lên
/ tìm trở xuống
*/and tìm từ kế tiếp của and
*?and tìm từ kết thúc là and
*/nThe tìm dòng kế bắt đầu bằng The
n tìm hướng xuống
N tìm hướng lên

##6. Nhóm lệnh tìm kiếm và thay thế
:s/text1/text2/g - thay thế text1 bằng text2
:1.$s/tập tin/thư mục - thay tập tin bằng thư mục từ hàng 1
:g/one/s/1/g - thay thế one bằng 1

##7. Nhóm lệnh copy, paste, undo:
Để copy ta dùng lệng y và để paste ta dùng lệnh p
y$ - copy từ vị trí hiện tại của cursor đến cuối cùng
yy - copy toàn bộ dòng tại vị trí cursor
3yy - copy 3 dòng liên tiếp
u - Undo lại thao tác trước đó

##8. Thao tác trên tập tin
:w - ghi vào tập tin
:x - lưu và thoát khỏi chế độ soạn thảo
:wq - lưu và thoát khỏi chế độ soạn thảo
:w - lưu vào tập tin mới
:q - thoát nếu ko có thay đổi
:q! - thoát không lưu
:r - mở tập tin đọc