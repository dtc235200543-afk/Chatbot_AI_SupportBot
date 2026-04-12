## PHẦN 3: LỰA CHỌN PHƯƠNG PHÁP & KẾ HOẠCH THỜI GIAN

## 3.1. Lựa chọn phương pháp quản lý dự án

### 3.1.1. So sánh các phương pháp

  -----------------------------------------------------------------------
  Tiêu chí          Waterfall (Thác   Agile (Linh hoạt) Scrum (Framework
                    nước)                               Agile)
  ----------------- ----------------- ----------------- -----------------
  Yêu cầu đầu vào   Cần đầy đủ, chi   Có thể thay đổi   Có thể thay đổi,
                    tiết từ đầu       trong quá trình   ưu tiên theo
                                                        Sprint

  Thời gian có sản  Cuối dự án (tháng Sau mỗi Sprint    Có thể thay đổi,
  phẩm chạy         thứ 3)            (2-4 tuần)        ưu tiên theo
                                                        Sprint

  Khả năng thích    Rất thấp          Rất cao           Rất cao
  ứng thay đổi                                          

  Mức độ tham gia   Chỉ ở đầu và cuối Liên tục (Sprint  Liên tục (Sprint
  của khách hàng                      Review)           Review)

  Quản lý rủi ro    Cuối dự án mới    Phát hiện sớm sau Phát hiện sớm sau
                    phát hiện         mỗi Sprint        mỗi Sprint

  Phù hợp với dự án Không (AI cần     Có                **Có (chọn)**
  AI                huấn luyện lặp)                     
  -----------------------------------------------------------------------

### 3.1.2. Lý do chọn Scrum cho dự án SupportBot

**- Lý do 1: Phát triển theo \"kỹ năng\" (skill-based development)**

Chatbot được chia thành các kỹ năng độc lập: hỏi chính sách, tra cứu đơn
hàng, hỏi thông tin sản phẩm\... Mỗi kỹ năng là một Sprint riêng, không
phụ thuộc nhiều vào nhau.

**- Lý do 2: Liên tục cải thiện chất lượng AI**

Sau mỗi Sprint, nhóm sẽ đo lường **độ chính xác (accuracy)** và **tỷ lệ
hiểu sai (fallback rate)**. Dựa vào đó, Sprint tiếp theo sẽ cải thiện.

**- Lý do 3: Giảm rủi ro sai lệch yêu cầu**

Khách hàng (phòng CSKH) tham gia Sprint Review, phát hiện sớm bot trả
lời sai chính sách → điều chỉnh kịp thời.

**- Lý do 4: Tối ưu ngân sách**

Các tính năng có giá trị kinh doanh cao nhất được ưu tiên làm trước
(chính sách, đơn hàng), đảm bảo ROI ngay cả khi dự án phải dừng sớm.

## 3.2. Cấu trúc Sprint cho dự án SupportBot

### 3.2.1. Xác định thời gian Sprint

Thời gian mỗi Sprint: 2 tuần (14 ngày làm việc)

Lý do chọn 2 tuần: Đủ dài để tạo ra increment có giá trị, đủ ngắn để
phản hồi nhanh với thay đổi

Tổng số Sprint: 5 Sprint

Tổng thời gian dự án: 10 tuần (từ 13/04/2026 đến 21/06/2026)

### 3.2.2. Danh sách các Sprint và mục tiêu

  ---------------------------------------------------------------------------
  Sprint     Thời    Tên Sprint        Mục tiêu chính           Sản phẩm đầu
             gian                                               ra
  ---------- ------- ----------------- ------------------------ -------------
  **Sprint   13/01   Xây dựng kỹ năng  Bot trả lời được câu hỏi Bot text cơ
  1**        --      trả lời FAQs tĩnh về chính sách, bảo hành, bản (MVP)
             26/01                     vận chuyển               

  **Sprint   27/01   Tra cứu đơn hàng  Bot gọi API để tra cứu   Bot có tích
  2**        --      qua API           trạng thái đơn hàng      hợp API
             10/02                     chính xác                

  **Sprint   11/02   Hỏi thông tin sản Bot trả lời thông tin    Bot full tính
  3**        --      phẩm & giá        sản phẩm, giá từ catalog năng cốt lõi
             24/02                                              

  **Sprint   25/02   Chuyển tiếp nhân  Bot phát hiện yêu cầu    Bot + Live
  4**        --      viên & gắn nhãn   phức tạp, chuyển sang    chat
             07/03   ticket            human agent              

  **Sprint   08/03   Tối ưu, giám sát  Dashboard giám sát, load Bot
  5**        --      & báo cáo         test, triển khai         production
             21/03                     production               ready
  ---------------------------------------------------------------------------

## 3.3. Bảng ước lượng PERT (Program Evaluation and Review Technique)

### 3.3.1. Ký hiệu và công thức

  --------------------------------------------------------------------------
  Ký hiệu   Ý nghĩa             Mô tả
  --------- ------------------- --------------------------------------------
  **MO**    Lạc quan nhất (Most Thời gian cần để hoàn thành Sprint trong
            Optimistic)         điều kiện lý tưởng nhất (không có trở ngại
                                nào)

  **ML**    Khả dĩ nhất (Most   Thời gian cần để hoàn thành Sprint trong
            Likely)             điều kiện hợp lý (có thể xảy ra trở ngại
                                nhỏ)

  **MP**    Bi quan nhất (Most  Thời gian cần để hoàn thành Sprint trong
            Pessimistic)        điều kiện tồi nhất (có nhiều trở ngại)

  **EST**   Ước lượng cuối cùng Được tính theo công thức
            (Estimation)        PERT: EST=(MO+4×ML+MP)/6
  --------------------------------------------------------------------------

### 3.3.2. Bảng PERT chi tiết cho 5 Sprint

  --------------------------------------------------------------------------------------
  STT      Đầu mục   Mã       MO       ML (ngày) MP (ngày)  EST (ngày) Khoảng    Mức độ
           công việc          (ngày)                                   dao động  rủi ro
                                                                       (MP-MO)   
  -------- --------- -------- -------- --------- ---------- ---------- --------- -------
  1        Sprint 1: SP-01    10       14        20         **14.3**   10 ngày   Trung
           FAQs tĩnh                                                             bình

  2        Sprint 2: SP-02    9        14        22         **14.5**   13 ngày   Cao
           Tra cứu                                                               
           đơn hàng                                                              

  3        Sprint 3: SP-03    11       14        19         **14.3**   8 ngày    Thấp
           Sản phẩm                                                              
           & giá                                                                 

  4        Sprint 4: SP-04    10       14        24         **15.0**   14 ngày   Rất cao
           Chuyển                                                                
           nhân viên                                                             

  5        Sprint 5: SP-05    11       14        18         **14.2**   7 ngày    Thấp
           Tối ưu &                                                              
           báo cáo                                                               

  **Tổng             **51**   **70**   **103**   **72.3**   **52                 
  cộng**                                                    ngày**               
  --------------------------------------------------------------------------------------

### 3.3.3. Biểu đồ so sánh MO, ML, MP, EST:

![**Hình 3: So sánh MO, ML, MP và EST theo
Sprint**](media/image1.png){alt="MO (Lạc quan), ML (Khả dĩ), MP (Bi quan) và EST (Ước lượng)"
width="5.7625in" height="3.5631944444444446in"}

**Biểu đồ thanh nhóm:** Mỗi Sprint có 4 cột (MO, ML, MP, EST). Sprint 4
có MP cao nhất (24 ngày) và EST cao nhất (15.0 ngày). Sprint 5 có khoảng
dao động nhỏ nhất (7 ngày).

### 3.3.4. Phân tích độ rủi ro và thời gian dự phòng

**Nhận xét về độ rủi ro của từng Sprint:**

  -------------------------------------------------------------------------
  Sprint   Mức độ rủi Giải thích                    Biện pháp giảm thiểu
           ro                                       
  -------- ---------- ----------------------------- -----------------------
  Sprint 1 Trung bình Dữ liệu FAQ có sẵn, nhưng cần Dành 2 ngày đầu để kiểm
                      làm sạch và chuẩn hóa         tra dữ liệu

  Sprint 2 Cao        Phụ thuộc vào API bên thứ ba, Có phương án dự phòng,
                      có thể thay đổi không báo     liên hệ sớm với đối tác
                      trước                         

  Sprint 3 Thấp       Catalog sản phẩm nội bộ, chủ  Không cần biện pháp đặc
                      động kiểm soát được           biệt

  Sprint 4 Rất cao    Tích hợp nhiều hệ thống (API  Dành nhiều thời gian
                      ticket, live chat)            test, có kế hoạch
                                                    rollback

  Sprint 5 Thấp       Chủ yếu là tối ưu và viết tài Không cần biện pháp đặc
                      liệu                          biệt
  -------------------------------------------------------------------------

**Thời gian dự phòng (Contingency):**

Dự phòng theo EST - ML=72.3−70=2.3 ngày

Dự phòng theo tổng biến động=(∑(*MP*−*MO*))/6​=(10+13+8+14+7)/6​=52/6​/6≈8.7 ngày

## 3.4. Biểu đồ Gantt chi tiết

### 3.4.1. Bảng tiến độ Gantt

  ----------------------------------------------------------------------------------------------------
  STT     Mã          Tên công việc   Bắt đầu     Kết thúc    Người phụ   Phụ thuộc   Kết quả
                                                              trách                   
  ------- ----------- --------------- ----------- ----------- ----------- ----------- ----------------
  **1**   **SP-01**   **Sprint 1:     **13/01**   **26/01**   **Nhóm AI**             **Bot MVP**
                      FAQs tĩnh**                                                     

  1.1     SP-01.1     Thu thập và     13/01       16/01       Kỹ sư AI    \-          File Excel
                      chuẩn hóa dữ                            (A)                     
                      liệu                                                            

  1.2     SP-01.2     Thiết kế luồng  15/01       19/01       Kỹ sư AI    1.1         6 sơ đồ
                      hội thoại                               (C)                     

  1.3     SP-01.3     Cấu hình        17/01       21/01       Kỹ sư AI    1.2         15 Intent
                      Intent/Entity                           (B)                     

  1.4     SP-01.4     Huấn luyện và   20/01       25/01       Tester      1.3         Model v1.0
                      kiểm thử                                                        

  1.5     SP-01.5     Tích hợp iframe 24/01       26/01       Front-end   1.4         Code tích hợp
                      chat                                                            

  **2**   **SP-02**   **Sprint 2: Tra **27/01**   **10/02**   **Nhóm AI** **SP-01**   **Bot có API**
                      cứu đơn hàng**                                                  

  2.1     SP-02.1     Phân tích API   27/01       28/01       Backend     \-          Tài liệu API
                      đơn hàng                                                        

  2.2     SP-02.2     Tạo webhook     29/01       02/02       Kỹ sư AI    2.1         Webhook code
                                                              (A)                     

  2.3     SP-02.3     Thiết kế luồng  30/01       03/02       Kỹ sư AI    2.1         Sơ đồ
                      xác thực                                (C)                     

  2.4     SP-02.4     Huấn luyện      03/02       06/02       Kỹ sư AI    2.3         Intent mới
                      intent mới                              (B)                     

  2.5     SP-02.5     Xử lý fallback  05/02       10/02       Kỹ sư AI    2.4         Cơ chế retry
                                                              (A)                     

  **3**   **SP-03**   **Sprint 3: Sản **11/02**   **24/02**   **Nhóm AI** **SP-02**   **Bot full**
                      phẩm & giá**                                                    

  3.1     SP-03.1     Kết nối catalog 11/02       13/02       Backend     \-          JDBC

  3.2     SP-03.2     Xây dựng intent 12/02       15/02       Kỹ sư AI    3.1         Intent mới
                      tìm kiếm                                (B)                     

  3.3     SP-03.3     Thiết kế phản   14/02       17/02       Front-end   3.2         Rich response
                      hồi rich                                                        

  3.4     SP-03.4     Huấn luyện 100  16/02       20/02       Kỹ sư AI    3.3         Model v3.0
                      câu                                     (C)                     

  3.5     SP-03.5     Kiểm thử        21/02       24/02       Tester      3.4         Báo cáo
                      accuracy                                                        

  **4**   **SP-04**   **Sprint 4:     **25/02**   **07/03**   **Nhóm AI** **SP-03**   **Bot+Live**
                      Chuyển nhân                                                     
                      viên**                                                          

  4.1     SP-04.1     Phát hiện yêu   25/02       28/02       Kỹ sư AI    \-          Classifier
                      cầu phức tạp                            (C)                     

  4.2     SP-04.2     Tích hợp API    27/02       30/02       Kỹ sư AI    4.1         Tạo ticket
                      ticket                                  (A)                     

  4.3     SP-04.3     Thiết kế luồng  29/02       01/03       Kỹ sư AI    4.2         Sơ đồ
                      chuyển                                  (C)                     

  4.4     SP-04.4     Đào tạo nhân    05/03       07/03       Scrum       4.3         Tài liệu
                      viên                                    Master                  

  **5**   **SP-05**   **Sprint 5: Tối **08/03**   **21/03**   **Nhóm AI** **SP-04**   **Production**
                      ưu & báo cáo**                                                  

  5.1     SP-05.1     Dashboard giám  08/03       11/03       Kỹ sư AI    \-          Dashboard
                      sát                                     (A)                     

  5.2     SP-05.2     Load test       12/03       14/03       Tester      5.1         Báo cáo

  5.3     SP-05.3     Triển khai      15/03       18/03       Kỹ sư AI    5.2         Bot live
                      production                              (A)                     

  5.4     SP-05.4     Tổng kết dự án  17/03       21/03       Scrum       5.3         
                                                              Master                  
  ----------------------------------------------------------------------------------------------------

### 3.4.2. Biểu đồ Gantt dạng trực quan

![**Hình 4: Biểu đồ Gantt dạng trực
quan**](media/image2.png){width="5.7659722222222225in"
height="3.573611111111111in"}

## 3.5. Sơ đồ mạng PERT (Network Diagram)

![](media/image3.png){width="5.768055555555556in"
height="3.0340277777777778in"}

**Hình 5: Sơ đồ thể hiện đường găng**
