# Hệ Thống Quản Lý Thư Viện

## Mô tả
Hệ thống quản lý thư viện là một ứng dụng web được phát triển bằng PHP và MySQL, cho phép quản lý sách, người dùng, mượn trả sách và xử lý phạt quá hạn.

## Các chức năng chính

### 1. Quản lý người dùng
- Đăng nhập/Đăng xuất
- Phân quyền người dùng (Admin, Thủ thư, Thành viên)
- Quản lý thông tin cá nhân
- Đổi mật khẩu

### 2. Quản lý sách
- Thêm sách mới
- Cập nhật thông tin sách
- Xóa sách
- Tìm kiếm sách theo nhiều tiêu chí
- Quản lý số lượng sách
- Phân loại sách theo danh mục

### 3. Quản lý mượn trả
- Đăng ký mượn sách
- Ghi nhận trả sách
- Theo dõi trạng thái mượn trả
- Tự động cập nhật số lượng sách có sẵn
- Kiểm tra điều kiện mượn sách

### 4. Quản lý phạt
- Tự động tính tiền phạt quá hạn
- Ghi nhận thanh toán phạt
- Báo cáo phạt chưa thanh toán
- Lịch sử phạt

### 5. Quản lý nhà xuất bản
- Thêm nhà xuất bản mới
- Cập nhật thông tin nhà xuất bản
- Xem danh sách sách theo nhà xuất bản

### 6. Báo cáo thống kê
- Thống kê sách mượn nhiều nhất
- Thống kê thành viên mượn nhiều nhất
- Báo cáo doanh thu phạt
- Thống kê sách quá hạn

### 7. Tìm kiếm nâng cao
- Tìm kiếm sách theo nhiều tiêu chí
- Tìm kiếm thành viên
- Tìm kiếm lịch sử mượn trả

### 8. Tính năng bảo mật
- Mã hóa mật khẩu
- Phân quyền chi tiết
- Kiểm tra đầu vào
- Bảo vệ SQL Injection
- Bảo vệ XSS

## Yêu cầu hệ thống
- PHP 7.4 trở lên
- MySQL 5.7 trở lên
- Web server (Apache/Nginx)
- mod_rewrite enabled (cho Apache)

## Cài đặt
1. Import file `database.sql` vào MySQL
2. Cấu hình kết nối database trong `config.php`
3. Đặt toàn bộ code vào thư mục web server
4. Truy cập qua trình duyệt web

## Tài khoản mặc định
- Admin: admin/password
- Thủ thư: librarian1/password
- Thành viên: member1/password

## Cấu trúc thư mục
```
ASM2/
├── config.php          # Cấu hình kết nối database
├── database.sql        # Cấu trúc database
├── index.php          # Trang chủ
├── login.php          # Trang đăng nhập
├── books/             # Quản lý sách
├── users/             # Quản lý người dùng
├── borrowings/        # Quản lý mượn trả
├── fines/             # Quản lý phạt
├── publishers/        # Quản lý nhà xuất bản
├── reports/           # Báo cáo thống kê
└── assets/            # CSS, JS, images
``` 