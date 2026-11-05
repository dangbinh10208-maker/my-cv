# Nhật ký thay đổi

Ghi lại các thay đổi lớn của dự án như tính năng mới, thay đổi cấu trúc, sửa lỗi quan trọng, cập nhật phát hành hoặc bổ sung minh chứng kiểm thử. Mỗi mục nêu ngày, nội dung, các tệp liên quan và ảnh hưởng; không cần ghi chỉnh sửa nhỏ về câu chữ hoặc định dạng.

## 05/11/2026 — Hoàn thiện tài liệu dự án

- **Nội dung:** Bổ sung hướng dẫn giới thiệu, cài đặt, cấu hình và chạy website portfolio trên Windows, macOS, Linux và Docker; bổ sung ghi chú phát hành phiên bản v1.0.
- **Tệp liên quan:** `README.md`, `docs/RELEASENOTE.MD`.
- **Ảnh hưởng:** Giúp người dùng hiểu chức năng dự án và có thể chạy thử trên các môi trường được hỗ trợ; không thay đổi mã nguồn hay chức năng của website.

## 05/11/2026 — Bổ sung báo cáo và minh chứng kiểm thử responsive

- **Nội dung:** Lập báo cáo kiểm thử theo sáu nhóm tiêu chí; chụp ảnh toàn trang ở ba viewport mô phỏng mobile, tablet và desktop; kiểm tra lưới dự án lần lượt hiển thị 1, 2 và 3 cột.
- **Tệp liên quan:** `docs/test_report.md`, `docs/screenshots/mobile.png`, `docs/screenshots/tablet.png`, `docs/screenshots/desktop.png`.
- **Ảnh hưởng:** Báo cáo có minh chứng trực quan cho bố cục responsive và ghi nhận các hạn chế cần khắc phục, gồm đường dẫn ảnh sai. Ảnh được chụp bằng Chrome headless, không phải thiết bị vật lý.