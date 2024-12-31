---
title: JavaScript Output Các Phương Thức Hiển Thị Kết Quả  
date: 2023-12-28  
tags: ["javascript", "output", "programming", "blog"]  
image: "/img/posts/img-30.png"  
Description: "Tìm hiểu các cách hiển thị kết quả trong JavaScript. Hướng dẫn chi tiết về document.write, console.log, alert, và innerHTML."  
---

### 1. JavaScript Output: Là Gì?  

JavaScript cung cấp nhiều cách khác nhau để hiển thị kết quả. Dưới đây là các phương thức phổ biến nhất.

---

### 2. `document.write()`  

Chức năng: Ghi nội dung trực tiếp vào tài liệu HTML.  

#### Cách sử dụng:  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document Write Example</title>
</head>
<body>
    <script>
        document.write("Hello, JavaScript Output!");
    </script>
</body>
</html>
```

### 3. `console.log()`
Chức năng: Ghi thông báo vào bảng điều khiển trình duyệt, thường được sử dụng để gỡ lỗi mã.

#### Cách sử dụng:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Console Log Example</title>
</head>
<body>
    <script>
        console.log("Hello, Console!");
    </script>
</body>
</html>
```

### 4. `alert()`
Chức năng: Hiển thị một hộp thoại bật lên với thông báo.

#### Cách sử dụng:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Alert Example</title>
</head>
<body>
    <script>
        alert("Hello, Alert Box!");
    </script>
</body>
</html>
```

### 5. `innerHTML`
Chức năng: Thay đổi nội dung của một phần tử HTML.

#### Cách sử dụng:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>InnerHTML Example</title>
</head>
<body>
    <p id="output"></p>
    <script>
        document.getElementById("output").innerHTML = "Hello, InnerHTML!";
    </script>
</body>
</html>
```

### 6. `window.print()`
Chức năng: Hiển thị hộp thoại in của trình duyệt, thường được sử dụng để in nội dung trang.

#### Cách sử dụng:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Print Example</title>
</head>
<body>
    <button onclick="window.print()">In Trang Này</button>
</body>
</html>
```