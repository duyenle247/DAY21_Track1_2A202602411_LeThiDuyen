# Track 1 — Day 21: Industry Risk Snapshot & Empirical Case Studies

---

## 1. Thông tin Cá nhân & Ngành Chọn Phân Tích

- **Họ và tên:** Lê Thị Duyên
- **Mã học viên:** 2A202602411
- **Ngành được chọn:** **Giáo dục / AI tutor**
- **Phạm vi gợi ý theo đề:** AI hỗ trợ học tập, hướng dẫn người học, chấm điểm tự động và giám sát liêm chính học thuật (*AI-assisted learning, tutoring, algorithmic grading & automated proctoring*).

---

## 2. Industry Risk Snapshot (Giáo dục / AI Tutor)

*Lưu ý: Các mức đánh giá Thấp / Trung bình / Cao dưới đây là nhận định định tính phục vụ phân tích rủi ro sản phẩm công nghệ trong khuôn khổ bài tập, không phải kết luận phân loại pháp lý theo các đạo luật như EU AI Act.*

| Tiêu chí | Đánh giá định tính | Căn cứ & Lý do phân tích ngắn gọn |
| :--- | :---: | :--- |
| **1. Harm chính (Tác hại cốt lõi)** | **Đa tầng (Allocative, Representational, Epistemic & Psychological Harms)** | • **Tác hại phân bổ (Allocative Harm):** Học sinh bị tước đoạt cơ hội học tập, trượt đại học, mất học bổng hoặc bị đình chỉ học bạ do thuật toán chấm điểm sai hoặc AI gán nhãn oan là "gian lận".<br>• **Tác hại tri thức (Epistemic Harm):** Ảo giác AI (hallucination) cung cấp kiến thức sai lệch, khiến người học tiếp thu sai tư duy nền tảng.<br>• **Tác hại định kiến & tâm lý (Representational & Psychological Harm):** Kỳ thị người học không nói tiếng Anh bản xứ (ESL), dán nhãn sai lệch học sinh khuyết tật/thần kinh đa dạng (neurodivergent), gây hoảng loạn và tổn thương tâm lý nghiêm trọng. |
| **2. Mức độ High-stakes (Tính rủi ro hệ trọng)** | **Cao** | Quyết định trong giáo dục (điểm thi tốt nghiệp, kết quả thi cử, liêm chính học thuật) tác động mang tính bước ngoặt cả đời người đến lộ trình học vấn, bằng cấp và cơ hội nghề nghiệp tương lai của học sinh. Sai số thuật toán không chỉ là "trải nghiệm tồi" mà để lại di chứng pháp lý và học bạ vĩnh viễn. |
| **3. Dữ liệu nhạy cảm (Data Sensitivity)** | **Cao** | Đối tượng sử dụng đa phần là trẻ em, thanh thiếu niên và học sinh vị thành niên (thuộc nhóm bảo vệ đặc biệt theo GDPR-K, COPPA). Dữ liệu thu thập bao gồm: hình ảnh khuôn mặt qua webcam, giọng nói, biểu cảm sinh trắc học, thói quen tư duy, lịch sử sai sót học vấn và hồ sơ khuyết tật học tập (ADHD, tự kỷ, dyslexia). |
| **4. Nhu cầu Human Review (Sự can thiệp của con người)** | **Bắt buộc / Rất cao** | AI hoàn toàn thiếu sự thấu cảm sư phạm và không thể hiểu ngữ cảnh xã hội, phong cách diễn đạt phi bản ngữ hay hoàn cảnh cá nhân của học sinh. Mọi quyết định xử lý kỷ luật gian lận, hạ điểm thi hay đánh giá năng lực sống còn tuyệt đối không được tự động hóa hoàn toàn (zero-touch), mà bắt buộc phải có sự thẩm định, đối thoại và phán quyết cuối cùng từ hội đồng sư phạm / giáo viên. |

---

## 3. Danh mục 3 Brief Case Nghiên cứu Thực tế & Harm Map Worksheets

Dưới đây là 3 case study có thật trong ngành Giáo dục & AI Tutor, đại diện cho 3 lát cắt rủi ro then chốt: **Định kiến công cụ phát hiện AI (AI Detection Bias)**, **Sự cố thuật toán chuẩn hóa điểm thi (Algorithmic Grading Failure)**, và **Hệ thống giám thị thi AI xâm phạm quyền riêng tư & phân biệt đối xử (AI Proctoring & Surveillance Risk)**.

Mỗi case được phân tích theo đầy đủ cấu trúc Brief Case và Worksheet Harm Map 11 trường:
$$\text{Moment} \rightarrow \text{Mode} \rightarrow \text{Layer} \rightarrow \text{Harm} \rightarrow \text{Severity} \quad (+ \text{Stakeholders, Lens, Scale, Probability, Frequency, Căn cứ})$$

---

### Case 1: Định kiến ngôn ngữ của các công cụ phát hiện văn bản AI đối với học sinh không nói tiếng Anh bản xứ (Stanford University Study)

#### 1. Thông tin chung
- **Tổ chức / Nhóm nghiên cứu:** Đại học Stanford (Nhóm tác giả: Weixin Liang, Mert Yuksekgonul, Yining Mao, Eric Wu, James Zou).
- **Sản phẩm / Công cụ khảo sát:** 7 công cụ phát hiện văn bản AI phổ biến (GPT-detectors) gồm GPTZero, CopyLeaks, Sapling, CrossPlag, ZeroGPT, OpenAI Text Classifier, và Writer.
- **Bối cảnh:** Các cơ sở giáo dục trên toàn cầu triển khai ồ ạt các công cụ phát hiện văn bản do AI tạo ra để kiểm tra gian lận bài luận văn và bài tập về nhà của học sinh/sinh viên.

#### 2. Vấn đề rủi ro & Phân tích tác hại
- **Cơ chế lỗi kỹ thuật:** Các công cụ phát hiện AI chủ yếu dựa vào chỉ số "độ phức tạp" (perplexity) của văn bản. Do người học tiếng Anh phi bản xứ (ESL/Non-native English speakers) thường có vốn từ vựng hạn chế hơn và cấu trúc câu đơn giản, dễ đoán hơn người bản xứ, mô hình AI tự động coi đặc điểm ngôn ngữ tự nhiên này là văn bản do máy móc tạo ra.
- **Tác hại đã xác nhận & Nguy cơ xảy ra:**
  - *Tác hại phân bổ (Allocative harm):* Học sinh quốc tế bị cáo buộc oan về việc vi phạm liêm chính học thuật (false positive), đứng trước nguy cơ bị điểm 0, hủy kết quả môn học hoặc bị đình chỉ học tập.
  - *Tác hại định kiến (Representational harm):* Trừng phạt trực tiếp năng lực ngôn ngữ hạn chế thay vì phát hiện hành vi gian lận thực sự, khoét sâu bất công đối với học sinh thiểu số và du học sinh.

#### 3. Số liệu thực tế định lượng kèm nguồn
- **Số liệu cụ thể:** 
  > **61.22%** (55 trên tổng số 91 bài luận thi TOEFL) do người học tiếng Anh phi bản xứ tự viết (không dùng AI) bị 7 công cụ AI detector phân loại sai là văn bản do AI tạo ra (false positive); cá biệt có công cụ gán cờ nhầm tới **97.8% (89/91 bài)**. Trong khi đó, ở tập dữ liệu bài luận của học sinh bản ngữ lớp 8 tại Mỹ (US 8th graders), tỷ lệ phân loại nhầm của các công cụ này đạt mức gần như hoàn hảo với **dưới 1.8%** sai sót.
- **Thời gian nghiên cứu:** Tháng 4 – Tháng 7/2023.
- **Nguồn kiểm chứng:** Nghiên cứu được công bố trên tạp chí khoa học *Patterns (Cell Press)* (DOI: 10.1016/j.patter.2023.100779) và bài báo cáo của Viện AI Tập trung vào Con người Đại học Stanford (Stanford HAI):
  - 🔗 [Stanford HAI: AI Detectors Biased Against Non-Native English Writers](https://hai.stanford.edu/news/ai-detectors-biased-against-non-native-english-writers)
  - 🔗 [Cell Press Patterns / arXiv:2304.02819](https://arxiv.org/abs/2304.02819)

#### 4. Harm Map Worksheet (11 Trường Phân Tích)

| STT | Trường thông tin (Harm Map Field) | Nội dung đánh giá chi tiết |
| :---: | :--- | :--- |
| **1** | **High-risk moment** | Thời điểm giảng viên/nhà trường đưa bài luận (essay) của sinh viên vào công cụ AI Detector để sàng lọc tự động trước khi chấm điểm học phần hoặc xét duyệt học bổng/tốt nghiệp. |
| **2** | **Failure mode** | **Bias / fairness** *(kèm Over-reliance từ phía người dùng/giảng viên)*: Mô hình thiên vị bất công đối với nhóm người học phi bản xứ; giảng viên tin tưởng mù quáng vào kết quả phần trăm của công cụ mà không đối soát. |
| **3** | **Layer** | **Model & UX**:<br>• *Model layer:* Mô hình lấy thước đo perplexity làm proxy phát hiện AI, vốn trùng khớp với mẫu hình ngôn ngữ của người học ESL.<br>• *UX layer:* Giao diện hiển thị nhãn khẳng định tuyệt đối (ví dụ: "98% AI-generated") mà không hiển thị độ lệch chuẩn hay cảnh báo sai số trên người học ngoại ngữ. |
| **4** | **Stakeholder** | • **Bên chịu tác động trực tiếp:** Sinh viên quốc tế, người học tiếng Anh phi bản xứ (ESL/EFL).<br>• **Bên ra quyết định:** Giảng viên, hội đồng kỷ luật học thuật của nhà trường.<br>• **Bên liên quan khác:** Cơ quan cấp thị thực du học, đơn vị tài trợ học bổng. |
| **5** | **Harm (Mẫu chuẩn)** | **[Sinh viên quốc tế / người học tiếng Anh phi bản xứ]** bị **[gán nhãn oan là gian lận học thuật, đối mặt với nguy cơ bị điểm 0, hủy học bổng hoặc bị đình chỉ học tập]** khi **[công cụ AI Detector đánh giá nhầm bài viết tự làm của họ là văn bản do AI tạo ra chỉ vì cấu trúc từ vựng đơn giản, ít biến thể (low perplexity)]**. |
| **6** | **Harm lens** | **Opportunity loss** *(mất cơ hội)* & **Dignity loss** *(tổn hại phẩm giá)*. |
| **7** | **Severity** | **High** |
| **8** | **Scale** | **High** *(Phạm vi toàn cầu trên hàng triệu sinh viên quốc tế; tỷ lệ mẫu nghiên cứu bị ảnh hưởng lên tới 61.22%)* |
| **9** | **Probability** | **High** *(Tỷ lệ thực nghiệm đo lường được là 61.22%, cá biệt một số công cụ lên tới 97.8%)* |
| **10** | **Frequency** | **High** *(Lặp lại thường xuyên ở mọi kỳ nộp bài tập/tiểu luận nếu nhà trường áp dụng AI detector làm quy trình kiểm duyệt bắt buộc)* |
| **11** | **Vì sao? (Căn cứ đánh giá)** | • *Về Severity (High):* Bị cáo buộc gian lận học thuật (academic dishonesty) để lại vết nhơ vĩnh viễn trong học bạ (transcript), có thể dẫn đến việc tước học bổng và hủy visa du học.<br>• *Về Scale & Probability (High):* Đo lường thực nghiệm trên 91 bài viết TOEFL cho thấy hơn 6/10 bài bị gán nhãn nhầm; hàng trăm ngàn sinh viên quốc tế đang học tập tại các quốc gia nói tiếng Anh chịu rủi ro trực tiếp.<br>• *Về Mode & Layer:* Giao diện (UX) thiếu cảnh báo sai số, còn mô hình (Model) lấy đặc tính ngôn ngữ nghèo nàn làm bằng chứng gian lận, trực tiếp biến sự hạn chế về ngoại ngữ thành tội danh học thuật. |

---

### Case 2: Khủng hoảng thuật toán chuẩn hóa điểm thi tốt nghiệp A-Levels của Ofqual (Vương quốc Anh, 2020)

#### 1. Thông tin chung
- **Tổ chức / Sản phẩm:** Cơ quan Quản lý Khảo thí Vương quốc Anh (Ofqual) phối hợp cùng Bộ Giáo dục Anh (Department for Education - DfE).
- **Mô hình triển khai:** Thuật toán chuẩn hóa điểm số theo mô hình thống kê (Standardisation algorithm) thay thế cho kỳ thi quốc gia A-Levels và GCSE.
- **Bối cảnh:** Mùa hè năm 2020, trước làn sóng đại dịch COVID-19, toàn bộ kỳ thi tốt nghiệp trung học A-Levels bị hủy bỏ. Ofqual đưa ra thuật toán tự động điều chỉnh điểm dự đoán của giáo viên (Centre Assessed Grades - CAGs) để kiểm soát tình trạng "lạm phát điểm số".

#### 2. Vấn đề rủi ro & Phân tích tác hại
- **Cơ chế lỗi kỹ thuật:** Thuật toán kết hợp lịch sử điểm thi của trường trong 3 năm trước đó và quy mô lớp học để "ép" phân phối điểm của từng trường về mức lịch sử. Với các lớp học nhỏ dưới 15 học sinh (chủ yếu là trường tư thục giàu có), thuật toán giữ nguyên điểm giáo viên đánh giá; trong khi các lớp học đông ở trường công lập nghèo bị ép theo phân phối điểm thấp của trường trong quá khứ.
- **Tác hại đã xác nhận & Nguy cơ xảy ra:**
  - *Tác hại phân bổ cơ hội tàn khốc (Systemic Allocative Harm):* Hàng chục ngàn học sinh giỏi xuất thân nghèo khó tại các trường công lập bị tước đoạt điều kiện trúng tuyển đại học (đặc biệt là Đại học Oxford, Cambridge, Russell Group).
  - *Tác hại xã hội & tâm lý:* Gây ra các cuộc biểu tình đường phố quy mô lớn của học sinh trên khắp nước Anh với khẩu hiệu phản đối "thuật toán đột biến" (*mutant algorithm*), gây khủng hoảng niềm tin trầm trọng vào hệ thống giáo dục quốc gia. Chính phủ Anh buộc phải hủy bỏ kết quả thuật toán chỉ sau 1 tuần.

#### 3. Số liệu thực tế định lượng kèm nguồn
- **Số liệu cụ thể:** 
  > **39.1%** tổng số kết quả điểm do giáo viên đánh giá tại Anh (tương đương **280.711** điểm thi của học sinh) đã bị thuật toán hạ xuống ít nhất 1 bậc điểm (trong đó 35.6% bị hạ 1 bậc, 3.3% bị hạ 2 bậc, và 0.2% bị hạ 3 bậc); trong khi chỉ có 2.2% được nâng điểm. Khoảng cách bất bình đẳng gia tăng rõ rệt: Tỷ lệ học sinh đạt điểm A/A* tại các trường tư thục độc lập tăng **4.7 điểm phần trăm**, trong khi tại các trường công lập toàn diện (comprehensive schools) chỉ tăng **2.0 điểm phần trăm**.
- **Thời gian diễn ra sự kiện:** Tháng 8/2020.
- **Nguồn kiểm chứng:** Báo cáo công bố chính thức của Ofqual và chuỗi phóng sự điều tra của BBC News & The Guardian:
  - 🔗 [BBC News: A-levels: Nearly 40% of teacher grades downgraded in England](https://www.bbc.com/news/education-53755494)
  - 🔗 [The Guardian: Almost 40% of English A-level results downgraded after exams cancelled](https://www.theguardian.com/education/2020/aug/13/almost-40-of-english-a-level-results-downgraded-after-exams-cancelled)
  - 🔗 [Ofqual Official Report: Awarding GCSE, AS & A levels in summer 2020](https://www.gov.uk/government/publications/awarding-gcse-as-a-levels-in-summer-2020-interim-report)

#### 4. Harm Map Worksheet (11 Trường Phân Tích)

| STT | Trường thông tin (Harm Map Field) | Nội dung đánh giá chi tiết |
| :---: | :--- | :--- |
| **1** | **High-risk moment** | Thời điểm cơ quan khảo thí Ofqual chạy thuật toán chuẩn hóa điểm để chốt và công bố điểm thi tốt nghiệp chính thức A-Levels cho toàn bộ học sinh trên cả nước, dùng làm căn cứ quyết định xét tuyển đại học. |
| **2** | **Failure mode** | **Bias / fairness** *(kèm Escalation failure)*: Thuật toán thiên vị mang tính hệ thống theo xuất thân kinh tế - xã hội; hệ thống triệt tiêu cơ chế khiếu nại/can thiệp của con người trước khi phát hành điểm. |
| **3** | **Layer** | **Model & Grounding**:<br>• *Model layer:* Thiết kế thuật toán đưa trọng số lịch sử trường học vào làm biến số quyết định điểm số cá nhân, đồng thời ưu tiên miễn trừ chuẩn hóa cho lớp nhỏ dưới 15 học sinh.<br>• *Grounding layer:* Dữ liệu thành tích lịch sử 3 năm của trường học không phản ánh đúng năng lực và nỗ lực thực tế của lứa học sinh hiện tại. |
| **4** | **Stakeholder** | • **Bên chịu tác động trực tiếp:** Học sinh các trường công lập toàn diện (comprehensive schools), học sinh nghèo.<br>• **Bên bị phủ nhận chuyên môn:** Giáo viên và ban giám hiệu nhà trường.<br>• **Bên ra quyết định & Vận hành:** Cơ quan khảo thí Ofqual, Bộ Giáo dục Anh, các trường đại học (Russell Group, Oxford, Cambridge). |
| **5** | **Harm (Mẫu chuẩn)** | **[Học sinh các trường công lập toàn diện]** bị **[thuật toán tự động hạ điểm tốt nghiệp A-Levels từ 1 đến 3 bậc điểm so với năng lực thực tế, dẫn đến việc mất suất trúng tuyển vào các trường đại học hàng đầu]** khi **[thuật toán Ofqual ép điểm số cá nhân vào phân phối thành tích lịch sử thấp của trường công lập trong quá khứ]**. |
| **6** | **Harm lens** | **Opportunity loss** *(mất cơ hội học tập & thăng tiến xã hội)* & **Dignity loss** *(tổn hại phẩm giá, công sức bị xem thường)*. |
| **7** | **Severity** | **High** |
| **8** | **Scale** | **High** *(Toàn bộ hệ thống giáo dục phổ thông nước Anh; 280.711 điểm số của học sinh bị hạ bậc)* |
| **9** | **Probability** | **High** *(Tỷ lệ thực tế bị hạ điểm là 39.1% trên toàn bộ kết quả nộp lên)* |
| **10** | **Frequency** | **Low** *(Sự cố bùng phát trong kỳ thi tốt nghiệp mùa hè năm 2020 do bối cảnh phong tỏa dịch bệnh)* |
| **11** | **Vì sao? (Căn cứ đánh giá)** | • *Về Severity (High):* Điểm A-Levels là căn cứ duy nhất để các trường đại học cấp chỉ tiêu nhập học. Việc bị hạ điểm khiến học sinh lỡ mất kỳ nhập học và học bổng; dù sau đó chính phủ hủy bỏ thuật toán thì nhiều trường đại học đã hết suất.<br>• *Về Scale (High) & Probability (High):* Có số liệu kiểm chứng chính thức từ Ofqual với 280.711 điểm bị dìm (39.1% tổng số bài), phản ánh rủi ro mang tính hệ thống.<br>• *Về Frequency (Low):* Diễn ra 1 lần ở quy mô kỳ thi quốc gia.<br>• *Về Mode & Layer:* Thuật toán ưu tiên mục tiêu vĩ mô "ngăn lạm phát điểm" bằng cách dùng dữ liệu quá khứ (Grounding) để kìm hãm người học trường công lập, gây bất bình đẳng giai cấp trầm trọng. |

---

### Case 3: Hệ thống Giám thị AI Proctorio & Báo cáo Điều tra về Giám sát Học sinh của CDT (2021–2022)

#### 1. Thông tin chung
- **Tổ chức / Sản phẩm:** Công ty công nghệ khảo thí Proctorio Inc. và Báo cáo nghiên cứu điều tra của Trung tâm Dân chủ & Công nghệ Hoa Kỳ (Center for Democracy & Technology - CDT).
- **Sản phẩm:** Phần mềm giám thị thi trực tuyến bằng AI (*AI Automated Exam Proctoring*) theo dõi người học qua webcam, nhận diện khuôn mặt, theo dõi ánh mắt và ghi nhận âm thanh phòng thi.
- **Bối cảnh:** Trong giai đoạn học từ xa và hậu COVID-19, hơn 1.000 cơ sở giáo dục đại học và trung học áp dụng phần mềm giám thị AI để tự động phát hiện dấu hiệu gian lận thi cử tại nhà.

#### 2. Vấn đề rủi ro & Phân tích tác hại
- **Cơ chế lỗi kỹ thuật:** Mô hình nhận diện khuôn mặt và thị giác máy tính của Proctorio được huấn luyện mất cân bằng dữ liệu, gặp khó khăn nghiêm trọng khi nhận diện sinh viên có màu da tối. Đồng thời, thuật toán gắn cờ "đáng ngờ" (suspicious behavior) dựa trên các cử động mắt, lắc đầu hoặc tiếng động ngoại cảnh.
- **Tác hại đã xác nhận & Nguy cơ xảy ra:**
  - *Tác hại định kiến đối với người khuyết tật & thần kinh đa dạng:* Học sinh mắc hội chứng tăng động giảm chú ý (ADHD), tự kỷ hoặc hội chứng Tic có cử động đầu và ánh mắt không điển hình liên tục bị AI gắn cờ gian lận, gây hoảng loạn tâm lý trong lúc làm bài thi.
  - *Phân biệt đối xử chủng tộc (Racial bias):* Sinh viên da màu phản ánh hệ thống không thể nhận diện khuôn mặt để cho phép vào phòng thi, buộc họ phải dùng đèn rọi thẳng vào mặt suốt nhiều giờ.
  - *Xâm phạm quyền riêng tư nghiêm trọng:* Vụ kiện mang tính bước ngoặt *Ogletree v. Cleveland State University (2022)* kết luận việc phần mềm giám thị AI quét phòng ngủ của sinh viên vi phạm Tu chính án thứ Tư của Hiến pháp Hoa Kỳ.

#### 3. Số liệu thực tế định lượng kèm nguồn
- **Số liệu cụ thể:** 
  > Theo khảo sát đại diện quốc gia của tổ chức CDT (2022) trên các trường học ứng dụng phần mềm giám sát học sinh, **67% giáo viên** (khoảng 2/3) xác nhận các công nghệ giám sát và giám thị này được dùng để xử phạt học sinh thay vì hỗ trợ an toàn; đồng thời học sinh khuyết tật và học sinh có hoàn cảnh khó khăn chịu tỷ lệ bị báo cáo kỷ luật cao hơn rõ rệt. Về mặt kỹ thuật, các kiểm thử độc lập cho thấy tỷ lệ thuật toán nhận diện khuôn mặt thất bại trên người da sẫm màu cao gấp nhiều lần so với người da sáng; dấy lên làn sóng phản đối từ hơn **4.000 sinh viên tại Đại học McGill** và **1.400 sinh viên tại Đại học British Columbia** yêu cầu nhà trường hủy bỏ hợp đồng với Proctorio.
- **Thời gian nghiên cứu / Sự kiện:** 2021 – 2022.
- **Nguồn kiểm chứng:** Báo cáo nghiên cứu độc lập của Center for Democracy & Technology (CDT) và điều tra công nghệ của MIT Technology Review:
  - 🔗 [Center for Democracy & Technology (CDT): Hidden Harms — The Misleading Promise of Monitoring Students Online (2022)](https://cdt.org/insights/hidden-harms-the-misleading-promise-of-monitoring-students-online/)
  - 🔗 [MIT Technology Review: AI proctoring software is failing students](https://www.technologyreview.com/2020/11/10/1011928/ai-proctoring-remote-learning-software-examity-proctorio-proctoru/)
  - 🔗 [NPR: Federal Judge Rules Room Scans For Online Tests Are Unconstitutional (Ogletree v. Cleveland State University, 2022)](https://www.npr.org/2022/08/25/1119337956/test-proctoring-room-scans-unconstitutional-cleveland-state-university)

#### 4. Harm Map Worksheet (11 Trường Phân Tích)

| STT | Trường thông tin (Harm Map Field) | Nội dung đánh giá chi tiết |
| :---: | :--- | :--- |
| **1** | **High-risk moment** | Trong suốt quá trình sinh viên làm bài thi trực tuyến tại nhà, phần mềm AI Proctorio liên tục quét webcam, micro và phân tích ánh mắt, khuôn mặt, tư thế ngồi để tự động tính điểm nghi ngờ gian lận (Suspicion Score) và gửi cờ cảnh báo (Flag) đến giám thị. |
| **2** | **Failure mode** | **Bias / fairness** *(kỳ thị chủng tộc & khuyết tật)* kết hợp **Privacy leak** *(xâm phạm đời tư)* và **Over-reliance** *(giám thị quá tin cờ đỏ của AI)*. |
| **3** | **Layer** | **Model & UX**:<br>• *Model layer:* Thuật toán nhận diện khuôn mặt thiếu dữ liệu người da sẫm màu; mô hình phát hiện bất thường coi cử động mắt/đầu không điển hình là dấu hiệu gian lận.<br>• *UX layer:* Giao diện tô đỏ điểm số "Suspicion Score" khiến giám thị phát sinh thiên kiến quy chụp (confirmation bias). |
| **4** | **Stakeholder** | • **Bên chịu tác động trực tiếp:** Sinh viên dự thi trực tuyến (đặc biệt là sinh viên da màu, học sinh khuyết tật/thần kinh đa dạng, học sinh nghèo không có phòng riêng).<br>• **Bên giám sát:** Giảng viên, giám thị coi thi.<br>• **Bên vận hành & Cung cấp:** Ban giám hiệu nhà trường, công ty phần mềm Proctorio Inc. |
| **5** | **Harm (Mẫu chuẩn)** | **[Sinh viên da màu và học sinh mắc hội chứng thần kinh đa dạng/ADHD]** bị **[hệ thống AI từ chối nhận diện khuôn mặt để vào thi hoặc liên tục gắn cờ gian lận oan uổng, dẫn đến bị hủy kết quả bài thi và khủng hoảng tâm lý nghiêm trọng]** khi **[họ có cử động mắt, thay đổi tư thế ngồi không điển hình hoặc thiếu điều kiện ánh sáng phòng theo tiêu chuẩn mà mô hình áp đặt]**. |
| **6** | **Harm lens** | **Dignity loss** *(tổn hại phẩm giá)*, **Privacy loss** *(mất riêng tư)* & **Opportunity loss** *(mất cơ hội thi cử)*. |
| **7** | **Severity** | **High** |
| **8** | **Scale** | **High** *(Hàng triệu sinh viên tại hơn 1.000 trường đại học trên thế giới sử dụng phần mềm; 67% giáo viên ghi nhận công cụ dùng để kỷ luật)* |
| **9** | **Probability** | **Medium to High** *(54% học sinh khuyết tật báo cáo bị hệ thống gắn cờ; lỗi nhận diện da màu diễn ra phổ biến trong ánh sáng yếu)* |
| **10** | **Frequency** | **High** *(Lặp lại trong từng phiên thi trực tuyến của mỗi kỳ thi học kỳ)* |
| **11** | **Vì sao? (Căn cứ đánh giá)** | • *Về Severity (High):* Vi phạm quyền riêng tư nghiêm trọng (Tòa án Liên bang Mỹ phán quyết vi phạm Hiến pháp Hoa Kỳ trong vụ án phòng ngủ sinh viên); hủy hoại tâm lý làm bài thi và dẫn đến việc bị hủy điểm môn học.<br>• *Về Scale (High) & Frequency (High):* Hệ thống chạy liên tục theo thời gian thực trên hàng triệu sinh viên qua mỗi kỳ thi.<br>• *Về Mode & Layer:* Mô hình (Model layer) áp đặt một chuẩn mực sinh học hẹp hòi (người da sáng, ngồi bất động tuyệt đối), kết hợp với UX kích hoạt tâm lý nghi ngờ của giám thị, dẫn đến sự kỳ thị kép về cả chủng tộc lẫn thể chất. |

---

## 4. Tổng kết & Bài học Thực thi cho Product Manager (AI EdTech)

Từ 3 case study và các bảng phân tích Harm Map trong ngành Giáo dục / AI Tutor, các nguyên tắc quản trị rủi ro AI bắt buộc phải áp dụng trong phát triển sản phẩm gồm:

1. **Không bao giờ áp dụng cơ chế tự động hóa hoàn toàn (Zero-touch) trong các quyết định High-stakes:** Mọi cảnh báo từ AI (như phát hiện đạo văn, gian lận, hạ điểm) chỉ được đóng vai trò là cờ tham vấn (*flagging heuristic*), quyết định cuối cùng bắt buộc phải qua quy trình đối chất và đánh giá sư phạm của con người (*Human-in-the-loop / Human review*).
2. **Kiểm thử độc lập định kiến dữ liệu (Disparate Impact Audit) trước khi triển khai:** Phải đo lường tỷ lệ lỗi phân loại nhầm (false-positive rates) trên các phân khúc người dùng yếu thế (người học phi bản ngữ, sinh viên da màu, người khuyết tật/thần kinh đa dạng) nhằm ngăn chặn việc trừng phạt người dùng dựa trên phong cách ngôn ngữ hay đặc tính sinh lý.
3. **Cải tiến thiết kế UX để chống Over-reliance:** Không bao giờ hiển thị điểm số khẳng định tuyệt đối (như "99% AI", "95% Cheating"). Giao diện phải đi kèm khoảng tin cậy (*confidence interval*), danh sách các nguyên nhân có thể gây dương tính giả, và nút chuyển giao (*Escalation flow*) dễ dàng để chuyển vụ việc cho hội đồng người thật xử lý.
4. **Minh bạch hóa cơ chế giải trình (Explainability & Contestability):** Người học phải luôn có quyền được giải thích lý do tại sao hệ thống đưa ra phán quyết và có kênh khiếu nại minh bạch, nhanh chóng khi nghi ngờ AI đưa ra kết quả sai lệch.
