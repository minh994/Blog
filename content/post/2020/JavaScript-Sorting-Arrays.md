---
title: JavaScript Sorting Arrays  
date: 2023-12-31  
tags: ["javascript", "arrays", "sorting", "blog"]  
image: "/img/posts/img-31.png"
Description: "Hướng dẫn cách sử dụng các phương thức sắp xếp mảng trong JavaScript, bao gồm các kỹ thuật sắp xếp số, chuỗi và các đối tượng phức tạp."  
---

### 1. Giới Thiệu về Sắp Xếp Mảng trong JavaScript

Sắp xếp mảng là một thao tác phổ biến trong lập trình. JavaScript cung cấp một số phương thức để sắp xếp mảng như `sort()`, và bạn có thể tùy chỉnh các phương thức này để sắp xếp các mảng theo nhu cầu của mình, từ số học đến chuỗi hay các đối tượng phức tạp.

### 2. Phương Thức `sort()`

Phương thức `sort()` được sử dụng để sắp xếp các phần tử trong mảng. Mặc định, `sort()` sắp xếp mảng theo thứ tự bảng chữ cái, đối với các phần tử chuỗi hoặc sắp xếp theo giá trị Unicode.

#### **Cách sử dụng cơ bản:**

```javascript
let fruits = ["banana", "apple", "orange", "grape"];

fruits.sort();
console.log(fruits); // ["apple", "banana", "grape", "orange"]
```

### 3. Sắp Xếp Số

Khi bạn sắp xếp các mảng chứa các giá trị số, cần phải sử dụng một hàm so sánh, vì phương thức `sort()` mặc định không sắp xếp theo thứ tự số học mà lại sắp xếp theo thứ tự chuỗi (Unicode).

#### **Cách sử dụng với hàm so sánh:**

```javascript
let numbers = [5, 12, 8, 130, 44];

numbers.sort(function(a, b) {
  return a - b; // Sắp xếp theo thứ tự tăng dần
});
console.log(numbers); // [5, 8, 12, 44, 130]
```

#### **Sắp xếp theo thứ tự giảm dần:**

```javascript
numbers.sort(function(a, b) {
  return b - a; // Sắp xếp theo thứ tự giảm dần
});
console.log(numbers); // [130, 44, 12, 8, 5]
```

### 4. Sắp Xếp Chuỗi

Khi làm việc với các chuỗi trong mảng, phương thức `sort()` sẽ sắp xếp theo thứ tự bảng chữ cái mặc định, tuy nhiên, có thể bạn sẽ muốn kiểm soát cách thức so sánh.

#### **Sắp xếp chuỗi theo thứ tự bảng chữ cái:**

```javascript
let words = ["banana", "apple", "grape", "orange"];

words.sort();
console.log(words); // ["apple", "banana", "grape", "orange"]
```

#### **Sắp xếp chuỗi theo thứ tự ngược lại:**

```javascript
words.sort(function(a, b) {
  return b.localeCompare(a); // Sắp xếp ngược lại theo bảng chữ cái
});
console.log(words); // ["orange", "grape", "banana", "apple"]
```

### 5. Sắp Xếp Mảng Các Đối Tượng

Khi làm việc với các đối tượng trong mảng, bạn có thể sử dụng phương thức `sort()` để sắp xếp các đối tượng theo các thuộc tính của chúng.

#### **Ví dụ: Sắp xếp đối tượng theo thuộc tính:**

```javascript
let people = [
  { name: "John", age: 30 },
  { name: "Alice", age: 25 },
  { name: "Bob", age: 35 }
];

people.sort(function(a, b) {
  return a.age - b.age; // Sắp xếp theo độ tuổi (thứ tự tăng dần)
});

console.log(people);
// [
//   { name: "Alice", age: 25 },
//   { name: "John", age: 30 },
//   { name: "Bob", age: 35 }
// ]
```

#### **Sắp xếp theo tên (theo thứ tự bảng chữ cái):**

```javascript
people.sort(function(a, b) {
  return a.name.localeCompare(b.name); // Sắp xếp theo tên
});

console.log(people);
// [
//   { name: "Alice", age: 25 },
//   { name: "Bob", age: 35 },
//   { name: "John", age: 30 }
// ]
```

### 6. Sắp Xếp Ngẫu Nhiên

Nếu bạn muốn sắp xếp một mảng theo thứ tự ngẫu nhiên, bạn có thể sử dụng phương thức `sort()` kết hợp với một hàm so sánh trả về giá trị ngẫu nhiên.

#### **Ví dụ:**

```javascript
let items = [1, 2, 3, 4, 5];

items.sort(function() {
  return Math.random() - 0.5; // Trả về giá trị ngẫu nhiên để sắp xếp ngẫu nhiên
});

console.log(items); // [3, 5, 2, 4, 1] (kết quả có thể thay đổi mỗi lần chạy)
```