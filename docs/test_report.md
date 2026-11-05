# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Chi tiết |
| --- | --- |
| **Tên dự án** | Portfolio cá nhân — Nguyễn Đăng Bình |
| **Phiên bản** | v1.0 |
| **Ngày kiểm thử** | 05/11/2026 |
| **Người thực hiện/đánh giá** | Rà soát mã nguồn và tài liệu có hỗ trợ AI; người kiểm thử nghiệm thu trên thiết bị thực chưa được chỉ định |
| **Đối tượng kiểm thử** | Website portfolio tĩnh xây dựng bằng HTML5 và CSS3 |
| **Phạm vi** | Rà soát HTML/CSS và tài nguyên; kiểm tra bố cục responsive bằng Chrome headless tại viewport mô phỏng rộng 390, 768 và 1440 px |
| **Giới hạn** | Ảnh responsive là viewport mô phỏng trên máy tính, không phải ảnh chụp thiết bị vật lý; chưa kiểm tra các trình duyệt khác, hiệu năng, quét bảo mật tự động hoặc triển khai Docker thực tế |

> **Cách hiểu trạng thái:** “Đạt” là có bằng chứng từ phạm vi đã kiểm tra; “Chưa đạt” là phát hiện lỗi cụ thể; “Cần cải thiện” là còn thiếu xác minh hoặc cần hoàn thiện trước khi nghiệm thu. Không xem các hạng mục chưa chạy thực tế là đã đạt.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
| --- | --- | --- | --- |
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các mục chính và liên kết điều hướng nội bộ có trong mã nguồn; liên kết chi tiết dự án chưa có đích thực tế. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Chưa đạt | Đã lưu minh chứng responsive cho ba viewport; ảnh dự án bị lỗi do đường dẫn sai và chưa kiểm tra trên trình duyệt/thiết bị khác. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Website là trang tĩnh; chưa chạy smoke test qua máy chủ hoặc đo hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy luồng backend hoặc biểu mẫu nhập liệu trong phạm vi rà soát; chưa thực hiện kiểm thử/quét bảo mật chuyên sâu. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có cấu trúc tài nguyên và tài liệu hướng dẫn; cần xử lý nội dung placeholder và xác minh HTML/CSS bằng công cụ chuyên dụng. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | README có hướng dẫn chạy nhiều hệ điều hành và Docker; chưa triển khai thực tế, chưa có kết quả kiểm thử trình duyệt hoặc ảnh minh chứng. |

## 3. Chi tiết kiểm tra theo tiêu chí

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
| --- | --- | --- |
| Các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ được khai báo | Đạt | `index.html` có các section với ID `about`, `skills`, `projects`, `contact` (dòng 48, 74, 91, 174). |
| Điều hướng nội bộ trỏ đến đúng section | Đạt | Menu sử dụng các anchor `#about`, `#skills`, `#projects`, `#contact`; các ID tương ứng tồn tại trong trang. |
| Nút xem dự án và liên hệ điều hướng đến đúng phần | Đạt | Các nút trong phần giới thiệu trỏ đến `#projects` và `#contact` (`index.html`, dòng 57–58). |
| Liên kết liên hệ email và Zalo được khai báo | Đạt | Có `mailto:` và liên kết HTTPS Zalo (`index.html`, dòng 180–181); chưa xác minh người nhận hoặc tài khoản còn hoạt động. |
| Liên kết “Xem chi tiết” mở đúng nội dung dự án | Chưa đạt | Bốn thẻ dự án dùng `href="#"` (`index.html`, dòng 114, 131, 148, 165), chưa dẫn đến trang hoặc nội dung chi tiết. |
| Nội dung hiển thị phản ánh chính xác dự án/kỹ năng | Cần cải thiện | Một số nội dung còn mang tính placeholder hoặc chưa được biên tập (ví dụ kỹ năng và mô tả thẻ); cần chủ sản phẩm duyệt nội dung trước bàn giao. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
| --- | --- | --- |
| Trang khai báo ngôn ngữ, viewport và tiêu đề | Đạt | Có `lang="vi"`, thẻ viewport và tiêu đề trang (`index.html`, dòng 3, 9, 12). |
| CSS và ảnh đại diện được liên kết | Đạt | CSS liên kết tại `./assets/css/styles.css`; ảnh đại diện dùng đường dẫn tồn tại trong repository (`index.html`, dòng 15, 66–68). |
| Bố cục responsive trên mobile, tablet và desktop | Đạt | Đã kiểm tra trang bằng Chrome headless ở viewport rộng 390/768/1440 px; lưới dự án lần lượt hiển thị 1/2/3 cột. Ảnh toàn trang: [mobile (390 px)](./screenshots/mobile.png), [tablet (768 px)](./screenshots/tablet.png), [desktop (1440 px)](./screenshots/desktop.png). CSS breakpoint tương ứng tại `assets/css/styles.css`, dòng 403–434. |
| Ảnh trong danh sách dự án tải được | Chưa đạt | Một ảnh có `src=".assets/img/..."` (`index.html`, dòng 137); kiểm tra đường dẫn cục bộ không tìm thấy tệp tương ứng. |
| Khả năng truy cập bằng bàn phím và giảm chuyển động | Cần cải thiện | CSS có kiểu `:focus-visible` và hỗ trợ `prefers-reduced-motion` (`assets/css/styles.css`, dòng 443–449); chưa kiểm tra thao tác bàn phím hoặc trình đọc màn hình thực tế. |
| Tương thích trên trình duyệt và thiết bị mục tiêu | Cần cải thiện | Đã xác minh bố cục trong Chrome headless mô phỏng ba độ rộng; chưa kiểm tra trên thiết bị vật lý, Chrome tương tác thông thường, Firefox, Safari hoặc Edge. |
| Chất lượng hiển thị, độ tương phản và nội dung thay thế ảnh | Cần cải thiện | Đã xem giao diện qua ảnh minh chứng; chưa đo tương phản bằng công cụ, và một số nội dung `alt` mô tả tên loại dự án mẫu thay vì nội dung ảnh cụ thể. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
| --- | --- | --- |
| Cấu trúc trang tĩnh và tài nguyên cục bộ | Đạt | Trang dùng HTML/CSS và ảnh trong `assets/`; không thấy yêu cầu backend để hiển thị nội dung cơ bản trong phạm vi đã rà soát. |
| Chạy bằng máy chủ HTTP cục bộ | Cần cải thiện | README hướng dẫn dùng Python HTTP server trên Windows, macOS và Linux; chưa khởi chạy máy chủ để xác nhận phản hồi HTTP. |
| Xử lý tài nguyên không tồn tại | Chưa đạt | Đường dẫn ảnh sai đã xác định tại `index.html`, dòng 137; trình duyệt có thể hiển thị ảnh lỗi. |
| Hành vi khi dịch vụ liên hệ bên ngoài không khả dụng | Cần cải thiện | Email và Zalo phụ thuộc ứng dụng/dịch vụ bên ngoài; chưa kiểm tra thiết bị có cấu hình xử lý liên kết hay trạng thái dịch vụ. |
| Hiệu năng tải trang cơ bản | Cần cải thiện | Chưa đo thời gian tải, kích thước ảnh, chỉ số Lighthouse hoặc tải mạng; chưa có số liệu định lượng để nghiệm thu. |
| Kiểm thử lỗi phía máy chủ hoặc phía ứng dụng | Cần cải thiện | Không có kịch bản lỗi backend trong phạm vi website tĩnh; chưa thử các tình huống 404, tệp CSS/ảnh bị chặn hoặc máy chủ dừng. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
| --- | --- | --- |
| Biểu mẫu nhập liệu hoặc xử lý dữ liệu người dùng | Đạt | Không thấy biểu mẫu hoặc luồng xử lý dữ liệu nhập trong trang HTML đã rà soát. |
| Backend, API và dữ liệu bí mật trong cấu hình ứng dụng | Cần cải thiện | Dự án được mô tả là trang tĩnh và không có cấu hình môi trường; chưa chạy quét bí mật/dependency hoặc kiểm tra toàn bộ lịch sử Git. |
| Liên kết dịch vụ bên ngoài dùng HTTPS | Đạt | Liên kết Zalo sử dụng HTTPS (`index.html`, dòng 181). |
| Quyền riêng tư của thông tin liên hệ công khai | Cần cải thiện | Email và số điện thoại được hiển thị công khai trong trang; chủ sản phẩm cần xác nhận đồng ý công bố trước khi triển khai. |
| Kiểm thử bảo mật chuyên sâu | Cần cải thiện | Chưa thực hiện quét lỗ hổng, kiểm thử cấu hình máy chủ, header bảo mật hoặc kiểm tra phụ thuộc của image Docker. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
| --- | --- | --- |
| Tách nội dung HTML, CSS và tài nguyên hình ảnh | Đạt | Repository có `index.html`, `assets/css/styles.css` và thư mục `assets/img/`. |
| README hướng dẫn cài đặt và chạy thử | Đạt | `README.md` có hướng dẫn cho Windows, macOS, Linux và Docker. |
| Có ghi chú phát hành phiên bản | Đạt | `docs/RELEASENOTE.MD` ghi phiên bản v1.0 và nêu hạn chế của các liên kết dự án, đường dẫn ảnh. |
| Mã nguồn không còn nội dung mẫu và placeholder | Cần cải thiện | Còn các liên kết `href="#"`, mô tả dự án/kỹ năng cần xác nhận và một ảnh được tái sử dụng ở nhiều thẻ. |
| Kiểm tra cú pháp và chất lượng mã tự động | Cần cải thiện | Chưa chạy HTML validator, CSS linter hoặc kiểm tra accessibility tự động; repository không thể hiện bộ kiểm thử tự động trong phạm vi đã xem. |
| Nhật ký thay đổi và báo cáo kiểm thử được bàn giao | Đạt | Có `docs/AI_LOG.md` và báo cáo này tại `docs/test_report.md`; cần bổ sung kết quả kiểm thử thực tế khi chạy nghiệm thu. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
| --- | --- | --- |
| Hướng dẫn chạy trên Windows | Đạt | README có lệnh Python HTTP server cho Windows (`README.md`, dòng 61–69); chưa chạy xác minh trên Windows sạch. |
| Hướng dẫn chạy trên macOS và Linux | Đạt | README có hướng dẫn `python3 -m http.server` cho hai hệ điều hành (`README.md`, dòng 71–89); chưa chạy trên các hệ điều hành này. |
| Hướng dẫn triển khai bằng Docker | Cần cải thiện | README dùng image `httpd:2.4` và bind mount thư mục; chưa build/chạy container. Repository không có Dockerfile hoặc Compose để triển khai lặp lại theo cấu hình dự án. |
| Bộ kiểm thử hồi quy hoặc CI | Cần cải thiện | Chưa thấy kịch bản test tự động hay cấu hình pipeline kiểm thử trong repository được rà soát. |
| Ảnh chụp màn hình responsive | Đạt | Đã lưu ảnh toàn trang trong `docs/screenshots/`: [mobile.png (390 px)](./screenshots/mobile.png), [tablet.png (768 px)](./screenshots/tablet.png), [desktop.png (1440 px)](./screenshots/desktop.png). Đây là viewport mô phỏng bằng Chrome headless, không phải ảnh chụp từ thiết bị thật. |
| Khả năng lặp lại quy trình kiểm thử | Cần cải thiện | README hỗ trợ chạy thử thủ công; cần bổ sung checklist nghiệm thu theo trình duyệt/viewport và lưu kết quả thực thi. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Website đã có cấu trúc portfolio cơ bản, các mục nội dung chính, điều hướng nội bộ, CSS responsive và tài liệu hướng dẫn chạy. Bố cục đã được kiểm tra bằng Chrome headless ở ba độ rộng viewport và có ảnh minh chứng. Tuy nhiên, kết quả rà soát phát hiện đường dẫn ảnh không hợp lệ và các liên kết chi tiết dự án chưa có đích sử dụng. Kiểm tra trên thiết bị/trình duyệt khác, hiệu năng, bảo mật chuyên sâu và triển khai Docker chưa được thực hiện.

**Đánh giá sẵn sàng bàn giao: Cần khắc phục và kiểm thử bổ sung trước khi nghiệm thu chính thức.** Kết luận này chỉ dựa trên phạm vi rà soát nêu trong báo cáo, không thay thế kiểm thử chấp nhận của chủ sản phẩm.

### Các vấn đề cần xử lý

| Mã | Mức độ | Vấn đề | Đề xuất |
| --- | --- | --- | --- |
| BUG-01 | Cao | Đường dẫn ảnh sai tại `index.html`, dòng 137 (`.assets/img/...`). | Sửa thành đường dẫn đúng dưới `assets/img/` và xác nhận ảnh tải được khi phục vụ qua HTTP. |
| BUG-02 | Trung bình | Bốn nút “Xem chi tiết” trỏ đến `#`, không mở nội dung cụ thể. | Cung cấp trang/đích nội dung hợp lệ hoặc đổi nhãn thành thành phần không tương tác nếu chưa có nội dung. |
| BUG-03 | Trung bình | Nội dung và mô tả thay thế ảnh còn mang tính mẫu/chưa nhất quán. | Chủ sản phẩm duyệt chính tả, thông tin kỹ năng/dự án và viết `alt` mô tả đúng ảnh. |
| TEST-01 | Trung bình | Bố cục mới được kiểm tra bằng viewport mô phỏng trong Chrome headless; chưa xác minh trên thiết bị vật lý hoặc các trình duyệt mục tiêu khác. | Kiểm tra trên thiết bị thật và các trình duyệt mục tiêu; lưu kết quả và ảnh bổ sung nếu có khác biệt. |
| TEST-02 | Trung bình | Chưa xác nhận quy trình Docker, hiệu năng hoặc cấu hình bảo mật khi triển khai. | Chạy thử theo README; kiểm tra mã HTTP và tài nguyên; ghi lại kết quả đo hiệu năng và cấu hình triển khai. |

### Điều kiện đề xuất trước bàn giao

1. Khắc phục BUG-01 và quyết định cách xử lý BUG-02; cập nhật nội dung, `alt` ảnh theo xác nhận của chủ sản phẩm.
2. Chạy lại kiểm tra liên kết tài nguyên cục bộ và xác nhận không còn ảnh/stylesheet bị thiếu.
3. Dùng các ảnh viewport mô phỏng làm bằng chứng ban đầu; kiểm tra bổ sung điều hướng, liên hệ và bố cục trên trình duyệt/thiết bị mục tiêu trước nghiệm thu.
4. Chạy thử ít nhất một phương thức triển khai (Python HTTP server hoặc Docker), ghi lại trình duyệt, hệ điều hành, kết quả và ảnh minh chứng.
5. Xác nhận email/số điện thoại được phép công khai; thực hiện kiểm tra accessibility và hiệu năng cơ bản trước khi chốt nghiệm thu.

## 5. Minh chứng và khả năng truy vết

- Mã nguồn trang: `index.html`.
- CSS giao diện và breakpoint responsive: `assets/css/styles.css`.
- Hướng dẫn cài đặt/chạy: `README.md`.
- Ghi chú phát hành: `docs/RELEASENOTE.MD`.
- Ảnh responsive: [mobile](./screenshots/mobile.png) (390 × 3400 px), [tablet](./screenshots/tablet.png) (768 × 2200 px), [desktop](./screenshots/desktop.png) (1440 × 2200 px). Ảnh được chụp bằng Chrome headless trên trang cục bộ; viewport được mô phỏng theo chiều rộng, không phải thiết bị vật lý.
- Cách xác minh đường dẫn ảnh lỗi: đối chiếu `src` tại `index.html`, dòng 137 với cấu trúc thư mục `assets/img/`; đường dẫn `.assets/img/...` không tồn tại.
- Kết quả kiểm tra responsive trong Chrome headless: độ rộng nội dung 375/753/1425 px lần lượt cho lưới 1/2/3 cột; ảnh lỗi vẫn hiển thị trong minh chứng do đường dẫn chưa được sửa.
- Kiểm thử trên trình duyệt/thiết bị khác, Docker, hiệu năng và bảo mật chuyên sâu: **chưa thực hiện trong đợt rà soát này**.