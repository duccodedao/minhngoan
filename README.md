# 🌐 Hub Portal - Vĩnh Trạch Đông

[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white)](https://firebase.google.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

**Hub Portal** là một ứng dụng Web Portal hiện đại, giúp quản lý tập trung các liên kết ứng dụng, danh bạ điện thoại và thông báo nội bộ. Được thiết kế tối ưu cho các đơn vị hành chính hoặc doanh nghiệp nhỏ.

[🌐 Xem Demo Trực Tuyến](https://your-app-url.web.app)

---

## ✨ Tính năng chính

### 👤 Người dùng (Guest)
- **Truy cập nhanh:** Tìm kiếm và mở ứng dụng/danh bạ chỉ với 1 cú chạm.
- **Đa giao diện:** Hỗ trợ Chế độ sáng (Light) và Tối (Dark).
- **PWA:** Cài đặt trực tiếp lên điện thoại (Add to Home Screen) như một ứng dụng thực thụ.
- **Thông báo:** Xem tin tức mới nhất từ bảng tin và thanh thông báo chạy chữ.

### 🔐 Quản trị viên (Admin)
- **Dashboard mạnh mẽ:** Quản lý toàn bộ ứng dụng, danh bạ qua Sidebar.
- **Phân quyền:** Hệ thống 2 cấp độ (Super Admin & Phó Admin).
- **Thùng rác:** Xóa tạm thời và khôi phục dữ liệu để tránh mất mát.
- **Sắp xếp kéo thả:** Thay đổi thứ tự danh mục và ứng dụng trực quan (Drag & Drop).
- **Xuất/Nhập dữ liệu:** Sao lưu dữ liệu ra file Excel hoặc JSON.
- **Nhật ký hoạt động:** Theo dõi mọi thay đổi từ các Admin khác.

---

## 🛠 Công nghệ sử dụng

- **Frontend:** HTML5, Tailwind CSS.
- **Backend:** Google Firebase (Firestore, Authentication, Hosting).
- **Icons:** [Lucide Icons](https://lucide.dev/).
- **Thư viện bổ trợ:** 
  - [SortableJS](https://sortablejs.github.io/Sortable/) (Kéo thả).
  - [SheetJS](https://sheetjs.com/) (Xử lý file Excel).

---

## 🚀 Hướng dẫn triển khai

### 1. Chuẩn bị
- Một tài khoản [Firebase](https://console.firebase.google.com/).
- Cài đặt [Firebase CLI](https://firebase.google.com/docs/cli) trên máy tính.

### 2. Thiết lập Firebase
1. **Authentication:** Bật phương thức đăng nhập bằng **Google**.
2. **Firestore Database:** 
   - Tạo database ở khu vực gần bạn nhất (ví dụ: `asia-southeast1`).
   - Cấu hình **Rules** (Xem file `firestore.rules` hoặc dán mã trong phần hướng dẫn chi tiết).
3. **Cấu hình ban đầu (Quan trọng):**
   - Đăng nhập vào web bằng Gmail của bạn để lấy **UID**.
   - Trong Firestore, tạo collection `settings` -> document `admins`.
   - Thêm trường `super_uid` (string) = `UID_CỦA_BẠN`.

### 3. Cài đặt mã nguồn
- Clone repository:
```bash
git clone https://github.com/username/hub-portal-vtd.git
