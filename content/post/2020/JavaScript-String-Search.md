---
title: JavaScript String Search  
date: 2023-12-31  
tags: ["javascript", "strings", "search", "blog"]  
image: "/img/posts/img-33.png"  
Description: "Tìm hiểu các phương thức tìm kiếm chuỗi trong JavaScript, giúp bạn kiểm tra sự tồn tại của chuỗi con trong một chuỗi lớn."  
---

### 1. Giới Thiệu về JavaScript String Search

Trong JavaScript, việc tìm kiếm chuỗi con trong một chuỗi lớn là một trong những thao tác cơ bản và phổ biến. JavaScript cung cấp một số phương thức để thực hiện công việc này, từ việc kiểm tra sự tồn tại của chuỗi con cho đến việc tìm vị trí của nó. Dưới đây là các phương thức tìm kiếm chuỗi trong JavaScript.

### 2. Các Phương Thức Tìm Kiếm Chuỗi

#### **1. indexOf()** - Tìm vị trí đầu tiên của chuỗi con

Phương thức `indexOf()` trả về chỉ số (index) đầu tiên của chuỗi con trong chuỗi, hoặc trả về `-1` nếu không tìm thấy chuỗi con.

```javascript
let str = "JavaScript is awesome!";
let result = str.indexOf("is");
console.log(result); // 10
```
- Nếu chuỗi con tồn tại, phương thức trả về chỉ số của ký tự đầu tiên của chuỗi con.
- Nếu chuỗi con không tồn tại, trả về -1.

#### **2. lastIndexOf()** - Tìm vị trí cuối cùng của chuỗi con

Phương thức `lastIndexOf()` tìm vị trí của chuỗi con từ cuối chuỗi ban đầu và trả về chỉ số của chuỗi con cuối cùng tìm thấy.

```javascript
let str = "JavaScript is fun, JavaScript is awesome!";
let result = str.lastIndexOf("JavaScript");
console.log(result); // 31
```
- Nếu không tìm thấy chuỗi con, phương thức trả về -1.

#### **3. includes()** - Kiểm tra chuỗi có chứa chuỗi con không

Phương thức `includes()` kiểm tra xem chuỗi có chứa chuỗi con hay không và trả về `true` nếu có, `false` nếu không.

```javascript
let str = "JavaScript is awesome!";
let result = str.includes("awesome");
console.log(result); // true
```
- Phương thức này không phân biệt chữ hoa và chữ thường (case-sensitive).

#### **4. startsWith()** - Kiểm tra chuỗi bắt đầu bằng chuỗi con

Phương thức `startsWith()` kiểm tra xem chuỗi có bắt đầu bằng chuỗi con xác định không.

```javascript
let str = "JavaScript is awesome!";
let result = str.startsWith("JavaScript");
console.log(result); // true
```
- Trả về `true` nếu chuỗi bắt đầu bằng chuỗi con, ngược lại trả về `false`.

#### **5. endsWith()** - Kiểm tra chuỗi kết thúc bằng chuỗi con

Phương thức `endsWith()` kiểm tra xem chuỗi có kết thúc bằng chuỗi con xác định không.

```javascript
let str = "JavaScript is awesome!";
let result = str.endsWith("awesome!");
console.log(result); // true
```
- Trả về `true` nếu chuỗi kết thúc bằng chuỗi con, ngược lại trả về `false`.

#### **6. search()** - Tìm chuỗi con sử dụng biểu thức chính quy

Phương thức `search()` tìm kiếm chuỗi con trong chuỗi lớn bằng cách sử dụng biểu thức chính quy và trả về chỉ số đầu tiên của chuỗi con tìm thấy.

```javascript
let str = "JavaScript is awesome!";
let result = str.search("awesome");
console.log(result); // 15
```
- Nếu không tìm thấy chuỗi con, phương thức trả về -1.

### 3. Sử Dụng Biểu Thức Chính Quy với search()

Phương thức `search()` rất hữu ích khi bạn cần tìm kiếm chuỗi con theo mẫu phức tạp, sử dụng biểu thức chính quy. Đây là ví dụ:

```javascript
let str = "JavaScript is awesome, isn't it?";
let result = str.search(/[A-Za-z]+/);  // Tìm kiếm từ đầu tiên là chữ cái
console.log(result); // 0
```
- Biểu thức chính quy `[A-Za-z]+` tìm kiếm tất cả các ký tự chữ cái đầu tiên trong chuỗi.
```