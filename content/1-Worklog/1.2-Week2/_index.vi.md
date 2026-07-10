---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:
* Tìm hiểu và thực hành khởi tạo máy chủ EC2 (Windows & Linux), nắm bắt vòng đời và cơ chế quản lý máy chủ.
* Thực hành kết nối SSH/RDP để quản trị hệ thống máy chủ, giám sát hiệu năng và quản lý chi phí EC2.
* Triển khai kiến trúc kết nối ứng dụng web (EC2) với cơ sở dữ liệu quan hệ (Amazon RDS), thực hiện sao lưu/sao chụp dữ liệu.
* Thiết lập hệ thống chịu lỗi và tự động co giãn bằng cách kết hợp Application Load Balancer (ALB) và Auto Scaling Group (ASG).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan kiến trúc, Điều kiện tiên quyết & Khởi tạo máy chủ EC2:<br>&emsp;+ Introduce (Giới thiệu tổng quan về mục tiêu thực hành EC2)<br>&emsp;+ Prerequisite (Thiết lập các điều kiện cần thiết: Key Pair, Security Group trước khi tạo máy chủ)<br>&emsp;+ Launch Windows Instance (Thực hành các bước khởi tạo máy chủ ảo chạy hệ điều hành Windows)<br>&emsp;+ Launch Linux Instance (Thực hành các bước khởi tạo máy chủ ảo chạy hệ điều hành Linux)<br>&emsp;+ Amazon EC2 Basic (Nắm vững các khái niệm căn bản về quản lý trạng thái, vòng đời của một instance) | 27/4/2026 | 27/4/2026 | <https://000004.awsstudygroup.com/1-introduce/><br><https://000004.awsstudygroup.com/2-prerequiste/><br><https://000004.awsstudygroup.com/3-launchwindowsinstance/><br><https://000004.awsstudygroup.com/4-launchlinuxinstance/><br><https://000004.awsstudygroup.com/5-amazonec2basic/> |
| 3 | - Quản trị hệ thống máy chủ, Kiểm soát chi phí & Dọn dẹp tài nguyên:<br>&emsp;+ AWS FCJ Management - Linux (Thực hành quản trị, kết nối SSH và cấu hình ứng dụng trên môi trường Linux)<br>&emsp;+ AWS FCJ Management - Windows (Thực hành kết nối RDP và quản lý hệ thống trên môi trường Windows)<br>&emsp;+ Cost Usage & Governance (Tìm hiểu các nguyên tắc quản trị, giám sát hiệu năng và tối ưu chi phí sử dụng EC2)<br>&emsp;+ Cleanup (Thực hành quy trình Terminate các instance và xóa tài nguyên đi kèm để tránh phát sinh chi phí ngoài ý muốn) | 28/4/2026 | 28/4/2026 | <https://000004.awsstudygroup.com/6-awsfcjmanagement-linux/><br><https://000004.awsstudygroup.com/7-awsfcjmanagement-windows/><br><https://000004.awsstudygroup.com/8-costusagegovernance/><br><https://000004.awsstudygroup.com/9-cleanup/> |
| 4 | - Tổng quan, Chuẩn bị điều kiện & Khởi tạo hạ tầng:<br>&emsp;+ Introduce (Tìm hiểu tổng quan về kiến trúc kết nối giữa ứng dụng và cơ sở dữ liệu)<br>&emsp;+ Prerequisite (Thiết lập các điều kiện cần thiết: Security Group cho phép kết nối chéo, Subnet Group)<br>&emsp;+ Create EC2 (Khởi tạo máy chủ ảo EC2 đóng vai trò Application Server làm môi trường chạy source code)<br>&emsp;+ Create RDS (Khởi tạo cơ sở dữ liệu quan hệ Amazon RDS - MySQL/PostgreSQL làm Database Server) | 29/4/2026 | 29/4/2026 | <https://000005.awsstudygroup.com/1-introduce/><br><https://000005.awsstudygroup.com/2-prerequiste/><br><https://000005.awsstudygroup.com/3-create-ec2/><br><https://000005.awsstudygroup.com/4-create-rds/> |
| 5 | - Triển khai ứng dụng, Quản lý sao lưu & Dọn dẹp hệ thống:<br>&emsp;+ Deploy App (Thực hành kết nối ứng dụng chạy trên EC2 với cơ sở dữ liệu RDS và kiểm tra vận hành thực tế)<br>&emsp;+ Backup (Tìm hiểu cơ chế sao lưu, tạo Snapshots để bảo vệ an toàn dữ liệu hệ thống)<br>&emsp;+ Cleanup (Quy trình dọn dẹp, xóa bỏ database instance RDS và terminate máy chủ EC2 tránh phát sinh chi phí ngoài ý muốn) | 30/4/2026 | 30/4/2026 | <https://000005.awsstudygroup.com/5-deploy-app/><br><https://000005.awsstudygroup.com/6-backup/><br><https://000005.awsstudygroup.com/7-cleanup/> |
| 6 | - Tổng quan kiến trúc, Chuẩn bị & Thiết lập Cân bằng tải:<br>&emsp;+ Introduction (Tìm hiểu tổng quan về kiến trúc mở rộng và khả năng chịu lỗi của hệ thống)<br>&emsp;+ Preparation (Thực hiện các bước chuẩn bị cấu hình mạng và tài nguyên nền tảng)<br>&emsp;+ Create Launch Template (Thực hành tạo mẫu cấu hình khởi tạo máy chủ hàng loạt)<br>&emsp;+ Setup Load Balancer (Khởi tạo và cấu hình bộ cân bằng tải Load Balancer để phân phối lưu lượng truy cập) | 1/5/2026 | 1/5/2026 | <https://000006.awsstudygroup.com/1-introduction/><br><https://000006.awsstudygroup.com/2-preparation/><br><https://000006.awsstudygroup.com/3-create-launch-template/><br><https://000006.awsstudygroup.com/4-setup-load-balancer/> |
| 7 | - Cấu hình Auto Scaling, Kiểm thử hệ thống & Dọn dẹp tài nguyên:<br>&emsp;+ Test (Kiểm tra hoạt động độc lập của Load Balancer trước khi tích hợp co giãn)<br>&emsp;+ Create Auto Scaling Group (Thực hành khởi tạo nhóm tự động co giãn ASG dựa trên Launch Template)<br>&emsp;+ Test Solutions (Giả lập các kịch bản quá tải hoặc lỗi máy chủ để kiểm thử tính năng tự động mở rộng và tự phục hồi)<br>&emsp;+ Cleanup (Quy trình dọn dẹp, xóa bỏ ASG, Load Balancer để tránh phát sinh chi phí ngoài ý muốn) | 2/5/2026 | 2/5/2026 | <https://000006.awsstudygroup.com/5-test/><br><https://000006.awsstudygroup.com/6-create-auto-scaling-group/><br><https://000006.awsstudygroup.com/7-test-solutions/><br><https://000006.awsstudygroup.com/8-cleanup/> |

### Kết quả đạt được tuần 2:
* Khởi tạo thành công các máy chủ ảo EC2 chạy hệ điều hành Windows và Linux.
* Kết nối quản trị máy chủ qua SSH (Linux) và RDP (Windows) thành công, cấu hình ứng dụng và kiểm soát tài nguyên.
* Triển khai thành công kiến trúc kết nối ứng dụng (EC2) tới cơ sở dữ liệu (RDS - MySQL/PostgreSQL), tạo snapshot sao lưu dữ liệu.
* Thiết lập hệ thống cân bằng tải (ALB) và nhóm tự động co giãn (ASG) hoạt động ổn định.
* Đã kiểm thử thành công khả năng tự động co giãn và phục hồi của hệ thống khi có sự cố giả lập, sau đó tiến hành dọn dẹp sạch tài nguyên.

