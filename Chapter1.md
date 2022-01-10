# I. Mạng điện báo
## Sơ lược
- Sử mã `Morse` (sử dụng 2 tín hiệu  `tic` (•) và `te` (**-**) để mã hóa dữ liệu truyền đi.
- Đây là 1 dạng mã nhị phân
- Sử dụng 1 chuỗi `tic` & `te` không đều nhau
  - -> Đơn giản
  - -> Tiết kiệm băng thông
  - Giải mã phức tạp 
- Bên gửi mã hóa lần lượt ký tự của mã
- Bên nhận thực hiện giải mã
## Cấu trúc
- Gồm 2 thành phần, nối bằng hệ thống dây dẫn truyền
  - Trạm điện báo `Telegraph Station`: cho phép truyền và nhận các thông điệp dạng mã `Morse`
  - Trạm chuyển điện báo `Telegraph Switching`: cho phép nhiều `trạm điện báo` sử dụng chung 1 đường truyền.
> Tại `trạm chuyển điện báo` 1 thao tác viên nhận các điện báo gửi tới, xác định nơi cần chuyển tới `trạm điện báo`.

> Đường truyền nơi nhận đang được sử dụng -> thao tác viên sẽ lưu lại và truyền đi khi đường truyền rãnh.
## Cải thiện
- Để tăng tốc độ truyền tin:
  - Hệ thống `Baudot` thay thế mã `Morse` bằng nhị phân `5bits` (có thể mã hóa cho 32 ký tự)
  - `Trạm điện báo` thay bằng `máy teletype terminal`
  - Hệ thống sử dụng kỹ thuật biến điệu `Modulation` và đa hợp `Multiplexing` để truyền tải thông 
# II. Mạng điện thoại
## Giới thiệu
- Truyền thông tin dưới dạng `âm thanh`
## Hoạt động
- Là mạng chuyển mạch `(Circuit Switching)` định hướng kết nối kết
- Thiết lập `nối kết tận hiến` giữa hai bên truyền nhận
=> Thiết lập kết nối trước khi thông tin được truyền 
# III. Mạng hướng đầu cuối
# IV. Mạng máy tính
## 1. Cấu trúc mạng máy tính
### a. Rìa của mạng (Network edge)
### b. Truy cập mạng (Physical media)
### c. Lõi của mạng (Network core)
