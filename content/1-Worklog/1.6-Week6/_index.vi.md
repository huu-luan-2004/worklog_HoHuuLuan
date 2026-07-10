---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:
* Tìm hiểu kiến trúc container serverless Amazon ECS, khởi tạo ECS Cluster, đăng ký Service Discovery với AWS Cloud Map và cấu hình Task Definition.
* Cấu hình Application Load Balancer (ALB) định tuyến microservices và khởi chạy dịch vụ ECS Services.
* Tìm hiểu và xây dựng các chu trình tích hợp/triển khai tự động CI/CD sử dụng GitLab, GitHub Actions và AWS CodeBuild.
* Triển khai giám sát chuyên sâu Container Insights và định tuyến log container sử dụng AWS FireLens và Fluent Bit.
* Tìm hiểu các tiêu chuẩn bảo mật đám mây (CIS, PCI DSS), kích hoạt và cấu hình AWS Security Hub để phân tích điểm bảo mật (Security Score).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Chuẩn bị môi trường, Khởi tạo ECS Cluster & Cấu hình Task Definition:<br>&emsp;+ Introduction & Preparation (Tìm hiểu kiến trúc Amazon ECS và chuẩn bị hạ tầng mạng, quyền hạn IAM)<br>&emsp;+ Prepare for deployment (Sắp xếp và kiểm tra các tài nguyên container trước khi đẩy lên đám mây)<br>&emsp;+ Register namespace in CloudMap (Đăng ký dịch vụ khám phá Service Discovery với AWS Cloud Map để các dịch vụ tự tìm thấy nhau)<br>&emsp;+ Create ECS Cluster (Khởi tạo cụm máy chủ ảo logic ECS làm môi trường chạy các ứng dụng)<br>&emsp;+ Create task definition (Định nghĩa cấu hình tài nguyên phần cứng, biến môi trường và Docker Image cho container) | 25/5/2026 | 25/5/2026 | <https://000016.awsstudygroup.com/1-introduction/><br><https://000016.awsstudygroup.com/2-preparation/><br><https://000016.awsstudygroup.com/3-prepare-for-deployment/><br><https://000016.awsstudygroup.com/4-register-namespace-in-cloudmap/><br><https://000016.awsstudygroup.com/5-create-ecs-cluster/><br><https://000016.awsstudygroup.com/6-create-task-definition/> |
| 3 | - Cấu hình Load Balancer, Khởi chạy dịch vụ ECS, Kiểm thử & Dọn dẹp:<br>&emsp;+ Configure ALB (Thiết lập bộ cân bằng tải Application Load Balancer để tiếp nhận và điều hướng luồng truy cập bên ngoài)<br>&emsp;+ Create ECS Services (Khởi chạy và duy trì số lượng container chạy ổn định theo cấu hình định sẵn từ Task Definition)<br>&emsp;+ Test result (Truy cập thông qua DNS của ALB để kiểm tra khả năng vận hành thực tế của ứng dụng microservices)<br>&emsp;+ Clean up (Tiến hành gỡ bỏ dịch vụ ECS Services, xóa ALB, Cloud Map và Cluster để đảm bảo tối ưu chi phí, tránh phát sinh hóa đơn ngoài ý muốn) | 26/5/2026 | 26/5/2026 | <https://000016.awsstudygroup.com/7-configure-alb/><br><https://000016.awsstudygroup.com/8-create-ecs-services/><br><https://000016.awsstudygroup.com/9-test-result/><br><https://000016.awsstudygroup.com/10-clean-up/> |
| 4 | - Tổng quan kiến trúc, Chuẩn bị & Thực hành Chu trình Tự động hóa CI/CD:<br>&emsp;+ Introduction & Preparation (Tìm hiểu tư duy tích hợp/triển khai tự động và chuẩn bị môi trường, phân quyền tài khoản)<br>&emsp;+ CICD GitLab (Thực hành viết file cấu hình để xây dựng pipeline tự động đóng gói và đẩy image từ GitLab CI/CD)<br>&emsp;+ CICD GitHub (Xây dựng chu trình tự động hóa tương tự sử dụng công cụ GitHub Actions)<br>&emsp;+ CICD CodeBuild (Sử dụng dịch vụ build mã nguồn chuyên dụng AWS CodeBuild để tối ưu hóa hiệu năng biên dịch trên đám mây) | 27/5/2026 | 27/5/2026 | <https://000017.awsstudygroup.com/1-introduction/><br><https://000017.awsstudygroup.com/2-preparation/><br><https://000017.awsstudygroup.com/3-cicd-gitlab/><br><https://000017.awsstudygroup.com/4-cicd-github/><br><https://000017.awsstudygroup.com/5-cicd-codebuild/> |
| 5 | - Giám sát chuyên sâu Container, Định tuyến Log nâng cao & Dọn dẹp:<br>&emsp;+ Monitoring with Container Insights (Bật tính năng thu thập chỉ số hiệu năng chi tiết của các cụm và tác vụ container bằng CloudWatch Container Insights)<br>&emsp;+ Logs router with FireLens (Sử dụng AWS FireLens kết hợp Fluent Bit để định tuyến, lọc và đẩy log từ container sang các kênh lưu trữ mong muốn một cách linh hoạt)<br>&emsp;+ Clean up (Thực hành quy trình xóa bỏ các pipeline thử nghiệm, hủy cấu hình định tuyến log và Container Insights để bảo mật tài khoản và tránh phát sinh chi phí phát sinh) | 28/5/2026 | 28/5/2026 | <https://000017.awsstudygroup.com/6-monitoring-with-container-insights/><br><https://000017.awsstudygroup.com/7-logs-router-with-firelens/><br><https://000017.awsstudygroup.com/8-clean-up/> |
| 6 | - Tìm hiểu tiêu chuẩn an ninh & Kích hoạt AWS Security Hub :<br>&emsp;+ Security standards (Tìm hiểu các tiêu chuẩn an ninh đám mây phổ biến như AWS Foundations Benchmark, CIS, PCI DSS và cách AWS đánh giá tuân thủ)<br>&emsp;+ Enable sec hub (Thực hành quy trình kích hoạt dịch vụ AWS Security Hub trên tài khoản và cấu hình thu thập dữ liệu an ninh từ các dịch vụ tích hợp) | 29/5/2026 | 29/5/2026 | <https://000018.awsstudygroup.com/1-security-standards/><br><https://000018.awsstudygroup.com/2-enable-sec-hub/> |
| 7 | - Phân tích điểm số bảo mật, Tối ưu cấu hình & Dọn dẹp hệ thống:<br>&emsp;+ Security score (Cách đọc hiểu bảng điều khiển - Dashboard, phân tích điểm số bảo mật phần trăm của tài khoản, nhận diện các lỗ hổng/cấu hình sai sót cần ưu tiên khắc phục)<br>&emsp;+ Cleanup (Thực hành quy trình tắt dịch vụ AWS Security Hub, xóa bỏ các dữ liệu kiểm tra cấu hình thử nghiệm để đưa tài khoản về trạng thái ban đầu và tránh phát sinh chi phí ngoài ý muốn) | 30/5/2026 | 30/5/2026 | <https://000018.awsstudygroup.com/3-security-score/><br><https://000018.awsstudygroup.com/4-cleanup/> |

### Kết quả đạt được tuần 6:
* Đã triển khai thành công ECS Cluster và Task Definition, tích hợp Service Discovery với AWS Cloud Map.
* Phân phối lưu lượng thành công cho ECS microservices thông qua Application Load Balancer (ALB).
* Tự động hóa thành công chu trình CI/CD build Docker Image bằng GitLab CI/CD, GitHub Actions và AWS CodeBuild.
* Thu thập chỉ số chi tiết qua Container Insights và định tuyến log qua AWS FireLens với Fluent Bit thành công.
* Kích hoạt và cấu hình thành công AWS Security Hub, phân tích Security Score và thực hiện dọn dẹp hạ tầng an toàn.

