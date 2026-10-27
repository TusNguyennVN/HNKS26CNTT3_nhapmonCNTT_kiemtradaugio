# Quản lý thiết bị
## Mã linh kiện

| MÃ linh kiện | Tên thiết bị | Đơn giá | Loại Storage |
|---|---|---|---|
| LK01 | Raspberry Pi 4 Model B | 1.450.000 | SSD |
| LK02 | Intel NUC i3 | 6.200.000 | SSD |
| LK03 | Orange Pi 5 | 2.300.000 | SSD |


## Lệnh sử dụng

```powershell
.\auto_report.ps1
```

## Công việc

- [x] Tạo cấu trúc thư mục
- [ ] Hoàn thiện báo cáo log
- [ ] Nộp báo cáo

## Mô hình IPO của chức năng lọc log:

-  Input: Dữ liệu trong file log
- Process: Hệ thống đọc file log, lọc ra các dòng có chứa lỗi 
- Output: File báo cáo lỗi được xuất ra tại: .\backup\bao-cao-su-co.txt

## Phân loại các phát biểu vào đúng tầng DIKW:

- **Data**: (b) “2026-10-12 08:15:01 [ERROR] sensor-03 Connection TIMEOUT after 30s” 
- **Information**: (c) “Hôm nay hệ thống ghi nhận 8 sự cố, trong đó 4 sự cố đến từ trạm sensor-03.” 
- **Knowledge**: (d) “Trạm sensor-03 hay mất kết nối vào buổi chiều do sóng yếu, nên cần lắp thêm anten.” 
-  **Wisdom**: (a) “Quyết định thay modem trạm sensor-03 trước thứ Sáu.” 