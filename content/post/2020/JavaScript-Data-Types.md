---
title: JavaScript Data Types  
date: 2023-12-30  
tags: ["javascript", "data types", "programming", "blog"]  
image: "/img/posts/img-23.png"  
Description: "Tìm hiểu các kiểu dữ liệu trong JavaScript, bao gồm các kiểu dữ liệu nguyên thủy và đối tượng, cùng với cách sử dụng chúng trong lập trình."  
---

### 1. JavaScript Data Types: Khái Niệm

JavaScript hỗ trợ hai loại kiểu dữ liệu chính: **Primitive (nguyên thủy)** và **Non-Primitive (phi nguyên thủy)**. Kiểu dữ liệu nguyên thủy là những kiểu dữ liệu không thể thay đổi, trong khi kiểu dữ liệu phi nguyên thủy là các đối tượng có thể thay đổi.

---

### 2. Các Kiểu Dữ Liệu Nguyên Thủy

#### **1. Number (Số)**

Kiểu `Number` được sử dụng để biểu diễn các giá trị số, bao gồm cả số nguyên và số thực.

- **Ví dụ**:
```javascript
let a = 10;   // Số nguyên
let b = 3.14; // Số thực
```

#### **2. String (Chuỗi)**

Kiểu `String` đại diện cho dãy ký tự. Dãy ký tự có thể được bao quanh bởi dấu nháy đơn (') hoặc nháy kép (").

- **Ví dụ**:
```javascript
let name = "John";  // Sử dụng dấu nháy kép
let greeting = 'Hello, World!';  // Sử dụng dấu nháy đơn
```

#### **3. Boolean (Boolean)**

Kiểu `Boolean` chỉ có hai giá trị là `true` và `false`, dùng để biểu diễn các giá trị logic.

- **Ví dụ**:
```javascript
let isJavaScriptFun = true;
let isCodingHard = false;
```

#### **4. Undefined (Chưa được định nghĩa)**

Kiểu `undefined` là giá trị mặc định của biến khi nó được khai báo nhưng chưa được gán giá trị.

- **Ví dụ**:
```javascript
let x;
console.log(x);  // In ra undefined
```

#### **5. Null (Null)**

Kiểu `null` đại diện cho một giá trị không tồn tại hoặc không hợp lệ. Đây là một kiểu dữ liệu đặc biệt, được sử dụng để chỉ rõ rằng một giá trị không có.

- **Ví dụ**:
```javascript
let y = null;
console.log(y);  // In ra null
```

#### **6. Symbol (Biểu tượng)**

Kiểu `Symbol` đại diện cho một giá trị duy nhất và không thể thay đổi. Symbol được sử dụng để tạo ra các giá trị không thể so sánh hoặc trùng lặp.

- **Ví dụ**:
```javascript
let sym = Symbol('description');
console.log(sym);  // In ra Symbol(description)
```

#### **7. BigInt (BigInt)**

Kiểu `BigInt` được sử dụng để biểu diễn các số nguyên rất lớn mà kiểu `Number` không thể lưu trữ được. BigInt có thể được tạo ra bằng cách thêm hậu tố `n` vào số nguyên.

- **Ví dụ**:
```javascript
let bigNumber = 1234567890123456789012345678901234567890n;
console.log(bigNumber);  // In ra 1234567890123456789012345678901234567890n
```

---

### 3. Các Kiểu Dữ Liệu Phi Nguyên Thủy

#### **1. Object (Đối tượng)**

Kiểu `Object` là một tập hợp các thuộc tính (properties), mỗi thuộc tính có một tên và giá trị. Đối tượng trong JavaScript có thể chứa các giá trị của bất kỳ kiểu dữ liệu nào, kể cả các đối tượng khác.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30,
  isStudent: false
};
```

#### **2. Array (Mảng)**

Mảng là một kiểu đối tượng đặc biệt dùng để lưu trữ danh sách các giá trị. Mảng có thể chứa các giá trị của nhiều kiểu dữ liệu khác nhau.

- **Ví dụ**:
```javascript
let colors = ["red", "green", "blue"];
console.log(colors[0]);  // In ra red
```

#### **3. Function (Hàm)**

Hàm là một đối tượng trong JavaScript có thể được gọi để thực thi một đoạn mã.

- **Ví dụ**:
```javascript
function greet(name) {
  return "Hello, " + name;
}
console.log(greet("John"));  // In ra Hello, John
```

---

### 4. Khi Nào Sử Dụng Các Kiểu Dữ Liệu

- **Number**: Khi bạn cần làm việc với các phép toán số học, chẳng hạn như cộng, trừ, nhân, chia.
- **String**: Khi bạn cần làm việc với chuỗi ký tự, chẳng hạn như hiển thị thông điệp hoặc thao tác với văn bản.
- **Boolean**: Khi bạn cần kiểm tra một điều kiện hoặc thực hiện các phép toán logic (true/false).
- **Undefined và Null**: Khi bạn muốn khởi tạo giá trị mặc định cho một biến mà chưa xác định giá trị cụ thể.
- **Symbol**: Khi bạn cần tạo các giá trị duy nhất mà không cần quan tâm đến giá trị cụ thể.
- **BigInt**: Khi bạn cần làm việc với số nguyên rất lớn, vượt qua giới hạn của Number.
- **Object và Array**: Khi bạn cần lưu trữ và xử lý nhiều giá trị dưới dạng các cặp khóa-giá trị hoặc danh sách dữ liệu.
- **Function**: Khi bạn cần tái sử dụng một đoạn mã nhiều lần thông qua một tên và có thể truyền đối số vào.