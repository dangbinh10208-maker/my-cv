# Portfolio cá nhân — Nguyễn Đăng Bình

## Giới thiệu

Đây là website portfolio/CV cá nhân giới thiệu Nguyễn Đăng Bình với định hướng Frontend Developer. Trang cung cấp phần giới thiệu, các mục kỹ năng, kỷ niệm/dự án và thông tin liên hệ. Giao diện được thiết kế responsive để sử dụng trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Hiển thị ảnh đại diện, nội dung giới thiệu và các thẻ dự án/kỷ niệm.
- Bố cục tự điều chỉnh theo kích thước màn hình.
- Cung cấp liên kết email và Zalo để liên hệ.
- Không cần tài khoản, cơ sở dữ liệu hay dịch vụ backend.

## Công nghệ sử dụng

- **HTML5:** cấu trúc và nội dung trang.
- **CSS3:** giao diện, bố cục responsive và hiệu ứng trình bày.
- **Git:** quản lý mã nguồn.
- **Docker (tùy chọn):** phục vụ trang tĩnh bằng Apache HTTP Server.

## Yêu cầu môi trường

Để xem trang, bạn chỉ cần một trình duyệt web hiện đại. Không cần cài Node.js, npm hay thư viện phụ thuộc.

Để chạy máy chủ web cục bộ, chọn một trong các cách sau:

- **Windows:** Python 3 (lệnh `py`) hoặc Docker Desktop.
- **macOS:** Python 3 (lệnh `python3`) hoặc Docker Desktop.
- **Linux:** Python 3 (lệnh `python3`) hoặc Docker Engine.

## Cài đặt mã nguồn

Mở Terminal, PowerShell hoặc Command Prompt và sao chép kho mã nguồn:

```bash
git clone https://github.com/dangbinh10208-maker/my-cv.git
cd my-cv
```

Nếu không dùng Git, tải mã nguồn từ trang GitHub của dự án và giải nén. Giữ nguyên cấu trúc thư mục, đặc biệt là `assets/`, để các tệp CSS và hình ảnh được tải đúng.

## Cấu hình và tùy chỉnh

Dự án không có tệp cấu hình môi trường, biến môi trường hay bước cài đặt phụ thuộc.

- Sửa nội dung, thông tin giới thiệu, dự án và liên hệ trong `index.html`.
- Sửa màu sắc, khoảng cách và kiểu hiển thị trong `assets/css/styles.css`. Các màu chính được khai báo bằng CSS custom properties ở đầu tệp.
- Thay hình ảnh trong `assets/img/` và cập nhật đường dẫn tương ứng trong `index.html`.
- Nếu thay đổi email hoặc số điện thoại, cập nhật cả nội dung hiển thị lẫn liên kết `mailto:` hoặc Zalo.

## Chạy thử

### Windows

Mở PowerShell hoặc Command Prompt tại thư mục `my-cv`, sau đó chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, cài Python 3 hoặc mở trực tiếp `index.html` trong trình duyệt. Mở [http://localhost:8000](http://localhost:8000) để xem trang. Nhấn `Ctrl+C` trong cửa sổ lệnh để dừng máy chủ.

### macOS

Mở Terminal tại thư mục `my-cv` và chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trong trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

### Linux

Mở Terminal tại thư mục `my-cv` và chạy:

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trong trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

> Nếu cổng `8000` đang được sử dụng, thay `8000` trong lệnh bằng một cổng khác, chẳng hạn `8080`, rồi mở đúng cổng đó trên trình duyệt.

## Chạy bằng Docker

Cài Docker Desktop trên Windows/macOS hoặc Docker Engine trên Linux, sau đó chạy lệnh tại thư mục gốc của dự án. Lệnh dùng image Apache chính thức và gắn thư mục dự án ở chế độ chỉ đọc; không cần Dockerfile hoặc build image.

**Windows PowerShell:**

```powershell
docker run --rm -p 8080:80 -v "${PWD}:/usr/local/apache2/htdocs:ro" httpd:2.4
```

**macOS và Linux:**

```bash
docker run --rm -p 8080:80 -v "$PWD:/usr/local/apache2/htdocs:ro" httpd:2.4
```

Mở [http://localhost:8080](http://localhost:8080) để xem trang. Nhấn `Ctrl+C` để dừng và xóa container. Nếu Docker báo không thể truy cập daemon, hãy khởi động Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux) rồi thử lại.

## Thông tin liên hệ

- **Tác giả:** Nguyễn Đăng Bình
- **Email:** [dangbinh10208@gmail.com](mailto:dangbinh10208@gmail.com)
- **Zalo:** [0968779255](https://zalo.me/0968779255)
- **Kho mã nguồn:** [dangbinh10208-maker/my-cv](https://github.com/dangbinh10208-maker/my-cv)