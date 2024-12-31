---
title: JavaScript const Khai Báo Biến Hằng  
date: 2023-12-30  
tags: ["javascript", "const", "programming", "blog"]  
image: "/img/posts/img-22.png"  
Description: "Tìm hiểu về `const` trong JavaScript, cách khai báo và sử dụng biến hằng, và khi nào nên sử dụng `const` thay vì các từ khóa khai báo biến khác."  
---

### 1. JavaScript `const`: Khái Niệm Cơ Bản

`const` là một từ khóa trong JavaScript được dùng để khai báo các biến mà giá trị của chúng không thể thay đổi sau khi đã được gán. Được giới thiệu trong ES6, `const` giúp tạo ra các biến hằng (constant) trong mã của bạn, giúp bảo vệ giá trị của biến khỏi sự thay đổi không mong muốn.

Khi bạn khai báo một biến với `const`, bạn không thể thay đổi giá trị của nó sau khi đã gán.

---

### 2. Cách Khai Báo và Sử Dụng `const`

Để khai báo một biến bằng `const`, bạn sử dụng cú pháp sau:
```javascript
const x = 10;  // Khai báo biến hằng
```
Không thể thay đổi giá trị của biến sau khi đã được gán:
```javascript
const x = 10;
x = 20;  // Lỗi: "Assignment to constant variable."
```
**Lưu ý:** Tuy nhiên, điều này không áp dụng với các đối tượng và mảng. Bạn có thể thay đổi các giá trị bên trong đối tượng hoặc mảng khai báo với `const`, nhưng không thể gán lại cả đối tượng hoặc mảng mới.

Ví dụ:
```javascript
const obj = { name: "John" };
obj.name = "Doe";  // Điều này hợp lệ
obj = {};  // Lỗi: "Assignment to constant variable."
```

### 3. Khi Nào Sử Dụng `const`

Sử dụng `const` khi bạn muốn khai báo một giá trị mà bạn không muốn thay đổi trong suốt vòng đời của chương trình, giúp bảo vệ giá trị của biến khỏi sự thay đổi ngẫu nhiên. Đây là lựa chọn lý tưởng khi bạn làm việc với các giá trị không đổi như:

- Các hằng số (ví dụ: số Pi).
- Các tham số không thay đổi trong hàm.
- Đối tượng hoặc mảng không thay đổi (dù các phần tử trong đó có thể thay đổi).

Ví dụ:
```javascript
const PI = 3.14159;  // Hằng số không đổi
const MAX_USERS = 100;  // Hằng số giới hạn
```

### 4. Phạm Vi của `const`

`const` có phạm vi khối (block scope), điều này có nghĩa là biến khai báo bằng `const` chỉ có thể truy cập trong khối mã (block) mà nó được khai báo, ví dụ: trong một vòng lặp hoặc một câu điều kiện.

Ví dụ:
```javascript
if (true) {
    const y = 50;
    console.log(y);  // In ra 50
}
console.log(y);  // Lỗi: "y is not defined"
```

### 5. `const` và Mảng/Đối Tượng

Dù giá trị của biến khai báo với `const` không thể thay đổi, nhưng nếu biến đó là một đối tượng hoặc mảng, bạn có thể thay đổi nội dung bên trong đối tượng/mảng đó.

Ví dụ với mảng:
```javascript
const numbers = [1, 2, 3];
numbers.push(4);  // Hợp lệ
console.log(numbers);  // In ra [1, 2, 3, 4]

numbers = [5, 6, 7];  // Lỗi: "Assignment to constant variable."
```

Ví dụ với đối tượng:
```javascript
const user = { name: "Alice", age: 25 };
user.age = 26;  // Hợp lệ
console.log(user);  // In ra { name: "Alice", age: 26 }

user = { name: "Bob", age: 30 };  // Lỗi: "Assignment to constant variable."
```