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
![Uploading image.png…]()

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
- 
# B. Kiến trúc phần mềm mạng
## I. Các thành phần phần mềm mạng
## II. Kiến trúc thứ bậc của giao thức
## III. Mô hình truyền tải tập tin 3 tầng
## IV. Bô giao thức  TCP/IP (quan trọng)
## V. Dịch vụ mạng
## VI. Các phép toán của dịch vụ
## VII. Sự khác biệt giữa dịch vụ & giao thức
