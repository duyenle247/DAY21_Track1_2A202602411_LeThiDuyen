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

## 3. Danh mục 3 Brief Case Nghiên cứu Thực tế

Dưới đây là 3 case study có thật trong ngành Giáo dục & AI Tutor, đại diện cho 3 lát cắt rủi ro then chốt: **Định kiến công cụ phát hiện AI (AI Detection Bias)**, **Sự cố thuật toán chuẩn hóa điểm thi (Algorithmic Grading Failure)**, và **Hệ thống giám thị thi AI xâm phạm quyền riêng tư & phân biệt đối xử (AI Proctoring & Surveillance Risk)**.

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

---

## 4. Tổng kết & Bài học Thực thi cho Product Manager (AI EdTech)

Từ 3 case study thực tế trong ngành Giáo dục / AI Tutor, các nguyên tắc quản trị rủi ro AI bắt buộc phải áp dụng trong phát triển sản phẩm gồm:

1. **Không bao giờ áp dụng cơ chế tự động hóa hoàn toàn (Zero-touch) trong các quyết định High-stakes:** Mọi cảnh báo từ AI (như phát hiện đạo văn, gian lận, hạ điểm) chỉ được đóng vai trò là cờ tham vấn (*flagging heuristic*), quyết định cuối cùng bắt buộc phải qua quy trình đối chất và đánh giá sư phạm của con người (*Human-in-the-loop / Human review*).
2. **Kiểm thử độc lập định kiến dữ liệu (Disparate Impact Audit) trước khi triển khai:** Phải đo lường tỷ lệ lỗi phân loại nhầm (false-positive rates) trên các phân khúc người dùng yếu thế (người học phi bản ngữ, sinh viên da màu, người khuyết tật/thần kinh đa dạng) nhằm ngăn chặn việc trừng phạt người dùng dựa trên phong cách ngôn ngữ hay đặc tính sinh lý.
3. **Minh bạch hóa cơ chế giải trình (Explainability & Contestability):** Người học phải luôn có quyền được giải thích lý do tại sao hệ thống đưa ra phán quyết và có kênh khiếu nại minh bạch, nhanh chóng khi nghi ngờ AI đưa ra kết quả sai lệch.
