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
- Còn được gọi là `End System`: điểm khởi đầu và kết thúc của các dòng thông tin với ý nghĩa đây chính là nơi xuất phát của thông tin di chuyển trên mạng, cũng như là điểm dừng của thông tin.
- Quá trình trao đổi thông tin giữa 2 máy tính trên mạng tổ chức theo mô hình:
  - `Client-Server`: Mô hình khách hàng/Người phục vụ
-> 1 máy Client; 1 máy Server. Client gửi yêu cầu đến máy tính Server yêu cầu Server thực hiện công việc.

![image](https://user-images.githubusercontent.com/88178841/148801962-fb875df9-0cec-491f-ae43-dd24cb5bc031.png)

  - `Peer-to-peer`: Mô hình ngang
 -> 1 máy tính vừa là Client vùa là Server. Một số ứng dụng như: [Gnutella](https://filegi.com/tech-term/gnutella-92/), KaZaA.
 
  ![image](https://user-images.githubusercontent.com/88178841/148926476-20da7664-18f1-4fcf-9fd8-fde42be6df3f.png)

### Truy cập mạng, đường truyền vật lí - Access Network, Physical media
- Kết `nối các máy tính` (host - end system) `vào` các `Router ngoài biên` (Edge Router)
### Đường trục mạng (lõi của mạng)- Network Core
- Là hệ thống mạng của các bộ chọn đường (Routers),
- Nhiệm vụ chọng đường và chuyển tiếp thông tin, đảm bảo sự trao đổi thông tin thông suốt giữa 2 máy tính nằm trên hai nhánh mạng cách xa nhau.
- Sử dụng `2 chế độ truyền tin`:
    `Chuyển mạch (Circuit switching)`
   - `Chuyển gói (Packet switching` sử dụng chủ yêu trên Internet
## Mạng chuyển mạch (Circuit switching network):
- Thiết lập kênh truyền tận hiến giữa 2 bên truyền nhận.
- Hoạt động theo mô hình `hệ thống điện thoại`. Có thể giao tiếp với máy B, máy A `phải` thực hiện 1 cuộc gọi. Nếu máy B chấp nhận cuộc gọi -> 1 kênh ảo được thiết lập dành riêng A & B trao đổi thông tin. Ngắt kết nối sau khi đã kết nối xong.
- `Tất cả tài nguyên` được cấp cho cuộc gọi này: băng thông đường truyền khả năng của các bộ hoán chuyển thông tin đều `dành riêng` cho cuộc gọi này, `không được chia sẻ`
- Phân chia băng thông bằng 2 phương pháp:
  - Phân chia theo tần số (FDMA-Frequency Division Multi Access)
  - Phân chia theo thời gian (TDMA- Time Division Multi Access) 
![image](https://user-images.githubusercontent.com/88178841/149615013-f9ef77bc-f560-4fa0-bae7-0d1f7ca21fdf.png)

## Mạng chuyển gói (Packet switching network)
- Thông tin truyền đi được chia thành các gói tin (Packets)
- Các gói tin của Host khác nhau `cùng chia sẻ tài nguyên mạng`
- Giải quyết `nghẽn mạch` -> sử dụng kỹ thuật `lưu & chuyển tiếp (Store and forward)`
- Gói tin của những người dùng khác nhau sẽ `chia sẻ` băng thông của kênh truyền. Mỗi gói tin `sử dụng toàn bộ băng thông` của kênh truyền khi được cho phép -> lượng thông tin cần truyền đi vượt quá khả năng đáp ứng kênh truyền (nghẽn mạch) -> Router sử dụng giải thuật Store & Forward (`lưu` lại các `gói tin chưa gửi đi` được vào `hàng đợi` chờ cho đến khi kênh truyền trống chúng sẽ lần lượt được gửi)

![image](https://user-images.githubusercontent.com/88178841/149615515-0a0fd3c2-ccb3-41ae-a695-2ae7916be957.png)

## So sánh Mạng chuyển mạch và mạng chuyển gói
![image](https://user-images.githubusercontent.com/88178841/149615579-2a5c2b45-26f9-4f64-8a17-d2ab96703e53.png)

- Ví dụ: 1 đường truyền 1Mbit, mỗi người dùng được cấp 100Kbps khi truy cập "active", thời gian "active" chiếm 10% tổng thời gian. Khi đó:
   -  Circuit-switching: cho phép tối đa 10 users
   -  Packet-switching: cho phép tối đa 35 

> Mạng chuyển gói:
>   -  Thích hợp lưu lượng thông tin lớn, cơ chế chia sẻ tài nguyên & không cần thiết lập kết nối
>   Cần cơ chế điều khiến tắt nghẽn và mất dữ liệu
>   Khó đảm bảo băng thông cố định cho các ứng dụng đa phương tiện.
