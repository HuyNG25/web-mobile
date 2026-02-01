# PCM Mobile - Pickleball Club Management

Ứng dụng quản lý câu lạc bộ Pickleball được xây dựng bằng Flutter Web.

## 🚀 Cách chạy ứng dụng

### Yêu cầu
- Node.js (để chạy local server)

### Chạy local
```bash
# Cài đặt serve (nếu chưa có)
npm install -g serve

# Chạy ứng dụng
cd pcm-web
npx serve . -l 3000
```

Truy cập: **http://localhost:3000**

---

## 📱 Hướng dẫn sử dụng

### 1. Đăng ký tài khoản
1. Tại màn hình đăng nhập, nhấn **"Đăng ký"**
2. Điền thông tin: Họ tên, Email, Số điện thoại, Mật khẩu
3. Nhấn **"Đăng ký"** để tạo tài khoản
4. Xác nhận OTP qua email/SMS

### 2. Đăng nhập
1. Nhập **Email** hoặc **Số điện thoại**
2. Nhập **Mật khẩu**
3. Nhấn **"Đăng nhập"**

### 3. Trang chủ (Dashboard)
- Xem thông tin tổng quan câu lạc bộ
- Xem lịch đặt sân sắp tới
- Thông báo mới nhất
- Truy cập nhanh các chức năng

### 4. Đặt sân (Court Booking)
1. Vào menu **"Đặt sân"**
2. Chọn ngày muốn đặt
3. Chọn sân và khung giờ trống
4. Xác nhận thông tin và thanh toán
5. Nhận xác nhận đặt sân qua thông báo

### 5. Ví điện tử (Wallet)
- **Nạp tiền**: Chọn số tiền → Chọn phương thức thanh toán → Xác nhận
- **Xem lịch sử**: Danh sách giao dịch nạp/rút/thanh toán
- **Số dư**: Hiển thị số dư hiện tại

### 6. Giải đấu (Tournament)
1. Vào menu **"Giải đấu"**
2. Xem danh sách giải đấu đang mở
3. Nhấn **"Đăng ký"** để tham gia
4. Điền thông tin đội/cá nhân
5. Thanh toán phí đăng ký
6. Theo dõi lịch thi đấu và kết quả

### 7. Thông báo
- Xem tất cả thông báo từ hệ thống
- Nhắc lịch đặt sân
- Cập nhật giải đấu
- Thông tin khuyến mãi

### 8. Hồ sơ cá nhân
- Xem và chỉnh sửa thông tin cá nhân
- Đổi mật khẩu
- Cài đặt thông báo
- Đăng xuất

---

## 🔧 Deploy lên server

### Sử dụng Nginx
```nginx
server {
    listen 80;
    server_name your-domain.com;
    
    root /path/to/pcm-web;
    index index.html;
    
    location / {
        try_files $uri $uri/ /index.html;
    }
}
```

### Sử dụng hosting tĩnh
Upload toàn bộ thư mục lên: Netlify, Vercel, GitHub Pages, Firebase Hosting...

---

## 📁 Cấu trúc thư mục

```
pcm-web/
├── index.html          # Entry point
├── main.dart.js        # Flutter compiled app
├── flutter.js          # Flutter engine
├── flutter_bootstrap.js
├── flutter_service_worker.js
├── manifest.json       # PWA manifest
├── favicon.png
├── version.json
├── assets/             # App resources
├── canvaskit/          # WebGL renderer
└── icons/              # App icons
```

---

## 📄 License

© 2026 PCM Mobile - All rights reserved.
