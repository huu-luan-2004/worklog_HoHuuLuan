---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:
* Tìm hiểu và cấu hình các dịch vụ Storage Gateway kết nối lưu trữ cục bộ với đám mây AWS.
* Tìm hiểu và kích hoạt các tính năng Data Deduplication để tiết kiệm dung lượng lưu trữ.
* Cấu hình và kích hoạt Shadow Copies hỗ trợ người dùng tự khôi phục tệp tin.
* Quản trị phiên làm việc, phân bổ hạn ngạch lưu trữ (Quotas) và mở rộng dung lượng tệp tin.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng quan, Chuẩn bị môi trường & Triển khai cấu hình dịch vụ nền tảng:<br>&emsp;+ Tổng quan nội dung bài thực hành và sơ đồ kiến trúc hệ thống.<br>&emsp;+ Cấu hình các điều kiện tiên quyết (Prerequisites), phân quyền IAM và mạng cơ bản.<br>&emsp;+ Khởi tạo và thiết lập các tài nguyên phần cứng hoặc dịch vụ lưu trữ cốt lõi.<br>&emsp;+ Cấu hình chi tiết các tham số vận hành và liên kết các thành phần hệ thống.<br>&emsp;+ Tích hợp logic xử lý hoặc thiết lập các chính sách bảo mật đi kèm. | 08/06/2026 | 08/06/2026 | <https://000023.awsstudygroup.com/1/><br><https://000023.awsstudygroup.com/2/><br><https://000023.awsstudygroup.com/3/><br><https://000023.awsstudygroup.com/4/><br><https://000023.awsstudygroup.com/5/> |
| 3 | - Hoàn thiện cấu hình nâng cao, Kiểm thử kết quả & Dọn dẹp tài nguyên:<br>&emsp;+ Triển khai các thành phần mở rộng hoặc giao diện quản trị.<br>&emsp;+ Thực hành kiểm thử hiệu năng, kiểm tra log hệ thống để xác nhận kết quả hoạt động.<br>&emsp;+ Đánh giá tối ưu hóa hệ thống và tổng kết các lưu ý kỹ thuật quan trọng.<br>&emsp;+ Quy trình dọn dẹp (Cleanup), xóa bỏ toàn bộ các tài nguyên thử nghiệm để tối ưu chi phí và tránh phát sinh hóa đơn ngoài ý muốn. | 09/06/2026 | 09/06/2026 | <https://000023.awsstudygroup.com/6/><br><https://000023.awsstudygroup.com/7/><br><https://000023.awsstudygroup.com/8/><br><https://000023.awsstudygroup.com/9/> |
| 4 | - Chuẩn bị hạ tầng & Khởi tạo AWS Storage Gateway:<br>&emsp;+ Prepare (Thiết lập môi trường giả lập On-Premises, cấu hình tài nguyên mạng và chuẩn bị quyền truy cập IAM cần thiết)<br>&emsp;+ Use AWS Storage Gateway (Thực hành triển khai, kích hoạt Storage Gateway và cấu hình kết nối lưu trữ giữa môi trường cục bộ với đám mây AWS) | 10/06/2026 | 10/06/2026 | <https://000024.awsstudygroup.com/1-prepare/><br><https://000024.awsstudygroup.com/2-useawsstoragegw/> |
| 5 | - Kiểm thử quy trình lưu trữ & Dọn dẹp hệ thống:<br>&emsp;+ Cleanup (Thực hành kiểm tra tính toàn vẹn của dữ liệu đồng bộ, sau đó thực hiện quy trình gỡ bỏ Gateway, xóa các File Share và tài nguyên thử nghiệm để tránh phát sinh chi phí phát sinh) | 11/06/2026 | 11/06/2026 | <https://000024.awsstudygroup.com/3-cleanup/> |
| 6 | - Khởi tạo, Kiểm thử hiệu năng & Cấu hình tính năng tối ưu dữ liệu (Bài 1 - 7):<br>&emsp;+ Introduce & Prerequisite (Tổng quan giải pháp lưu trữ và chuẩn bị môi trường mạng, quyền hạn)<br>&emsp;+ Create new file shares (Thực hành tạo mới các vùng chia sẻ tệp tin để kết nối dữ liệu)<br>&emsp;+ Test performance & Monitor performance (Đo đạc tốc độ đọc/ghi và cấu hình giám sát hiệu năng hệ thống)<br>&emsp;+ Enable data dedup (Kích hoạt tính năng chống trùng lặp dữ liệu - Data Deduplication để tiết kiệm không gian lưu trữ)<br>&emsp;+ Enable shadow copies (Cấu hình tính năng sao chép bóng Shadow Copies giúp người dùng tự khôi phục các phiên bản tệp tin cũ) | 12/06/2026 | 12/06/2026 | <https://000025.awsstudygroup.com/1-introduce/><br><https://000025.awsstudygroup.com/2-prerequiste/><br><https://000025.awsstudygroup.com/3-create-new-file-shares/><br><https://000025.awsstudygroup.com/4-test-performance/><br><https://000025.awsstudygroup.com/5-monitor-performance/><br><https://000025.awsstudygroup.com/6-enable-data-dedup/><br><https://000025.awsstudygroup.com/7-enable-shadow-copies/> |
| 7 | - Quản trị truy cập, Mở rộng quy mô, Thao tác CLI & Dọn dẹp hệ thống:<br>&emsp;+ Manage user sessions open files (Quản lý các phiên làm việc của người dùng và giám sát trạng thái các tệp tin đang mở)<br>&emsp;+ Enable quotas (Thiết lập hạn ngạch lưu trữ - Quotas để giới hạn dung lượng sử dụng cho từng thư mục/đối tượng)<br>&emsp;+ Enable Continuous Access share (Kích hoạt tính năng chia sẻ liên tục sẵn sàng - Continuously Available Shares nhằm tăng độ ổn định)<br>&emsp;+ Scale throughput capacity & Scale storage capacity (Thực hành nâng cấp băng thông xử lý và mở rộng linh hoạt dung lượng ổ đĩa trực tuyến)<br>&emsp;+ Delete environment (Quy trình gỡ bỏ, giải phóng môi trường thử nghiệm để tối ưu chi phí tài khoản)<br>&emsp;+ Using CLI (Củng cố và thực hành lại các thao tác quản trị tài nguyên lưu trữ bằng công cụ dòng lệnh AWS CLI) | 13/06/2026 | 13/06/2026 | <https://000025.awsstudygroup.com/8-manage-user-sessions-open-files/><br><https://000025.awsstudygroup.com/9-enable-quotas/><br><https://000025.awsstudygroup.com/10-enable-ca-share/><br><https://000025.awsstudygroup.com/11-scale-throughput-capacity/><br><https://000025.awsstudygroup.com/12-scale-storage-capacity/><br><https://000025.awsstudygroup.com/13-delete-environment/><br><https://000025.awsstudygroup.com/14-usingcli/> |

### Kết quả đạt được tuần 8:
* Cấu hình thành công các dịch vụ hạ tầng phần cứng và dịch vụ lưu trữ cốt lõi.
* Triển khai thành công AWS Storage Gateway kết nối tệp tin cục bộ với S3 trên đám mây.
* Kích hoạt thành công chống trùng lặp dữ liệu (Data Deduplication) và sao chép bóng (Shadow Copies) bảo vệ dữ liệu.
* Quản trị hiệu quả hạn ngạch (Quotas) người dùng, giám sát các tệp tin đang mở và mở rộng thành công dung lượng ổ đĩa.
* Thực hiện quy trình dọn dẹp sạch tài nguyên sau khi kết thúc lab để tối ưu hóa chi phí.
