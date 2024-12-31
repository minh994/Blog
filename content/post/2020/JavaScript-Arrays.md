---
title: JavaScript Arrays  
date: 2023-12-31  
tags: ["javascript", "arrays", "blog"]  
image: "/img/posts/img-21.png"  
Description: "Tìm hiểu về mảng trong JavaScript, cách khai báo, thao tác và các phương thức phổ biến khi làm việc với mảng."  
---

### 1. Giới Thiệu về Mảng trong JavaScript

Mảng trong JavaScript là một kiểu dữ liệu đặc biệt dùng để lưu trữ một tập hợp các giá trị. Mảng có thể chứa các giá trị cùng kiểu hoặc khác kiểu, và có thể có kích thước thay đổi linh hoạt trong quá trình thực thi chương trình.

JavaScript hỗ trợ một số phương thức hữu ích để làm việc với mảng, từ việc thêm, xóa phần tử đến việc duyệt qua các phần tử của mảng.

### 2. Cách Khai Báo Mảng trong JavaScript

#### **Khai báo mảng rỗng**

```javascript
let fruits = [];
```

#### **Khai báo mảng với các phần tử**

```javascript
let fruits = ["apple", "banana", "orange"];
```

#### **Khai báo mảng với các kiểu dữ liệu khác nhau**

```javascript
let mixedArray = [1, "apple", true, null];
```

#### **Khai báo mảng với nhiều mảng con**

```javascript
let nestedArray = [[1, 2], [3, 4], [5, 6]];
```

### 3. Truy Cập Các Phần Tử Trong Mảng

Mảng trong JavaScript có chỉ số (index) bắt đầu từ 0, vì vậy phần tử đầu tiên có chỉ số 0, phần tử thứ hai có chỉ số 1, v.v.

#### **Truy cập phần tử của mảng**

```javascript
let fruits = ["apple", "banana", "orange"];
console.log(fruits[0]); // "apple"
console.log(fruits[1]); // "banana"
```

#### **Truy cập phần tử cuối cùng của mảng**

```javascript
let fruits = ["apple", "banana", "orange"];
console.log(fruits[fruits.length - 1]); // "orange"
```

### 4. Các Phương Thức Thường Dùng với Mảng

JavaScript cung cấp nhiều phương thức để thao tác với mảng. Dưới đây là một số phương thức phổ biến:

- **push()** - Thêm phần tử vào cuối mảng

```javascript
let fruits = ["apple", "banana"];
fruits.push("orange");
console.log(fruits); // ["apple", "banana", "orange"]
```

- **pop()** - Loại bỏ phần tử cuối cùng của mảng

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.pop();
console.log(fruits); // ["apple", "banana"]
```

- **shift()** - Loại bỏ phần tử đầu tiên của mảng

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.shift();
console.log(fruits); // ["banana", "orange"]
```

- **unshift()** - Thêm phần tử vào đầu mảng

```javascript
let fruits = ["banana", "orange"];
fruits.unshift("apple");
console.log(fruits); // ["apple", "banana", "orange"]
```

- **concat()** - Kết hợp nhiều mảng

```javascript
let fruits = ["apple", "banana"];
let moreFruits = ["orange", "grape"];
let allFruits = fruits.concat(moreFruits);
console.log(allFruits); // ["apple", "banana", "orange", "grape"]
```

- **join()** - Kết hợp các phần tử trong mảng thành chuỗi

```javascript
let fruits = ["apple", "banana", "orange"];
let result = fruits.join(", ");
console.log(result); // "apple, banana, orange"
```

- **slice()** - Lấy một phần mảng

```javascript
let fruits = ["apple", "banana", "orange", "grape"];
let slicedFruits = fruits.slice(1, 3);
console.log(slicedFruits); // ["banana", "orange"]
```

- **splice()** - Thêm hoặc xóa phần tử trong mảng

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.splice(1, 1, "grape", "pear");
console.log(fruits); // ["apple", "grape", "pear", "orange"]
```

### 5. Duyệt qua Mảng

- **forEach()** - Duyệt qua tất cả các phần tử trong mảng

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.forEach(function(fruit) {
  console.log(fruit);
});
```

- **map()** - Tạo một mảng mới với các phần tử được chuyển đổi

```javascript
let numbers = [1, 2, 3];
let squares = numbers.map(function(number) {
  return number * number;
});
console.log(squares); // [1, 4, 9]
```

- **filter()** - Lọc mảng theo điều kiện

```javascript
let numbers = [1, 2, 3, 4, 5];
let evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});
console.log(evenNumbers); // [2, 4]
```

- **reduce()** - Tính toán giá trị duy nhất từ các phần tử của mảng

```javascript
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce(function(accumulator, currentValue) {
  return accumulator + currentValue;
}, 0);
console.log(sum); // 10
```

### 6. Mảng và Độ Dài

- **length** - Độ dài của mảng

```javascript
let fruits = ["apple", "banana", "orange"];
console.log(fruits.length); // 3
```

- **sort()** - Sắp xếp mảng

```javascript
let fruits = ["banana", "apple", "orange"];
fruits.sort();
console.log(fruits); // ["apple", "banana", "orange"]
```