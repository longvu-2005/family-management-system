# 🏡 Family Management System (Hệ Thống Quản Lý Gia Đình Tích Hợp AI)

> **Dự án Startup Web Application** giúp kết nối các thành viên trong gia đình, hỗ trợ quản lý tài chính cá nhân/gia đình, lập kế hoạch công việc chung và tích hợp trợ lý AI thông minh qua API.

---

## 📌 1. Giới thiệu dự án

**Family Management System** là nền tảng quản lý gia đình toàn diện, giúp đơn giản hóa việc quản lý chi tiêu, phân công công việc và tăng cường tương tác giữa các thành viên. Hệ thống được tích hợp trợ lý AI thông minh giúp tự động phân tích ngân sách, tư vấn tài chính và đề xuất kế hoạch hoạt động dựa trên dữ liệu thực tế.

---

## 🚀 2. Tính năng chính (Key Features)

### 👨‍👩‍👧‍👦 Quản lý thành viên & Gia đình
* **Tạo & Tham gia nhóm:** Chủ hộ (Admin) khởi tạo nhóm gia đình và tạo **mã mời (Invite Code)** để các thành viên khác tham gia.
* **Phân quyền người dùng:** Quản lý vai trò (Admin / Member) với các quyền hạn xem, thêm, sửa dữ liệu thu chi và công việc.

### 💰 Quản lý Tài chính & Thu Chi Gia Đình
* **Ghi nhận giao dịch:** Thêm, sửa, xóa các khoản thu/chi theo danh mục (Ăn uống, Điện nước, Lương, Mua sắm...).
* **Thống kê & Báo cáo:** Hiển thị biểu đồ chi tiêu trực quan theo tuần, tháng, năm.
* **Ngân sách chung:** Theo dõi quỹ chung của gia đình và số tiền do từng thành viên đóng góp/chi tiêu.

### 🤖 Trợ lý AI Thông Minh (AI Assistant Integration)
* **Tư vấn tài chính tự động:** AI phân tích thói quen chi tiêu hàng tháng và đưa ra lời khuyên tiết kiệm cụ thể.
* **Hỗ trợ lập kế hoạch:** Tự động tạo danh sách công việc và dự trù chi phí dựa trên yêu cầu (ví dụ: *"Lập kế hoạch du lịch 3 ngày 2 đêm cho 4 người"*).
* **Lưu trữ lịch sử:** Hệ thống lưu vết các đoạn hội thoại với AI để thành viên xem lại khi cần.

### 💬 Nhắn tin Trực tiếp (Real-time Family Chat)
* **Trò chuyện gia đình:** Nhắn tin thời gian thực giữa các thành viên qua WebSocket.
* **Tích hợp Bot AI:** Tương tác trực tiếp với Trợ lý AI ngay trong khung chat nhóm.

### 📋 Lập Kế Hoạch & Công Việc Chung (Family Tasks & Plans)
* **Quản lý To-do List:** Tạo công việc, phân công người thực hiện, đặt hạn chót (Due date).
* **Theo dõi tiến độ:** Cập nhật trạng thái công việc (Chưa làm, Đang làm, Đã hoàn thành).

---

## 🛠️ 3. Công nghệ sử dụng (Tech Stack)

### Backend
* **Language:** Java 17+
* **Framework:** Spring Boot (Spring Data JPA, Spring Security, Spring WebSocket)
* **Database:** Microsoft SQL Server
* **Authentication:** JWT (JSON Web Token)
* **AI Integration:** Google Gemini API / OpenAI API

### Frontend
* **Framework:** ReactJS / Next.js
* **Styling:** Bootstrap 5 / Tailwind CSS
* **State Management & HTTP:** Redux Toolkit / Axios
* **Real-time:** SockJS & STOMP (WebSocket)

### DevOps & Tools
* **Version Control:** Git, GitHub
* **IDE:** VS Code, IntelliJ IDEA
* **Database Management:** SQL Server Management Studio (SSMS)

---

## 🗄️ 4. Sơ đồ Cấu trúc Cơ sở Dữ liệu (Database Schema)

Hệ thống bao gồm 7 bảng cốt lõi trong SQL Server:

1. **`Users`**: Lưu trữ thông tin tài khoản người dùng.
2. **`Families`**: Lưu trữ thông tin nhóm gia đình và mã mời (`invite_code`).
3. **`Family_Members`**: Liên kết User với Family và phân quyền (`ADMIN` / `MEMBER`).
4. **`Categories`**: Danh mục thu/chi (Ăn uống, Điện nước, Lương...).
5. **`Transactions`**: Giao dịch thu/chi chi tiết của từng thành viên.
6. **`Messages`**: Lịch sử tin nhắn giữa các thành viên và phản hồi từ AI Bot.
7. **`Plans`**: Danh sách công việc/kế hoạch cần làm của gia đình.

---

## 💻 5. Hướng dẫn Cài đặt & Chạy dự án (Local Setup)

### Yêu cầu hệ thống
* **Java JDK:** 17 trở lên
* **Node.js:** v18+
* **SQL Server:** 2019 trở lên (hoặc SSMS)
* **Git**

### Bước 1: Clone Repository
```bash
git clone [https://github.com/longvu-2005/family-management-system.git](https://github.com/longvu-2005/family-management-system.git)
cd family-management-system