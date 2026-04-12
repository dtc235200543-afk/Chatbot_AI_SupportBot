# PHẦN 8: ĐÁNH GIÁ KẾT QUẢ & BÀI HỌC KINH NGHIỆM

## 8.1. Kết quả đạt được so với mục tiêu

Dự án kết thúc sau 10.5 tuần (chậm 0.5 tuần), chi phí thực tế
168.200.000 VND (vượt 8.9% so với dự kiến 154.400.000 VND). Các chỉ số
chất lượng đều đạt hoặc vượt mục tiêu.

 | Mục tiêu       |       Kế hoạch  |  Thực tế  |   Kết luận |
 | --------------------- | ----------- | ----------- | ----------------------- |
  | Thời gian |	10 tuần |	10.5 tuần |	Chậm 0.5 tuần |
| Chi phí |	154.4 triệu	| 168.2 triệu |	Vượt 8.9% |
| Độ chính xác |	≥ 85% |	87.3% |	Đạt |
| Tỷ lệ hiểu sai |	< 15%	 |  12.7% |	Đạt |
| Thời gian phản hồi | 	< 5 giây |	3.2 giây |	Đạt |
| CSAT |	≥ 4.0 |	4.2 |	Đạt |
| Tỷ lệ giải quyết tự động |	≥ 70% |	67% |	Chưa đạt (95.7% mục tiêu) |


  : **Bảng 6: So sánh mục tiêu và kết quả thực tế**

**Nhận xét:** Dự án thành công ở các chỉ số chất lượng, nhưng chậm tiến
độ và vượt ngân sách nhẹ. Tỷ lệ giải quyết tự động chưa đạt mục tiêu do
một số khách hàng vẫn thích gọi điện thoại thay vì sử dụng chat.

## 8.2. Phân tích chênh lệch chi phí

|  Hạng mục |   Dự kiến |   Thực tế  |  Chênh lệch | Nguyên nhân |
 | ---------- | ---------- | ---------- | ----------- | ---------------------------- |
 | Hệ thống |	11 triệu	| 13 triệu |	+2 triệu |	Tăng dung lượng VPS do lưu lượng test cao |
| Vận hành |	33.4 triệu |	31 triệu |	-2.4 triệu |	Tiết kiệm điện, internet |
| Nhân công |	110 triệu |	124.2 triệu |	+14.2 triệu |	Kéo dài 0.5 tuần + phát sinh ngoài giờ |
| Tổng |	154.4 triệu |	168.2 triệu |	+13.8 triệu |	Vượt 8.9% |

  : **Bảng 7: So sánh chi phí dự kiến và thực tế**

Chi phí nhân công tăng nhiều nhất do dự án kéo dài thêm 0.5 tuần và phát
sinh làm thêm giờ ở Sprint 2 (sự cố API) và Sprint 4 (tích hợp API
ticket). Chi phí hệ thống tăng nhẹ do phải nâng cấp VPS để đáp ứng lưu
lượng test cao hơn dự kiến.

## 8.3. Đánh giá từ các bên liên quan

  ------------------------------------------------------------------------
  Bên liên quan      Kỳ vọng                     Mức độ đáp ứng
  ------------------ --------------------------- -------------------------
  Nhà tài trợ (Ban   ROI trong 6 tháng, giảm chi Đạt (chi phí CSKH giảm
  Giám đốc)          phí CSKH                    40% sau 2 tháng)

  Khách hàng (Phòng  Bot trả lời chính xác, giảm Rất hài lòng (giảm 67%
  CSKH)              tải                         câu hỏi đơn giản)

  Đội dự án          Hoàn thành đúng hạn, tích   Hài lòng (dù chậm 0.5
                     lũy kinh nghiệm             tuần)

  Người dùng cuối    Được hỗ trợ nhanh chóng     CSAT 4.2/5
  ------------------------------------------------------------------------

  : **Bảng 8: Đánh giá từ góc nhìn các bên**

Phòng CSKH đánh giá rất cao vì bot đã giảm được 67% câu hỏi đơn giản,
giúp nhân viên tập trung vào các yêu cầu phức tạp. Ban Giám đốc hài lòng
với hiệu quả giảm chi phí, nhưng đề nghị cải thiện thời gian triển khai
cho các dự án sau.

## 8.4. Phân tích quá trình thực hiện

### 8.4.1. Các sự kiện quan trọng

**Sự kiện 1 (Tuần 2):** Phát hiện dữ liệu FAQ bị nhiễm, nhiều câu trùng
lặp, độ chính xác chỉ đạt 72%. Nhóm quyết định kéo dài Sprint 1 thêm 2
ngày để làm sạch dữ liệu. Kết quả: độ chính xác tăng lên 91%, tiến độ
chậm 2 ngày.

**Sự kiện 2 (Tuần 5):** API đơn hàng thay đổi endpoint không báo trước.
Nhóm áp dụng phương án dự phòng (webhook versioning), khắc phục trong 4
giờ. Sprint 2 chỉ chậm 1 ngày thay vì 3-4 ngày.

**Sự kiện 3 (Tuần 8):** API ticket không có tài liệu đầy đủ, mất 3 ngày
làm việc với đối tác. Nhóm quyết định cắt bỏ tính năng gợi ý sản phẩm để
bù tiến độ.

### 8.4.2. Phân tích SPI và CPI

  -------------------------------------------------------------------
  Sprint   SPI (Tiến độ)  CPI (Chi phí)  Nhận xét
  -------- -------------- -------------- ----------------------------
  Sprint 1 0.96           1.02           Hơi chậm do làm sạch dữ liệu

  Sprint 2 0.93           0.97           Chậm nhất do sự cố API

  Sprint 3 1.02           1.05           Bắt kịp tiến độ

  Sprint 4 0.95           0.95           Chậm do API ticket, chi phí
                                         tăng

  Sprint 5 1.00           1.00           Đúng tiến độ, đúng chi phí
  -------------------------------------------------------------------

  : **Bảng 9: Biến động SPI/CPI theo Sprint**

SPI thấp nhất ở Sprint 2 (0.93) do sự cố API đơn hàng. CPI thấp nhất ở
Sprint 4 (0.95) do phát sinh chi phí làm việc với đối tác. Nhờ cắt bỏ
tính năng phụ ở Sprint 5, dự án kịp \"gỡ lại\" một phần tiến độ.

## 8.5. Bài học kinh nghiệm

  -----------------------------------------------------------------------
  Sự kiện            Bài học                  Hành động cho dự án sau
  ------------------ ------------------------ ---------------------------
  Dữ liệu FAQ bị     Cần kiểm tra dữ liệu     Thêm \"Sprint 0\" (1 tuần)
  nhiễm              trước khi huấn luyện     chỉ để làm sạch dữ liệu

  API đơn hàng thay  API bên thứ ba rất dễ    Áp dụng contract testing,
  đổi                thay đổi                 kiểm tra API tự động mỗi
                                              ngày

  API ticket thiếu   Cần xác nhận sự sẵn sàng Lập checklist kiểm tra API
  tài liệu           của API trước Sprint     trước khi bắt đầu Sprint

  Ước lượng thời     Task tích hợp API cần    Nhân hệ số 1.5 cho các task
  gian thiếu chính   thêm thời gian dự phòng  liên quan đến API
  xác                                         

  Phải cắt bỏ tính   Cần ưu tiên chức năng    Phân loại Must have / Nice
  năng               cốt lõi từ đầu           to have rõ ràng
  -----------------------------------------------------------------------

  : **Bảng 10: Bài học và hành động cải tiến**

> 

## 8.6. Đề xuất cải tiến quy trình

Từ những bài học trên, nhóm đề xuất 4 cải tiến cho các dự án tương lai:

- **Thứ nhất,** áp dụng \"Sprint 0\" -- một tuần đầu tiên chỉ để làm
  sạch và kiểm tra dữ liệu trước khi bắt đầu các Sprint phát triển. Chi
  phí cho Sprint 0 khoảng 5-7 triệu, rẻ hơn nhiều so với việc sửa lỗi
  sau này.

- **Thứ hai,** xây dựng \"API Contract Testing\" -- một bộ kiểm tra tự
  động chạy mỗi ngày để phát hiện thay đổi từ API bên thứ ba, gửi cảnh
  báo ngay qua Slack.

- **Thứ ba,** lập \"Checklist kiểm tra API\" trước khi bắt đầu bất kỳ
  Sprint nào có tích hợp API: tài liệu có đầy đủ không, quyền truy cập
  đã có chưa, có môi trường test riêng không.

- **Thứ tư,** phân loại yêu cầu theo mô hình Must have (bắt buộc) và
  Nice to have (nếu có thì tốt). Các tính năng Nice to have chỉ được làm
  nếu còn thời gian và ngân sách. Trong dự án này, tính năng \"gợi ý sản
  phẩm\" là Nice to have và đã bị cắt bỏ đúng lúc.

## 8.7. Tổng kết

Dự án SupportBot đạt được hầu hết các mục tiêu chất lượng, với độ chính
xác 87.3% và điểm CSAT 4.2/5. Tuy nhiên, dự án chậm 0.5 tuần và vượt
ngân sách 8.9% (13.8 triệu) do các sự cố liên quan đến API bên thứ ba.

  -----------------------------------------------------------------------
  Tiêu chí                 Đánh giá
  ------------------------ ----------------------------------------------
  Chất lượng sản phẩm      Tốt (87.3% accuracy)

  Thời gian                Trung bình (chậm 0.5 tuần)

  Chi phí                  Trung bình (vượt 8.9%)

  Hài lòng khách hàng      Tốt (CSAT 4.2)

  Bài học rút ra           Nhiều giá trị, có thể áp dụng cho dự án sau
  -----------------------------------------------------------------------

  : **Bảng 11: Tổng kết đánh giá dự án**

Bài học lớn nhất là cần kiểm tra kỹ dữ liệu và API trước khi bắt đầu
phát triển. Các đề xuất cải tiến như Sprint 0, contract testing, và
checklist API sẽ được áp dụng cho các dự án chatbot tiếp theo của E-Com
Global.
