# Blog-app

Dự án Blog-app là một ứng dụng web fullstack gồm 2 phần:
- **Frontend (client):** ReactJS
- **Backend (server):** NodeJS, Express, Sequelize, MySQL

---

## Chức năng chính
- Xem danh sách các bài viết
- Đăng bài viết mới
- (Có thể mở rộng: Đăng nhập/Đăng ký, sửa/xóa bài viết...)

---

## Cấu trúc thư mục
```
Blog-app/
│
├── client/   # ReactJS frontend
│   └── README.md
│
├── server/   # NodeJS backend (Express, Sequelize)
│   └── README.md
│
└── README.md # File này (tổng thể)
```

---

## Hướng dẫn cài đặt & chạy toàn bộ dự án

### 1. Cài đặt backend (server)
```bash
cd server
npm install
```
- Tạo file `.env` trong thư mục `server/` với nội dung:
  ```
  DB_USER=your_mysql_user
  DB_PASSWORD=your_mysql_password
  DB_NAME=tutorialdb
  DB_HOST=127.0.0.1
  ```
- Tạo database `tutorialdb` trong MySQL.
- Chạy server:
  ```bash
  npm start
  ```
  Server chạy tại: http://localhost:3001

### 2. Cài đặt frontend (client)
```bash
cd client
npm install
npm start
```
Frontend chạy tại: http://localhost:3000

**Lưu ý:** Backend phải chạy trước để frontend hoạt động đúng.

---

## API Backend tiêu biểu
- `GET /posts` : Lấy danh sách bài viết
- `POST /posts` : Thêm bài viết mới (body: `{ title, postText, username }`)

---

## Bảo mật
- Không public file `.env` lên GitHub.
- Thông tin database được lấy từ biến môi trường.

---

## Tác giả
- VickyJang
"# BlogWeb" 
