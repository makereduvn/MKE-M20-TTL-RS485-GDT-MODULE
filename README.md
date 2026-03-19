# Mạch chuyển giao tiếp MKE-M20 TTL to RS485 GDT Module

## Giới thiệu sản phẩm
Mạch chuyển giao tiếp MKE-M20 TTL to RS485 GDT Module là giải pháp lý tưởng giúp chuyển đổi tín hiệu giữa chuẩn UART TTL (vi điều khiển, máy tính nhúng, SBC,...) và chuẩn truyền thông công nghiệp RS485 hai chiều.

Sản phẩm sử dụng IC MAX13487E chính hãng Analog Devices (Maxim) tích hợp cơ chế điều khiển tự động hướng truyền (Auto Direction Control), giúp đơn giản hóa việc lập trình và tăng độ ổn định so với các dòng IC truyền thống như MAX485. Mạch hỗ trợ tốc độ truyền lên đến 500kbps, đảm bảo hiệu suất cao trong các hệ thống truyền thông công nghiệp.

Đặc biệt, Mạch chuyển giao tiếp MKE-M20 TTL to RS485 GDT Module được trang bị đầy đủ các cơ chế bảo vệ phần cứng như GDT (Gas Discharge Tube) chống sét, TVS chống ESD/xung điện áp, và cầu chì bảo vệ quá dòng, giúp hệ thống hoạt động bền bỉ và an toàn trong môi trường nhiễu cao hoặc ngoài trời.

Ngoài ra, mạch tích hợp chuyển mức logic tương thích với cả 3.3VDC và 5VDC, cho phép kết nối trực tiếp với các nền tảng phổ biến như ESP32, Arduino, Raspberry Pi mà không cần mạch phụ trợ.

## Ưu điểm nổi bật

- Sử dụng IC MAX13487E chất lượng cao từ Analog Devices (Maxim)
- Tích hợp Auto Direction Control – không cần điều khiển DE/RE bằng phần mềm
- Tốc độ truyền cao lên đến 500kbps
- Hỗ trợ kết nối đa điểm (multi-drop) trên bus RS485
- Cho phép hot-plug (cắm nóng) an toàn, hạn chế hư hỏng thiết bị
- Tích hợp mạch chuyển mức logic 3.3VDC / 5VDC
- Bảo vệ toàn diện:
  - GDT chống sét lan truyền
  - TVS chống ESD và xung điện áp
  - Cầu chì chống quá dòng, ngắn mạch
- Khoảng cách truyền xa lên đến 1.2 km
- LED hiển thị trạng thái TX/RX trực quan
- Thiết kế nhỏ gọn dễ tích hợp, phù hợp môi trường công nghiệp

## Thông số kỹ thuật

- IC chính: MAX13487E (Half-duplex RS485 Transceiver)
- Điện áp hoạt động: 5VDC
- Mức logic TTL: 3.3VDC / 5VDC
- Chuẩn giao tiếp: UART TTL ↔ RS485
- Tốc độ truyền tối đa: 500 kbps
- Khoảng cách truyền:
  - Tối đa: ~1200 m
  - Khuyến nghị: ≤ 800 m (sử dụng cáp RS485 chuyên dụng)
- Chế độ truyền: Half-duplex (2 dây)
- Tính năng IC MAX13487E:
  - Tự động điều khiển hướng truyền (Auto Direction)
  - Khả năng chống nhiễu cao
  - Bảo vệ ESD lên đến ±15kV (HBM)
  - Fail-safe receiver (ổn định khi bus hở/ngắn mạch)
- Bảo vệ phần cứng:
  - GDT (Gas Discharge Tube) chống sét
  - TVS chống xung điện áp
  - Cầu chì bảo vệ quá dòng
- Chuẩn kết nối:
  - UART TTL: XH2.54-4P
  - RS485: Terminal block 5.08mm
- Đèn báo: LED TX / RX
- Tích hợp chân nối đất (Mass) tăng chống nhiễu & chống sét tại cổng RS485.

## Lưu ý sử dụng

- Nên nối chân chân nối đất (Mass) tại cổng RS485 với hệ thống tiếp địa (nếu có) để tăng hiệu quả chống nhiễu và chống sét.
- Sử dụng cáp xoắn đôi chuyên dụng RS485 để đảm bảo chất lượng truyền tín hiệu.

## Các chân tín hiệu
<table><thead>
  <tr>
    <th>MKE-M20</th>
    <th>Ghi chú</th>
  </tr></thead>
<tbody>
  <tr>
    <td>GND</td>
    <td>Chân cấp nguồn âm 0VDC</td>
  </tr>
  <tr>
    <td>5V</td>
    <td>Chân cấp nguồn dương 5VDC</td>
  </tr>
  <tr>
    <td>TXD</td>
    <td>Chân truyền tín hiệu UART TTL</td>
  </tr>
  <tr>
    <td>RXD</td>
    <td>Chân nhận tín hiệu UART TTL</td>
  </tr>
  <tr>
    <td>B</td>
    <td>Chân tín hiệu vi sai RS485</td>
  </tr>
  <tr>
    <td>A</td>
    <td>Chân tín hiệu vi sai RS485</td>
  </tr>
  <tr>
    <td>|||</td>
    <td>Chân chân nối đất (Mass)</td>
  </tr>
</tbody>
</table>

## Hướng dẫn sử dụng

- Cấp nguồn 5VDC cho mạch thông qua hai chân 5V và GND. (lưu ý cần nối chung GND giữa mạch MKE-M20 và thiết bị sử dụng giao tiếp UART TTL)
- Kết nối giao tiếp UART TTL:
  - Chân TX của MKE-M20 → chân RX của thiết bị
  - Chân RX của MKE-M20 → chân TX của thiết bị
- Kết nối đường truyền RS485:
  - Chân A của MKE-M20 → chân A của thiết bị RS485
  - Chân B của MKE-M20 → chân B của thiết bị RS485

Để tăng khả năng chống nhiễu và chống sét, nên nối chân Mass (GND nối đất) của mạch với hệ thống tiếp địa (nếu có).

## Kích thước sản phẩm
![MKE-M20 TTL RS485 GDT](/extras/MKE-M20_1.jpg)

## Hình ảnh sản phẩm
![MKE-M20 TTL RS485 GDT](/extras/MKE-M20_2.png)
![MKE-M20 TTL RS485 GDT](/extras/MKE-M20_3.png)
