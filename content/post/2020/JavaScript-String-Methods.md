---
title: JavaScript String Methods  
date: 2023-12-31  
tags: ["javascript", "strings", "programming", "blog"]  
image: "/img/posts/img-32.png"  
Description: "Khám phá các phương thức chuỗi trong JavaScript, giúp bạn thao tác và xử lý các chuỗi một cách linh hoạt và hiệu quả."  
---

### 1. Giới Thiệu về JavaScript String Methods

JavaScript cung cấp rất nhiều phương thức để thao tác với chuỗi. Các phương thức này cho phép bạn xử lý và thay đổi chuỗi, từ việc tìm kiếm, thay thế, tách chuỗi đến việc thay đổi định dạng chuỗi. Dưới đây là một số phương thức chuỗi cơ bản và phổ biến trong JavaScript.

### 2. Các Phương Thức Chuỗi Cơ Bản

#### **1. length** - Độ dài của chuỗi

Trả về số lượng ký tự trong chuỗi.

```javascript
let str = "Hello, World!";
console.log(str.length); // 13
```

#### **2. indexOf()** - Tìm chỉ số của ký tự trong chuỗi

Trả về chỉ số đầu tiên của chuỗi con trong chuỗi (hoặc -1 nếu không tìm thấy).

```javascript
let str = "JavaScript is awesome!";
console.log(str.indexOf("is")); // 10
```

#### **3. lastIndexOf()** - Tìm chỉ số của ký tự trong chuỗi từ cuối

Tìm chỉ số của chuỗi con bắt đầu từ cuối chuỗi.

```javascript
let str = "JavaScript is awesome, JavaScript!";
console.log(str.lastIndexOf("JavaScript")); // 25
```

#### **4. slice()** - Cắt chuỗi

Cắt chuỗi từ vị trí bắt đầu đến vị trí kết thúc (không bao gồm vị trí kết thúc).

```javascript
let str = "JavaScript is fun!";
console.log(str.slice(0, 10)); // "JavaScript"
```

#### **5. substring()** - Tạo chuỗi con từ vị trí bắt đầu

Tạo chuỗi con từ vị trí bắt đầu đến vị trí kết thúc.

```javascript
let str = "JavaScript is fun!";
console.log(str.substring(0, 10)); // "JavaScript"
```

#### **6. substr()** - Tạo chuỗi con từ vị trí bắt đầu với độ dài xác định

Tạo chuỗi con từ vị trí bắt đầu với một độ dài xác định.

```javascript
let str = "JavaScript is fun!";
console.log(str.substr(0, 10)); // "JavaScript"
```

### 3. Các Phương Thức Định Dạng Chuỗi

#### **1. toLowerCase()** - Chuyển chuỗi thành chữ thường

Chuyển tất cả các ký tự trong chuỗi thành chữ thường.

```javascript
let str = "HELLO, WORLD!";
console.log(str.toLowerCase()); // "hello, world!"
```

#### **2. toUpperCase()** - Chuyển chuỗi thành chữ hoa

Chuyển tất cả các ký tự trong chuỗi thành chữ hoa.

```javascript
let str = "hello, world!";
console.log(str.toUpperCase()); // "HELLO, WORLD!"
```

#### **3. trim()** - Loại bỏ khoảng trắng ở đầu và cuối chuỗi

Loại bỏ tất cả khoảng trắng (spaces, tabs, newlines) ở đầu và cuối chuỗi.

```javascript
let str = "   Hello, World!   ";
console.log(str.trim()); // "Hello, World!"
```

### 4. Các Phương Thức Tìm Kiếm Chuỗi

#### **1. includes()** - Kiểm tra chuỗi có chứa một đoạn văn bản

Kiểm tra xem một chuỗi có chứa một đoạn chuỗi con không.

```javascript
let str = "JavaScript is awesome!";
console.log(str.includes("JavaScript")); // true
```

#### **2. startsWith()** - Kiểm tra chuỗi bắt đầu bằng một đoạn văn bản

Kiểm tra xem chuỗi có bắt đầu bằng một đoạn chuỗi con không.

```javascript
let str = "JavaScript is awesome!";
console.log(str.startsWith("Java")); // true
```

#### **3. endsWith()** - Kiểm tra chuỗi kết thúc bằng một đoạn văn bản

Kiểm tra xem chuỗi có kết thúc bằng một đoạn chuỗi con không.

```javascript
let str = "JavaScript is awesome!";
console.log(str.endsWith("awesome!")); // true
```

### 5. Các Phương Thức Thao Tác Với Các Ký Tự Trong Chuỗi

#### **1. charAt()** - Lấy ký tự tại một vị trí cụ thể

Trả về ký tự tại chỉ số xác định trong chuỗi.

```javascript
let str = "JavaScript";
console.log(str.charAt(4)); // "S"
```

#### **2. charCodeAt()** - Lấy mã ASCII của ký tự tại vị trí cụ thể

Trả về mã ASCII của ký tự tại vị trí xác định.

```javascript
let str = "JavaScript";
console.log(str.charCodeAt(4)); // 83
```

#### **3. codePointAt()** - Lấy mã điểm mã Unicode của ký tự tại vị trí cụ thể

Trả về mã điểm Unicode của ký tự tại vị trí xác định.

```javascript
let str = "JavaScript";
console.log(str.codePointAt(4)); // 83
```

#### **4. split()** - Tách chuỗi thành mảng

Chia chuỗi thành mảng dựa trên ký tự phân cách.

```javascript
let str = "apple,banana,cherry";
let arr = str.split(",");
console.log(arr); // ["apple", "banana", "cherry"]
```

#### **5. replace()** - Thay thế chuỗi con bằng chuỗi mới

Thay thế một phần của chuỗi bằng chuỗi khác.

```javascript
let str = "Hello, World!";
console.log(str.replace("World", "JavaScript")); // "Hello, JavaScript!"
```

### 6. Các Phương Thức Tạo Chuỗi Mới

#### **1. concat()** - Nối hai hoặc nhiều chuỗi lại với nhau

Nối hai hoặc nhiều chuỗi lại thành một chuỗi mới.

```javascript
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(", ", str2, "!")); // "Hello, World!"
```

#### **2. repeat()** - Lặp lại chuỗi một số lần

Tạo ra một chuỗi mới bằng cách lặp lại chuỗi ban đầu một số lần.

```javascript
let str = "Hello!";
console.log(str.repeat(3)); // "Hello!Hello!Hello!"
```

#### **3. padStart()** - Thêm ký tự vào đầu chuỗi

Thêm ký tự vào đầu chuỗi cho đến khi chuỗi đạt độ dài yêu cầu.

```javascript
let str = "5";
console.log(str.padStart(3, "0")); // "005"
```

#### **4. padEnd()** - Thêm ký tự vào cuối chuỗi

Thêm ký tự vào cuối chuỗi cho đến khi chuỗi đạt độ dài yêu cầu.

```javascript
let str = "5";
console.log(str.padEnd(3, "0")); // "500"
```
```