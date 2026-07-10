---
title: "Worklog Tuần 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:
* Hiểu và nắm vững chương trình AWS Free Tier, cách nhận credit và tránh các chi phí phát sinh ngoài ý muốn.
* Tìm hiểu và thực hành quản trị định danh và phân quyền với AWS IAM (User, Group, Policy, Role, Switch Role).
* Khởi tạo hạ tầng mạng VPC cơ bản, cấu hình tường lửa (Security Group, Network ACL) và tạo máy chủ EC2.
* Thực hành kết nối VPN Site-to-Site và tự động hóa hạ tầng (IaC), nắm vững quy trình dọn dẹp tài nguyên (Cleanup).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu tổng quan về cuộc cách mạng AWS Free Tier & Săn Credit:<br>&emsp;+ AWS Free Tier 2025 Revolution (Tổng quan chiến dịch)<br>&emsp;+ So sánh chi tiết Free Plan vs Paid Plan (Phân biệt quyền lợi)<br>&emsp;+ Chiến lược nhận đủ 200$ Credit (Các bước chuẩn bị)<br>&emsp;+ Hướng dẫn chi tiết 5 nhiệm vụ kiếm tiền (Thực hiện task nhận thưởng)<br>&emsp;+ Danh sách "sát thủ" Credit cần tránh (Nhận diện các dịch vụ dễ gây mất tiền oan) | 20/4/2026 | 20/4/2026 | <https://000001.awsstudygroup.com/1-aws-free-tier-2025-revolution/><br><https://000001.awsstudygroup.com/2-so-s%C3%A1nh-chi-ti%E1%BA%BFt-free-plan-vs-paid-plan/><br><https://000001.awsstudygroup.com/3-chi%E1%BA%BFn-l%C6%B0%E1%BB%A3n-nh%E1%BA%ADn-%C4%91%E1%BB%A7-200-credit/><br><https://000001.awsstudygroup.com/4-h%C6%B0%E1%BB%9Bng-d%E1%BA%ABn-chi-ti%E1%BA%BFt-5-nhi%E1%BB%87m-v%E1%BB%A5-ki%E1%BA%BFm-ti%E1%BB%81n/><br><https://000001.awsstudygroup.com/5-danh-s%C3%A1ch-s%C3%A1t-th%E1%BB%A7-credit-c%E1%BA%A7n-tr%C3%A1nh/> |
| 3 | - Triển khai kiến trúc mẫu, Giám sát chi phí & Lập lộ trình:<br>&emsp;+ Kiến trúc mẫu với 200$ Credit (Xây dựng hệ thống tối ưu với số vốn được cấp)<br>&emsp;+ Monitoring và tối ưu chi phí (Cài đặt cảnh báo, quản lý ngân sách)<br>&emsp;+ FAQ - Giải đáp mọi thắc mắc thường gặp<br>&emsp;+ Roadmap học AWS với Free Tier (Lập lộ trình học tập lâu dài)<br>&emsp;+ Tổng kết và Next Steps (Các bước hành động tiếp theo) | 21/4/2026 | 21/4/2026 | <https://000001.awsstudygroup.com/6-ki%E1%BA%BFn-tr%C3%BAc-m%E1%BA%ABu-v%E1%BB%9Bi-200-credit/><br><https://000001.awsstudygroup.com/7-monitoring-v%C3%A0-t%E1%BB%91i-%C6%B0u-chi-ph%C3%AD/><br><https://000001.awsstudygroup.com/8-faq---gi%E1%BA%A3i-%C4%91%C3%A1p-m%E1%BB%8Di-th%E1%BA%AFc-m%E1%BA%AFc/><br><https://000001.awsstudygroup.com/9-roadmap-h%E1%BB%8Dc-aws-v%E1%BB%9Bi-free-tier/><br><https://000001.awsstudygroup.com/10-t%E1%BB%95ng-k%E1%BA%BFt-v%C3%A0-next-steps/> |
| 4 | - Quản lý người dùng và Phân quyền cơ bản với AWS IAM:<br>&emsp;+ Create Admin User and Group (Hướng dẫn tạo tài khoản quản trị viên và nhóm người dùng)<br>&emsp;+ Thực hành thiết lập chính sách (Policies) để giới hạn hoặc cấp quyền truy cập tài nguyên cho nhóm Admin thay vì sử dụng tài khoản Root | 22/4/2026 | 22/4/2026 | <https://000002.awsstudygroup.com/1-create-admin-user-and-group/> |
| 5 | - Cơ chế ủy quyền nâng cao với AWS Role:<br>&emsp;+ AWS Role (Tìm hiểu khái niệm IAM Role và các trường hợp áp dụng cấp quyền tạm thời)<br>&emsp;+ Switch Roles (Thực hành cơ chế chuyển đổi giữa các Roles để quản lý tài nguyên linh hoạt và an toàn)<br>&emsp;+ Đánh giá ưu điểm bảo mật của Role so với việc dùng Access Key tĩnh | 23/4/2026 | 23/4/2026 | <https://000002.awsstudygroup.com/2-aws-role/><br><https://000002.awsstudygroup.com/3-switch-roles/> |
| 6 | - Tổng quan kiến trúc, Bảo mật VPC & Khởi tạo máy chủ:<br>&emsp;+ Introduce (Giới thiệu tổng quan về mô hình kiến trúc và mục tiêu bài học)<br>&emsp;+ Firewall in VPC (Tìm hiểu và thiết lập tường lửa trong mạng VPC, quản lý Security Groups và Network ACLs)<br>&emsp;+ Prerequisite (Kiểm tra và thiết lập các điều kiện tiên quyết trước khi cấu hình)<br>&emsp;+ Create EC2 Server (Thực hành khởi tạo máy chủ ảo EC2 nằm trong hạ tầng mạng an toàn) | 24/4/2026 | 24/4/2026 | <https://000003.awsstudygroup.com/1-introduce/><br><https://000003.awsstudygroup.com/2-firewallinvpc/><br><https://000003.awsstudygroup.com/3-prerequisite/><br><https://000003.awsstudygroup.com/4-createec2server/> |
| 7 | - Kết nối mạng nâng cao, Tự động hóa hạ tầng & Dọn dẹp:<br>&emsp;+ VPN Site-to-Site (Tìm hiểu lý thuyết và thực hành kết nối mạng bảo mật mã hóa Site-to-Site VPN)<br>&emsp;+ Cleanup (Thực hành quy trình dọn dẹp, xóa bỏ các tài nguyên mạng và máy chủ nâng cao để tránh phát sinh chi phí ngoài ý muốn)<br>&emsp;+ Infrastructure as Code - IaC (Quản lý, định nghĩa và tự động hóa việc khởi tạo hạ tầng AWS bằng mã nguồn)<br>&emsp;+ Tổng kết toàn bộ tiến độ | 25/4/2026 | 25/4/2026 | <https://000003.awsstudygroup.com/5-vpnsitetosite/><br><https://000003.awsstudygroup.com/6-cleanup/><br><https://000003.awsstudygroup.com/7-infrastructureascode/> |

### Kết quả đạt được tuần 1:
* Đã hoàn thành tìm hiểu về AWS Free Tier, nhận diện các dịch vụ dễ phát sinh chi phí và thiết lập hệ thống cảnh báo ngân sách.
* Khởi tạo thành công tài khoản Admin User, Group và thực hiện phân quyền thông qua IAM Policies.
* Hiểu cấu trúc và thực hành chuyển đổi IAM Role để nâng cao bảo mật hệ thống.
* Thiết lập thành công tường lửa trong VPC và tạo máy chủ EC2 an toàn.
* Cấu hình kết nối VPN Site-to-Site thành công và áp dụng Infrastructure as Code (IaC) để quản lý hạ tầng.
* Thực hiện dọn dẹp tài nguyên (Cleanup) đúng quy trình để tránh phát sinh chi phí ngoài ý muốn.


