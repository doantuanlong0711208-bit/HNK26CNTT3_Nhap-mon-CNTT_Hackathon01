# BÀI LÀM – HACKATHON 01

- **Mã đề:** 21
- **Họ tên: Đoàn Tuấn Long** 
- **Lớp: CNTT3** 
- **Link repository: https://github.com/doantuanlong0711208-bit/HNK26CNTT3_Nhap-mon-CNTT_Hackathon01.git** 
- **Hệ điều hành (Windows/macOS): Windows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```Powershell
1. pwd
2. ls -Force
3. mv .\mau_goi_qua.txt .\docs\
   mv .\logo_qua_luu_niem.png .\media\
4. cp .\media\logo_qua_luu_niem.png .\backup\
5. rm .\temp_293.tmp
6. cd .\logs\
   ls -Force
   cd..


```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
PS D:\starter-kit (1)\starter-kit\qua-luu-niem-website> ls -Force


    Directory: D:\starter-kit (1)\starter-kit\qua-luu-niem-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  10:48 AM                backup
d-----        10/28/2026  10:50 AM                data
d-----        10/28/2026  10:51 AM                docs
d-----        10/28/2026  10:50 AM                logs
d-----        10/28/2026  10:51 AM                media
------        10/27/2026   1:32 AM             74 .env
-a----        10/27/2026   1:32 AM           2224 bai_lam.md

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```Powershell
1. Get-Content .\logs\gift.log | Select-String "ERROR" > .\logs\daily_report.txt
2. Get-Content .\logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-12-28 07:38:36 [ERROR] Khong tim thay trang /qua-tet (404)
2026-12-28 07:44:36 [ERROR] Het thoi gian cho (timeout)

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```Powershell
 Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
 .\auto_report.ps1

```

### Kết quả hiển thị

```text
Dang loc log...
Hoan thanh!
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```Powershell
(Get-Content .\logs\gift.log | Select-String "ERROR").count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
7

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```Powershell
"=== TONG HOP LOG ===" > .\logs\tong_hop.txt
"CAC DONG CHUA WARNING" >> .\logs\tong_hop.txt
Get-Content .\logs\gift.log | Select-String "WARNING" >> .\logs\tong_hop.txt
"SO DONG CHUA ERROR" >> .\logs\tong_hop.txt
(Get-Content .\logs\gift.log | Select-String "ERROR").count >> .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===
CAC DONG CHUA WARNING

2026-12-28 07:32:36 [WARNING] Anh mau qua dung luong lon
2026-12-28 08:02:36 [WARNING] Anh mau qua dung luong lon
2026-12-28 08:20:36 [WARNING] Don giao gap trong ngay


SO DONG CHUA ERROR
7


```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_qua_thang_12.xlsx`, không cần ghi vào đây.
