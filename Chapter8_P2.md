Thư điện tử(Email – Electronic Mail)![image](https://user-images.githubusercontent.com/88178841/164975582-f0681ba4-3e9b-498d-956a-bac83857a896.png)
- Gồm 3 thành phần chính:
# 1. User Agent (Mail reader)
- Soạn thư, trả lời thư, đọc thư
# 2. Mail Server
- Hộp thư (Mailbox) chứa thư gởi đến người sử dụng (thường là chưa đọc)
- Hàng đợi chứa thư sẽ được gửi đi
- Trao đổi giữa các máy chủ mail
  - `Client`: máy chủ thực hiện việc gửi thư
  - `Server`: msdy chủ thực hiện việc nhận  
# 3. Mail Protocols
## SMTP - Simple Mail Transfer Protocol [RFC ]
- Sử dụng TCP: Client -> Server, port 25
- Chuyển mail trực tiếp: Sending Server to Receiving Server
- Chuyển qua 3 giai đoạn:
  - `Handshaking (greeting)`: Bắt tay
  - `Transfer of messages`: truyền thư
  - `Closure`: đóng kết nối
- Tương tác theo kiểu ` command/response`:
  - Command: ASCII text
  - Response: status code & phrase
- Thông điệp mã hóa dưới dạng `7-bit ASCII` 
