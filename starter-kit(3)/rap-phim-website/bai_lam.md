# BÀI LÀM – (ĐỀ LUYỆN TẬP SỐ 02)

- **Mã đề:** 02
- **Họ tên:**Ngô Thu Thúy
- **Lớp:**CNTT3
- **Link repository:**Githup
- **Hệ điều hành (Windows/macOS):**Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# 1:pwd
  2:ls -Force
  3:mv .\bien_ban_ban_giao.txt  .\docs
  4:mkdir .\backup
  5:cp .\data\ban_ve_thang_11.xlsx .\backup
  6:rm .\cache_991.tmp
  7:cd .\logs\
    Get-content .\clinic.log
    cd..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Get-ChildItem -Recurse -Force -Name

.env
.env.example
.gitignore
backup
bai_lam.md
data
docs
evidence
logs
README.md
tong_hop.ps1
web
backup\ban_ve_thang_11.xlsx
data\ban_ve_thang_11.xlsx
docs\bien_ban_ban_giao.txt
logs\loi_error.txt
logs\server.log
logs\tong_hop.txt
web\app.js
web\images
web\index.html
web\style.css
web\images\logo-cinebox.png

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng ERROR

```shell
# Get-Content logs\server.log | Select-String "ERROR" > logs\loi_error.txt
Get-Content logs\loi_error.txt -TotalCount 2


```

### 2 dòng đầu tiên trong logs/loi_error.txt

```text
2026-11-01 09:25:40 ERROR POST /api/mua-ve
2026-11-01 09:29:11 ERROR POST /api/thanh-toan-qr

```

### b) Lệnh đếm số dòng WARNING và kết quả

```shell
# Get-Content logs\server.log | Select-String "WARNING" | Measure-Object

```

```text
Count    : 5
Average  :
Sum      :
Maximum  :
Minimum  :
Property :

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
# Chạy bị chặn nên dùng Phụ lục 2 (2 lệnh):
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\tong_hop.ps1

```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO SU CO WEBSITE ===
2026-11-01 09:08:10 WARNING GET /phim-sap-chieu-cu
2026-11-01 09:15:30 WARNING GET /uu-dai-thang-9
2026-11-01 09:36:50 WARNING GET /images/phong-imax.jpg
2026-11-01 10:01:20 WARNING GET /voucher-het-han
2026-11-01 10:12:55 WARNING GET /combo-bap-nuoc

Count    : 6
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :

```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, mô tả có **in đậm** và _in nghiêng_, bảng, code block, task list, blockquote
- [x] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [x] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   |                            |                             |                |
| 2   |                            |                             |                |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:**
- **Expected:**
- **Actual:**
- **Log:**

### Câu tìm kiếm Google

```text
site:stackoverflow.com "Uncaught ReferenceError: hienThiBangGia is not defined"


```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_ve_thang_11.xlsx`, không cần ghi vào đây.
