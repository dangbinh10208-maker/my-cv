# Portfolio cá nhân — Nguyễn Đăng Bình

## Tên dự án

**Portfolio cá nhân của Nguyễn Đăng Bình** — trang giới thiệu cá nhân theo định hướng Frontend Developer.

## Mô tả

Đây là website tĩnh giới thiệu Nguyễn Đăng Bình, các kỹ năng, dự án/kỷ niệm và thông tin liên hệ. Giao diện hỗ trợ nhiều kích thước màn hình, từ điện thoại đến máy tính. Dự án chỉ dùng HTML và CSS, không cần máy chủ backend, cơ sở dữ liệu hoặc bước cài thư viện.

## Chức năng

- Điều hướng đến Trang chủ, Giới thiệu, Kỹ năng, Kỷ niệm, Dự án và Liên hệ.
- Hiển thị phần giới thiệu, mục tiêu nghề nghiệp, ảnh đại diện và kỹ năng dạng thẻ.
- Trưng bày thư viện ảnh kỷ niệm dạng lưới và các dự án/mục tiêu học tập.
- Bố cục responsive cho điện thoại, máy tính bảng và máy tính; có hiệu ứng chuyển động nhẹ và hỗ trợ giảm chuyển động.
- Cung cấp liên kết Facebook, email và Zalo để liên hệ.

## Công nghệ

- **HTML5:** cấu trúc và nội dung trang.
- **CSS3:** giao diện, bố cục responsive và hiệu ứng trình bày.
- **Git:** quản lý mã nguồn.
- **Docker (tùy chọn):** phục vụ trang tĩnh bằng Apache HTTP Server.

## Yêu cầu môi trường

Để xem trang, cần một trình duyệt web hiện đại. Không bắt buộc cài Node.js, npm hay thư viện phụ thuộc.

Để chạy máy chủ web cục bộ, chọn một trong các cách sau:

| Hệ điều hành | Yêu cầu |
| --- | --- |
| Windows | Python 3 (có lệnh `py`) hoặc Docker Desktop |
| macOS | Python 3 (có lệnh `python3`) hoặc Docker Desktop |
| Linux | Python 3 (có lệnh `python3`) hoặc Docker Engine |

## Cài đặt mã nguồn

Mở PowerShell, Command Prompt hoặc Terminal và chạy:

```bash
git clone https://github.com/dangbinh10208-maker/my-cv.git
cd my-cv
```

Hoặc tải mã nguồn từ GitHub và giải nén. Giữ nguyên cấu trúc thư mục, đặc biệt là `assets/`, để trang tải được CSS và hình ảnh.

## Cấu hình và tùy chỉnh

Dự án không có tệp cấu hình môi trường, biến môi trường hay bước cài đặt phụ thuộc.

- Sửa nội dung giới thiệu, kỹ năng, dự án và liên hệ trong `index.html`.
- Sửa màu sắc và kiểu trình bày trong `assets/css/styles.css`; các màu chính được khai báo bằng CSS custom properties ở đầu tệp.
- Thay hình ảnh trong `assets/img/` và cập nhật đường dẫn ảnh tương ứng trong `index.html`.
- Khi đổi thông tin liên hệ, cập nhật cả nội dung hiển thị và liên kết `mailto:` hoặc Zalo.

## Chạy thử

Chạy lệnh từ thư mục gốc của dự án, sau đó mở địa chỉ tương ứng trên trình duyệt. Nếu cổng `8000` đang được sử dụng, thay `8000` bằng một cổng khác trong lệnh và địa chỉ truy cập.

### Windows

Mở PowerShell hoặc Command Prompt tại thư mục dự án:

```powershell
py -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Nhấn `Ctrl+C` trong cửa sổ lệnh để dừng máy chủ. Nếu không có lệnh `py`, cài Python 3 hoặc mở trực tiếp `index.html` bằng trình duyệt.

### macOS

Mở Terminal tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Nhấn `Ctrl+C` để dừng máy chủ.

### Linux

Mở Terminal tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Nhấn `Ctrl+C` để dừng máy chủ.

## Chạy bằng Docker

Cài Docker Desktop trên Windows/macOS hoặc Docker Engine trên Linux, khởi động Docker rồi chạy lệnh tại thư mục gốc của dự án. Lệnh dùng image Apache chính thức và gắn thư mục dự án ở chế độ chỉ đọc; không cần Dockerfile hoặc build image.

**Windows PowerShell:**

```powershell
docker run --rm -p 8080:80 -v "${PWD}:/usr/local/apache2/htdocs:ro" httpd:2.4
```

**macOS và Linux:**

```bash
docker run --rm -p 8080:80 -v "$PWD:/usr/local/apache2/htdocs:ro" httpd:2.4
```

Truy cập [http://localhost:8080](http://localhost:8080). Nhấn `Ctrl+C` để dừng và xóa container. Nếu Docker không kết nối được tới daemon, hãy khởi động Docker Desktop hoặc Docker Engine rồi chạy lại.

## Thông tin liên hệ

- **Tác giả:** Nguyễn Đăng Bình
- **Email:** [dangbinh10208@gmail.com](mailto:dangbinh10208@gmail.com)
- **Zalo:** [0968779255](https://zalo.me/0968779255)
- **Kho mã nguồn:** [dangbinh10208-maker/my-cv](https://github.com/dangbinh10208-maker/my-cv)