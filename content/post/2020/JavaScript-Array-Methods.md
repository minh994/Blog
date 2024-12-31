---
title: JavaScript Array Methods  
date: 2023-12-31  
tags: ["javascript", "arrays", "methods", "blog"]  
image: "/img/posts/img-19.png"  
Description: "Tìm hiểu các phương thức cơ bản và phổ biến khi làm việc với mảng trong JavaScript. Các phương thức này giúp bạn thao tác và quản lý mảng dễ dàng hơn."  
---

### 1. Giới Thiệu về JavaScript Array Methods

Mảng trong JavaScript là một kiểu dữ liệu dùng để lưu trữ một tập hợp các giá trị có thể có cùng hoặc khác kiểu dữ liệu. JavaScript cung cấp rất nhiều phương thức hữu ích để thao tác với mảng. Dưới đây là một số phương thức phổ biến khi làm việc với mảng trong JavaScript.

### 2. Các Phương Thức Cơ Bản của Mảng

#### **1. push()** - Thêm phần tử vào cuối mảng

Phương thức `push()` thêm một hoặc nhiều phần tử vào cuối mảng và trả về độ dài mới của mảng.

```javascript
let fruits = ["apple", "banana"];
fruits.push("orange");
console.log(fruits); // ["apple", "banana", "orange"]
```

#### **2. pop()** - Loại bỏ phần tử cuối cùng của mảng

Phương thức `pop()` loại bỏ phần tử cuối cùng của mảng và trả về phần tử đó.

```javascript
let fruits = ["apple", "banana", "orange"];
let removed = fruits.pop();
console.log(fruits); // ["apple", "banana"]
console.log(removed); // "orange"
```

#### **3. shift()** - Loại bỏ phần tử đầu tiên của mảng

Phương thức `shift()` loại bỏ phần tử đầu tiên của mảng và trả về phần tử đó.

```javascript
let fruits = ["apple", "banana", "orange"];
let removed = fruits.shift();
console.log(fruits); // ["banana", "orange"]
console.log(removed); // "apple"
```

#### **4. unshift()** - Thêm phần tử vào đầu mảng

Phương thức `unshift()` thêm một hoặc nhiều phần tử vào đầu mảng và trả về độ dài mới của mảng.

```javascript
let fruits = ["banana", "orange"];
fruits.unshift("apple");
console.log(fruits); // ["apple", "banana", "orange"]
```

#### **5. concat()** - Kết hợp các mảng

Phương thức `concat()` dùng để kết hợp hai hoặc nhiều mảng lại với nhau và trả về một mảng mới.

```javascript
let fruits = ["apple", "banana"];
let moreFruits = ["orange", "grape"];
let allFruits = fruits.concat(moreFruits);
console.log(allFruits); // ["apple", "banana", "orange", "grape"]
```

#### **6. join()** - Kết hợp các phần tử trong mảng thành một chuỗi

Phương thức `join()` nối tất cả các phần tử trong mảng thành một chuỗi, phân tách bằng dấu phân cách tùy chọn.

```javascript
let fruits = ["apple", "banana", "orange"];
let result = fruits.join(", ");
console.log(result); // "apple, banana, orange"
```

#### **7. slice()** - Lấy một phần mảng

Phương thức `slice()` trả về một bản sao của mảng con trong mảng ban đầu từ chỉ số start đến chỉ số end (không bao gồm phần tử tại chỉ số end).

```javascript
let fruits = ["apple", "banana", "orange", "grape"];
let slicedFruits = fruits.slice(1, 3);
console.log(slicedFruits); // ["banana", "orange"]
```

#### **8. splice()** - Thêm hoặc xóa phần tử trong mảng

Phương thức `splice()` cho phép bạn thêm hoặc xóa phần tử tại vị trí cụ thể trong mảng.

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.splice(1, 1, "grape", "pear");
console.log(fruits); // ["apple", "grape", "pear", "orange"]
```
Tham số thứ nhất là chỉ số bắt đầu, tham số thứ hai là số phần tử cần xóa, và các tham số còn lại là các phần tử mới sẽ được thêm vào.

#### **9. forEach()** - Duyệt qua tất cả các phần tử trong mảng

Phương thức `forEach()` thực hiện một hàm callback cho mỗi phần tử trong mảng.

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.forEach(function(fruit) {
  console.log(fruit);
});
```

#### **10. map()** - Tạo mảng mới với các phần tử được chuyển đổi

Phương thức `map()` tạo một mảng mới với các phần tử đã được chuyển đổi từ mảng ban đầu theo một hàm callback.

```javascript
let numbers = [1, 2, 3];
let squares = numbers.map(function(number) {
  return number * number;
});
console.log(squares); // [1, 4, 9]
```

#### **11. filter()** - Lọc mảng dựa trên điều kiện

Phương thức `filter()` tạo một mảng mới chỉ chứa các phần tử thỏa mãn điều kiện được cung cấp trong hàm callback.

```javascript
let numbers = [1, 2, 3, 4, 5];
let evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});
console.log(evenNumbers); // [2, 4]
```

#### **12. reduce()** - Lấy giá trị duy nhất từ mảng

Phương thức `reduce()` áp dụng một hàm callback cho mỗi phần tử trong mảng (từ trái sang phải) để tạo ra một giá trị duy nhất.

```javascript
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce(function(accumulator, currentValue) {
  return accumulator + currentValue;
}, 0);
console.log(sum); // 10
```

#### **13. find()** - Tìm phần tử đầu tiên thỏa mãn điều kiện

Phương thức `find()` trả về phần tử đầu tiên trong mảng thỏa mãn điều kiện được xác định trong hàm callback.

```javascript
let numbers = [1, 2, 3, 4, 5];
let found = numbers.find(function(number) {
  return number > 3;
});
console.log(found); // 4
```
```