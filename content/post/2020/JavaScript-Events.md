---
title: JavaScript Events  
date: 2023-12-30  
tags: ["javascript", "events", "programming", "blog"]  
image: "/img/posts/img-26.png"  
Description: "Khám phá cách sử dụng và xử lý các sự kiện trong JavaScript. Bài viết này cung cấp thông tin chi tiết về các sự kiện phổ biến và cách sử dụng chúng trong các ứng dụng web."  
---

### 1. Giới Thiệu về JavaScript Events

Trong JavaScript, **events** (sự kiện) là các hành động hoặc sự thay đổi xảy ra trong ứng dụng mà bạn có thể xử lý. Các sự kiện thường được liên kết với các yếu tố DOM (Document Object Model) như nút nhấn, di chuyển chuột, gõ phím, và nhiều hành động khác.

Sự kiện giúp bạn tương tác với người dùng, thực hiện các hành động như thay đổi nội dung, hiển thị thông báo, hoặc gửi dữ liệu mà không làm mới trang.

---

### 2. Các Loại JavaScript Events

Dưới đây là một số sự kiện phổ biến trong JavaScript:

- **click**: Khi người dùng nhấp chuột vào một phần tử.
- **keypress**: Khi người dùng nhấn một phím.
- **mouseover**: Khi con trỏ chuột di chuyển vào phần tử.
- **mouseout**: Khi con trỏ chuột di chuyển ra khỏi phần tử.
- **keydown**: Khi người dùng nhấn một phím và giữ.
- **keyup**: Khi người dùng nhấn và thả một phím.
- **submit**: Khi một biểu mẫu được gửi.

---

### 3. Cách Đăng Ký và Xử Lý Sự Kiện

Để xử lý một sự kiện trong JavaScript, bạn cần đăng ký sự kiện cho một phần tử và chỉ định một hàm xử lý sự kiện (event handler). Có thể đăng ký sự kiện bằng cách sử dụng `addEventListener()` hoặc các thuộc tính sự kiện như `onclick`.

#### **1. Sử Dụng addEventListener()**

Phương thức `addEventListener()` cho phép bạn đăng ký một sự kiện và chỉ định một hàm để xử lý khi sự kiện xảy ra.

- **Cú pháp**:
```javascript
element.addEventListener(event, function, useCapture);
```

- **Ví dụ**:
```javascript
const button = document.getElementById("myButton");

button.addEventListener("click", function() {
  alert("Button clicked!");
});
```
Khi người dùng nhấp vào nút, hàm sẽ được gọi và hiển thị thông báo.

#### **2. Sử Dụng Thuộc Tính Sự Kiện**

Bạn cũng có thể đăng ký sự kiện trực tiếp trên phần tử bằng cách sử dụng các thuộc tính sự kiện như `onclick`, `onmouseover`, v.v.

- **Ví dụ**:
```html
<button id="myButton" onclick="alert('Button clicked!')">Click Me</button>
```
Mặc dù cách này nhanh chóng, nhưng sử dụng `addEventListener()` giúp bạn có thể gắn nhiều sự kiện cho một phần tử, điều mà thuộc tính sự kiện không hỗ trợ.

#### **3. Sử Dụng Tham Số Event**

Khi một sự kiện xảy ra, JavaScript tự động truyền một đối tượng sự kiện (Event object) vào hàm xử lý sự kiện. Đối tượng này chứa các thông tin về sự kiện, như loại sự kiện, phần tử kích hoạt sự kiện, và các thuộc tính khác.

- **Ví dụ**:
```javascript
const button = document.getElementById("myButton");

button.addEventListener("click", function(event) {
  console.log("Event type: " + event.type);
  console.log("Event target: " + event.target);
});
```
Trong ví dụ trên, đối tượng `event` cung cấp thông tin về sự kiện đã xảy ra, như loại sự kiện (click) và phần tử kích hoạt sự kiện.

#### **4. Ngừng Propagation và Ngăn Chặn Mặc Định**

Trong JavaScript, bạn có thể kiểm soát sự lan truyền của sự kiện và ngừng hành động mặc định của sự kiện.

- **Ngừng Lan Truyền (Event Propagation)**: Lan truyền sự kiện là quá trình sự kiện được truyền từ phần tử con đến phần tử cha. Để ngừng quá trình này, bạn có thể sử dụng phương thức `stopPropagation()`.

- **Ví dụ**:
```javascript
document.getElementById("parent").addEventListener("click", function() {
  console.log("Parent clicked!");
});

document.getElementById("child").addEventListener("click", function(event) {
  event.stopPropagation();
  console.log("Child clicked!");
});
```
Trong ví dụ này, khi người dùng nhấp vào phần tử con, sự kiện không được truyền lên phần tử cha.

- **Ngừng Hành Động Mặc Định (Prevent Default Action)**: Phương thức `preventDefault()` ngừng hành động mặc định của sự kiện, chẳng hạn như gửi một biểu mẫu khi nhấp vào nút gửi.

- **Ví dụ**:
```javascript
document.getElementById("myForm").addEventListener("submit", function(event) {
  event.preventDefault();
  alert("Form submission prevented!");
});
```

---

### 4. Trình xử lý sự kiện JavaScript

Trình xử lý sự kiện có thể được sử dụng để xử lý và xác minh dữ liệu đầu vào của người dùng, hành động của người dùng và hành động của trình duyệt:

- Những việc cần làm mỗi khi tải trang
- Những việc cần làm khi đóng trang
- Hành động cần thực hiện khi người dùng nhấp vào nút
- Nội dung cần được xác minh khi người dùng nhập dữ liệu
- Và nhiều hơn nữa...

Có thể sử dụng nhiều phương pháp khác nhau để JavaScript hoạt động với các sự kiện:

- Thuộc tính sự kiện HTML có thể thực thi mã JavaScript trực tiếp
- Thuộc tính sự kiện HTML có thể gọi các hàm JavaScript
- Bạn có thể gán các hàm xử lý sự kiện của riêng bạn cho các phần tử HTML
- Bạn có thể ngăn chặn các sự kiện được gửi hoặc được xử lý
- Và nhiều hơn nữa...
```