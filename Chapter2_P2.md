# Mô hình tham khảo OSI (Open System Interconnection Model)
- Thành lập 1947, đưa ra các tiêu chuẩn quốc tế thuộc mọi lĩnh vực
- Dựa trên cách tiếp cận phân tầng 
- Mỗi tầng đảm nhận 1 số chức năng cơ bản
- Gồm 7 tầng

![image](https://user-images.githubusercontent.com/88178841/154833859-e583695e-bc03-4c21-b618-e976084d9e02.png)
## 1. Tầng ứng dụng (Application layer) - tầng 7
`Xác định giao diện giữa user và OSI`
- Giao tiếp người và môi trường mạng
- Phương tiện cho người dùng truy nhập các thông tin, dữ liệu trên mạng thông qua chương trình ứng dụng
- Tầng giao diện chính -> user tương tác với chương trình ứng dụng -> qua đó với mạng
- User phát triển, định nghĩa các giao thức của ứng dụng: HTTP, SMTP, POP, IMAP,..
## 2. Tầng trình bày (Presentation layer) - tầng 6
`Giải quyết vấn đề cú pháp, ngữ nghĩa của thông tin được truyền`
- Chuyển đổi cú pháp dữ liệu để đáp ứng yêu cầu truyền thông của các ứng dụng
- Chuẩn hóa dữ liệu trao đổi giữa các hệ thống khác nhau -> đảm bảo có thể trao đổi dữ liệu (nhiệm vụ)
- Mã hóa và nén thông tin thực hiện ở tầng này.
## 3. Tầng giao dịch (Session layer) - tầng 5
`Cho phép User trên máy khác nhau thiết lập, duy trì, đồng bộ phiên truyền thông giữa họ`
- Quản lý các cuộc liên lạc giữa các thực thể bằng cách thiết lập, duy trì, đồng bộ hóa và hủy bỏ các phiên truyền thông giữa các ứng dụng
- Quản lí giao dịch: cho phép ứng dụng thiết lập sử dụng và xóa các kênh giao tiếp giữa chúng
- Đồng bộ hóa dữ liệu truyền, nhận -> bổ sung các điểm kiểm tra trung gian.
## 4. Tầng vận chuyển (Transport layer) - tầng 4
`Chia nhỏ các Packet lớn và đánh STT trước khi gửi đi, đảm bảo truyền đúng thứ tự`
- Vận chuyển thông tin giữa các máy chủ (End to End). Kiểm soát lỗi và luồng dữ liệu
- Đảm bảo việc truyền toàn bộ thông điệp từ `nguồn` đến `đích`
  - Định địa chỉ dịch vụ
  - Phân đoạn (gửi) và lắp ghép (nhận)
  - Điều khiển kết nối
  - Kiểm tra các gói tin truyền nhận: mất, trùng
## 5. Tầng mạng (Network layer) - tầng 3
`Chọn Routing cho các Packet từ nguồn tới đích trong cùng mạng hay khác mạng`
- Thực hiện chọn đường và đảm bảo trao đổi thông tin trong liên mạng với công nghệ chuyển mạch thích hợp.
- Định địa chỉ, `vạch đường (Routing)` và `chuyển tiếp(Forwarding)` các gói tin ` nguồn -> đích`
- Kiểm tra, khắc phục nghẽn đường truyền
- Cung cấp cơ chế tính tiền thông tin vận chuyển
- Đơn vị truyền nhận dữ liệu là ` Gói tin (Packet)`

![image](https://user-images.githubusercontent.com/88178841/156939518-05732130-6440-4007-8584-cf43db03d337.png)
## 6. Tầng liên kết dữ liệu (Data link layer) - tầng 2
`Thực hiện thiết lập các liên kết, duy trì và hủy bỏ các liên kết dữ liệu. Kiểm soát lỗi và kiểm soát lưu lượng`
- Truyền tải khung dữ liệu (Frame) giữa 2 máy tính kết nối trực tiếp
- Cơ chế phát hiện xử lí lỗi
- Điều khiển luồng (Flow control)
- Giải quyết tranh chấp đường truyền

`Truyền dữ liệu giữa các thực thể mạng (truy cập đường truyền, đưa dữ liệu vào mạng). Phát hiện và sửa chữa lỗi trong tầng vật lí nếu có. Các thiết bị chuyển mạch hoạt động (Switch)`
## 7. Tầng vật lý (Physical layer) - tầng 1
- Truyền tải các bit thô (raw bit) trên kênh truyền vật lý
- Định chuẩn thiết kế:
  - Số hóa kênh truyền
  - Phương pháp truyền tải
  - CÁc kênh truyền vật lý, cấu trúc đầu nối

`Đảm bảo gửi đúng số bit bên gửi đã gửi`

![image](https://user-images.githubusercontent.com/88178841/156940353-535b63db-02ae-438e-9af3-a8be77c19df3.png)

## 8. Tóm tắt chức năng
- `Tầng 7 - Application`: 	Giao tiếp người và môi trường mạng 
- `Tầng 6 - Presentation`: Chuyển đổi cú pháp dữ liệu để đáp ứng yêu cầu truyền thông của các ứng dụng
- `Tầng 5 - Session`: Quản lý các cuộc liên lạc giữa các thực thể bằng cách thiết lập, duy trì, đồng bộ hóa và hủy bỏ các phiên truyền thông giữa các ứng dụng
- `Tầng 4 - Transpost`: Vận chuyển thông tin giữa các máy chủ (End to End). Kiểm soát lỗi và luồng dữ liệu
- `Tầng 3 - Network`: Thực hiện chọn đường và đảm bảo trao đổi thông tin trong liên mạng với công nghệ chuyển mạch thích hợp.
- `Tầng 2 - Data Link`: Tạo/gỡ bỏ khung thông tin (Frames), kiểm soát luồng và kiểm soát lỗi.
- `Tầng 1 -  Physical`: 	
Đảm bảo các yêu cầu truyền/nhận các chuỗi bit qua các phương tiện vật lý.
