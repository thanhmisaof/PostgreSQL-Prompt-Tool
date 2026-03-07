# PostgreSQL Prompt Tool

Công cụ được thiết kế dành riêng cho môi trường làm việc trên Windows, giúp tự động gợi ý code, viết tắt và lấy thiết kế cấu trúc database PostgreSQL nhanh chóng ngay trên DBeaver (tương tự như **SQL Prompt** của Redgate).

## Tính Năng Nổi Bật
- **Tự Động Cập Nhật (Auto-Update)**: Tự động kiểm tra và nâng cấp lên phiên bản phần mềm mới nhất từ GitHub.
- **Phím Tắt Viết Code (Snippet)**: Gõ các phím tắt siêu tốc để sinh ra template code phức tạp (`ssf` -> `SELECT * FROM`, `crf` -> `CREATE FUNCTION`, v.v.).
- **Truy Cập Gốc (Object Binding)**: Chỉ cần gõ `af ten_ham` và nhấn `Ctrl+SPACE`, nội dung code của hàm (function), thủ tục (procedure) hoặc bảng (table) từ Database sẽ lập tức được chèn vào cửa sổ code của bạn.
- **Bảo Mật Cấu Hình**: Mật khẩu database của bạn trong file `config.ini` sẽ được công cụ tự động mã hoá ở dưới nền để tránh lộ.

## Hướng Dẫn Cài Đặt & Sử Dụng
1. Tải ứng dụng [**PgPromptApp.exe**](PgPromptApp.exe).
2. Tốt nhất hãy gom nó vào trong một thư mục rỗng và Nhấp đúp (Double-click) để khởi chạy `PgPromptApp.exe`.
3. Trong lần chạy đầu tiên, công cụ sẽ tự sinh ra 2 file cấu hình `config.ini` và `snippets.ini` bên cạnh file `.exe`.
4. Tìm **biểu tượng con voi PostgreSQL** ở góc dưới cùng khay hệ thống (System Tray) -> Bấm **Edit Config**.
5. Điền thông tin kết nối DB của bạn vào (Host, Port, User, Password, Schema). *Hãy yên tâm, mật khẩu sẽ tự mã hoá ở lần chạy kế!*
6. Bấm **Test Connection** trên màn hình chính của ứng dụng để đảm bảo thông tin DB đã chính xác.
7. Mở phần mềm Database của bạn (**DBeaver**, DBeaver CE), gõ `af ten_ham_cua_ban` và Tab nhấn **`Ctrl+SPACE`**.

## Phím Tắt Tùy Chỉnh
Bộ phím tắt có thể được tuỳ biến tùy ý. Bạn chỉ cần sửa file `snippets.ini` sinh ra trong thư mục:
```ini
[CustomSnippets]
sc=SELECT COUNT(*) FROM
ii=INSERT INTO
```

## Cách Cập Nhật Phần Mềm
Bạn có thể tự tay nhấn nút **Update New Version** ở dưới System Tray Menu để ép máy chủ lấy cập nhật ngay lập tức. Nếu bạn không bấm, công cụ cũng sẽ âm thầm tự cập nhật phiên bản mới nhất ở các lần khởi động tiếp theo.
