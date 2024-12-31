---
title: JavaScript Syntax Cú Pháp Cơ Bản  
date: 2023-12-30  
tags: ["javascript", "syntax", "programming", "blog"]  
image: "/img/posts/img-15.png"  
Description: "Khám phá cú pháp cơ bản trong JavaScript. Bài viết sẽ hướng dẫn về cách viết mã JavaScript chuẩn, bao gồm khai báo biến, lệnh điều kiện, vòng lặp và hàm."  
---

### 1. JavaScript Syntax: Là Gì?  

Cú pháp JavaScript xác định cách thức viết mã JavaScript đúng để trình duyệt hoặc môi trường JavaScript có thể hiểu và thực thi. Các quy tắc cú pháp cơ bản bao gồm cách khai báo biến, cách viết các biểu thức, lệnh điều kiện, vòng lặp, và các hàm.

---

### 2. Cú Pháp Cơ Bản trong JavaScript  

#### 2.1. Khai Báo Biến  

JavaScript cung cấp ba cách để khai báo biến: `var`, `let`, và `const`.  

- **`var`**: Khai báo biến với phạm vi toàn cục hoặc hàm.
- **`let`**: Khai báo biến với phạm vi khối (block-level).
- **`const`**: Khai báo hằng số, không thể thay đổi giá trị sau khi đã được gán.

Cách sử dụng:
```javascript
let x = 10;  // Biến có thể thay đổi giá trị
const y = 20;  // Hằng số không thay đổi giá trị
```

#### 2.2. Các Lệnh Điều Kiện
JavaScript cung cấp các cấu trúc điều kiện như `if`, `else`, `else if`, và `switch`.

Cách sử dụng:
```javascript
let age = 20;

if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}
```

Cách sử dụng `switch`:
```javascript
let day = 2;
switch(day) {
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    default:
        console.log("Other day");
}
```

#### 2.3. Vòng Lặp
Các vòng lặp cơ bản trong JavaScript gồm `for`, `while`, và `do...while`.

Cách sử dụng vòng lặp `for`:
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

Cách sử dụng vòng lặp `while`:
```javascript
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

#### 2.4. Hàm
Hàm trong JavaScript được định nghĩa bằng từ khóa `function`. Hàm có thể nhận đối số và trả về giá trị.

Cách sử dụng:
```javascript
function add(a, b) {
    return a + b;
}

let sum = add(3, 4);
console.log(sum);  // In ra 7
```

#### 2.5. Biểu Thức và Toán Tử
Biểu thức trong JavaScript là các phép toán hoặc các phép tính có thể trả về giá trị. Toán tử là các ký hiệu dùng để thực hiện các phép toán.

Cách sử dụng:
```javascript
let x = 10;
let y = 5;
let sum = x + y;  // Toán tử cộng
let product = x * y;  // Toán tử nhân
```

#### 2.6. Câu Lệnh Trả Về (return)
Câu lệnh `return` được sử dụng trong hàm để trả về giá trị từ hàm.

Cách sử dụng:
```javascript
function multiply(a, b) {
    return a * b;
}

let result = multiply(3, 5);
console.log(result);  // In ra 15
```