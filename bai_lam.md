# BÀI LÀM – HACKATHON 01

- **Mã đề:** 17
- **Họ tên:*Nguyen Thuan Phat* 
- **Lớp:*CNTT3* 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):*Windows* 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\nguon_hang.txt .\docs\
mv .\logo_trai_cay_sach.PNG .\media\
 cp .\media\logo_trai_cay_sach.PNG .\backup\
 rm -r *.tmp
 cd .\logs\
cat .\fruit.log
cd ..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026  10:59 AM                backup
d-----        10/28/2026  10:51 AM                data
d-----        10/28/2026  10:53 AM                docs
d-----        10/28/2026  10:51 AM                logs
d-----        10/28/2026  10:54 AM                media
------        10/27/2026   1:32 AM             70 .env
-a----        10/27/2026   1:32 AM           2228 bai_lam.md


    Directory: C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-we
    bsite\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           7054 logo_trai_cay_sach.PNG


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           6095 ban_trai_cay_thang_7.xlsx


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM             66 nguon_hang.txt


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           1041 fruit.log


    Directory:
    C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/27/2026   1:32 AM           7054 logo_trai_cay_sach.PNG


PS C:\Users\admin\Downloads\starter-kit\starter-kit\trai-cay-website>

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
# Ghi lệnh vào đây (xoá dòng này)
cat .\logs\fruit.log | Select-String "ERROR" > .\logs\daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-07-28 10:04:32 [ERROR] Thanh toan bi tu choi
2026-07-28 10:16:32 [ERROR] Het thoi gian cho (timeout)

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] Heading 1: tên dự án
- [ ] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [ ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [ ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [ ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\auto_report.ps1

```

### Kết quả hiển thị

```text
Dang loc log ...
Hoan thanh!

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
 (cat .\logs\fruit.log | select-string "ERROR").count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
5

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell

“=== TONG HOP LOG ===“ > .\logs\tong_hop.txt
 cat .\logs\fruit.log | Select-String “WARNING” >> .\logs\tong_hop.txt
  (cat .\logs\fruit.log | Select-String “ERROR”).count >> .\logs\tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_trai_cay_thang_7.xlsx`, không cần ghi vào đây.
