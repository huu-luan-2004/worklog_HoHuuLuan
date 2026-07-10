---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:
* Lập kế hoạch kiến trúc mạng và hạ tầng triển khai dự án thực tế trên AWS.
* Cấu hình môi trường mạng VPC, Security Groups, IAM Roles và bảo mật truy cập.
* Khởi tạo cơ sở dữ liệu Amazon RDS phục vụ lưu trữ dữ liệu ứng dụng.
* Đóng gói ứng dụng thành Docker Container, đẩy hình ảnh lên Amazon ECR.
* Triển khai container chạy thực tế bằng Amazon ECS (Fargate) kết hợp ALB (Application Load Balancer) để phân tải lưu lượng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Lập kế hoạch kiến trúc hệ thống mạng, hạ tầng, vẽ sơ đồ kết nối và tạo các IAM Roles cần thiết | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Cấu hình mạng VPC (Public/Private Subnets), Internet Gateway, NAT Gateway và các bảng định tuyến Route Tables | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Khởi tạo và thiết lập database Amazon RDS (PostgreSQL/MySQL), cấu hình Security Groups chặn các truy cập ngoài hệ thống | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Thực hiện build Docker Image ứng dụng, khởi tạo Amazon ECR repository và push Docker Image lên ECR | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Khởi tạo Amazon ECS Cluster, định nghĩa Task Definition cấu hình CPU/RAM và khởi tạo Service chạy ECS Fargate | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7 | - Triển khai Application Load Balancer (ALB), cấu hình Target Group trỏ về ECS Service và cấu hình Route 53 map domain riêng | 04/07/2026 | 04/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| CN | - Viết script CI/CD (GitHub Actions / GitLab CI) tự động đóng gói và cập nhật ECS Service khi có code mới | 05/07/2026 | 05/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 11:
* Xây dựng thành công bản vẽ kiến trúc mạng dự án chuẩn hóa AWS Well-Architected Framework.
* Khởi tạo thành công VPC phân tách mạng rạch ròi giữa Public Subnet (chứa ALB) và Private Subnet (chứa ECS, RDS).
* Triển khai thành công database RDS và kết nối an toàn từ ECS container qua Security Groups nội bộ.
* Đóng gói mã nguồn thành công và lưu trữ an toàn trong Amazon ECR.
* Triển khai thành công container chạy không máy chủ (Serverless Container) qua Amazon ECS Fargate, phân tải tự động qua ALB ổn định.
* Tích hợp thành công pipeline CI/CD tự động hóa toàn bộ luồng cập nhật ứng dụng.
