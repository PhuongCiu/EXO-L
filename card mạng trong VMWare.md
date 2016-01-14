#CÁC CHẾ ĐỘ CARD MẠNG TRONG VMWARE WORKSTATION

##1. Switch ảo (Virtual Switch):
- Cũng giống như switch vật lý, một Virtual Switch kết nối các thành phần mạng ảo lại với nhau.
- Những  switch ảo hay còn gọi là mạng ảo, chúng có tên là VMnet0, VMnet1, VMnet2… một số switch ảo được gắn vào mạng một cách mặc định.
- Mặc định khi ta cài Wmware thì có sẵn 3 Switch ảo như sau: VMnet0 chế độ Bridged (cầu nối), VMnet8 chế độ NAT và VMnet1 chế độ Host-only. (Ta có thể thêm, bớt, chỉnh các option của VMnet bằng cách vào menu Edit -> Virtual Network Editor...)
- VMware Workstation 9 và 10 cho phép tạo 10 switch ảo trên Windows và 255 cái trên Linux. Trên mỗi Switch ảo trên Windows thì cố kế nối với các máy tính ảo (host) là không giớ hạng còn trên Linux thì 32 máy ảo. Để thêm hoặc bớt VMnet ta có thể chọn Add Network... và Remove Network...

##2. Card mạng ảo:
- Khi bạn tạo một máy ảo mới (New Virtual Machine wizard), card mạng ảo được tạo ra cho máy ảo.
- Những card mạng này hiển thị trên hệ điều hành máy ảo như là AMD PCNET PCI hay Intel Pro/1000 MT Server Adapter.
- Từ VM Workstation 6.0 trở về sau này máy ảo có thể hổ trợ đến 10 card, các phiên bản trước bị giới hạn ở 3 card mạng. Thêm bớt card mạng bạn nhấn vào nút Add... hoặc Remove... trong Virtual Machine Setting

##3. DHCP server ảo:
- DHCP (Dynamic Host Configuration) server ảo cung cấp địa chỉ IP cho các máy ảo trong việc kết nối máy ảo vào các Switch ảo không có tính năng Bridged (VMnet0). Ví dụ như DHCP ảo cấp đến các máy ảo có kết nối đến Host-only và NAT.
- LAN Segment: Các card mạng của máy ảo có thể gắn kết với nhau thành từng LAN Segment. Không giống như VMnet, LAN Segment chỉ kết nối các card ảo lại với nhau mà không có những tính năng như DHCP hoặc kết nối chung với một card mạng ảo được tạo bên ngoài (các VMware Network Adapter VMnet được tạo bên ngoài máy thật).

##4. Các chế độ hoạt động:
- Chế độ Bridge: ở chế độ này thì card mạng trên máy ảo sẹ được gắn vào VMnet0 và VMnet0 này liên kết trực tiếp với card mạng vật lý. Ở chế độ này máy ảo sẽ kết nối internet thông qua lớp card mạng vật lý và có chung lớp mạng với card mạng vật lý.
- Chế độ NAT: ở chế độ này thì card mạng của máy ảo kết nối với VMnet8, VNnet8 cho phép máy ảo đi internet thông qua cơ chế NAT (NAT device). Lúc này lớp mạng bên trong máy ảo khác hoàn toàn với lớp mạng của card vật lý bên ngoài. IP của card mạng sẽ được cấp bởi DHCP VMnet8 cấp, trong trường hợp bạn muốn thiết lập IP tĩnh cho card mạng máy ảo bạn phải đảm bảo chung lớp mạng với VNnet8 thì máy ảo mới có thể đi internet.
- Cơ chế Host-only: ở cơ chế này máy ảo được kết nối với VMnet có tính năng Host-only, VNnet Host-only kết nối ra một card mạng ảo tương ứng ngoài máy thật (như đã nói ở phần trên, khi ta add một VMnet thì có một card tương ứng với VMnet sẽ được tạo ra ở phần trên. Ở chế độ này máy ảo không có kết nối internet. IP của máy ảo được cấp bởi DHCP của VMnet tương ứng.Trong nhiều trường hợp đặc biệt cần cấu hình riêng, ta có thể tắt DHCP trên VMnet và cấu hình IP bằng tay cho máy ảo.