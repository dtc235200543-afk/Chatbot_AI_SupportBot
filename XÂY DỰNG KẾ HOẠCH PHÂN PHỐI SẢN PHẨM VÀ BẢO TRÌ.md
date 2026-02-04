**4. XÂY DỰNG KẾ HOẠCH PHÂN PHỐI SẢN PHẨM VÀ BẢO TRÌ**

**4.1. Mục tiêu phân phối sản phẩm**

- Đảm bảo sản phẩm được bàn giao đúng phiên bản đã thống nhất trong phạm
  vi dự án.

- Đảm bảo sản phẩm có thể triển khai, vận hành ổn định và dễ bảo trì.

- Đảm bảo khách hàng/người dùng cuối có khả năng sử dụng hệ thống sau
  khi bàn giao.

**4.2. Công cụ hỗ trợ phân phối và quản lý phiên bản**

Nhóm sử dụng **GitHub** làm công cụ chính để:

- Quản lý mã nguồn tập trung.

- Theo dõi tiến độ phát triển thông qua Issues và Pull Requests.

- Quản lý phiên bản sản phẩm thông qua các bản Release.

**4.3. Quy trình phân phối sản phẩm (Deployment Plan)**

**Bước 1: Chuẩn bị trước khi phân phối**

- Kiểm tra toàn bộ mã nguồn trên nhánh main.

- Đảm bảo tất cả Issues quan trọng đã được đóng (Closed).

- Kiểm tra lịch sử commit để xác nhận không còn lỗi nghiêm trọng.

- Tổng hợp tài liệu hướng dẫn sử dụng và tài liệu kỹ thuật.

**Bước 2: Đóng gói và phát hành sản phẩm**

- Tạo **Release trên GitHub** với:

  - Tên phiên bản

  - Mô tả các chức năng đã hoàn thành.

- Đính kèm:

  - Source code.

  - File hướng dẫn cài đặt (README.md).

**Bước 3: Bàn giao và chuyển giao**

- Chuyển giao repository GitHub cho khách hàng/giảng viên.

- Giải thích cấu trúc source code và cách triển khai.

- Hướng dẫn cách sử dụng Issues để báo lỗi hoặc yêu cầu cải tiến.

**4.4. Đào tạo người dùng cuối**

- Hướng dẫn sử dụng các chức năng chính của hệ thống.

- Hướng dẫn thao tác cơ bản thông qua tài liệu hoặc demo trực tiếp.

- Giải thích quy trình phản hồi lỗi thông qua GitHub Issues.

**4.5. Kế hoạch bảo trì sản phẩm**

**4.5.1. Các loại hình bảo trì**

- **Bảo trì sửa lỗi (Corrective Maintenance):**

  - Sửa các lỗi phát sinh trong quá trình sử dụng.

- **Bảo trì cải tiến (Adaptive/Perfective Maintenance):**

  - Cải thiện hiệu năng, giao diện, hoặc bổ sung tính năng mới.

**4.5.2. Quy trình bảo trì**

1.  Người dùng tạo Issue trên GitHub.

2.  Nhóm phân loại Issue (bug / enhancement).

3.  Phân công thành viên xử lý.

4.  Cập nhật trạng thái Issue cho đến khi hoàn thành.

**4.5.3. SLA giả định (Service Level Agreement)**

- Thời gian phản hồi Issue: ≤ 24 giờ.

- Thời gian xử lý lỗi nghiêm trọng: ≤ 48 giờ.

- Thời gian xử lý lỗi thông thường: ≤ 5 ngày làm việc.

**5. ÁP DỤNG KỸ NĂNG MỀM TRONG QUẢN LÝ XUNG ĐỘT VÀ TẠO ĐỘNG LỰC**

**5.1. Nhận diện vấn đề trong nhóm**

Trong quá trình thực hiện dự án, nhóm gặp một số vấn đề liên quan đến
con người như:

- Bất đồng về phương án kỹ thuật.

- Một số thành viên chậm tiến độ so với kế hoạch.

- Áp lực deadline gây giảm động lực làm việc.

**5.2. Tình huống xung đột cụ thể**

Hai thành viên trong nhóm có ý kiến trái ngược về cách tổ chức cấu trúc
mã nguồn trên GitHub, dẫn đến tranh luận kéo dài và ảnh hưởng đến tiến
độ chung.

**5.3. Giải pháp xử lý xung đột**

Nhóm áp dụng các kỹ năng mềm đã học:

- **Lắng nghe tích cực:** Mỗi thành viên trình bày quan điểm kỹ thuật
  của mình.

- **Thảo luận dựa trên dữ liệu:** So sánh ưu/nhược điểm của từng phương
  án.

- **Thống nhất chung:** Chọn phương án phù hợp nhất với mục tiêu dự án.

- **Phân công rõ ràng:** Giao trách nhiệm cụ thể để tránh mâu thuẫn lặp
  lại.

**5.4. Tạo động lực và duy trì sự gắn kết**

- Công khai tiến độ trên GitHub để mọi thành viên theo dõi.

- Ghi nhận đóng góp của từng thành viên thông qua commit và Issues.

- Chia nhỏ công việc giúp giảm áp lực và tăng hiệu quả.

- Khuyến khích trao đổi thường xuyên thông qua họp nhóm ngắn.

**6. ĐÁNH GIÁ KẾT QUẢ DỰ ÁN (MÔ PHỎNG)**

**6.1. Đánh giá theo tam giác quản lý dự án**

**6.1.1. Phạm vi**

- Hoàn thành đầy đủ các chức năng đã đề ra ban đầu.

- Không phát sinh yêu cầu ngoài phạm vi nghiêm trọng.

**6.1.2. Thời gian**

- Dự án hoàn thành đúng tiến độ theo kế hoạch.

- Một số task nhỏ bị trễ nhưng không ảnh hưởng tổng thể.

**6.1.3. Chi phí**

- Dự án học tập nên không phát sinh chi phí thực tế.

- Nguồn lực được sử dụng hiệu quả.

**6.2. Đánh giá theo KPIs**

|                            |              |             |
|----------------------------|--------------|-------------|
| **KPI**                    | **Mục tiêu** | **Kết quả** |
| Hoàn thành chức năng chính | 100%         | Đạt         |
| Số Issue được xử lý        | ≥ 90%        | Đạt         |
| Tỷ lệ đúng deadline        | ≥ 85%        | Đạt         |
| Mức độ phối hợp nhóm       | Tốt          | Tốt         |

**6.3. Lessons Learned (Bài học kinh nghiệm)**

- Cần thống nhất quy ước làm việc trên GitHub ngay từ đầu.

- Chia nhỏ công việc giúp kiểm soát tiến độ tốt hơn.

- Giao tiếp thường xuyên giúp giảm xung đột và hiểu lầm.

- Việc theo dõi tiến độ bằng công cụ giúp dự án minh bạch và hiệu quả
  hơn.
