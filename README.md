# Messenger

Ứng dụng Messenger Desktop cho Windows, hỗ trợ nhiều tài khoản, chạy trên Electron/Chromium.

## Tính năng chính

- Quản lý nhiều tài khoản Messenger bằng session riêng.
- Chuyển nhanh giữa các tài khoản ở sidebar.
- Khóa app bằng PIN.
- Thông báo và badge tin nhắn chưa đọc.
- Chế độ sáng/tối, ghim cửa sổ, thu nhỏ xuống khay hệ thống.
- Hỗ trợ gọi điện/video call qua Messenger Web.

## Cài đặt và chạy

Yêu cầu Node.js LTS.

```bash
npm install
npm start
```

## Build

```bash
npm run build
```

Hoặc build bản portable:

```bash
npm run build:portable
```

File build xuất hiện trong thư mục `dist/`.

## Cấu trúc

| File / thư mục | Chức năng |
| --- | --- |
| `main.js` | Quản lý vòng đời app, BrowserView, session, IPC. |
| `renderer.js` | Logic sidebar, profile, modal và điều khiển giao diện. |
| `index.html` | Giao diện shell của ứng dụng. |
| `preload.js` | Cầu nối an toàn giữa web content và app. |
| `custom_style.css` | CSS tùy chỉnh cho Messenger Web. |

## Lưu ý

Dữ liệu đăng nhập, cookies và session được lưu cục bộ theo profile trên máy đang chạy app.
