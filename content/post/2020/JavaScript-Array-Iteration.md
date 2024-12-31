---
title: JavaScript Array Iteration  
date: 2023-12-31  
tags: ["javascript", "arrays", "iteration", "blog"]  
image: "/img/posts/img-18.png"  
Description: "Hướng dẫn cách sử dụng các phương thức lặp qua mảng trong JavaScript, từ các phương thức đơn giản đến các phương thức mạnh mẽ như `forEach()`, `map()`, `filter()`, và `reduce()`."  
---

### 1. Giới Thiệu về Lặp qua Mảng trong JavaScript

Lặp qua mảng là một trong những thao tác phổ biến khi làm việc với JavaScript. Các phương thức lặp qua mảng giúp bạn dễ dàng thao tác với từng phần tử trong mảng, từ việc hiển thị thông tin, xử lý dữ liệu, đến việc tạo ra các mảng mới.

JavaScript cung cấp nhiều cách để lặp qua mảng, bao gồm cả các phương thức cơ bản và các phương thức nâng cao cho phép bạn thực hiện các phép toán phức tạp.

### 2. Phương Thức `forEach()`

Phương thức `forEach()` cho phép bạn thực hiện một hành động trên mỗi phần tử trong mảng.

#### **Cách sử dụng:**

```javascript
let numbers = [1, 2, 3, 4, 5];

numbers.forEach(function(number) {
  console.log(number);  // In ra từng phần tử trong mảng
});
```

#### **Sử dụng với Arrow Function:**

```javascript
numbers.forEach(number => console.log(number));
```

- `forEach()` không trả về giá trị, chỉ thực hiện một hành động với từng phần tử.
- Không thể dừng hoặc tiếp tục vòng lặp bằng `break` hay `continue` như trong vòng lặp `for`.

### 3. Phương Thức `map()`

Phương thức `map()` cho phép bạn tạo một mảng mới với kết quả của mỗi phần tử trong mảng cũ được xử lý bởi một hàm callback.

#### **Cách sử dụng:**

```javascript
let numbers = [1, 2, 3, 4, 5];

let doubled = numbers.map(function(number) {
  return number * 2;
});

console.log(doubled);  // [2, 4, 6, 8, 10]
```

- `map()` trả về một mảng mới, mảng gốc không thay đổi.

#### **Sử dụng với Arrow Function:**

```javascript
let doubled = numbers.map(number => number * 2);
console.log(doubled);  // [2, 4, 6, 8, 10]
```

### 4. Phương Thức `filter()`

Phương thức `filter()` tạo ra một mảng mới chứa các phần tử đáp ứng điều kiện nhất định từ mảng gốc.

#### **Cách sử dụng:**

```javascript
let numbers = [1, 2, 3, 4, 5];

let evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});

console.log(evenNumbers);  // [2, 4]
```

- `filter()` trả về một mảng mới chứa tất cả các phần tử thỏa mãn điều kiện, hoặc một mảng rỗng nếu không có phần tử nào thỏa mãn.

#### **Sử dụng với Arrow Function:**

```javascript
let evenNumbers = numbers.filter(number => number % 2 === 0);
console.log(evenNumbers);  // [2, 4]
```

### 5. Phương Thức `reduce()`

Phương thức `reduce()` cho phép bạn tính toán và trả về một giá trị duy nhất từ tất cả các phần tử trong mảng, thông qua một hàm xử lý.

#### **Cách sử dụng:**

```javascript
let numbers = [1, 2, 3, 4, 5];

let sum = numbers.reduce(function(total, number) {
  return total + number;
}, 0);

console.log(sum);  // 15
```

- `reduce()` nhận hai tham số: hàm callback (với tham số là accumulator và currentValue) và một giá trị khởi tạo cho accumulator.
- Giá trị trả về là một giá trị duy nhất (ví dụ, tổng, trung bình, v.v.).

#### **Sử dụng với Arrow Function:**

```javascript
let sum = numbers.reduce((total, number) => total + number, 0);
console.log(sum);  // 15
```

### 6. Phương Thức `find()`

Phương thức `find()` trả về phần tử đầu tiên trong mảng thỏa mãn điều kiện tìm kiếm.

#### **Cách sử dụng:**

```javascript
let numbers = [1, 2, 3, 4, 5];

let firstEven = numbers.find(function(number) {
  return number % 2 === 0;
});

console.log(firstEven);  // 2
```

- `find()` chỉ trả về phần tử đầu tiên thỏa mãn điều kiện, hoặc `undefined` nếu không tìm thấy phần tử nào.

### 7. Phương Thức `every()` và `some()`

- **`every()`**: Kiểm tra nếu tất cả các phần tử trong mảng thỏa mãn một điều kiện.

```javascript
let numbers = [1, 2, 3, 4, 5];
let allPositive = numbers.every(number => number > 0);
console.log(allPositive);  // true
```

- **`some()`**: Kiểm tra nếu ít nhất một phần tử trong mảng thỏa mãn điều kiện.

```javascript
let numbers = [1, 2, 3, 4, 5];
let hasNegative = numbers.some(number => number < 0);
console.log(hasNegative);  // false
```

### 8. Phương Thức `for...of`

Phương thức `for...of` là một cú pháp mới trong JavaScript cho phép lặp qua các phần tử của mảng mà không cần sử dụng chỉ số.

#### **Cách sử dụng:**

```javascript
let numbers = [1, 2, 3, 4, 5];

for (let number of numbers) {
  console.log(number);
}
```

- `for...of` dễ đọc và sử dụng khi chỉ cần truy cập phần tử, không cần chỉ số của phần tử.