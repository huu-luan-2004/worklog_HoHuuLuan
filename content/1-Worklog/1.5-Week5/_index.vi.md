---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:
* Tìm hiểu giải pháp sao lưu tập trung AWS Backup, cấu hình kế hoạch tự động (Backup Plan) và cảnh báo trạng thái.
* Thực hiện kiểm thử quy trình phục hồi dữ liệu từ bản sao lưu và dọn dẹp tài nguyên.
* Thực hành quy trình di chuyển máy chủ VM Import/Export giữa môi trường ảo hóa cục bộ và đám mây AWS.
* Triển khai thử nghiệm ứng dụng Docker cục bộ (local) và chuẩn bị hạ tầng AWS (RDS, EC2) tương ứng.
* Đóng gói mã nguồn thành Docker Image, viết Docker Compose quản lý đa container và đưa ứng dụng chạy thực tế trên đám mây.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan giải pháp, Điều kiện tiên quyết & Thiết lập kế hoạch sao lưu:<br>&emsp;+ Introduce (Tìm hiểu tổng quan về giải pháp quản lý sao lưu dữ liệu tập trung với AWS Backup)<br>&emsp;+ Prerequisite (Thực hiện các bước chuẩn bị tài nguyên nền tảng và phân quyền IAM cho dịch vụ sao lưu)<br>&emsp;+ Create Backup Plan (Thực hành thiết lập kế hoạch sao lưu tự động: cấu hình tần suất, thời gian lưu trữ - Retention period)<br>&emsp;+ Enable Noti (Cấu hình bật tính năng gửi thông báo tự động về trạng thái của các tác vụ sao lưu thành công hoặc thất bại) | 18/5/2026 | 18/5/2026 | <https://000013.awsstudygroup.com/1-introduce/><br><https://000013.awsstudygroup.com/2-prerequiste/><br><https://000013.awsstudygroup.com/3-createbackupplan/><br><https://000013.awsstudygroup.com/4-enablenoti/> |
| 3 | - Kiểm thử quy trình khôi phục & Dọn dẹp tài nguyên hệ thống:<br>&emsp;+ Test Restore (Thực hành quy trình giả lập sự cố mất dữ liệu, tiến hành khôi phục dữ liệu từ các bản sao lưu có sẵn để kiểm tra tính toàn vẹn và sẵn sàng của hệ thống)<br>&emsp;+ Cleanup (Quy trình dọn dẹp, xóa bỏ các Backup Plans, các bản Recovery Points thử nghiệm và tài nguyên liên quan để tránh phát sinh chi phí ngoài ý muốn) | 19/5/2026 | 19/5/2026 | <https://000013.awsstudygroup.com/5-testrestore/><br><https://000013.awsstudygroup.com/6-cleanup/> |
| 4 | - Triển khai máy chủ ứng dụng & Thực hành Import máy chủ ảo lên Cloud:<br>&emsp;+ Deploy Application Server (Thực hành các bước triển khai và cấu hình một máy chủ chạy ứng dụng thực tế)<br>&emsp;+ Import VM to AWS (Tìm hiểu quy trình và thực hành di chuyển, chuyển đổi file ảnh đĩa của máy chủ ảo - Virtual Machine từ môi trường local lên thành một Amazon EC2 Instance) | 20/5/2026 | 20/5/2026 | <https://000014.awsstudygroup.com/1-deploy-application-server/><br><https://000014.awsstudygroup.com/2-import-vm-to-aws/> |
| 5 | - Thực hành Export máy chủ ảo, Xem video trực quan & Dọn dẹp tài nguyên:<br>&emsp;+ Export VM from AWS (Thực hành quy trình ngược lại, xuất bản một EC2 Instance hiện có thành file định dạng VM để chạy offline ở hạ tầng nội bộ)<br>&emsp;+ Video (Theo dõi video hướng dẫn từng bước và lưu ý quan trọng để củng cố các kỹ thuật Import/Export VM)<br>&emsp;+ Clean up (Tiến hành quy trình dọn dẹp hệ thống, xóa bỏ các tệp tin ảnh đĩa, terminate các instance thử nghiệm để tối ưu chi phí) | 21/5/2026 | 21/5/2026 | <https://000014.awsstudygroup.com/3-export-vm-from-aws/><br><https://000014.awsstudygroup.com/4-video/><br><https://000014.awsstudygroup.com/5-clean-up/> |
| 6 | - Tổng quan kiến trúc, Chạy thử local & Cấu hình hạ tầng AWS:<br>&emsp;+ Introduction (Tìm hiểu mục tiêu và kiến trúc kết hợp giữa Docker và hạ tầng AWS Cloud)<br>&emsp;+ Deploy local (Thực hành triển khai và chạy thử nghiệm ứng dụng chạy ổn định ở môi trường máy cá nhân)<br>&emsp;+ Preparation (Chuẩn bị mạng, Security Group và các tài nguyên nền tảng trên AWS)<br>&emsp;+ Configure RDS (Khởi tạo và cấu hình hệ quản trị cơ sở dữ liệu Amazon RDS bảo mật)<br>&emsp;+ Configure EC2 (Chuẩn bị máy chủ ảo EC2 sẵn sàng để cài đặt môi trường chạy Docker) | 22/5/2026 | 22/5/2026 | <https://000015.awsstudygroup.com/1-introduction/><br><https://000015.awsstudygroup.com/2-deploy-local/><br><https://000015.awsstudygroup.com/3-preparation/><br><https://000015.awsstudygroup.com/4-configure-rds/><br><https://000015.awsstudygroup.com/5-configure-ec2/> |
| 7 | - Đóng gói Docker, Triển khai ứng dụng lên Cloud & Dọn dẹp :<br>&emsp;+ Docker image (Thực hành viết Dockerfile để đóng gói mã nguồn ứng dụng thành Image)<br>&emsp;+ Docker compose (Sử dụng Docker Compose để định nghĩa và quản lý đa container một cách có hệ thống)<br>&emsp;+ Push image (Thực hành đẩy Image lên kho lưu trữ và kéo về triển khai chạy thực tế trên máy chủ EC2 kết nối với RDS)<br>&emsp;+ Clean up (Quy trình dọn dẹp triệt để các container, xóa database RDS và terminate máy chủ EC2 để tránh phát sinh chi phí) | 23/5/2026 | 23/5/2026 | <https://000015.awsstudygroup.com/6-docker-image/><br><https://000015.awsstudygroup.com/7-docker-compose/><br><https://000015.awsstudygroup.com/8-push-image/><br><https://000015.awsstudygroup.com/9-clean-up/> |

### Kết quả đạt được tuần 5:
* Thiết lập thành công AWS Backup Plan và cấu hình thông báo trạng thái qua SNS.
* Thực hiện khôi phục thành công máy chủ ảo từ các điểm khôi phục (Recovery Points) thử nghiệm.
* Di chuyển thành công tệp đĩa VM cục bộ thành EC2 Instance và xuất EC2 Instance thành file đĩa VM.
* Xây dựng thành công ứng dụng Docker chạy cục bộ và chuẩn bị hạ tầng mạng, RDS, EC2 tương ứng trên đám mây.
* Đóng gói mã nguồn thành Docker Image, quản lý bằng Docker Compose và đẩy lên máy chủ EC2 chạy thực tế kết nối database RDS.
* Thực hiện dọn dẹp các container, database RDS và terminate EC2 Instance tối ưu hóa hóa đơn AWS.

