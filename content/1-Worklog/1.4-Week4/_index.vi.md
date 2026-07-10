---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
* Tìm hiểu giải pháp quản lý truy cập và thực hành kết nối an toàn qua Remote Desktop Gateway (RD GW).
* Triển khai dịch vụ định danh Active Directory (AD) và cấu hình hệ thống phân giải tên miền hỗn hợp Hybrid DNS.
* Thực hành cài đặt AWS CLI và xây dựng chuỗi dịch vụ nâng cao tích hợp S3 (lưu trữ) và SNS (thông báo).
* Cấu hình phân quyền nâng cao (IAM Policies), phân chia hệ thống mạng, khởi tạo EC2 và học cách Troubleshoot xử lý lỗi.
* Thiết lập kiểm soát truy cập theo thời gian (Time-based Access Control) và quản lý chính sách tự định nghĩa (Customer Managed Policies).
* Tìm hiểu các API của IAM Identity Center và thực hiện quy trình dọn dẹp sạch tài nguyên (Cleanup).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan kiến trúc, Điều kiện tiên quyết & Kết nối hệ thống:<br>&emsp;+ Introduce (Giới thiệu tổng quan về giải pháp quản lý truy cập và kiến trúc hệ thống)<br>&emsp;+ Prerequisite (Thiết lập các điều kiện hạ tầng cần thiết và cấu hình mạng nền tảng)<br>&emsp;+ Connect to RD GW (Thực hành kết nối bảo mật vào hệ thống thông qua Remote Desktop Gateway) | 11/5/2026 | 11/5/2026 | <https://000010.awsstudygroup.com/1-introduce/><br><https://000010.awsstudygroup.com/2-prerequiste/><br><https://000010.awsstudygroup.com/3-connecttordgw/> |
| 3 | - Cấu hình Active Directory, Hybrid DNS & Quy trình dọn dẹp:<br>&emsp;+ Setup AD (Thực hành các bước triển khai và cấu hình dịch vụ thư mục định danh Active Directory)<br>&emsp;+ Setup Hybrid DNS (Xây dựng và cấu hình hệ thống phân giải tên miền hỗn hợp giữa môi trường On-Premises và AWS Cloud)<br>&emsp;+ Cleanup (Thực hành quy trình gỡ bỏ các dịch vụ Directory, DNS Inbound/Outbound Endpoints và các tài nguyên đi kèm để tránh phát sinh chi phí) | 12/5/2026 | 12/5/2026 | <https://000010.awsstudygroup.com/4-setupad/><br><https://000010.awsstudygroup.com/5-setuphyriddns/><br><https://000010.awsstudygroup.com/6-cleanup/> |
| 4 | - Cài đặt công cụ, Khởi tạo hạ tầng, Lưu trữ & Cấu hình thông báo:<br>&emsp;+ Introduce (Giới thiệu tổng quan nội dung thực hành chuỗi dịch vụ nâng cao)<br>&emsp;+ Prerequisite (Các bước chuẩn bị môi trường và phân quyền tài khoản trước khi lab)<br>&emsp;+ Install CLI (Thực hành cài đặt và cấu hình công cụ giao diện dòng lệnh AWS CLI)<br>&emsp;+ Infras (Xây dựng nền móng cấu trúc hạ tầng cơ bản ban đầu)<br>&emsp;+ S3 (Triển khai, cấu hình và thao tác trên dịch vụ lưu trữ đối tượng Amazon S3)<br>&emsp;+ SNS (Cấu hình dịch vụ thông báo đơn giản Amazon SNS để quản lý luồng gửi tin nhắn) | 13/5/2026 | 13/5/2026 | <https://000011.awsstudygroup.com/1-introduce/><br><https://000011.awsstudygroup.com/2-prerequiste/><br><https://000011.awsstudygroup.com/3-installcli/><br><https://000011.awsstudygroup.com/4-infras/><br><https://000011.awsstudygroup.com/5-s3/><br><https://000011.awsstudygroup.com/6-sns/> |
| 5 | - Quản lý phân quyền, Hệ thống mạng, Máy chủ, Fix lỗi & Dọn dẹp:<br>&emsp;+ IAM (Thực hành thiết lập chính sách bảo mật và phân quyền nâng cao cho các dịch vụ)<br>&emsp;+ Network (Cấu hình chi tiết phân vùng mạng, subnets và định tuyến luồng dữ liệu)<br>&emsp;+ Bài 9: EC2 (Triển khai máy chủ ảo EC2 tích hợp đồng bộ vào hệ thống hạ tầng mạng đã tạo)<br>&emsp;+ Troubleshoot (Học phương pháp kiểm tra log, phân tích nguyên nhân và xử lý các lỗi thường gặp trong quá trình lab)<br>&emsp;+ Cleanup (Quy trình dọn dẹp triệt để tất cả tài nguyên máy chủ, mạng, lưu trữ vừa tạo để tránh phát sinh chi phí) | 14/5/2026 | 14/5/2026 | <https://000011.awsstudygroup.com/7-iam/><br><https://000011.awsstudygroup.com/8-network/><br><https://000011.awsstudygroup.com/9-ec2/><br><https://000011.awsstudygroup.com/10-troubleshoot/><br><https://000011.awsstudygroup.com/11-cleanup/> |
| 6 | - Chuẩn bị môi trường & Cấu hình kiểm soát truy cập nâng cao:<br>&emsp;+ Prerequisite (Thực hiện các bước chuẩn bị hệ thống và thiết lập quyền hạn ban đầu trước khi lab)<br>&emsp;+ AWS CLI Access (Thực hành cấu hình và kiểm tra quyền truy cập tài nguyên thông qua giao diện dòng lệnh AWS CLI)<br>&emsp;+ Using Time-based Access Control (Triển khai chính sách bảo mật kiểm soát quyền truy cập dựa trên thời gian thực tế để giới hạn khung giờ thao tác của User) | 15/5/2026 | 15/5/2026 | <https://000012.awsstudygroup.com/1-prerequisite/><br><https://000012.awsstudygroup.com/2-aws-cli-access/><br><https://000012.awsstudygroup.com/3-using-time-based-access-control/> |
| 7 | - Quản trị chính sách tự định nghĩa, Tích hợp API & Dọn dẹp hệ thống:<br>&emsp;+ Using Customer Managed Policies (Thực hành tự viết và quản lý các chính sách phân quyền tùy biến theo nhu cầu doanh nghiệp)<br>&emsp;+ IAM Identity Center Identity Store APIs (Tìm hiểu và thực hành tương tác với các APIs của Identity Store để quản lý danh tính tập trung)<br>&emsp;+ Clean up (Quy trình kiểm tra và xóa bỏ hoàn toàn các cấu hình chính sách, quyền truy cập nâng cao đã tạo nhằm đảm bảo an toàn tài khoản và tránh phát sinh chi phí ngoài ý muốn) | 16/5/2026 | 16/5/2026 | <https://000012.awsstudygroup.com/4-using-customer-managed-policies/><br><https://000012.awsstudygroup.com/%CC%805-iam-identity-center-identity-store-apis/><br><https://000012.awsstudygroup.com/6-clean-up/> |

### Kết quả đạt được tuần 4:
* Kết nối từ xa thành công qua Remote Desktop Gateway trên môi trường bảo mật.
* Triển khai thành công Active Directory, cấu hình phân giải Hybrid DNS giữa Cloud và On-Premises.
* Cài đặt thành công AWS CLI và khởi tạo lưu trữ S3, đăng ký dịch vụ thông báo SNS thành công.
* Thực hiện cấu hình mạng, phân quyền và triển khai EC2, biết cách phân tích log xử lý lỗi (Troubleshoot).
* Triển khai chính sách giới hạn giờ truy cập Time-based Access Control và thiết lập các Customer Managed Policies tùy biến an toàn.
* Tích hợp thành công các API quản lý định danh của IAM Identity Center và thực hiện dọn dẹp hạ tầng an toàn.

