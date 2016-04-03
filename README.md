# Cách Sử Dụng WireShark
## Mục lục

[1.Khái Niệm] (#1)

[2.Cách Sử Dụng] (#2)

[a.Chọn Interface cần capture ] (#2a)

[b.Start, Stop, Restart Capture] (#2b)

[c.Xem gói tin] (#2c)

[d.Lọc gói tin] (#2d)

[e.Phân tích gói tin] (#2e)

[f.Theo dõi dòng TCP] (#2f)

[3.Tham Khhảo] (#3)

<a name="1"></a>
### 1.Khái Niệm
Là 1 phần mềm thu thập, phân tích, giám sát các gói tin truyền trên mạng.

<a name="2"></a>
### 2.Cách Sử Dụng

<a name="2a"></a>
#### a.Chọn Interface cần capture
<img src="http://i.imgur.com/Qkf2FSy.png" />

- Sau khi chọn Interface sẽ hiện ra 1 box cho bạn tùy chọn, bạn nên để mặc định.

<a name="2b"></a>
#### b.Start, Stop, Restart Capture
- Vào Capture rồi chọn các tùy chọn hoặc có thể bấm thằng cá biểu tượng trên thanh công cụ.
- Phím tắt: Start và Stop (Ctrl + E), Restart (Ctrl + R)

<img src="http://i.imgur.com/JuqmEji.png" />

- Chương trình sẽ tự động tìm, dò, bắt và phân tích gói tin.
- Mỗi gói tin sẽ tương ứng với 1 frame, mỗi frame có màu tương ứng với protocol của nó.

<img src="http://i.imgur.com/X28AZjd.png" />

<a name="2c"></a>
#### c.Xem gói tin
- Click vào gói tin tương ứng, hoặc chuột phải chọn "Show Packet in new Window"
- VD: ta xem gói tin 4960

<img src="http://i.imgur.com/SJUzBLw.png" />

- Có các thông tin về Frame, Ethernet, IP, UDP, data

<a name="2d"></a>
#### d.Lọc gói tin
- Biểu thức: [not] primitive [and|or [not] primitive …]
- Viết tắt tiếng anh:eq, ne, gt, lt, ge, le ...
- Cú pháp của c: ==, !=, >, <, >=, <= ...
- Bạn cũng có thể lọc nhiều tham số cùng 1 lúc bằng cách dùng and,or ...
- Nhập biểu thức vào ô Filter hoặc mở trong tùy chọn Capture.
VD:tìm các gói tin chạy giao thức UDP, muốn hủy điều kiện đi bấm clear

<img src="http://i.imgur.com/JzptP3z.png" />

- Ngoài ra bạn có thể lọc gói tin trên chính những thông tin của gói tin.
VD:
- Chọn 1 gói tin bất kì
- Vào xem thông tin của gói tin và chọn 1 thông tin bất kì để lọc.
- Ở đây, tôi sẽ ví dụ chọn những gói tin có source:192.168.1.33 và des:212.129.37.161

<img src="http://i.imgur.com/fui2FrM.png" />

<a name="2e"></a>
#### e.Phân tích gói tin
- Mỗi thông tin về Frame:Ethernet, IP, UDP hay data sẽ tương ứng với đoạn hexa riêng.
- Bạn có thể vào từng thông tin để xem chi tiết về nó.

VD:Ethernet

<img src="http://i.imgur.com/4wNgu2I.png" />

VD:IP

<img src="http://i.imgur.com/9TxwmfP.png" />

<a name="2f"></a>
##### f.Theo dõi dòng TCP
- Chuột phải vào gói tin và chọn "follow TCP stream"
- Sau đó sẽ hiện ra 1 đoạn mã ASCII, bạn close nó đi.
- Hiện ra sự trao đổi qua lại giữa 2 IP.

<img src="http://i.imgur.com/CK99EsN.png" />

<a name="3"></a>
3.Tham Khảo:
- http://giaoan.violet.vn/present/show/entry_id/9542849

