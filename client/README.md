# Blog-app

Ứng dụng Blog-app gồm 2 phần:
- **Frontend (client):** ReactJS
- **Backend (server):** NodeJS, Express, Sequelize, MySQL

---

## 1. Chức năng chính
- Xem danh sách các bài viết
- Đăng bài viết mới
- (Có thể mở rộng: Đăng nhập/Đăng ký, sửa/xóa bài viết...)

---

## 2. Cấu trúc thư mục
```
Blog-app/
│
├── client/   # ReactJS frontend
│
└── server/   # NodeJS backend (Express, Sequelize)
```

---

## 3. Hướng dẫn cài đặt & chạy ứng dụng

### 3.1. Cài đặt backend (server)
```bash
cd server
npm install
```
- **Bảo mật database:**
  - Tạo file `.env` trong thư mục `server/` với nội dung:
    ```
    DB_USER=your_mysql_user
    DB_PASSWORD=your_mysql_password
    DB_NAME=tutorialdb
    DB_HOST=127.0.0.1
    ```
  - Không public thông tin này lên GitHub.
- Khởi động backend:
```bash
npm start
```
Server chạy tại: http://localhost:3001

### 3.2. Cài đặt frontend (client)
```bash
cd client
npm install
npm start
```
Frontend chạy tại: http://localhost:3000

---

## 4. API Backend
- **GET /posts**: Lấy danh sách bài viết
- **POST /posts**: Thêm bài viết mới (body: `{ title, postText, username }`)

### Cấu trúc dữ liệu bài viết (Posts):
- `title`: Tiêu đề (string)
- `postText`: Nội dung (string)
- `username`: Người đăng (string)

---

## 5. Database
- Sử dụng MySQL
- Bạn cần tạo database `tutorialdb` trước khi chạy backend.
- Thông tin kết nối được lưu trong file `.env` (xem hướng dẫn trên).

---

## 6. Tác giả
- VickyJang