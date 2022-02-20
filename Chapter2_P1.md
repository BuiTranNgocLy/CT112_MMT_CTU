> Vấn đề cần hiểu:
> 
> Phân loại mạng máy tính:
> 
>   Theo kĩ thuật truyền tin
>   
>   Theo phạm vi địa lí
>   
> Kiến trúc phần mềm mạng máy tính
> 
> Kiến trúc thứ bậc của giao thức mạng

# A. Phân loại mạng
## I. Theo kĩ thuật truyền tin
### 1. Mạng quảng bá (Broadcast)
- Tất cả các máy tính trong mạng `chia sẻ 1 kênh truyền` -> `mô hình tuyến tính`
- `Đặc điểm`: khi 1 máy gửi thông tin -> tất cả máy khác ở trạng thái "nghe". 
- Tại 1 thời điểm `chỉ` có 1 máy được gửi. Nếu có 2 máy cùng gửi thông tin -> xung đột xảy ra.
- => Giống môi trường 1 lớp học.
- `Có 3 dạng truyền tải thông tin(traffic)`:
   - `Unicast Traffic`: trên các khung/gói có địa chỉ người gửi/nhận cụ. Tất cả mọi máy đều nhận được thông tin, `chỉ` máy nào trong danh sách nhận sẽ xử lí thông tin.
   - `Boardcast Traffic`: thông tin gửi cho tất cả các máy. Tất cả các máy đều xử lí thông tin để kiểm tra câu trả lời cho yêu cầu nhận được.
   - `Multicast Traffic`: yêu cầu/thông tin gửi cho `1 nhóm` máy
### 2. Mạng điểm nối điểm (Point ts point) - Mạng chuyển mạch (Switched Network)
- Có nhiều kết nối giữa 2 máy tính
- Thông tin gửi từ nguồn có thể qua các điểm trung gian.
- Cần cơ chế xác định đường đi tốt 
## II. Theo khoản cách địa lý - GAN, WAN, MAN, LAN
### 1. Mạng cục bộ (LAN - Local Area Netwrok)
- Thuộc `Mạng quảng bá`
- Có thể `kết nối các mạng LAN` với nhau `thành mạng WAN`
- Dùng đường truyền băng thông rộng (tối thiểu 10Mb/s)
- Hình dạng kết nối đơn giản:
    - Mạng tuyến tính (BUS)
    - Mạng hình sao (Star) - chủ yếu
    - Mạng hình vòng (Ring)
#### Mạng tuyến tính (Bus)
![image](https://user-images.githubusercontent.com/88178841/154828865-aeca2ca4-813b-4c18-b40b-f917017669c2.png)

- Máy tính kết nối với nhau bằng 1 dây dẫn (cáp đồng trục)
- Ưu: dễ cài, chi phí xây dựng thấp
- Khuyết: khó phát hiện lỗi
#### Mạng hình sao (star)

- Máy tính kết nối vào 1 thiết bị tập trung `(Hub/Switch)` thông qua 1 liên kết riêng `(UTP/Cáp quang)`
- Ưu: dễ cài, dễ phát hiện lỗi. Mạng vẫn hoạt động khi `thêm Host`
- Khuyết: Chi phí cao so với Bus, không hoạt động nếu Hub bị lỗi
#### Mạng hình vòng (Ring)
![image](https://user-images.githubusercontent.com/88178841/154831362-b2773231-0a56-4709-aa23-6d06edfa4fa9.png)

- Truyền thông tin bằng 1 thẻ `(token)` lần lượt qua các máy tính
- Ưu: không xảy ra đụng độ -> hiệu suất 100%
- Khuyết: chi phí xây dựng cao, không hoạt động khi vòng gãy
### 2. Mạng đô thị (MAN - Metropolitan Area Network)
- Phạm vi địa lí: 1 thành phố, khu đô thị, khu kinh tế
### 3. Mạng diện rộng (WAN - Wide Area Network)
- Thuộc dạng `Mạng quảng bá`
- Kết nối máy tính nội bộ QG, giữa các QG trên châu lục
- Đáp ứng:
   - Tăng khoản cách giữa các host trong mạng
   - Tăng số lượng host
- Sử dụng kĩ thuật `lưu & chuyển tiếp (Store & forward)`- `Mạng chuyển gói`
## III. Phân loại mạng (hữu tuyến / vô tuyến)
### 1. Mạng không dây (wireless Network)
### Liên mạng (Internetwork)
- Hình thành từ kết nối nhiều mạng lại với nhau
- `LAN = LAN + LAN`
- `WAN = LAN + LAN`
- `WAN = WAN + WAN`
# B. Kiến trúc phần mềm mạng
## I. Các thành phần phần mềm mạng - 3tp
- Thành phần làm cho Mạng máy tính hoạt động, xây dựng dưa trên nền tảng 3 khái niệm
   - `Giao thức (Protocol)`: mô tả cách thức 2 thành phần mạng giao tiếp, trao đổi thông tin với nhau.
   - `Dịch vụ (Services)`: mô tả những điều mà 1 thành phần mạng cung cấp cho các thành phần khác muốn giao tiếp với nó.
   - `Giao diện (Interfaces)`: mô tả cách Khách hàng có thể sử dụng dịch vụ mạng và cách các dịch vụ có thể truy cập
## II. Kiến trúc thứ bậc của giao thức
- `Giảm độ phức tạp` trong quá trình thiết kế, xây dựng các hệ thống mạng -> tổ chức thành `Stack`, các lớp khác nhau, dựa theo nguyên tắc:
   - Tầng trên sử dụng dịch vụ của tầng dưới
   - 2 tầng ngang cấp nhau, trên 2 đối tượng mạng -> thống nhất về `giao thức` mà chúng trao đổi thông
   - Giữa 2 tầng liền kề tồn tại 1 `giao diện`
- Hệ thống mạng kháu nhau -> khác số tầng, tên/chức năng từng 
## III. Mô hình truyền tải tập tin 3 tầng
## IV. Bô giao thức  TCP/IP (quan trọng)
### 1. TCP/IP là gì?
- Transmission Control Protocol/Internet Protocol (Giao thức điều khiển truyền vận / giao thức)
- Bộ các giao thức trao đổi thông tin -> kết nối các thiết bị mạng trên Internet
- Trao đổi bằng cách cung cấp thông tin trao đổi đầu cuối -> xác định cách thức nó được chia thành các gói, gắn đại chỉ, vận chuyển, định tuyến và nhận ở điểm đến
- `TCP`: xác định ứng dụng tạo kênh giao tiếp trong mạng, quản lí cách các tin được phân thành các gói nhỏ trước khi chuyển qua Internet & tập hợp đúng thứ tự tại địa chỉ đến
- `IP`: xác định cách gán địa chỉ & định tuyến từng gói -> đảm bảo đến đúng nơi
### 2. Hoạt động
- Mô hình `Client/Server`: Server cung cấp dịch vụ
- Mỗi yêu cầu của Client xem là mới, nó không liên quan đến yêu cầu trước -> Giúp giải phóng đường mạng -> sử dụng liên tục.
- Tầng vận chuyển có trạng thái: truyền 1 tin duy nhất -> giữ nguyên -> nhận được tất cả các gói & tập trung tại điểm
### 3. Các tầng
![image](https://user-images.githubusercontent.com/88178841/154832757-9b57f6f5-d45a-44b0-90a7-8037edc0dffe.png)

- `Application`: cung cấp ứng dụng  trao đổi dữ liệu được chuẩn hóa. Bao gồm các giao thức HTTP, FTP, POP3, SMTP, SNMP.
- `Transport`: duy trì liên lạc đầu cuối trên toàn mạng. Xử lí thông tin liên lạc giữa các máy chủ -> cung cấp điều khiển luồng, ghép kênh, độ tin cậy. Bao gồm các giao thức: TCP, UDP
- `Internet`: xử lí các gói & kết nối các mạng độc lập -> vận chuyển các gói dữ liệu qua ranh giới mạng. Bao gồm các giao thức: IP, ICMP -> báo cáo lỗi.
- `Network Acess`: chỉ hoạt động trên 1 liên kết- thành phần mạng kết nối/ nút/ máy chủ trong mạng. Bao gồm các giao thức: Ethmet cho mạng LAN, ARP - phân giải địa chỉ
## V. Dịch vụ mạng - 2 dịch vụ
### 1. Dịch vụ định hướng kết nối (Connection - Oriented)
- Vận hành `mô hình hệ thống điện thoại`
- Trước khi trao đổi thông tin -> thiết lập nối kết
- Sau khi trao đổi xong -> ngắt kết nối.
### 2. Dịch vụ không kết nối (Connectionless)
- Vận hành `mô hình thư tín`
- Dữ liệu trước khi truyền đi -> vào trong gói tin (Packets)
- Trên các gói tin có thông tin về địa chỉ người gửi & địa chỉ người nhận
## VI. Các phép toán của dịch vụ
- Listen: nghe, chờ kết nối kết gửi đến
- Connect: yêu cầu thiết lập với bên muốn giao tiếp
- Recieve: Chờ nhận các thông điệp gửi đến
- Send: gửi thông diệp
- Disconnect: kết thúc 1 nối 
- Mô hình Client - Server có kết nối

![Uploading image.png…]()

- Mô hình không kết nối bỏ đi 1, 2, 5, 6
## VII. Sự khác biệt giữa dịch vụ & giao thức
- `Dịch vụ`: các thủ tục 1 tầng cung cấp cho tầng phía trên của nó
- `Giao thức`: tập hợp các quy tắc mô tả khuôn dạng, ý nghĩa của các gói tin được trao đổi
- 1 dịch vụ -> có thể thực hiện bởi các giao thức kahsc nhau
