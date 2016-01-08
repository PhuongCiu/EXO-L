#A. MÔ HÌNH OSI
##1. Chức năng:
Mô hình tham chiếu OSI là một cấu trúc phả hệ có 7 tầng, nó xác định các yêu cầu cho sự giao tiếp giữa hai máy tính. Mục đích của mô hình là cho phép sự tương giao (interoperability) giữa các hệ máy (platform) đa dạng được cung cấp bởi các nhà sản xuất khác nhau. Mô hình cho phép tất cả các thành phần của mạng hoạt động hòa đồng, bất kể thành phần ấy do ai tạo dựng.

##2. Mô hình OSI:

<img src="https://www.google.com/search?q=m%C3%B4+h%C3%ACnh+osi&biw=1366&bih=665&tbm=isch&imgil=vbC9xoTOaLDtCM%253A%253B8Udd5ePQLkJgMM%253Bhttp%25253A%25252F%25252Fkimnguyen.info%25252Fmang-may-tinh-mo-hinh-osi.html&source=iu&pf=m&fir=vbC9xoTOaLDtCM%253A%252C8Udd5ePQLkJgMM%252C_&usg=__1q566tz-46VpzsuaF4LKnjUp_m0%3D&ved=0ahUKEwiSvKa1o_fJAhURjo4KHdIWA0YQyjcIJw&ei=Alp9VpKzApGcugTSrYywBA#imgrc=AQc_CtrmBgLj6M%3A&usg=__1q566tz-46VpzsuaF4LKnjUp_m0%3D">

###2.1. Tầng vật lí (Physical):
- Là tầng thấp nhất trong mô hình 7 lớp OSI.
- Xác định các chức năng, thủ tục về điện, cơ, quang để kích hoạt, duy trì và giải phóng các kết nối vật lý giữa các hệ thống mạng.
- Cung cấp các cơ chế về điện, cơ hàm, thủ tục ... nhằm thực hiện việc kết nối các phần tử của mạng thành một hệ thống bằng các phương pháp vật lý.
- Tham gia vào quy trình mà trong đó các tài nguyên truyền thông được chia sẻ hiệu quả giữa nhiều người dùng. Chẳng hạn giải quyết tranh chấp tài nguyên (contention) và điều khiển lưu lượng.
- Điều chế (modulation), hoặc biến đổi giữa biểu diễn dữ liệu số (digital data) của các thiết bị người dùng và các tín hiệu tương ứng được truyền qua kênh truyền thông (communication channel).

###2.2. Tầng liên kết dữ liệu (Data Link):
- Tầng liên kết dữ liệu cung cấp các phương tiện có tính chức năng và quy trình để truyền dữ liệu giữa các thực thể mạng, phát hiện và có thể sửa chữa các lỗi trong tầng vật lý nếu có.
- Để thực hiện việc này, lớp liên kết dữ liệu cung cấp:
<ul>
<li>Thiết lập và kết thúc liên kết: thiết lập và kết thúc liên kết hợp lý giữa hai nút.</li>
<li>Kiểm soát lưu lượng truy cập khung: yêu cầu nút truyền "trở lại" khi không có bộ đệm khung nào.</li>
<li>Trình tự khung: truyền/nhận khung tuần tự.</li>
<li>Báo nhận khung: cung cấp/nhận báo nhận khung. Phát hiện và khôi phục từ lỗi xảy ra trong lớp vật lý bằng cách truyền lại khung không được báo nhận và xử lý nhận khung trùng lặp.</li>
<li>Đặt giới hạn khung: tạo và nhận diện ranh giới khung.</li>
<li>Kiểm tra lỗi khung: kiểm tra khung đã nhận xem có toàn vẹn không.</li>
<li>Quản lý truy cập phương tiện: xác định khi nút "có quyền" sử dụng các phương tiện vật lý.</li>

###2.3. Tầng mạng (Network):
Tầng mạng cung cấp các chức năng và qui trình cho việc truyền các chuỗi dữ liệu có độ dài đa dạng, từ một nguồn tới một đích, thông qua một hoặc nhiều mạng, trong khi vẫn duy trì chất lượng dịch vụ (quality of service) mà tầng giao vận yêu cầu. Tầng mạng thực hiện chức năng định tuyến.Các thiết bị định tuyến (router) hoạt động tại tầng này — gửi dữ liệu ra khắp mạng mở rộng, làm cho liên mạng trở nên khả thi (còn có thiết bị chuyển mạch (switch) tầng 3, còn gọi là chuyển mạch IP).
- Định tuyến: định tuyến khung trong mạng.
- Điều khiển lưu lượng mạng con: bộ định tuyến (hệ thống trung gian lớp mạng) có thể khiến trạm gửi "giảm tiết lưu" truyền khung khi bộ đệm của bộ định tuyến đầy lên.
- Phân mảnh khung: nếu phân mảnh này xác định rằng kích thước đơn vị truyền tối đa (MTU) của bộ định tuyến hạ lưu nhỏ hơn kích thước khung, bộ định tuyến có thể phân mảnh khung để truyền và kết hợp lại tại trạm đích.
- Ánh xạ địa chỉ vật lý logic: dịch địa chỉ hoặc tên logic thành địa chỉ vật lý.
- Tính toán việc sử dụng mạng con: có chức năng tính toán để theo dõi khung được chuyển tiếp bởi các hệ thống trung gian của mạng con để tạo ra thông tin thanh toán.

###2.4. Tầng giao vận (Transport):
- Tầng giao vận cung cấp dịch vụ chuyên dụng chuyển dữ liệu giữa các người dùng tại đầu cuối, nhờ đó các tầng trên không phải quan tâm đến việc cung cấp dịch vụ truyền dữ liệu đáng tin cậy và hiệu quả.
- Tầng giao vận kiểm soát độ tin cậy của một kết nối được cho trước.
- Một số giao thức có định hướng trạng thái và kết nối (state and connection orientated). Có nghĩa là tầng giao vận có thể theo dõi các gói tin và truyền lại các gói bị thất bại.
Tầng giao vận cung cấp:
- Phân đoạn thư: chấp nhận thư từ lớp (phiên) ở trên, chia thư thành các đơn vị nhỏ hơn (nếu chưa đủ nhỏ) và chuyển các đơn vị nhỏ hơn xuống lớp mạng. Lớp truyền tải nhà đích từng thư.
- Báo nhận thư: cung cấp báo nhận chuyển phát thư đầu cuối đáng tin cậy.
- Kiểm soát lưu lượng thư: yêu cầu trạm truyền "gửi trả lại" khi không có bộ đệm thư.
- Đa hợp phiên: kết hợp một số luồng thư hoặc phiên vào một liên kết logic và theo dõi thư nào thuộc phiên nào (xem lớp phiên).
Thông thường, tầng giao vận có thể chấp nhận thư tương đối lớn nhưng có những giới hạn kích thước thư nghiêm ngặt do tầng mạng (hoặc tầng thấp hơn) áp đặt. Do đó, tầng giao vận phải chia thư thành các đơn vị nhỏ hơn hoặc khung, thêm tiêu đề vào mỗi khung. 
Khi đó, thông tin tiêu đề tầng giao vận phải bao gồm thông tin kiểm soát, chẳng hạn như cờ bắt đầu và kết thúc thư, để cho phép tầng giao vận ở đầu kia nhận ra ranh giới thư.

###2.5. Tầng phiên (Session):
- Tầng phiên kiểm soát các (phiên) hội thoại giữa các máy tính.
- Tầng này thiết lập, quản lý và kết thúc các kết nối giữa trình ứng dụng địa phương và trình ứng dụng ở xa.
- Tầng này còn hỗ trợ hoạt động song công (duplex) hoặc bán song công (half-duplex) hoặc đơn công (Single) và thiết lập các qui trình đánh dấu điểm hoàn thành (checkpointing) - giúp việc phục hồi truyền thông nhanh hơn khi có lỗi xảy ra, vì điểm đã hoàn thành đã được đánh dấu - trì hoãn (adjournment), kết thúc (termination) và khởi động lại (restart).

###2.6. Tầng trình diễn (Presentation):
Lớp trình diễn hoạt động như tầng dữ liệu trên mạng. lớp này trên máy tính truyền dữ liệu làm nhiệm vụ dịch dữ liệu được gửi từ tầng Application sang dạng Fomat chung. Và tại máy tính nhận, lớp này lại chuyển từ Fomat chung sang định dạng của tầng Application.
Lớp thể hiện thực hiện các chức năng sau:
- Dịch các mã kí tự từ ASCII sang EBCDIC.
- Chuyển đổi dữ liệu, ví dụ từ số interger sang số dấu phảy động.
- Nén dữ liệu để giảm lượng dữ liệu truyền trên mạng.
- Mã hoá và giải mã dữ liệu để đảm bảo sự bảo mật trên mạng.

###2.7. Tầng ứng dụng (Application):
Lớp ứng dụng đóng vai trò như một cửa sổ cho người dùng và quy trình ứng dụng để truy cập dịch vụ mạng. Lớp này bao gồm một loạt các chức năng thường cần thiết: 
- Chuyển hướng thiết bị và chia sẻ tài nguyên
- Truy cập tệp từ xa
- Truy cập máy in từ xa
- Kết nối giữa các quy trình
- Quản lý mạng
- Dịch vụ thư mục
- Nhắn tin điện tử (chẳng hạn như thư)
- Điểm đầu cuối mạng ảo

#B. MÔ HÌNH TCP/IP:

##1. Chức năng:
TCP/IP có cấu trúc tương tự như mô hình OSI, tuy nhiên để đảm bảo tính tương thích giữa các mạng và sự tin cậy của việc truyền thông tin trên mạng, bộ giao thức TCP/IP được chia thành 2 phần riêng biệt: giao thức IP sử dụng cho việc kết nối mạng và giao thức TCP để đảm bảo việc truyền dữ liệu một cách tin cậy.

##2. Mô hình TCP/IP:
<img src="https://www.google.com/search?q=m%C3%B4+h%C3%ACnh+osi&biw=1366&bih=665&tbm=isch&imgil=vbC9xoTOaLDtCM%253A%253B8Udd5ePQLkJgMM%253Bhttp%25253A%25252F%25252Fkimnguyen.info%25252Fmang-may-tinh-mo-hinh-osi.html&source=iu&pf=m&fir=vbC9xoTOaLDtCM%253A%252C8Udd5ePQLkJgMM%252C_&usg=__1q566tz-46VpzsuaF4LKnjUp_m0%3D&ved=0ahUKEwiSvKa1o_fJAhURjo4KHdIWA0YQyjcIJw&ei=Alp9VpKzApGcugTSrYywBA#tbm=isch&q=m%C3%B4+h%C3%ACnh+tcp%2Fip&imgdii=qrI8fQd8ZkH28M%3A%3BqrI8fQd8ZkH28M%3A%3BJF3nILUT0m6lAM%3A&imgrc=qrI8fQd8ZkH28M%3A">

###2.1. Tầng liên kết.
Tầng liên kết - phương pháp được sử dụng để chuyển các gói tin từ tầng mạng tới các máy chủ (host) khác nhau - không hẳn là một phần của bộ giao thức TCP/IP, vì giao thức IP có thể chạy trên nhiều tầng liên kết khác nhau. Các quá trình truyền các gói tin trên một liên kết cho trước và nhận các gói tin từ một liên kết cho trước có thể được điều khiển cả trong phần mềm điều vận thiết bị (device driver) dành cho cạc mạng, cũng như trong phần sụn (firmware) hay các chipset chuyên dụng. Những thứ đó sẽ thực hiện các chức năng liên kết dữ liệu chẳng hạn như bổ sung một tín đầu (packet header) để chuẩn bị cho việc truyền gói tin đó, rồi thực sự truyền frame dữ liệu qua một môi trường vật lý.
Tầng liên kết còn có thể là tầng nơi các gói tin được chặn (intercepted) để gửi qua một mạng riêng ảo (virtual private network). Khi xong việc, dữ liệu tầng liên kết được coi là dữ liệu của ứng dụng và tiếp tục đi xuống theo chồng giao thức TCP/IP để được thực sự truyền đi. Tại đầu nhận, dữ liệu đi lên theo chồng TCP/IP hai lần (một lần cho mạng riêng ảo và lần thứ hai cho việc định tuyến).
Tầng liên kết còn có thể được xem là bao gồm cả tầng vật lý - tầng là kết hợp của các thành phần mạng vật lý thực sự (hub, các bộ lặp (repeater), cáp mạng, cáp quang, cáp đồng trục (coaxial cable), cạc mạng, cạc HBA (Host Bus Adapter) và các thiết bị nối mạng có liên quan: RJ-45, BNC, etc), và các đặc tả mức thấp về các tín hiệu (mức hiệu điện thế, tần số, v.v..).

###2.2. Tầng mạng.
Nằm bên trên tầng giao diện mạng. Tầng này có chức năng gán địa chỉ, đóng gói và định tuyến (Route) dữ liệu. 4 giao thức quan trọng nhất trong tầng này gồm:
- IP (Internet Protocol): Có chức năng gán địa chỉ cho dữ liệu trước khi truyền và định tuyến chúng tới đích.
- ARP (Address Resolution Protocol): Có chức năng biên dịch địa chỉ IP của máy đích thành địa chỉ MAC.
- ICMP (Internet Control Message Protocol): Có chức năng thông báo lỗi trong trường hợp truyền dữ liệu bị hỏng.
- IGMP (Internet Group Management Protocol): Có chức năng điều khiển truyền đa hướng (Multicast) 

###2.3. Tầng giao vận.
Có trách nhiệm thiết lập phiên truyền thông giữa các máy tính và quy định cách truyền dữ liệu. 2 giao thức chính trong tầng này gồm:
+ UDP (User Datagram Protocol): Còn gọi là Giao Thức Gói Người Dùng. UDP cung cấp các kênh truyền thông phi kết nối nên nó không đảm bảo truyền dữ liệu 1 cách tin cậy. Các ứng dụng dùng UDP thường chỉ truyền những gói có kích thước nhỏ, độ tin cậy dữ liệu phụ thuộc vào từng ứng dụng 
+ TCP (Transmission Control Protocol): Ngược lại với UDP, TCP cung cấp các kênh truyền thông hướng kết nối và đảm bảo truyền dữ liệu 1 cách tin cậy. TCP thường truyền các gói tin có kích thước lớn và yêu cầu phía nhận xác nhận về các gói tin đã nhận.

###2.4. Tầng ứng dụng:
Gồm nhiều giao thức cung cấp cho các ứng dụng người dùng. Được sử dụng để định dạng và trao đổi thông tin người dùng. 1 số giao thức thông dụng trong tầng này là:
+ DHCP (Dynamic Host Configuration Protocol): Giao Thức Cấu Hình Trạm Động
+ DNS (Domain Name System): Hệ Thống Tên Miền
+ SNMP (Simple Network Management Protocol): Giao Thức Quản Lý Mạng Đơn Giản
+ FTP (File Transfer Protocol): Giao Thức Truyền Tập Tin
+ TFTP (Trivial File Transfer Protocol): Giao Thức Truyền Tập Tin Bình Thường 
+ SMTP (Simple Mail Transfer Protocol): Giao Thức Truyền Thư Đơn Giản 
+ TELNET

 ##3. Một số giao thức trong tầng ứng dụng:
 
- HTTP - Giao thức truyền siêu văn bản dùng cổng 80; 
- FTP - Giao thức truyền tệp dùng cổng 21.