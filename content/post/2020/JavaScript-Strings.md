---
title: JavaScript Strings  
date: 2023-12-31  
tags: ["javascript", "strings", "programming", "blog"]  
image: "/img/posts/img-34.png"  
Description: "Khám phá cách sử dụng chuỗi trong JavaScript. Bài viết này sẽ giới thiệu về cú pháp và các phương thức thường dùng để làm việc với chuỗi trong JavaScript."  
---

### 1. Giới Thiệu về JavaScript Strings

Trong JavaScript, **String** là một kiểu dữ liệu đại diện cho một chuỗi các ký tự. Chuỗi có thể bao gồm chữ cái, số, hoặc các ký tự đặc biệt. Chúng được sử dụng để lưu trữ và thao tác với văn bản.

### 2. Cách Khai Báo và Khởi Tạo Chuỗi

Bạn có thể khai báo chuỗi trong JavaScript bằng cách sử dụng dấu ngoặc kép (`""`), dấu nháy đơn (`''`), hoặc dấu nháy kép với backticks (````) cho các chuỗi đa dòng.

#### **Ví dụ:**

```javascript
let str1 = "Hello, World!";
let str2 = 'JavaScript is fun!';
let str3 = `This is a string with a line break
and this is on a new line.`;
```
Dấu ngoặc kép ("") và dấu nháy đơn ('') hoạt động tương tự nhau.  
Dấu backticks (````) cho phép bạn tạo chuỗi đa dòng và sử dụng template literals để chèn các biến vào trong chuỗi.

### 3. Các Phương Thức Thường Dùng với Chuỗi

JavaScript cung cấp một số phương thức để thao tác với chuỗi. Dưới đây là một số phương thức phổ biến:

1. **length** - Độ dài của chuỗi  
   Trả về số lượng ký tự trong chuỗi.
   ```javascript
   let str = "Hello, World!";
   console.log(str.length); // 13
   ```

2. **indexOf()** - Tìm chỉ số của ký tự đầu tiên  
   Trả về chỉ số của ký tự đầu tiên trong chuỗi (hoặc -1 nếu không tìm thấy).
   ```javascript
   let str = "JavaScript is awesome!";
   console.log(str.indexOf("is")); // 10
   ```

3. **toLowerCase()** - Chuyển chuỗi thành chữ thường  
   Chuyển tất cả các ký tự trong chuỗi thành chữ thường.
   ```javascript
   let str = "HELLO, WORLD!";
   console.log(str.toLowerCase()); // "hello, world!"
   ```

4. **toUpperCase()** - Chuyển chuỗi thành chữ hoa  
   Chuyển tất cả các ký tự trong chuỗi thành chữ hoa.
   ```javascript
   let str = "hello, world!";
   console.log(str.toUpperCase()); // "HELLO, WORLD!"
   ```

5. **trim()** - Loại bỏ khoảng trắng ở đầu và cuối chuỗi  
   Loại bỏ tất cả khoảng trắng (spaces, tabs, newlines) ở đầu và cuối chuỗi.
   ```javascript
   let str = "   Hello, World!   ";
   console.log(str.trim()); // "Hello, World!"
   ```

6. **slice()** - Cắt một phần của chuỗi  
   Trả về một phần chuỗi từ vị trí bắt đầu (inclusive) đến vị trí kết thúc (exclusive).
   ```javascript
   let str = "JavaScript is fun!";
   console.log(str.slice(0, 10)); // "JavaScript"
   ```

7. **replace()** - Thay thế một phần chuỗi  
   Thay thế một phần của chuỗi bằng chuỗi khác.
   ```javascript
   let str = "Hello, World!";
   console.log(str.replace("World", "JavaScript")); // "Hello, JavaScript!"
   ```

8. **split()** - Chia chuỗi thành mảng  
   Chia chuỗi thành mảng dựa trên ký tự phân cách.
   ```javascript
   let str = "apple,banana,cherry";
   let arr = str.split(",");
   console.log(arr); // ["apple", "banana", "cherry"]
   ```

9. **charAt()** - Lấy ký tự tại một vị trí cụ thể  
   Trả về ký tự tại chỉ số xác định.
   ```javascript
   let str = "JavaScript";
   console.log(str.charAt(4)); // "S"
   ```

### 4. Template Literals (Chuỗi Mẫu)

Template literals là cách mới để tạo chuỗi trong JavaScript, cho phép bạn chèn các biến và biểu thức vào trong chuỗi dễ dàng hơn.

Cú pháp:
```javascript
let name = "John";
let age = 25;
let sentence = `My name is ${name} and I am ${age} years old.`;
console.log(sentence); // "My name is John and I am 25 years old."
```
`${variable}` cho phép bạn chèn giá trị của một biến hoặc biểu thức vào trong chuỗi.

### 5. Các Phương Thức Tìm Kiếm Chuỗi

1. **includes()** - Kiểm tra chuỗi có chứa một đoạn văn bản  
   Kiểm tra xem một chuỗi có chứa một đoạn chuỗi con không.
   ```javascript
   let str = "JavaScript is awesome!";
   console.log(str.includes("JavaScript")); // true
   ```

2. **startsWith()** - Kiểm tra chuỗi bắt đầu bằng một đoạn văn bản  
   Kiểm tra xem chuỗi có bắt đầu bằng một đoạn chuỗi con không.
   ```javascript
   let str = "JavaScript is awesome!";
   console.log(str.startsWith("Java")); // true
   ```

3. **endsWith()** - Kiểm tra chuỗi kết thúc bằng một đoạn văn bản  
   Kiểm tra xem chuỗi có kết thúc bằng một đoạn chuỗi con không.
   ```javascript
   let str = "JavaScript is awesome!";
   console.log(str.endsWith("awesome!")); // true
   ```
```