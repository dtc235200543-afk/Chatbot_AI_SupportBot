**6. Áp dụng các Chỉ số KPIs để Đo lường và Đánh giá Hiệu quả Dự án**

Trong dự án tích hợp chatbot AI "SupportBot" cho website chăm sóc khách
hàng của công ty E-Com Global, nhóm dự án sử dụng các chỉ số đo lường
hiệu quả **(Key Performance Indicators -- KPIs)** nhằm theo dõi tiến độ
thực hiện, kiểm soát chi phí và đánh giá mức độ hoàn thành các mục tiêu
đã đề ra.

Việc áp dụng KPIs giúp nhóm có cơ sở định lượng rõ ràng để đánh giá tình
trạng triển khai dự án theo từng giai đoạn, đồng thời hỗ trợ việc ra
quyết định quản lý và điều chỉnh kế hoạch kịp thời.

**6.1. Xác định các KPIs chính của dự án**

Dựa trên mục tiêu và phạm vi của dự án, nhóm xác định hệ thống KPIs phù
hợp và chia thành hai nhóm chính:

- KPIs đánh giá hiệu quả hệ thống chatbot

- KPIs đánh giá tiến độ và chi phí dự án

**6.1.1. KPIs đánh giá hiệu quả hệ thống chatbot**

- **Tỷ lệ tự động hóa (Automation Rate):**

Đo lường tỷ lệ câu hỏi của khách hàng được chatbot xử lý hoàn toàn mà
không cần sự hỗ trợ của nhân viên chăm sóc khách hàng, phản ánh mức độ
giảm tải cho bộ phận CSKH.

- **Độ chính xác nhận diện ý định (Intent Recognition Accuracy):**

Đo lường tỷ lệ chatbot nhận diện đúng ý định của người dùng. Theo yêu
cầu phi chức năng của dự án, độ chính xác mục tiêu ở giai đoạn triển
khai ban đầu là tối thiểu 85%.

- **Tỷ lệ chuyển tiếp hội thoại (Escalation Rate):**

Đo lường tỷ lệ các cuộc hội thoại chatbot không xử lý được và phải
chuyển sang nhân viên hỗ trợ, qua đó đánh giá khả năng xử lý các yêu cầu
phức tạp của hệ thống.

- **Mức độ hài lòng của khách hàng (Customer Satisfaction Score --
  CSAT):**

Được thu thập thông qua khảo sát sau mỗi phiên trò chuyện, phản ánh trải
nghiệm thực tế của người dùng đối với chatbot SupportBot.

**6.1.2. KPIs đánh giá tiến độ và chi phí dự án**

Bên cạnh các KPIs đánh giá chất lượng hoạt động của chatbot, nhóm dự án
cũng sử dụng các chỉ số nhằm theo dõi tiến độ thực hiện và hiệu quả sử
dụng chi phí của dự án, bao gồm:

- **Planned Value (PV):** Giá trị công việc theo kế hoạch tại một thời
  điểm.

- **Earned Value (EV):** Giá trị của khối lượng công việc thực tế đã
  hoàn thành.

- **Actual Cost (AC):** Chi phí thực tế đã sử dụng.

- **Schedule Performance Index (SPI):** Chỉ số đánh giá mức độ tuân thủ
  tiến độ.

- **Cost Performance Index (CPI):** Chỉ số đánh giá hiệu quả sử dụng chi
  phí.

**6.2. Áp dụng các chỉ số EV, PV, AC, SPI và CPI**

Nhóm áp dụng phương pháp **Earned Value Management (EVM)** để đánh giá
tiến độ và chi phí của dự án tại **thời điểm kết thúc Sprint 1 (tuần thứ
6/12)**, phù hợp với báo cáo tiến độ của dự án.

**6.2.1. Dữ liệu đầu vào**

Tại thời điểm kết thúc Sprint 1, các thông số được xác định như sau:

- BAC (Budget at Completion): Tổng ngân sách dự án = 45 triệu VNĐ

- PV (Planned Value):\
  **Tiến độ theo kế hoạch:** 100% khối lượng công việc của Sprint 1\
  ![](Bảng1.4.png)\
  → **PV = 100% × 45 = 45 triệu VNĐ**

- EV (Earned Value):\
  **Tiến độ thực tế:** 85% khối lượng công việc của Sprint 1
  ![](media/Bảng1.4.png){width="4.781917104111986in"
  height="0.6667596237970254in"}\
  → **EV = 85% × 45 = 38,25 triệu VNĐ**

<!-- -->

- **AC (Actual Cost):** Chi phí thực tế đã sử dụng = **42,3 triệu VNĐ**

**6.2.2. Tính toán và phân tích chỉ số SPI**

Công thức: ![](media/media/image3.png){width="1.156411854768154in"
height="0.5834142607174103in"}

Trong đó:

EV (Earned Value): Giá trị công việc đã hoàn thành.\
PV (Planned Value): Giá trị công việc dự kiến hoàn thành theo kế hoạch.\
SPI đo lường tiến độ của dự án. Nếu SPI \> 1 dự án đang đi nhanh hơn kế
hoạch, nếu SPI \< 1 dự án đang chậm hơn so với kế hoạch

Kết quả:

SPI = 38,25 / 45 = 0,85

**Nhận xét:** Chỉ số SPI = 0,85 \< 1 cho thấy dự án chậm tiến độ so với
kế hoạch, cụ thể mới hoàn thành khoảng 85% khối lượng công việc dự kiến.
Nguyên nhân từ việc một số công việc thiết kế giao diện và kịch bản hội
thoại bị trễ so với kế hoạch ban đầu.

**6.2.3. Tính toán và phân tích chỉ số CPI**

Công thức: ![](media/media/image4.png){width="3.2087806211723535in"
height="0.6667596237970254in"}

Trong đó:

EV (Earned Value): Giá trị công việc đã hoàn thành.\
AC (Planned Value): Chi phí thực tế

Kết quả:

CPI = 38,25 / 42,3 ≈ 0,90

**Nhận xét:** Chỉ số CPI ≈ 0,90 \< 1 cho thấy hiệu quả sử dụng chi phí
chưa tối ưu, tuy nhiên mức chênh lệch không lớn. Dự án đang sử dụng chi
phí cao hơn so với giá trị công việc hoàn thành, nhưng vẫn nằm trong
ngưỡng kiểm soát và chưa vượt ngân sách tổng thể.

6.3. Dự báo chi phí khi hoàn thành dự án (EAC)

Công thức:

EAC = AC + (BAC − EV)

Áp dụng:

EAC = 42,3 + (45 -- 38,25) = 49,05 triệu VNĐ

**Nhận xét:** Chi phí dự kiến khi hoàn thành dự án cao hơn ngân sách ban
đầu khoảng 5 triệu VNĐ, cho thấy cần tăng cường kiểm soát chi phí trong
các Sprint tiếp theo.

**6.4. Đánh giá tổng thể hiệu quả dự án dựa trên KPIs**

Dựa trên các chỉ số đã phân tích:

- **SPI = 0,85:** Dự án chậm tiến độ nhẹ về khối lượng công việc.

- **CPI ≈ 0,90:** Hiệu quả sử dụng chi phí tương đối hợp lý, chưa vượt
  ngân sách.

- C**hi phí thực tế:** 42,3 / 45 triệu VNĐ → dự án vẫn đang được kiểm
  soát tốt về tài chính.

- **Các KPIs về chatbot (Accuracy, CSAT):** Đạt mức chấp nhận được theo
  yêu cầu dự án.

**Dự án SupportBot vẫn trong trạng thái kiểm soát**, dù tiến độ Sprint 1
chưa đạt 100% như kế hoạch ban đầu. Các sai lệch hiện tại không nghiêm
trọng và có thể được khắc phục trong các Sprint tiếp theo thông qua việc
điều chỉnh phân công công việc và tăng cường theo dõi tiến độ.

**6.5. Vai trò của KPIs trong quản lý dự án**

Việc áp dụng các chỉ số KPIs giúp nhóm dự án:

- Theo dõi tiến độ và chi phí một cách **định lượng và minh bạch**.

- Phát hiện sớm các sai lệch so với kế hoạch.

- Hỗ trợ ra quyết định điều chỉnh phạm vi, nguồn lực và lịch trình.

- Nâng cao hiệu quả quản lý và khả năng kiểm soát tổng thể dự án.
