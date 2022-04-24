Chapter 8: Application layer![image](https://user-images.githubusercontent.com/88178841/164969979-97c08093-75d3-4240-992c-218fe08f59b3.png)
# I. Giới thiệu
- `Application`: các tiến trình phân tán và giao tiếp
  - Chạy trên máy tính mạng ở không gian người dùng (uper space)
  - Trao đổi thông điệp
  - Ex: email, web   
- `Application-layer protocols`: 1 thành phần của ứng dụng
  - Định nghĩa các thông điệp được trao đổi, các tác vụ được thực hiện
  - Sử dụng các dịch vụ của `tầng vận chuyển (TCP/UDP)`
# II. DNS (Domain Name System)
- Giao thức IP -> địa chỉ IP định vị các máy tính trong mạng
- Router -> vạch đường đi cho các gói tin
- Là 1 CSDL phân tán, sử dụng trên hệ thống mạng TCP/IP -> chuyển tên (tên miền) thành địa chỉ IP tương ứng và ngược lại
- Tên DNS tồn tại lâu hơn IP
- User kết nối tới các Server cục bộ bằng khái niệm đjawt tên của Internet
## 1. Thành phần chính DNS
- `DNS servers`: quản lí CSDL
- `Bộ phân giải DNS (DNS revolvers)`: DNS client
- `Các mẫu tin tài nguyên DNS (DNS resource records)`: ánh xạ giữa tên miền và địa chỉ IP trong CSDL
- `DNS zones`: 1 phần không gian tên miền, thường là miền của 1 tổ chức
## 2. Các khái niệm của DNS
- `Domain Namespace`: cơ chế đặt tên có cấu trúc, có thứ bậc
- Domain con tạo ra theo sau tên của Domain cha
- Tên của Domain con là duy nhất trong domain
### a. Nguyên tắc tạo Domain Namespace
- Hệ thống thứ cấp có từ 3 hoặc 4 mức
- Tên phải ngắn gọn, đơn giản, có ý nghĩa: A-Z, a-z, 0-9, dấu nối(-)
### b. Zones - vùng
- Là một phần không gian tên miền liên tục và được ủy quyền quản lí cho một máy chủ 
### c. Chuyển vùng
- Một vùng quản lí bởi nhiều DNS server
  - DNS server chính: quản lí CSDL
  - Các DNS server phụ: chứa bản sao của CSDL
- CSDL chính thay đổi -> quá trình nhân bản CSDL vùng xảy ra -> chuyển vùng
  - Chuyển vùng hoàn toàn (AXFR)
  - Chuyển vùng gia tăng (IXFR)
#### Name server
- Quản lí CSDL của Zone, có thể quản lí của 1 hoặc nhiều zone
- 1 Name server Chứa `Primary Zone database file` cho 1 zone -> ít nhất phải có 1 cái
- Thay đổi trên 1 zone -> thực hiện trên Name server chứa `Primary Zone database file`
- Những `Name server khác` hoạt động như `Backup Name server`
- `Cachinh Name server`: trữ lại yêu cầu phân tích tên đã giải quyết, `không quản lí zone`
#### Các mẫu tin tài nguyên DNS (DNS resource records)
- Cung cấp thông tin về CSDL DNS, cho biết tên miền, địa chỉ Ip gắn với tên, cách xử lí đối với tên miền, lưu trong các file CSDL của DNS
- Khi 1 zone mới được tạo ra -> DNS thêm `2 Resource Record` vào Zone: 
  - `Start of Authority - SOA`: thành phần duy nhất mỗi tập tin CSDL DNS gồm thông tin về `zone transfer` và `domain trên DNS server`
  - `Name server - NS`: chứa địa chỉ IP của DNS 
- Các kiểu `Resource Records`:
  - `PTR - Pointer`: phân giải địa chỉ IP sang hostname
  - `MX record (Mail Exchange)`: xác định Mail server cho 1 domain
  - `SRV`: xác định vị trí đặc biệt trong 1 domain -> tên máy chủ, số cổng của các máy chủ cho các dịch vụ được chỉ định
  - `AAAA`: phân giải Host ra địa chỉ 128-bit IPv6
  - `Cname - Canonical Name`: xây dựng 1 tên khác trỏ vào `server hosting website`
  - `A - address`: phân giải Host ra địa chỉ 32-bit IPv4
