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
=> Thiết lập kết nối trước khi thông tin được truyền đi

![image](https://user-images.githubusercontent.com/88178841/148788217-d34e3aa2-fcde-4991-b03d-01478b971c4e.png)
# III. Mạng hướng đầu cuối
## Giới thiệu
- Mạng của các máy tính lớpn `Main Frame`
- Máy tính có khả năng xử lí lớn
- Kết nối các thiết bị đầu/cuối
- Kết nối thông qua `mạng cục bộ`
- Sử dụng công cụ truy cập từ xa
## Hoạt động
- 1 máy chủ mạnh `Host` có khả năng tính toán cao, nối kết với nhiều thiết bị đầu cuối `Dumb Terminal`
-> Xuất nhập thông tin & giao tiếp với người 

![image](https://user-images.githubusercontent.com/88178841/148789804-db7458b9-b14c-4098-8ed9-ee8f825cfbdc.png)

# IV. Mạng máy tính
- Là mạng của 2 hay nhiều máy tính được nối lại với nhau bằng đường truyền vật lí theo một kiến trúc nào đó.
![image](https://user-images.githubusercontent.com/88178841/148792310-f6f8e1a0-5b1d-49c4-9bf6-27766ebb166f.png)
![image](https://user-images.githubusercontent.com/88178841/148792352-b8fa7e13-b7d8-44f5-8cab-c174ab50739c.png)

## Cấu trúc mạng máy tính
- Gồm 3 thành phần
  - `Đường biên mạng (rìa của mạng)`- Network edge: các "máy chủ/trạm làm việc"(Host) và các chương trình ứng dụng mạng (Network Application)
  -  `Truy cập mạng, đường truyền vật lí` - Access Network, Physical media: các kênh truyền tải thông tin `hữu tuyến` hoặc `vô tuyến`-> Nối các đường biên
  -  `Đường trục mạng (lõi của mạng)`- Network Core: gồm hệ thống các bộ chọn đường (router) có vai trò là mạng trung tâm nối kết các mạng lại với nhau

![image](https://user-images.githubusercontent.com/88178841/148796357-28e5ac8a-5c1e-4a9c-bd04-6e147a62e4d5.png)

### Đường biên mạng (rìa của mạng)- Network edge
- Các "máy chủ/máy trạm" (Host) thực thi các chương trình ứng dụng (Network Application)
- Còn được gọi là `End System`: điểm khởi đầu và kết thúc của các dòng thông tin
- Tổ chức theo mô hình:
  - Client-Server: Mô hình khách hàng/Người phục vụ
  
![image](https://user-images.githubusercontent.com/88178841/148801962-fb875df9-0cec-491f-ae43-dd24cb5bc031.png)
  - Peer-to-peer: Mô hình ngang
 
  ![image](https://user-images.githubusercontent.com/88178841/148926476-20da7664-18f1-4fcf-9fd8-fde42be6df3f.png)

### b. Truy cập mạng (Physical media)
### c. Lõi của mạng (Network core)
