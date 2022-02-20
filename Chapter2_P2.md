# Mô hình tham khảo OSI (Open System Interconnection Model)
- Thành lập 1947, đưa ra các tiêu chuẩn quốc tế thuộc mọi lĩnh vực
- Dựa trên cách tiếp cận phân tầng 
- Mỗi tầng đảm nhận 1 số chức năng cơ bản
- Gồm 7 tầng

![image](https://user-images.githubusercontent.com/88178841/154833859-e583695e-bc03-4c21-b618-e976084d9e02.png)
## 1. Tầng ứng dụng (Application layer) - tầng 7
- Giao tiếp người và môi trường mạng
- Phương tiện cho người dùng truy nhập các thông tin, dữ liệu trên mạng thông qua chương trình ứng dụng
- Tầng giao diện chính -> user tương tác với chương trình ứng dụng -> qua đó với mạng
- User phát triển, định nghĩa các giao thức của ứng dụng: HTTP, SMTP, POP, IMAP,..
## 2. Tầng trình bày (Presentation layer) - tầng 6
- Chuyển đổi cú pháp dữ liệu để đáp ứng yêu cầu truyền thông của các ứng dụng
- Chuẩn hóa dữ liệu trao đổi giữa các hệ thống khác nhau -> đảm bảo có thể trao đổi dữ liệu (nhiệm vụ)
- Mã hóa và nén thông tin thực hiện ở tầng này.
## 3. Tầng giao dịch (Session layer) - tầng 5
- Quản lý các cuộc liên lạc giữa các thực thể bằng cách thiết lập, duy trì, đồng bộ hóa và hủy bỏ các phiên truyền thông giữa các ứng dụng
- Quản lí giao dịch: cho phép ứng dụng thiết lập sử dụng và xóa các kênh giao tiếp giữa chúng
- Đồng bộ hóa dữ liệu truyền, nhận -> bổ sung các điểm kiểm tra trung gian.
## 4. Tầng vận chuyển (Transport layer) - tầng 4
- Vận chuyển thông tin giữa các máy chủ (End to End). Kiểm soát lỗi và luồng dữ liệu
- Đảm bảo việc truyền toàn bộ thông điệp từ `nguồn` đến `đích`
  - Định địa chỉ dịch vụ
  - Phân đoạn (gửi) và lắp ghép (nhận)
  - Điều khiển kết nối
  - Kiểm tra các gói tin truyền nhận: mất, trùng
## 5. Tầng mạng (Network layer)
- Thực hiện chọn đường và đảm bảo trao đổi thông tin trong liên mạng với công nghệ chuyển mạch thích hợp.
- Định địa chỉ, vạch đường ......
