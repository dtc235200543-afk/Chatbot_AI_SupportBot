# PHẦN 5: QUẢN LÝ CHẤT LƯỢNG & RỦI RO

## 5.1. Kế hoạch quản lý chất lượng:

### 5.1.1. Mục tiêu chất lượng

Để đảm bảo chatbot \"SupportBot\" hoạt động hiệu quả và đáp ứng được kỳ
vọng của khách hàng, nhóm dự án đã xây dựng các mục tiêu chất lượng cụ
thể như sau:

  | STT | Chỉ số chất lượng           | Mục tiêu | Cách đo lường                                      | Tần suất   |
|-----|----------------------------|----------|----------------------------------------------------|------------|
| 1   | Độ chính xác của chatbot   | ≥ 85%    | (Số câu trả lời đúng) / (Tổng số câu hỏi)          | Hàng tuần  |
| 2   | Tỷ lệ hiểu sai (Fallback)  | < 15%    | (Số lần bot nói "không hiểu") / (Tổng số câu hỏi)  | Hàng tuần  |
| 3   | Thời gian phản hồi TB      | < 5 giây | Tổng thời gian / Số câu hỏi                        | Hàng ngày  |
| 4   | Tỷ lệ chuyển tiếp đúng     | 100%     | (Số yêu cầu chuyển đúng) / (Tổng số yêu cầu)       | Sau Sprint |
| 5   | Điểm hài lòng (CSAT)       | ≥ 4.0/5  | Trung bình điểm đánh giá sau mỗi chat              | Hàng tuần  |

**Nhận xét:** Các mục tiêu chất lượng được xây dựng dựa trên yêu cầu
thực tế từ phòng CSKH và khả năng kỹ thuật của nền tảng Dialogflow CX.
Mục tiêu độ chính xác 85% là hoàn toàn khả thi dựa trên các nghiên cứu
điển hình về chatbot trong lĩnh vực thương mại điện tử.

### 5.1.2. Các loại hình kiểm thử:

  |Loại kiểm thử |  Mục đích   |   Thời điểm thực hiện  | Người thực hiện | Tiêu chí đạt
  |--------------|-------------|------------------------|---------------- |---------------
 | **Unit Test** |  Kiểm tra từng Intent/Entity hoạt động đúng   |  Trong khi phát triển |  Kỹ sư AI  |  Không lỗi cú pháp, Intent kích hoạt đúng |
 |**Integration Test** |  Kiểm tra webhook kết nối được với API |   Cuối mỗi Sprint |  Tester |     Gọi API thành công, xử lý  đúng response |
 |**Accuracy Test** | Đo độ chính xác của chatbot | Cuối mỗi Sprint | Tester | Độ chính xác ≥ 85% |
 | **UAT (User Test)** | Kiểm tra bởi người dùng thực tế | Cuối Sprint 4 | 5 nhân viên CSKH | Tỷ lệ hài lòng ≥ 80% | 
 | **Load Test** | Kiểm tra khả năng chịu tải | Sprint 5 | Tester | Xử lý 500 người dùng đồng thời | 
|**Regression Test** | Đảm bảo tính năng cũ không bị ảnh hưởng | Trước mỗi release | Tester | 100% tính năng cũ hoạt động bình thường | 

**Nhận xét:** Việc kết hợp nhiều loại hình kiểm thử khác nhau giúp phát
hiện sớm các lỗi tiềm ẩn ở từng cấp độ. Đặc biệt, UAT có sự tham gia
trực tiếp của 5 nhân viên CSKH -- những người sẽ sử dụng chatbot hàng
ngày -- giúp đảm bảo sản phẩm đáp ứng đúng nhu cầu thực tế.

### 5.1.3. Kịch bản kiểm thử mẫu (Test Case)

**Test Case TC-01: Kiểm tra tra cứu đơn hàng thành công**

  | **Bước** | **Hành động của người dùng** | **Phản hồi mong đợi từ chatbot** | **Kết quả** | 
|------|-------------|------------------------|---------------- |---------------|
| 1 | User nhập: "Kiểm tra đơn hàng #12345" | Bot hỏi: "Vui lòng cung cấp số điện thoại đã đặt hàng" | Pass |
| 2 | User nhập: "0987654321" | Bot gọi API, trả về trạng thái đơn hàng chi tiết |  Pass |
| 3| Bot hiển thị trạng thái | "Đơn hàng #12345 đã được giao thành công lúc 14:30 ngày 10/06/2026" | Pass | 

**Test Case TC-02: Kiểm tra khi không tìm thấy đơn hàng**

  -------------------------------------------------------------------------
  Bước   Hành động của người     Phản hồi mong đợi từ chatbot       Kết quả
         dùng                                                       
  ------ ----------------------- ---------------------------------- -------
  1      User nhập: \"Kiểm tra   Bot hỏi: \"Vui lòng cung cấp số    Pass
         đơn hàng #99999\"       điện thoại\"                       

  2      User nhập:              API trả về không tìm thấy          Pass
         \"0987654321\"                                             

  3      Bot phản hồi            \"Rất tiếc, không tìm thấy đơn     Pass
                                 hàng #99999 với số điện thoại này. 
                                 Vui lòng kiểm tra lại.\"           
  -------------------------------------------------------------------------

**Test Case TC-03: Kiểm tra xử lý lỗi API**

  -------------------------------------------------------------------------
  Bước   Hành động của người dùng    Phản hồi mong đợi từ chatbot  Kết quả
  ------ --------------------------- ----------------------------- --------
  1      User nhập: \"Kiểm tra đơn   Bot hỏi số điện thoại         Pass
         hàng #12345\"                                             

  2      User nhập: \"0987654321\"   API timeout (giả lập)         Pass

  3      Bot phản hồi                \"Hệ thống đang bận, vui lòng Pass
                                     thử lại sau ít phút\"         
  -------------------------------------------------------------------------

Các kịch bản kiểm thử được xây dựng bao gồm cả trường hợp thành công
(happy path) và trường hợp thất bại (error path), giúp đánh giá toàn
diện khả năng xử lý của chatbot trong các tình huống khác nhau.

## 5.2. Kế hoạch quản lý rủi ro

### 5.2.1. Nhận diện rủi ro

Qua quá trình phân tích, nhóm dự án nhận diện được 8 rủi ro chính.

Về mặt kỹ thuật, rủi ro lớn nhất là dữ liệu huấn luyện không đủ tốt
(R01) -- với chỉ 10.000 dòng chat lịch sử, nhiều câu bị trùng lặp, có
thể khiến chatbot trả lời sai. Rủi ro thứ hai là API đơn hàng có thể
thay đổi (R03) khi bên đối tác không báo trước. Rủi ro thứ ba là tích
hợp API ticket thất bại (R07) do thiếu tài liệu hoặc quyền truy cập.

Về mặt kinh doanh, rủi ro nghiêm trọng nhất là chatbot trả lời sai chính
sách (R02) -- một câu trả lời sai có thể gây thiệt hại tài chính và ảnh
hưởng uy tín. Ngoài ra, người dùng có thể không hài lòng (R04) nếu bot
thường xuyên không hiểu câu hỏi.

Về tài chính và nhân sự, chi phí Dialogflow có thể vượt ngân sách (R05).
Nhân sự nghỉ ốm (R06) cũng là rủi ro cần tính đến. Cuối cùng, rủi ro bảo
mật dữ liệu khách hàng (R08) luôn hiện hữu.

  ----------------------------------------------------------------------
  ID    Rủi ro                        Loại          Điểm số   Mức độ
  ----- ----------------------------- ------------- --------- ----------
  R01   Dữ liệu huấn luyện không đủ   Kỹ thuật      20        Cao
        tốt                                                   

  R02   Chatbot trả lời sai chính     Kinh doanh    15        Cao
        sách                                                  

  R03   API đơn hàng thay đổi         Kỹ thuật      16        Cao

  R04   Người dùng không hài lòng     Trải nghiệm   16        Cao

  R05   Chi phí vượt ngân sách        Tài chính     12        Trung bình

  R06   Nhân sự nghỉ ốm               Nhân sự       6         Thấp

  R07   Tích hợp API ticket thất bại  Kỹ thuật      16        Cao

  R08   Bảo mật dữ liệu               Bảo mật       12        Trung bình
  ----------------------------------------------------------------------

  : **Bảng 1: Danh sách rủi ro và mức độ ưu tiên**

Như vậy, 5/8 rủi ro (62.5%) ở mức độ cao, cho thấy dự án có nhiều yếu tố
bất định, đặc biệt liên quan đến chất lượng dữ liệu và sự phụ thuộc vào
API bên thứ ba.

## 5.3. Kế hoạch kiểm thử UAT

Sau 4 Sprint phát triển, UAT được tổ chức với 5 nhân viên CSKH. Bảy kịch
bản được đưa ra kiểm thử: hỏi chính sách bảo hành, hỏi chính sách đổi
trả, tra cứu đơn hàng thành công, tra cứu đơn hàng thất bại, hỏi thông
tin sản phẩm, yêu cầu hỗ trợ phức tạp, và khiếu nại.

Kết quả, 6/7 kịch bản thành công (86%). Kịch bản hỏi thông tin sản phẩm
với tên sản phẩm dài và đặc biệt chưa được xử lý tốt -- lỗi này được ghi
nhận và sửa trong Sprint 5. Điểm đánh giá trung bình từ nhân viên CSKH
đạt 4.2/5. Không có lỗi nghiêm trọng nào, có 2 lỗi trung bình đều đã
được sửa trước khi triển khai.

## 5.4. Chỉ số KPIs đo lường hiệu quả

Để đánh giá thành công sau triển khai, nhóm sử dụng 7 chỉ số KPI. Tỷ lệ
giải quyết tự động (mục tiêu ≥70%) cho biết bao nhiêu câu hỏi được bot
xử lý không cần nhân viên. Độ chính xác (≥85%) và tỷ lệ hiểu sai (\<15%)
đánh giá chất lượng câu trả lời. Thời gian phản hồi (\<5 giây) đảm bảo
trải nghiệm mượt mà. CSAT (≥4.0/5) đo sự hài lòng của khách hàng. Tỷ lệ
chuyển tiếp (\<30%) cho biết bot xử lý được bao nhiêu. Chi phí mỗi hội
thoại (\<1.000 VND) đảm bảo hiệu quả kinh tế.

  -----------------------------------------------------------------------
  KPI                        Công thức                      Mục tiêu
  -------------------------- ------------------------------ -------------
  Tỷ lệ giải quyết tự động   Bot tự xử lý / Tổng số         ≥ 70%

  Độ chính xác               Số đúng / Tổng số              ≥ 85%

  Tỷ lệ hiểu sai             Fallback / Tổng số             \< 15%

  Thời gian phản hồi TB      Tổng thời gian / Số câu        \< 5 giây

  CSAT                       Trung bình điểm đánh giá       ≥ 4.0/5
  -----------------------------------------------------------------------

  : **Bảng 2: Các KPI của dự án**

## 5.5. Nhận xét chung

Kế hoạch quản lý chất lượng và rủi ro của dự án được xây dựng tương đối
toàn diện. Điểm mạnh là có quy trình kiểm thử đa cấp độ, kịch bản test
chi tiết, và UAT có sự tham gia của người dùng thực. Tuy nhiên, còn một
số điểm cần cải thiện: thiếu kiểm thử bảo mật chuyên sâu, chưa có công
cụ tự động hóa kiểm thử, và rủi ro mức độ cao chiếm tỷ lệ lớn.

Đối với các dự án tương lai, nhóm đề xuất đầu tư vào CI/CD pipeline với
kiểm thử tự động, bổ sung Security Test với chuyên gia bảo mật, và có
thêm nguồn lực để giám sát các rủi ro mức độ cao.
