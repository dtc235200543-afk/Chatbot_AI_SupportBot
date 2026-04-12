# PHẦN 7: PHÂN TÍCH QUÁ TRÌNH THỰC HIỆN

## 7.1. So sánh kế hoạch và thực tế

Dự án được thực hiện trong 10.5 tuần, chậm hơn kế hoạch 0.5 tuần. Dưới
đây là so sánh tiến độ giữa kế hoạch và thực tế cho từng Sprint.

  ---------------------------------------------------------------------------
  Sprint     Kế hoạch   Thực tế   Chênh lệch   Nguyên nhân
  ---------- ---------- --------- ------------ ------------------------------
  Sprint 1   14 ngày    16 ngày   +2 ngày      Dữ liệu FAQ bị nhiễm, phải làm
                                               sạch

  Sprint 2   14 ngày    15 ngày   +1 ngày      API đơn hàng thay đổi endpoint

  Sprint 3   14 ngày    14 ngày   0            Đúng tiến độ

  Sprint 4   14 ngày    16 ngày   +2 ngày      API ticket thiếu tài liệu

  Sprint 5   14 ngày    12 ngày   -2 ngày      Cắt bỏ tính năng phụ, tăng tốc

  **Tổng**   **70       **73      **+3 ngày**  **(chậm 0.5 tuần)**
             ngày**     ngày**                 
  ---------------------------------------------------------------------------

  : **Bảng 3: So sánh tiến độ kế hoạch và thực tế**

**Nhận xét:** Sprint 1 và Sprint 4 chậm nhất do các vấn đề liên quan đến
dữ liệu và API bên thứ ba. Sprint 5 được đẩy nhanh bằng cách cắt bỏ tính
năng gợi ý sản phẩm (US-08), giúp thu hẹp khoảng cách tiến độ.

## 7.2. Phân tích SPI và CPI

SPI (Schedule Performance Index) đo lường hiệu quả tiến độ, CPI (Cost
Performance Index) đo lường hiệu quả chi phí.

Công thức:

> **SPI = EV / PV** (giá trị đạt được / giá trị kế hoạch).
>
> **Trong đó:** SPI \> 1: vượt tiến độ, SPI \< 1: chậm tiến độ.
>
> **CPI = EV / AC** (giá trị đạt được / chi phí thực tế).
>
> **Trong đó:** CPI \> 1: tiết kiệm chi phí, CPI \< 1: vượt chi phí.

  -------------------------------------------------------------------
  Sprint      SPI        CPI        Nhận xét
  ----------- ---------- ---------- ---------------------------------
  Sprint 1    0.96       1.02       Hơi chậm, chi phí ổn

  Sprint 2    0.93       0.97       Chậm nhất, chi phí hơi vượt

  Sprint 3    1.02       1.05       Vượt tiến độ, tiết kiệm chi phí

  Sprint 4    0.95       0.95       Chậm, chi phí vượt

  Sprint 5    1.00       1.00       Đúng tiến độ, đúng chi phí

  **Trung     **0.97**   **1.00**   Hơi chậm, chi phí đúng bằng kế
  bình**                            hoạch
  -------------------------------------------------------------------

  : **Bảng 4: Biến động SPI và CPI theo Sprint**

![**Hình 7: Biến động SPI và CPI theo
tuần**](media/image1.png){width="5.7659722222222225in"
height="3.5243055555555554in"}

**Nhận xét:** Sprint 2 có SPI thấp nhất (0.93) do sự cố API đơn hàng.
Sprint 4 có CPI thấp nhất (0.95) do phát sinh chi phí làm việc với đối
tác tích hợp API ticket. Nhờ Sprint 3 và Sprint 5 hoạt động tốt, các chỉ
số trung bình của dự án ở mức chấp nhận được.

## 7.3. Các sự kiện quan trọng trong quá trình thực hiện

- **Sự kiện 1 (Tuần 2): Dữ liệu FAQ bị nhiễm**

Trong Sprint 1, khi kiểm thử độ chính xác của chatbot, nhóm phát hiện
chỉ số chỉ đạt 72%, thấp hơn nhiều so với mục tiêu 90%. Nguyên nhân là
dữ liệu 10.000 dòng chat lịch sử có nhiều câu trùng lặp và dữ liệu
nhiễu. Nhóm đã họp khẩn và quyết định kéo dài Sprint 1 thêm 2 ngày để
làm sạch dữ liệu. Kết quả, độ chính xác tăng lên 91%, nhưng tiến độ bắt
đầu chậm từ sớm.

- **Sự kiện 2 (Tuần 5): API đơn hàng thay đổi**

Đang trong Sprint 2, webhook gọi API đơn hàng bỗng nhiên báo lỗi. Bên
đối tác (phòng Kỹ thuật) đã thay đổi endpoint mà không báo trước. Rất
may, nhóm đã có phương án dự phòng: webhook được thiết kế với cơ chế
versioning. Chỉ mất 4 giờ để cập nhật sang endpoint mới. Nếu không có
phương án dự phòng, Sprint 2 có thể chậm 3-4 ngày.

- **Sự kiện 3 (Tuần 8): API ticket thiếu tài liệu**

Khi bắt đầu tích hợp API ticket ở Sprint 4, nhóm phát hiện API không có
tài liệu hướng dẫn và thiếu quyền truy cập. Phải mất 3 ngày làm việc với
bên đối tác để có được tài liệu và quyền truy cập. Để bù tiến độ, nhóm
quyết định cắt bỏ tính năng \"gợi ý sản phẩm tương tự\" (US-08) - một
tính năng phụ không quan trọng.

## 7.4. Quyết định quản lý quan trọng

  ------------------------------------------------------------------------
  Thời     Quyết định                       Tác động
  điểm                                      
  -------- -------------------------------- ------------------------------
  Tuần 2   Kéo dài Sprint 1 thêm 2 ngày để  Độ chính xác tăng từ 72% lên
           làm sạch dữ liệu                 91%, nhưng chậm tiến độ

  Tuần 5   Áp dụng webhook versioning để    Giảm thời gian khắc phục từ
           ứng phó API thay đổi             3-4 ngày xuống 4 giờ

  Tuần 8   Cắt bỏ tính năng gợi ý sản phẩm  Giúp Sprint 5 tăng tốc, thu
           (US-08)                          hẹp khoảng cách tiến độ

  Tuần 10  Không sử dụng hết chi phí dự     Tiết kiệm được 4 triệu, bù vào
           phòng                            các khoản vượt khác
  ------------------------------------------------------------------------

  : **Bảng 5: Các quyết định quản lý và tác động**

## 7.5. Xử lý thay đổi

Trong quá trình thực hiện, có hai yêu cầu thay đổi chính:

- **Thay đổi 1:** API đơn hàng thay đổi endpoint ( từ /api/v1/orders
   sang 

> /api/v2/orders ). Nhóm đã xử lý bằng cách cập nhật webhook, mất 4 giờ.
> Không phát sinh thêm chi phí.

- **Thay đổi 2:** Cắt bỏ tính năng gợi ý sản phẩm (US-08) do không đủ
  thời gian. Quyết định này được đưa ra sau khi phân tích tác động: tính
  năng này không ảnh hưởng đến các chức năng cốt lõi, và việc cắt bỏ
  giúp tiết kiệm 2 ngày phát triển.

## 7.6. Nhận xét chung

Quá trình thực hiện dự án cho thấy:

- **Điểm mạnh:** Nhóm đã có phương án dự phòng cho rủi ro API (webhook
  versioning), giúp giảm thiểu tác động khi sự cố xảy ra. Việc cắt bỏ
  tính năng phụ đúng lúc cũng là một quyết định sáng suốt.

- **Điểm yếu:** Công tác kiểm tra dữ liệu trước khi huấn luyện chưa được
  thực hiện kỹ, dẫn đến mất thời gian làm sạch dữ liệu ở Sprint 1. Việc
  phụ thuộc vào API bên thứ ba (API đơn hàng, API ticket) là rủi ro lớn
  nhất của dự án.

- **Cải tiến cho dự án sau:** Cần có \"Sprint 0\" để kiểm tra dữ liệu,
  và cần có \"API Contract Testing\" để phát hiện sớm thay đổi từ API
  bên thứ ba.
