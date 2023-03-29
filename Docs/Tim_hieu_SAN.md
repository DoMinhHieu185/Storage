# Tìm hiểu về SAN

### SAN là gì?
![](F:\GITHUB\Storage\img\san.png)

SAN(Storage Area Network - Vùng mạng lưu trữ) là một mạng các thiết bị lưu trữ có thể được truy cập bởi nhiều máy chủ hoặc máy tính, cung cấp một nhóm không gian lưu trữ được chia sẻ. Mỗi máy tính trong mạng có thể truy cập bộ nhớ trên SAN như thể chúng là các địa cục bộ được kết nối trực tiếp  với máy tính.

### Ưu điểm
* Khắc phục vấn đề suy giảm bằng thông mạng LAN
* Tăng cường bảo vệ dữ liệu 
* Sao lưu khôi phục dễ dàng 
* Tăng khả năng mở rộng
* Có thể phân quyền truy cập theo block
* Hiệu suất cao, đáp ứng cả file dung lượng lớn

### Các thành phần chính trong SAN
#### Lưu trữ(Storage)
Thiết bị lưu trữ trong SAN là các tủ đĩa có dung lượng lớn, khả năng truy xuất dữ liệu nhanh, hỗ trợ các chức năng như RAID, Local Replica,… Đây cũng là nơi chứa dữ liệu chung cho toàn bộ hệ thống.

#### Chuyển mạch (Switch)
Bộ chuyển mạch SAN là phần cứng kết nối máy chủ với các nhóm thiết bị lưu trữ được chia sẻ trong SAN. Nó dành riêng cho việc di chuyển lưu lượng lưu trữ trong SAN. Chức năng của nó bao gồm:
* Cung cấp các điểm kết nối trong SAN
* Cung cấp khả năng điều tiết số lượng kết nối SAN từ máy chủ và số lượng kết nối được cung cấp bởi mảng lưu trữ (Storage array).
* Cung cấp đường dẫn dự phòng trong trường hợp có lỗi.

#### Máy chủ hoặc máy trạm (Host)
Các thành phần máy chủ hoặc máy trạm của SAN bao gồm: các máy chủ và các thành phần cho phép các máy chủ được kết nối vật lý với SAN. Các máy chủ được kết nối đến bộ chuyển mạch bằng cáp quang thông qua HBA card.

### Phân loại SAN
Có 4 loại giao thức SAN phổ biến.

#### Fibre Channel Protocol (FCP)
FCP là giao thức SAN được sử dụng phổ biến nhất, FCP sử dụng giao thức vận chuyển Fibre Channel cùng với các lệnh SCSI tích hợp.

#### Internet Small Computer System Interface (iSCSI)
iSCSI hay giao thức hệ thống máy tính internet quy mô nhỏ là giao thức SAN phổ biến thứ 2 với 10-15% thị phần. iSCSI đóng gói các lệnh SCSI trong một Ethernet frame và sử dụng mạng Ethernet dựa trên IP để truyền tải.

#### Fibre Channel over Ethernet (FCoE)
FCoE chiếm ít hơn 5% thị trường SAN. Tương tự như iSCSI, FCoE đóng gói một khung FC (Fibre Channel) bên trong một Ethernet diagram, sau đó sử dụng mạng Ethernet IP để truyền tải.

#### Non-Volatile Memory Express over Fibre Channel (FC-NVMe)
NVMe (giao thức truy cập bộ nhớ điện tĩnh) là một giao thức giao diện để truy cập bộ nhớ flash thông qua một bus PCI Express (PCIe). Không giống như kiến trúc all-flash truyền thống bị giới hạn trong một hàng đợi lệnh nối tiếp, NVMe hỗ trợ hàng chục nghìn hàng đợi song song, mỗi hàng có khả năng hỗ trợ hàng chục nghìn lệnh đồng thời. Do đó FC-NVMe cho tốc độ truy cập cao và độ trễ thấp.