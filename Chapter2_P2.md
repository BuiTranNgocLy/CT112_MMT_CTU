# Mô hình tham khảo OSI (Open System Interconnection Model)
- Thành lập 1947, đưa ra các tiêu chuẩn quốc tế thuộc mọi lĩnh vực
- Dựa trên cách tiếp cận phân tầng 
- Mỗi tầng đảm nhận 1 số chức năng cơ bản
- Gồm 7 tầng

![image](https://user-images.githubusercontent.com/88178841/154833859-e583695e-bc03-4c21-b618-e976084d9e02.png)
## 1. Tầng ứng dụng (Application layer) - tầng 7
- Phương tiện cho người dùng truy nhập các thông tin, dữ liệu trên mạng thông qua chương trình ứng dụng
- Tầng giao diện chính -> user tương tác với chương trình ứng dụng -> qua đó với mạng
- User phát triển, định nghĩa các giao thức của ứng dụng: HTTP, SMTP, POP, IMAP,..
## 2. Tầng trình bày (Presentation layer) - tầng 6
- Chuẩn hóa dữ liệu trao đổi giữa các hệ thống khác nhau -> đảm bảo có thể trao đổi dữ liệu (nhiệm vụ)
- Mã hóa và nén thông tin thực hiện ở tầng này.
## 3. Tầng giao dịch (Session layer) - tầng 5
- Quản lí giao dịch: cho phép ứng dụng thiết lập sử dụng và xóa các kênh giao tiếp giữa chúng
- Đồng bộ hóa dữ liệu truyền, nhận -> bổ sung các điểm kiểm tra trung gian.
## 4. Tầng vận chuyển (Transport layer) - tầng 4
- Đảm bảo việc truyền toàn bộ thông điệp từ `nguồn` đến `đích`
