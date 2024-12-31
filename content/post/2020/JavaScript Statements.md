---
title: JavaScript Statements Các Lệnh Cơ Bản  
date: 2023-12-29  
tags: ["javascript", "statements", "programming", "blog"]  
image: "/img/posts/img-14.png"  
Description: "Khám phá các loại lệnh trong JavaScript và cách sử dụng chúng. Tìm hiểu các lệnh cơ bản như expressions, declarations, loops và conditionals."  
---

### 1. JavaScript Statements: Là Gì?  

Một lệnh trong JavaScript là một câu lệnh thực thi một hành động cụ thể. Lệnh có thể là một biểu thức (expression) hoặc một lệnh điều kiện, vòng lặp, khai báo biến, v.v.

---

### 2. Các Loại Lệnh trong JavaScript  

#### 2.1. Lệnh Biểu Thức (Expression Statements)  

Chức năng: Các biểu thức trong JavaScript có thể thực thi hành động và trả về giá trị.  

Cách sử dụng:  
```javascript
let x = 10;  // Biểu thức gán
console.log(x);  // Biểu thức gọi hàm
```

#### 2.2. Lệnh Điều Kiện (Conditional Statements)
Chức năng: Sử dụng để kiểm tra một điều kiện và thực hiện các hành động khác nhau tùy thuộc vào kết quả điều kiện.

Cách sử dụng:
```javascript
let age = 18;
if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}
```

#### 2.3. Lệnh Vòng Lặp (Loop Statements)
Chức năng: Lệnh vòng lặp được sử dụng để lặp lại một đoạn mã nhiều lần. Các vòng lặp phổ biến trong JavaScript bao gồm for, while, và do...while.

Cách sử dụng (vòng lặp for):
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

Cách sử dụng (vòng lặp while):
```javascript
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

#### 2.4. Lệnh Khai Báo Biến (Declaration Statements)
Chức năng: Được sử dụng để khai báo các biến, hằng số hoặc các đối tượng trong JavaScript.

Cách sử dụng:
```javascript
let x = 5;   // Khai báo biến
const y = 10; // Khai báo hằng số
```

#### 2.5. Lệnh Trả Về (Return Statements)
Chức năng: Lệnh return được sử dụng để trả về giá trị từ một hàm.

Cách sử dụng:
```javascript
function add(a, b) {
    return a + b;
}

let sum = add(3, 4);
console.log(sum);  // In ra 7
```

#### 2.6. Lệnh Thử (Throw Statements)
Chức năng: Lệnh throw được sử dụng để ném ra một ngoại lệ (exception) khi có lỗi xảy ra.

Cách sử dụng:
```javascript
function checkAge(age) {
    if (age < 18) {
        throw "Age must be 18 or older";
    } else {
        console.log("Age is valid");
    }
}

checkAge(15);  // Ném ra lỗi: "Age must be 18 or older"
```