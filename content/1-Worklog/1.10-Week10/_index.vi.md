---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:
* Tìm hiểu và cấu hình Amazon S3 Gateway Endpoint để kết nối an toàn từ VPC mà không qua Internet.
* Tìm hiểu và cấu hình Amazon S3 Interface Endpoint (AWS PrivateLink) cho truy cập từ môi trường On-Premises.
* Cấu hình Route 53 Resolver (Inbound/Outbound Endpoints) để giải quyết DNS lai (Hybrid DNS) giữa local và AWS.
* Áp dụng chính sách bảo mật S3 Bucket Policy để kiểm soát quyền truy cập chỉ cho phép từ VPC Endpoint.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan giải pháp, kiến trúc mạng kết nối S3 Endpoint và thiết lập môi trường giả lập (Prerequisites) | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Thực hành tạo và cấu hình S3 Gateway Endpoint, cập nhật bảng định tuyến Route Tables và kiểm tra kết nối từ EC2 | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Thiết lập môi trường On-Premises giả lập, cấu hình VPN/Routing và tạo S3 Interface Endpoint | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Cấu hình phân giải DNS chéo (Route 53 Resolver Endpoints) và các quy tắc chuyển tiếp DNS Rule | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Thực hành kiểm tra truy cập S3 từ máy chủ giả lập On-Premises thông qua PrivateLink và Route 53 | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7 | - Cấu hình bảo mật S3 Bucket Policy giới hạn truy cập qua Endpoint, tổng kiểm tra hiệu năng, bảo mật và dọn dẹp hệ thống | 27/06/2026 | 27/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 10:
* Triển khai thành công S3 Gateway Endpoint cho phép EC2 trong Private Subnet tải tệp tin an toàn lên S3.
* Cấu hình thành công S3 Interface Endpoint và định tuyến mạng lai từ môi trường cục bộ qua AWS.
* Thiết lập thành công hệ thống Hybrid DNS phân giải tên miền S3 riêng tư qua Route 53 Resolver Endpoints.
* Cấu hình thành công Bucket Policy hạn chế quyền truy cập chỉ cho phép lưu lượng đi qua VPC Endpoint chỉ định.
* Hoàn thành dọn dẹp sạch tài nguyên (xóa File Share, Gateway, Resolver Endpoints, VPC và EC2) tránh phát sinh chi phí.
