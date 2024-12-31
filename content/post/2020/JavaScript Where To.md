---
title: Tìm Hiểu JavaScript nên đặt ở đâu ?
date: 2023-12-28  
tags: ["javascript", "html", "programming", "blog"]  
image: "/img/posts/img-16.png"  
Description: "Hướng dẫn chi tiết về cách nhúng JavaScript vào trang HTML của bạn. Tìm hiểu sự khác biệt giữa <script> nội dòng, trong phần <head>, hoặc cuối <body> để tối ưu hiệu suất và trải nghiệm người dùng."  
---

### 1. JavaScript: Where To?  

Khi phát triển web, một câu hỏi phổ biến là: **"Nên đặt JavaScript ở đâu trong HTML?"**. JavaScript có thể được nhúng trực tiếp vào trang HTML thông qua ba cách chính:  

- Nội dòng (inline).  
- Trong phần `<head>`.  
- Trước thẻ đóng `</body>`.  

Hãy cùng tìm hiểu ưu, nhược điểm của từng cách!

---

### 2. Sử Dụng Nội Dòng (Inline Script)  

JavaScript có thể được viết trực tiếp trong thẻ HTML bằng cách sử dụng thuộc tính `onclick`, `onchange`, hoặc các sự kiện khác.  

#### **Ví dụ:**  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Inline JavaScript</title>
</head>
<body>
    <button onclick="alert('Hello, Inline JavaScript!')">Click Me</button>
</body>
</html>
```
**Ưu điểm:**
- Đơn giản, dễ dùng cho các dự án nhỏ.
- Không cần tệp JavaScript riêng biệt.

**Nhược điểm:**
- Khó bảo trì khi dự án lớn.
- Khó tách biệt mã HTML và JavaScript, làm giảm tính tái sử dụng.

### 3. Nhúng Trong `<head>`
Bạn có thể thêm JavaScript vào thẻ `<head>` trong HTML bằng thẻ `<script>`.

#### **Ví dụ:**  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>JavaScript in Head</title>
    <script>
        function greet() {
            alert('Hello, JavaScript in Head!');
        }
    </script>
</head>
<body>
    <button onclick="greet()">Click Me</button>
</body>
</html>
```
**Ưu điểm:**
- Tất cả mã JavaScript được đặt trong một nơi dễ quản lý.
- Tốt cho việc định nghĩa biến và hàm toàn cục.

**Nhược điểm:**
- Có thể làm chậm quá trình tải trang vì JavaScript sẽ được thực thi trước khi HTML được hiển thị.

### 4. Đặt Trước `</body>`
Cách phổ biến nhất là đặt JavaScript trước thẻ đóng `</body>`.

#### **Ví dụ:**  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>JavaScript Before Body</title>
</head>
<body>
    <button id="btn">Click Me</button>
    <script>
        document.getElementById('btn').addEventListener('click', function () {
            alert('Hello, JavaScript Before Body!');
        });
    </script>
</body>
</html>
```
**Ưu điểm:**
- Tăng tốc hiển thị trang: HTML được tải và hiển thị trước.
- Tối ưu trải nghiệm người dùng.

**Nhược điểm:**
- Mã JavaScript không sẵn sàng cho đến khi toàn bộ HTML được tải.

### 5. Tách JavaScript Thành File Riêng
Một cách tối ưu hơn là lưu mã JavaScript trong một tệp `.js` riêng biệt và nhúng vào HTML bằng thẻ `<script>`.

#### **Ví dụ:**  
**HTML:**  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>External JavaScript</title>
</head>
<body>
    <button id="btn">Click Me</button>
    <script src="script.js"></script>
</body>
</html>
```
**script.js:**  
```javascript
document.getElementById('btn').addEventListener('click', function () {
    alert('Hello, External JavaScript!');
});
```
**Ưu điểm:**
- Tách biệt rõ ràng giữa mã HTML và JavaScript.
- Dễ dàng tái sử dụng mã JavaScript.

**Nhược điểm:**
- Phụ thuộc vào mạng để tải tệp `.js`.

### 6. Kết Luận
Việc lựa chọn vị trí nhúng JavaScript trong HTML có thể ảnh hưởng đến hiệu suất và trải nghiệm người dùng. Hãy cân nhắc các ưu nhược điểm của từng phương pháp để đưa ra quyết định phù hợp cho dự án của bạn.