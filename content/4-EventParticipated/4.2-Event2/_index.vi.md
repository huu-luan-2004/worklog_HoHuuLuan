---
title: "Event 2"
date: 2026-06-13
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch: “GenAI-powered App-DB Modernization workshop”

### Mục tiêu sự kiện (Event Objectives)

- Chia sẻ các thực hành tốt nhất (best practices) trong thiết kế ứng dụng hiện đại, giải bài toán dịch chuyển từ kiến trúc cũ sang đám mây.
- Giới thiệu Thiết kế hướng miền (Domain-Driven Design - DDD), kiến trúc hướng sự kiện (event-driven architecture), và mô hình DevOps thực tế.
- Cung cấp hướng dẫn lựa chọn dịch vụ tính toán (compute services) phù hợp (EC2, ECS, Fargate, Lambda) và hệ sinh thái công cụ hiện đại.
- Định hình tư duy cốt lõi về mối quan hệ giữa "Làm Người - Làm Nghề - Làm Dân" trong kỷ nguyên số cùng các công cụ GenAI hỗ trợ vòng đời phát triển phần mềm (SDLC).

### Diễn giả (Speakers)

- **Jignesh Shah** – Director, Open Source Databases
- **Erica Liu** – Sr. GTM Specialist, AppMod
- **Fabrianne Effendi** – Assc. Specialist SA, Serverless Amazon Web Services
- **Danh Hoàng Hiếu Nghị** – AI Engineer, AWS Community Builder, AWS Student Builder Group Leader
- **Trọng H. Trương** – DevOps Engineer @ Endava Vietnam
- **Cường Nguyễn & Đạt Phạm** – Data Analytics Engineers / Chuyên gia văn hóa & chuỗi cung ứng doanh nghiệp đa quốc gia

### Điểm nhấn chính (Key Highlights)

#### Nhận diện những hạn chế của kiến trúc ứng dụng cũ (Legacy) và Vai trò Data Analytics

- Chu kỳ phát hành sản phẩm kéo dài → Gây thất thoát doanh thu, giảm GMV (Gross Merchandise Value) và bỏ lỡ cơ hội thị trường.  
- Vận hành kém hiệu quả → Giảm năng suất, thiếu tư duy phản biện khi phân tích số liệu cải thiện hệ thống, chi phí hạ tầng tăng cao.  
- Không tuân thủ các quy định bảo mật → Nguy cơ rò rỉ dữ liệu nghiêm trọng, tổn hại uy tín doanh nghiệp trên quy mô toàn cầu.  

#### Transitioning to modern application architecture – Microservices & DevOps

Dịch chuyển sang hệ thống mô-đun hóa — nơi mỗi chức năng là một dịch vụ độc lập giao tiếp bất đồng bộ qua sự kiện (events) và được vận hành bằng tư duy DevOps tự động hóa:
- Quản lý hàng đợi (Queue Management) & CI/CD Pipelines: Tự động hóa quy trình Build, Test, Deploy liên tục.  
- Chiến lược bộ nhớ đệm (Caching Strategy) & Containerization: Ứng dụng Docker/Kubernetes giúp tối ưu hiệu năng và cô lập tài nguyên.  
- Xử lý thông điệp (Message Handling) & IaC (Infrastructure as Code): Định nghĩa hạ tầng bằng mã, quản lý cấu hình linh hoạt.  

#### Domain-Driven Design (DDD) và Case Study Thực tế

- Phương pháp 4 bước cốt lõi: Xác định sự kiện miền (domain events) → Sắp xếp dòng thời gian → Xác định tác nhân (actors) → Định nghĩa bối cảnh giới hạn (bounded contexts).  
- Case study Nhà sách (Bookstore) & Hệ thống vận hành: Minh họa cách phân rã nghiệp vụ phức tạp của hệ thống lớn.  
- Bản đồ bối cảnh (Context mapping): 7 mô hình mẫu kết nối các bounded contexts, tạo ra sự ăn khớp giữa luồng dữ liệu kỹ thuật và dòng chảy vận hành của doanh nghiệp.  

#### Kiến trúc hướng sự kiện (Event-Driven Architecture)

- 3 mô hình tích hợp chủ đạo: Publish/Subscribe (Xuất bản/Đăng ký), Point-to-point (Điểm - Điểm), Streaming (Luồng dữ liệu liên tục).  
- Lợi ích thực tế: Giảm tối đa sự phụ thuộc (loose coupling), nâng cao khả năng mở rộng (scalability) và khả năng phục hồi tự động khi có lỗi (resilience).  
- So sánh Sync vs Async: Đánh đổi kỹ thuật rõ ràng; áp dụng văn hóa No-Blame Post-Mortem khi hệ thống xảy ra sự cố (tập trung tìm lỗi gốc rễ thay vì đổ lỗi cho kỹ sư).  

#### Sự tiến hóa của dịch vụ tính toán (Compute Evolution)

- Mô hình trách nhiệm chung (Shared Responsibility Model): Tiến trình phát triển hạ tầng từ EC2 (Máy ảo) → ECS/Fargate (Containers) → Lambda (Serverless).  
- Serverless & Triết lý Tối ưu: Loại bỏ gánh nặng quản lý máy chủ, tự động mở rộng theo thời gian thực, chi trả tối ưu 100% dựa trên giá trị sử dụng.  
- Functions vs Containers: Lựa chọn dựa trên đặc thù công việc: kiến trúc vi mô, tác vụ chạy nhanh dùng Functions; hệ thống phức tạp, trạng thái lâu dài dùng Containers.  

#### Amazon Q Developer và GenAI trong SDLC

- Tự động hóa toàn diện: Hỗ trợ tăng tốc toàn bộ vòng đời phần mềm (SDLC) từ lập kế hoạch, viết code chuẩn hóa, tối ưu hóa câu lệnh cho tới bảo trì.  
- Code Transformation & Modernization: Trợ lý đắc lực trong nâng cấp Java, hiện đại hóa .NET và hỗ trợ dịch chuyển các hệ thống VMware, Mainframe lên đám mây.  
- Sử dụng AI thông minh: Khai thác tối đa sức mạnh GenAI để bứt phá năng suất cá nhân nhưng luôn giữ vững kiến thức nền tảng vững chắc (Fundamentals) để không "tắt đi tư duy của bộ não".  

### Bài học cốt lõi (Key Takeaways)

#### Tư duy thiết kế (Design Mindset)

- Tiếp cận hướng nghiệp vụ trước tiên (Business-first approach): Hệ thống sinh ra để giải quyết bài toán nghiệp vụ, công nghệ chỉ là công cụ hỗ trợ.  
- Ngôn ngữ chung (Ubiquitous language): Thu hẹp khoảng cách từ vựng giữa đội ngũ kinh doanh (Business) và kỹ thuật (Tech). Xây dựng môi trường hòa hợp văn hóa doanh nghiệp (Caring & Inclusive).  
- Học hỏi & Kiến tạo tiêu chuẩn: Bài học từ mô hình Wakon Yosai của Nhật Bản (Hòa hồn Dương tài) và mô hình Chaebol của Hàn Quốc — làm chủ kỹ nghệ phương Tây, tuân thủ nghiêm ngặt chuẩn quốc tế khắt khe nhất nhưng giữ vững bản sắc nội tại.  

#### Kiến trúc kỹ thuật (Technical Architecture)

- Kỹ thuật Event Storming: Phương pháp trực quan kết nối chuyên gia nghiệp vụ và kỹ sư để mô hình hóa nhanh chóng toàn bộ quy trình.  
- Ưu tiên giao tiếp bất đồng bộ: Giảm các cuộc gọi đồng bộ trực tiếp không cần thiết để tránh lỗi domino làm sập toàn bộ hệ thống.  
- Làm chủ nền tảng cốt lõi (Fundamentals): Các công cụ thay đổi liên tục theo thời gian (Tool landscape dịch chuyển rất nhanh), nhưng nền tảng về Linux, Networking cơ bản, Git, Python, Golang và cấu trúc ứng dụng là những giá trị cốt lõi không thay đổi.  

#### Chiến lược hiện đại hóa (Modernization Strategy)

- Tiếp cận theo lộ trình bài bản: Sự tiến hóa hạ tầng của một quốc gia từ "cô lập" sang "đổi mới phá băng" và "Internet gõ cửa" (1975 - 1997) tương tự như lộ trình nâng cấp hệ thống công nghệ thông tin. Cần chia nhỏ theo các giai đoạn rõ ràng thay vì dịch chuyển ồ ạt một cách nóng vội.  
- Mô hình 7Rs & Chuỗi Domino số: Tận dụng làn sóng hạ tầng số (Cloud, 4G, Smartphone) để kiến tạo các Factory số (Digital Factory).  
- Quy trình tuyển dụng chuẩn tại các Tập đoàn lớn (MNCs): Áp dụng quy trình 4 bước ngặt nghèo (Sàng lọc hồ sơ bằng ATS -> Test năng lực/Logic thuật toán -> Phỏng vấn chuyên môn đào sâu bài toán bằng mô hình STAR -> Đánh giá sự tương thích về giá trị cốt lõi).  

### Áp dụng vào công việc (Applying to Work)

- Áp dụng DDD & Tổ chức Event Storming: Lên kế hoạch phối hợp chặt chẽ với các phòng ban nghiệp vụ để bóc tách rõ ranh giới các dịch vụ (Bounded Contexts) cho dự án hiện tại.  
- Cải tiến mô hình DevOps: Không chỉ dừng lại ở việc copy-paste các câu lệnh tự động hóa, cần chủ động tìm hiểu sâu nguyên nhân gốc rễ, đặt câu hỏi "Tại sao" trước khi tìm giải pháp "Làm thế nào". Giao tiếp tốt với đội ngũ phát triển và không biến mình thành "người hùng sửa lỗi hệ thống lúc nửa đêm".  
- Triển khai kiến trúc hướng sự kiện & Serverless: Thử nghiệm thay thế các API đồng bộ sang hàng đợi tin nhắn bất đồng bộ, pilot các dịch vụ AWS Lambda cho các tác vụ xử lý độc lập.  
- Tận dụng GenAI hợp lý: Sử dụng Amazon Q Developer để tăng tốc viết code, rà soát lỗi nhưng liên tục trau dồi kỹ năng cơ bản để làm chủ công nghệ.  
- Tham gia Cộng đồng Công nghệ: Kết nối sâu rộng với hệ sinh thái thông qua các chương trình hành trình như AWS Community Builder, First Cloud AI Journey, và AWS Student Builder Groups để liên tục nâng cấp bản thân và học hỏi từ các chuyên gia.  

### Trải nghiệm tại sự kiện (Event Experience)

Chuỗi sự kiện workshop và meetup “GenAI-powered App-DB Modernization” đã mang lại những trải nghiệm vô cùng thực tế, mở rộng góc nhìn toàn diện từ kỹ thuật chuyên sâu cho đến văn hóa làm việc toàn cầu:

#### Học hỏi từ các chuyên gia giàu kinh nghiệm
- Cơ hội quý giá khi được nghe chia sẻ trực tiếp từ các kỹ sư, AWS Community Builders hàng đầu về các bài học xương máu (Things learned the hard way) khi vận hành hệ thống lớn trong thực tế.  
- Các bài học giúp tôi hiểu rằng giao tiếp hiệu quả và thấu hiểu bài toán chung chiếm một phần cực kỳ quan trọng trong công việc của một kỹ sư công nghệ.  

#### Tiếp cận kỹ thuật và tư duy thực tế
- Được trải nghiệm cách tư duy phản biện, cách phân tích "kể chuyện với dữ liệu" nhằm tìm ra điểm nghẽn của hệ thống kinh doanh.  
- Thực hành phân rã hệ thống Microservices thông qua mô hình hóa sự kiện miền, nắm rõ ranh giới trách nhiệm khi xử lý sự cố.  

#### Khai thác các công cụ hiện đại và GenAI
- Trực tiếp nhìn thấy bức tranh toàn cảnh về hệ sinh thái công cụ hiện đại (Tool Landscape) đồ sộ và cách ứng dụng linh hoạt GenAI để bứt phá năng suất lao động trong kỷ nguyên số.  

#### Kết nối và phát triển cộng đồng
- Môi trường thảo luận cởi mở giúp thắt chặt vòng kết nối trên mạng lưới chuyên nghiệp (LinkedIn), thúc đẩy tinh thần học hỏi không ngừng (Be curious and keep learning).  
- Giúp reshaping lại hoàn toàn hệ tư duy, thấm nhuần triết lý ứng dụng vào đời sống và công việc: "Làm Người - Làm Nghề - Làm Dân" để sẵn sàng trở thành một nhân tố chất lượng cao, đáp ứng mọi tiêu chuẩn quốc tế khắt khe nhất.  
 

> **Tổng kết**: Sự kiện đã vượt ra khỏi giới hạn của một buổi chia sẻ công nghệ đơn thuần. Đây là bệ phóng tư duy quan trọng, giúp tôi định hình lại toàn diện từ cách thiết kế hệ thống, tối ưu hóa hạ tầng DevOps, cho tới kỹ năng mềm và tinh thần trách nhiệm cần có để sải bước tự tin trong môi trường công nghệ toàn cầu.
