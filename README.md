# TRIUMPH GAME - HỘI THI KÉO CO 2026
### CĐCS CÔNG TY TNHH TRIUMPH INTERNATIONAL VIỆT NAM
Chào mừng Ngày Phụ Nữ Việt Nam 20/10/2026

Hệ thống Bình chọn Đội Vô Địch Thời Gian Thực (Single-Page Realtime Web App) xây dựng bằng HTML5, TailwindCSS, Lucide Icons và Firebase v10 Modular SDK (Realtime Database & Anonymous Auth).

---

## 🌟 Tính năng nổi bật

1. **Kiến trúc Đa Chương Trình (Multi-Campaign Realtime Architecture):**
   - Đồng bộ thời gian thực 4 nhánh dữ liệu: `system/activeCampaignId`, `campaigns/{id}`, `votes/{id}/{empId}`, `usedDevices/{id}/{uid}`.
   - Khi Ban Tổ Chức kích hoạt đợt bình chọn mới, toàn bộ màn hình người chơi tự động chuyển sang vòng mới.

2. **Bảo mật 1 Người / 1 Phiếu Bầu:**
   - Khóa chặt chẽ theo từng đợt bằng Mã số nhân viên (`empId`), Thiết bị (`deviceUid`) và `localStorage`.
   - Hiển thị ngay **Phiếu / Thẻ Bình Chọn Điện Tử** có mã MSNV, thông tin người bầu, đội chọn, dự đoán số người và thời gian ghi nhận chính xác đến mili-giây.

3. **Giao diện Arena Cyber Đẳng Cấp:**
   - Thiết kế chuẩn theo mẫu thi đấu thể thao với hiệu ứng ánh sáng Neon Cyan & Magenta.
   - Hiển thị đầy đủ **16 Đội Tuyển - 8 Cặp Đấu Vòng 3** kèm Thanh lực kéo co (Momentum Bar) chuyển động hai chiều.
   - Nút **"Bảng Đấu"** xem lịch thi đấu và sơ đồ bảng đấu chi tiết toàn giải.
   - Nút **"Poster"** xem poster khổ lớn chính thức của chương trình.

4. **Bảng Điều Khiển Ban Tổ Chức (Mã PIN: `2010`):**
   - **Khối A:** Quản lý và chuyển đổi phát sóng đợt bình chọn (`ĐANG HIỂN THỊ`, `ĐANG MỞ`, `ĐÃ ĐÓNG`).
   - **Khối B:** Tạo nhanh đợt bình chọn mới trong 15 giây (tick chọn nhanh 16 đội hoặc nhập danh sách tùy ý).
   - **Khối C:** Lọc kết quả và Bảng xếp hạng TOP 10 người trúng giải theo thuật toán độ lệch $\Delta = |\text{predictedCount} - N_{actual}|$.
   - **Xuất báo cáo:** Xuất file Excel/CSV Top giải thưởng và Toàn bộ phiếu bầu chuẩn UTF-8 BOM.

5. **Cơ chế Chạy Thử Ngay (Fallback Mode):**
   - Tự động chuyển đổi mượt mà sang `localStorage` với đồng bộ liên tab (cross-tab sync) khi cần thử nghiệm nhanh hoặc khi không có kết nối Firebase.

---

## 🚀 Cấu trúc thư mục

```text
├── index.html          # File ứng dụng hoàn chỉnh duy nhất (Single-file SPA)
├── poster.jpg          # Ảnh poster chính thức của chương trình
├── triumph_logo.png    # Logo Vương miện Triumph International
└── README.md           # Tài liệu hướng dẫn dự án
```
