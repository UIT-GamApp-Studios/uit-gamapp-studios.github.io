---
layout: default
---
<style>
table {
  border-collapse: collapse;
  width: 100%;
  margin: 16px 0;
}
th, td {
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 8px 12px;
  text-align: left;
}
thead {
  background-color: rgba(255, 255, 255, 0.1);
  font-weight: bold;
}
tbody tr:nth-child(even) {
  background-color: rgba(255, 255, 255, 0.05);
}
body, p, li, td, th, h1, h2, h3, h4, h5, h6 {
  color: #ffffff !important;
}
</style>

# HƯỚNG DẪN CHUẨN BỊ VÀ ĐĂNG GAME LÊN GOOGLE PLAY

Tài liệu hướng dẫn chi tiết quy trình chuẩn bị và triển khai game lên **Google Play Console**.



## 1. Build file APK để test
- Trước khi phát hành, **build 1 file .apk** để cài và test.
- Kiểm tra kỹ các chức năng: gameplay, giao diện, lưu dữ liệu, v.v.  
- Chuyển sang bước build **.aab** sau khi đã test ổn định.

<p align="center">
  <img src="/media/instruction/apk.png" alt="Build định dạng apk" width="400">
</p>



## 2. Thiết lập Player Settings
- Trước khi build, vào Player Setting để thiết lập các thông tin cần thiết.
- Điền tên company, game và chọn icon (kích thước 512x512).

<p align="center">
  <img src="/media/instruction/companyname.png" alt="Thiết lập thông tin" width="800">
</p>

- Mỗi game cần có một **bundle ID riêng**. Đây là mã nhận dạng Google Play sử dụng để phân biệt giữa các game và ứng dụng. Mã không được trùng lặp và thường có dạng: *com.yourcompany.yourgamename*.

<p align="center">
  <img src="/media/instruction/bundleid.png" alt="Thiết lập thông tin" width="800">
</p>

## 3. Build file **.aab**, tạo và lưu keystore
- Chọn **Custom Keystore**, vào **Keystore Manager**.
- Tạo mới **keystore**.  
- Cần lưu giữ lại đầy đủ các thành phần sau:
  - File **.keystore**.
  - Mật khẩu keystore.
  - Alias và mật khẩu.

<p align="center">
  <img src="/media/instruction/keystore.png" alt="Tạo keystore" width="800">
</p>
<p align="center">
  <img src="/media/instruction/keystore2.png" alt="Thiết lập keystore" width="800">
</p>

- Sau khi hoàn thành thiết lập, chọn và build file **định dạng .aab (Android App Bundle)**.

<p align="center">
  <img src="/media/instruction/aab.png" alt="Chọn định dạng aab" width="800">
</p>

## 4. Chuẩn bị hình ảnh

<table>
  <thead>
    <tr>
      <th>Loại</th>
      <th>Kích thước</th>
      <th>Ghi chú</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Screenshot (dọc/ngang)</strong></td>
      <td>1080x1920 hoặc 1920x1080</td>
      <td>4–6 hình, thể hiện gameplay thực tế.</td>
    </tr>
    <tr>
      <td><strong>App Icon</strong></td>
      <td>512x512 px</td>
      <td>Icon của game.</td>
    </tr>
    <tr>
      <td><strong>Feature Graphic</strong></td>
      <td>1024x500 px</td>
      <td>Hình đại diện cho game trước khi chạy video demo.</td>
    </tr>
  </tbody>
</table>

<p align="center">
  <img src="/media/instruction/feature.png" alt="Feature" width="300">
</p>

<p align="center">
  <img src="/media/instruction/screenshot.jpg" alt="Screenshot" width="300">
</p>


## 5. Soạn mô tả game
- **Short Description** (mô tả ngắn): ≤ 80 ký tự.  
  > Giới thiệu ngắn gọn điểm nổi bật.
- **Full Description** (mô tả đầy đủ): ≤ 4000 ký tự.  
  > Mô tả chi tiết các tính năng.


## 6. Liệt kê các plugin sử dụng trong game
Các công cụ, phần mềm bổ trợ được tích hợp vào game.
Ví dụ:
- In-App Purchase (IAP)
- Firebase 
- Google Ads
- Các plugin khác...


## 7. Chuẩn bị video demo (nếu có)
- Upload video gameplay lên **YouTube**.
- Video được dùng cho mục **Promo Video** trên Google Play.  
- Video dài 30–90s, thể hiện rõ gameplay chính.


## 8. Nộp sản phẩm
Mỗi sản phẩm lưu trong **một thư mục Google Drive riêng**, bao gồm:
  - File **.aab**, **.apk**
  - Ảnh & mô tả như yêu cầu, ghi chú plugin
  - Video demo (nếu có)



## 9. CHÚ Ý
- Nếu game có quảng cáo hoặc In-App Purchase (IAP), **Tài khoản quảng cáo và IAP** sẽ được tạo và gắn liền với **email Google Console** của khoa. Id sẽ được khoa cung cấp để sử dụng cho các game.
- **<mark>Không tự tạo ID riêng</mark>**, vì:
  - Dẫn đến **sai lệch** giữa tài khoản game và tài khoản quảng cáo.
  - Google có thể đánh policy vi phạm quản lý tài khoản.
