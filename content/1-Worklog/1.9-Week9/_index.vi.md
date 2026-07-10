---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:
* Tìm hiểu dịch vụ AWS WAF để bảo vệ ứng dụng web khỏi các cuộc tấn công phổ biến.
* Cấu hình Web ACL và áp dụng AWS Managed Rules để chặn đứng các mối đe dọa.
* Thiết lập các custom rules (IP block, Rate-based, Geo-match) và cấu hình logging lên CloudWatch/S3.
* Quản lý tài nguyên AWS bằng thẻ tag (Resource Tagging) trên giao diện Console và AWS CLI.
* Thiết lập chính sách phân quyền IAM Policy dựa trên Tag (Attribute-Based Access Control) để kiểm soát quyền truy cập EC2.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - AWS WAF - Phần 1: Đọc Introduction & Overview, tạo Web ACL, áp dụng Managed Rules (Core Rule Set), cấu hình bảo vệ cơ bản cho ứng dụng web | 15/06/2026 | 15/06/2026 | <https://000026.awsstudygroup.com/> |
| 3 | - AWS WAF - Phần 2: Tạo Custom Rule (block specific IP, URI, header), Advanced Custom Rule (rate-based, geo-match, AND/OR logic), Testing New Rules | 16/06/2026 | 16/06/2026 | <https://000026.awsstudygroup.com/> |
| 4 | - AWS WAF - Phần 3: Cấu hình Logging requests (S3/CloudWatch), Review toàn bộ lab, test rule, Cleanup resources | 17/06/2026 | 17/06/2026 | <https://000026.awsstudygroup.com/> |
| 5 | - Managing Resources with Tags - Phần 1: Tạo và gán Tag cho nhiều resource (EC2, S3, VPC...), sử dụng Tag trên Console & AWS CLI | 18/06/2026 | 18/06/2026 | <https://000027.awsstudygroup.com/> |
| 6 | - Managing Resources with Tags - Phần 2: Tạo Resource Group theo Tag, quản lý nhóm resource, Review & Cleanup | 19/06/2026 | 19/06/2026 | <https://000027.awsstudygroup.com/> |
| 7 | - Manage Access to EC2 with Resource Tags through IAM: Tạo IAM Policy với condition Tag, tạo IAM Role, Switch Role, kiểm tra quyền EC2 theo Region (Tokyo & N.Virginia) | 20/06/2026 | 20/06/2026 | <https://000028.awsstudygroup.com/> |
| CN | - Tổng review & củng cố: Ôn lại toàn bộ 3 lab, so sánh cách dùng Tag, Cleanup tài nguyên, ghi chép best practices | 21/06/2026 | 21/06/2026 | Cả 3 link trên |

### Kết quả đạt được tuần 9:
* Triển khai thành công Web ACL bằng AWS WAF, áp dụng luật kiểm soát để ngăn chặn các kiểu tấn công web thông thường.
* Tạo thành công các custom rules bao gồm block IP, URI, rate-limiting bảo vệ máy chủ ứng dụng web.
* Cấu hình lưu trữ log truy cập AWS WAF và phân tích các request đáng ngờ.
* Quản trị tập trung tài nguyên AWS sử dụng Tags và phân loại nhóm tài nguyên bằng AWS Resource Groups.
* Xây dựng thành công chính sách bảo mật ABAC (Attribute-Based Access Control) cho EC2 thông qua IAM Policy kết hợp các điều kiện Tag chi tiết.
* Thực hiện dọn dẹp sạch toàn bộ tài nguyên thử nghiệm để kiểm soát chi phí.
