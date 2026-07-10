---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:
* Tìm hiểu và cấu hình Network ACL cấp độ subnet để bảo mật kiểm soát lưu lượng Inbound/Outbound.
* Thiết lập liên kết VPC Peering kết nối 2 mạng VPC độc lập và cấu hình Route Tables, DNS private.
* Tìm hiểu và cấu hình Transit Gateway để kết nối đa VPC tập trung theo mô hình Hub-and-Spoke.
* Triển khai giải pháp Serverless tự động tắt/bật EC2 Instance bằng AWS Lambda và Amazon EventBridge (CloudWatch Events).
* Viết code Lambda (Python/Node.js sử dụng AWS SDK), cấu hình IAM Role, kiểm thử và thực hiện dọn dẹp tài nguyên (Cleanup).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan kiến trúc, Điều kiện tiên quyết & Cấu hình kiểm soát mạng:<br>&emsp;+ Introduce (Tìm hiểu tổng quan về kiến trúc kết nối đa mạng VPC và các thành phần bảo mật mạng)<br>&emsp;+ Prerequisite (Thực hiện các bước chuẩn bị khởi tạo 2 vùng mạng VPC độc lập và tài nguyên máy chủ để thử nghiệm)<br>&emsp;+ Update network ACL (Thực hành cấu hình luật Inbound/Outbound trên Network ACL để kiểm soát tường lửa ở cấp độ Subnet) | 8/6/2026 | 8/6/2026 | <https://000019.awsstudygroup.com/1-introduce/><br><https://000019.awsstudygroup.com/2-prerequiste/><br><https://000019.awsstudygroup.com/3-updatenetworkacl/> |
| 3 | - Đấu nối mạng VPC Peering, Cấu hình định tuyến, DNS & Dọn dẹp:<br>&emsp;+ VPC Peering (Thực hành thiết lập liên kết VPC Peering Connection giữa 2 vùng mạng độc lập để giao tiếp nội bộ)<br>&emsp;+ Route Tables (Cấu hình và cập nhật bảng định tuyến Route Tables giúp các gói tin đi qua cổng kết nối Peering chính xác)<br>&emsp;+ Cross peer DNS (Cấu hình tính năng phân giải tên miền qua lại giữa các vùng mạng để máy chủ gọi nhau bằng DNS private)<br>&emsp;+ Cleanup (Quy trình gỡ bỏ liên kết Peering, khôi phục Route Tables, NACL và xóa các VPC thử nghiệm để tối ưu chi phí) | 2/6/2026 | 3/6/2026 | <https://000019.awsstudygroup.com/4-vpcpeering/><br><https://000019.awsstudygroup.com/5-routetables/><br><https://000019.awsstudygroup.com/6-crosspeerdns/><br><https://000019.awsstudygroup.com/7-cleanup/> |
| 4 | - Tổng quan giải pháp, Điều kiện tiên quyết & Khởi tạo Transit Gateway:<br>&emsp;+ Introduce (Tìm hiểu về mô hình Hub-and-Spoke và vai trò của Transit Gateway trong việc thay thế mạng lưới VPC Peering phức tạp)<br>&emsp;+ Prerequisite (Khởi tạo các mạng VPC thành phần và máy chủ EC2 để làm môi trường mô phỏng)<br>&emsp;+ Transit Gateway (Thực hành các bước cấu hình và khởi tạo bộ định tuyến trung tâm Transit Gateway trên AWS Console) | 4/6/2026 | 4/6/2026 | <https://000020.awsstudygroup.com/1-introduce/><br><https://000020.awsstudygroup.com/2-prerequiste/><br><https://000020.awsstudygroup.com/3-transitgateway/> |
| 5 | - Đấu nối hệ thống mạng, Cấu hình định tuyến, Kiểm tra kết quả & Dọn dẹp:<br>&emsp;+ Transit Gateway Attachments (Thực hành đấu nối các mạng VPC đơn lẻ vào cổng trung tâm Transit Gateway)<br>&emsp;+ Route Table (Cấu hình bảng định tuyến cho Transit Gateway và các VPC để luồng dữ liệu đi đúng hướng)<br>&emsp;+ Result (Thực hiện ping/kiểm tra kết nối giữa các máy chủ thuộc các VPC khác nhau thông qua mạng nội bộ đám mây)<br>&emsp;+ Cleanup (Quy trình gỡ bỏ các liên kết Attachment, xóa Transit Gateway và các VPC thử nghiệm để đưa hệ thống về trạng thái ban đầu, tránh phát sinh chi phí) | 5/6/2026 | 5/6/2026 | <https://000020.awsstudygroup.com/4-transigatewayattachments/><br><https://000020.awsstudygroup.com/5-routetable/><br><https://000020.awsstudygroup.com/6-result/><br><https://000020.awsstudygroup.com/7-cleanup/> |
| 6 | - Tổng quan kiến trúc, Điều kiện tiên quyết & Cấu hình phân quyền hệ thống:<br>&emsp;+ Introduce (Tìm hiểu ý tưởng thiết kế giải pháp dùng Serverless để tối ưu chi phí vận hành máy chủ EC2 tự động)<br>&emsp;+ Prerequisite (Khởi tạo sẵn các máy chủ ảo EC2 thử nghiệm làm môi trường đích cho hệ thống điều khiển)<br>&emsp;+ Create Tag for Instance (Thực hành thiết lập chiến lược gắn thẻ - Tagging, ví dụ Auto-Stop, để hàm điều khiển nhận diện đúng mục tiêu)<br>&emsp;+ Create Role for Lambda (Cấu hình chính sách bảo mật IAM Role, cấp quyền cho phép hàm Lambda có thể can thiệp trạng thái Start/Stop của máy chủ EC2) | 6/6/2026 | 6/6/2026 | <https://000022.awsstudygroup.com/1-introduce/><br><https://000022.awsstudygroup.com/2-prerequiste/><br><https://000022.awsstudygroup.com/3-createtagforinstance/><br><https://000022.awsstudygroup.com/4-createroleforlambda/> |
| 7 | - Viết code Lambda, Kiểm thử tự động hóa & Dọn dẹp tài nguyên:<br>&emsp;+ Create Lambda Function (Thực hành tạo hàm Lambda, viết mã nguồn (Python/Node.js) sử dụng thư viện SDK để quét tag và ra lệnh cho máy chủ)<br>&emsp;+ Testing Results (Tiến hành chạy thử nghiệm - Test Execution, kiểm tra log trên CloudWatch và xác nhận trạng thái các máy chủ EC2 thay đổi tự động thành công)<br>&emsp;+ Cleanup (Thực hành quy trình xóa bỏ hàm Lambda, hủy IAM Role và terminate các máy chủ EC2 thử nghiệm để làm sạch tài khoản, tránh phát sinh chi phí ngoài ý muốn) | 8/6/2026 | 8/6/2026 | <https://000022.awsstudygroup.com/5-createlambdafunction/><br><https://000022.awsstudygroup.com/6-testingresults/><br><https://000022.awsstudygroup.com/7-cleanup/> |

### Kết quả đạt được tuần 7:
* Đã cấu hình thành công Network ACL chặn và lọc lưu lượng truy cập ở cấp độ Subnet bảo mật.
* Thiết lập thành công liên kết VPC Peering giữa 2 VPC riêng biệt, hỗ trợ định tuyến và phân giải DNS Private chéo.
* Đã đấu nối 3 VPC vào Transit Gateway, định cấu hình bảng định tuyến định tuyến lưu lượng tập trung Hub-and-Spoke thành công.
* Xây dựng thành công hệ thống tự động hóa Serverless: Tạo tag Auto-Stop cho EC2 và cấp quyền IAM Role đầy đủ cho Lambda.
* Viết thành công code Lambda tương tác AWS SDK thực thi Start/Stop EC2 theo tag và kiểm thử hoạt động tự động thành công qua CloudWatch.
* Thực hiện dọn dẹp sạch Lambda, IAM Role, VPC Peering, Transit Gateway và các VPC/EC2 Instance thử nghiệm.

