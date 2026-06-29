# ZVPS CLI (Releases)

**ZVPS CLI** là công cụ dòng lệnh (TUI - Terminal User Interface) mạnh mẽ, giúp quản lý cấu hình và vận hành máy chủ VPS Linux (Ubuntu/Debian) một cách dễ dàng, nhanh chóng và chuyên nghiệp. 
---

## 🛠️ Hướng dẫn cài đặt (Installation)

Để cài đặt ZVPS CLI lên VPS của bạn, hãy đăng nhập qua SSH bằng quyền `root` (hoặc tài khoản có quyền `sudo`) và thực hiện các bước sau:

### Bước 1: Tải tệp thực thi từ Releases
Tải phiên bản mới nhất từ GitHub Releases:

```bash
# Tải về phiên bản dành cho Linux
curl -L -o zvps https://github.com/zeo-developer/zvps-cli/releases/latest/download/zvps
```

### Bước 2: Cấp quyền thực thi và di chuyển vào thư mục hệ thống
```bash
# Cấp quyền chạy cho file nhị phân
chmod +x zvps

# Di chuyển tệp tin vào thư mục /usr/local/bin để chạy toàn cục từ bất cứ đâu
sudo mv zvps /usr/local/bin/zvps
```

---

## 🚀 Cách sử dụng

Sau khi cài đặt thành công, bạn chỉ cần gõ lệnh sau ở bất kỳ thư mục nào trên VPS để mở giao diện quản trị:

```bash
zvps
```

Giao diện Terminal User Interface (TUI) trực quan sẽ xuất hiện và hướng dẫn bạn quản lý máy chủ.

---

## 📋 Yêu cầu hệ thống

Để ZVPS CLI hoạt động tốt nhất và tự động cấu hình các dịch vụ cho bạn, VPS nên đáp ứng các yêu cầu sau:
* **Hệ điều hành**: Ubuntu 20.04 LTS trở lên hoặc Debian 10 trở lên.
* **Quyền hạn**: Chạy bằng quyền `root` (hoặc tài khoản có quyền `sudo`).
* **Kết nối mạng**: Cần có kết nối internet để tự động cài đặt các thành phần phụ thuộc (như Nginx, MariaDB, PHP, Node.js, Certbot...) khi được yêu cầu từ giao diện quản trị.

---

## 🗺️ Các tính năng chính

ZVPS CLI hỗ trợ đầy đủ các chức năng quản trị máy chủ thông dụng:

1. **Quản lý Website (Website Management)**: Thêm mới, chỉnh sửa cấu hình (PHP/NodeJS version, domain aliases), danh sách website và xóa hoàn toàn website.
2. **Chứng chỉ SSL Let's Encrypt**: Cài đặt SSL tự động cho domain chính/aliases, gỡ bỏ SSL và gia hạn tất cả chứng chỉ.
3. **Triển khai mã nguồn (Zero-Downtime Deploy & Rollback)**: Deploy qua Git repo theo quy trình chuẩn, hỗ trợ rollback phiên bản tức thời khi gặp lỗi.
4. **Quản lý Database (MariaDB)**: Đổi mật khẩu database user của website, cấu hình kết nối từ xa (mở/khóa cổng 3306), và sao lưu tự động hàng ngày.
5. **Theo dõi Log trực tiếp (Realtime Logs)**: Stream log trực tiếp từ Laravel (`laravel.log`), Supervisor queue worker, Nginx Access/Error logs.
6. **Cấu hình SWAP**: Xem trạng thái SWAP, tạo/thay đổi kích thước SWAP và cấu hình tham số `swappiness`.
7. **Tường lửa & Bảo mật (UFW)**: Danh sách IP bị chặn, chặn/bỏ chặn IP, bật/tắt truy cập trực tiếp qua địa chỉ IP của VPS.
8. **Cập nhật hệ thống (OS Update)**: Tự động nâng cấp các gói cập nhật hệ điều hành Ubuntu/Debian một cách an toàn.

---

*Cảm ơn bạn đã tin tưởng và sử dụng ZVPS CLI!*
