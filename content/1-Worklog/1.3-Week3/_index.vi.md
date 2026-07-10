---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:
* Tìm hiểu công cụ AWS Budgets và thiết lập các loại ngân sách cơ bản để kiểm soát chi phí thực tế và dự báo.
* Cấu hình giám sát ngân sách dành cho các gói cam kết sử dụng (Reserved Instances và Savings Plans).
* Tìm hiểu và triển khai thu thập chỉ số hiệu năng (Metrics) và nhật ký hoạt động (Logs) với Amazon CloudWatch.
* Thiết lập hệ thống cảnh báo (Alarms) tự động và xây dựng bảng điều khiển (Dashboards) trực quan hóa dữ liệu hạ tầng.
* Phân biệt các gói hỗ trợ AWS Support plans và thực hành quy trình quản lý, tạo các ca hỗ trợ kỹ thuật (Support Cases).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan công cụ AWS Budgets & Thiết lập các dạng ngân sách cơ bản:<br>&emsp;+ Create Budget (Tìm hiểu tổng quan giao diện và các bước khởi tạo một ngân sách cảnh báo chi phí ban đầu)<br>&emsp;+ Cost Budgets (Thực hành cấu hình ngân sách dựa trên số tiền tiêu thụ thực tế hoặc dự báo để nhận thông báo qua Email/SNS)<br>&emsp;+ Usage Budget (Thực hành thiết lập giới hạn và giám sát tần suất sử dụng các tài nguyên cụ thể của AWS) | 4/5/2026 | 4/5/2026 | <https://000007.awsstudygroup.com/1-create-budget/><br><https://000007.awsstudygroup.com/2-cost-budgets/><br><https://000007.awsstudygroup.com/3-usage-budget/> |
| 3 | - Cấu hình ngân sách tối ưu cam kết & Quy trình dọn dẹp:<br>&emsp;+ Reservation Budget (Tìm hiểu và thiết lập ngân sách theo dõi tỷ lệ sử dụng/độ bao phủ của các tài nguyên đã mua trước - Reserved Instances)<br>&emsp;+ Saving Plans Budget (Cấu hình giám sát ngân sách dành riêng cho các gói tiết kiệm chi phí linh hoạt Savings Plans)<br>&emsp;+ Clean up (Thực hành quy trình xóa bỏ các cấu hình kiểm soát ngân sách hoặc tài nguyên thử nghiệm để tránh bị ảnh hưởng đến hệ thống thực tế) | 5/5/2026 | 5/5/2026 | <https://000007.awsstudygroup.com/4-reservation-budget/><br><https://000007.awsstudygroup.com/5-saving-plans-budget/><br><https://000007.awsstudygroup.com/6-clean-up/> |
| 4 | - Tổng quan giám sát, Các bước chuẩn bị & Quản lý dữ liệu hệ thống:<br>&emsp;+ Introduction (Tìm hiểu tổng quan về vai trò của công cụ giám sát và quản lý tài nguyên Amazon CloudWatch)<br>&emsp;+ Preparatory steps (Thực hiện các cấu hình nền tảng, phân quyền IAM cần thiết trước khi thu thập dữ liệu)<br>&emsp;+ CloudWatch Metric (Thực hành giám sát, phân tích các chỉ số hiệu năng hệ thống như CPU, RAM, Network của tài nguyên)<br>&emsp;+ CloudWatch Logs (Cấu hình thu thập, lưu trữ và truy vấn tập trung nhật ký hoạt động từ ứng dụng và máy chủ) | 6/5/2026 | 6/5/2026 | <https://000008.awsstudygroup.com/1-introduction/><br><https://000008.awsstudygroup.com/2-preparatory-steps/><br><https://000008.awsstudygroup.com/3-cloud-watch-metric/><br><https://000008.awsstudygroup.com/4-cloud-watch-logs/> |
| 5 | - Thiết lập cảnh báo, Trực quan hóa hạ tầng & Dọn dẹp hệ thống:<br>&emsp;+ CloudWatch Alarm (Thực hành tạo các ngưỡng cảnh báo tự động gửi thông báo khi tài nguyên gặp sự cố hoặc quá tải)<br>&emsp;+ CloudWatch Dashboard (Tự tay thiết kế bảng điều khiển trực quan hóa dữ liệu giúp theo dõi toàn diện trạng thái hệ thống)<br>&emsp;+ Clean up resources (Quy trình dọn dẹp, xóa bỏ các cấu hình Alarms, Dashboards và Logs Streams thử nghiệm để tránh phát sinh chi phí ngoài ý muốn) | 7/5/2026 | 7/5/2026 | <https://000008.awsstudygroup.com/5-cloud-watch-alarm/><br><https://000008.awsstudygroup.com/6-cloud-watch-dashboard/><br><https://000008.awsstudygroup.com/7-clean-up-resources/> |
| 6 | - Tìm hiểu tổng quan các gói hỗ trợ và Cách tiếp cận AWS Support:<br>&emsp;+ Support plans (Phân biệt chi tiết quyền lợi, thời gian phản hồi và chi phí của các gói hỗ trợ AWS: Basic, Developer, Business, Enterprise On-Ramp, Enterprise)<br>&emsp;+ Access support (Hướng dẫn cách truy cập vào trung tâm hỗ trợ AWS Support Center thông qua Console) | 8/5/2026 | 8/5/2026 | <https://000009.awsstudygroup.com/1-support-plans/><br><https://000009.awsstudygroup.com/2-access-support/> |
| 7 | - Thực hành quy trình tạo và Quản lý các ca hỗ trợ:<br>&emsp;+ Manage cases (Thực hành các bước mở một Support Case mới về lỗi kỹ thuật hoặc yêu cầu tăng hạn mức tài nguyên - Service Limit Increase)<br>&emsp;+ Tìm hiểu cách theo dõi tiến độ phản hồi, giao tiếp với kỹ sư AWS và quy trình đóng/mở lại (reopen) các case hỗ trợ khi cần thiết<br>&emsp;+ Tổng kết toàn bộ nội dung giai đoạn | 9/5/2026 | 9/5/2026 | <https://000009.awsstudygroup.com/3-manage-cases/> |

### Kết quả đạt được tuần 3:
* Tạo và thiết lập thành công các bộ ngân sách theo dõi chi phí thực tế và cảnh báo dự báo qua Email/SNS.
* Cấu hình thành công Reservation Budget và Saving Plans Budget giúp theo dõi chi phí mua trước tối ưu.
* Thu thập thành công các chỉ số hiệu năng phần cứng và tập trung hóa nhật ký ứng dụng vào CloudWatch Logs.
* Thiết lập thành công các ngưỡng cảnh báo tự động (Alarms) gửi thông báo về SNS và thiết kế Dashboard trực quan hóa hạ tầng hoàn chỉnh.
* Nắm vững cách phân loại các gói hỗ trợ khách hàng của AWS và thực hành gửi yêu cầu, tương tác hỗ trợ qua AWS Support Center thành công.

