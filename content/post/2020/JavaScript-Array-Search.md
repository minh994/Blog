---
title: JavaScript Array Search  
date: 2023-12-31  
tags: ["javascript", "arrays", "search", "blog"]  
image: "/img/posts/img-20.png"  
Description: "Hướng dẫn cách sử dụng các phương thức tìm kiếm mảng trong JavaScript để tìm kiếm phần tử trong mảng."  
---

### 1. Giới Thiệu về Tìm Kiếm Mảng trong JavaScript

Tìm kiếm mảng là một thao tác quan trọng khi làm việc với dữ liệu trong JavaScript. Để tìm kiếm phần tử trong mảng, JavaScript cung cấp một số phương thức hữu ích như `indexOf()`, `includes()`, `find()`, và `findIndex()`. Mỗi phương thức này có các tính năng và cách sử dụng khác nhau.

### 2. Phương Thức `indexOf()`

Phương thức `indexOf()` dùng để tìm kiếm một phần tử trong mảng và trả về chỉ số (index) của phần tử đầu tiên được tìm thấy. Nếu phần tử không tồn tại trong mảng, phương thức sẽ trả về `-1`.

#### **Cách sử dụng:**

```javascript
let fruits = ["apple", "banana", "orange", "grape"];

let index = fruits.indexOf("banana");
console.log(index); // 1

let notFound = fruits.indexOf("pear");
console.log(notFound); // -1
```
**Lưu ý:**
- `indexOf()` so sánh các phần tử bằng cách sử dụng phép so sánh chặt chẽ (strict equality).

### 3. Phương Thức `includes()`

Phương thức `includes()` kiểm tra xem một phần tử có tồn tại trong mảng hay không và trả về `true` hoặc `false`. Phương thức này không trả về chỉ số mà chỉ cho biết phần tử có nằm trong mảng hay không.

#### **Cách sử dụng:**

```javascript
let fruits = ["apple", "banana", "orange", "grape"];

let hasBanana = fruits.includes("banana");
console.log(hasBanana); // true

let hasPear = fruits.includes("pear");
console.log(hasPear); // false
```
**Lưu ý:**
- `includes()` cũng sử dụng phép so sánh chặt chẽ (strict equality).

### 4. Phương Thức `find()`

Phương thức `find()` dùng để tìm phần tử đầu tiên trong mảng thỏa mãn điều kiện mà bạn chỉ định. Phương thức này sẽ trả về phần tử đó nếu tìm thấy, hoặc `undefined` nếu không có phần tử nào thỏa mãn.

#### **Cách sử dụng:**

```javascript
let numbers = [5, 12, 8, 130, 44];

let firstEven = numbers.find(function(number) {
  return number % 2 === 0;
});
console.log(firstEven); // 12

let notFound = numbers.find(function(number) {
  return number > 200;
});
console.log(notFound); // undefined
```
**Lưu ý:**
- Phương thức `find()` dừng lại ngay khi tìm thấy phần tử thỏa mãn điều kiện.

### 5. Phương Thức `findIndex()`

Phương thức `findIndex()` tương tự như `find()`, nhưng thay vì trả về phần tử, nó trả về chỉ số (index) của phần tử đầu tiên thỏa mãn điều kiện. Nếu không tìm thấy, nó sẽ trả về `-1`.

#### **Cách sử dụng:**

```javascript
let numbers = [5, 12, 8, 130, 44];

let indexEven = numbers.findIndex(function(number) {
  return number % 2 === 0;
});
console.log(indexEven); // 1

let notFound = numbers.findIndex(function(number) {
  return number > 200;
});
console.log(notFound); // -1
```
**Lưu ý:**
- `findIndex()` cũng chỉ tìm kiếm phần tử đầu tiên thỏa mãn điều kiện.

### 6. Phương Thức `filter()`

Phương thức `filter()` không chỉ dừng lại khi tìm thấy phần tử đầu tiên mà nó sẽ trả về tất cả các phần tử trong mảng thỏa mãn điều kiện mà bạn chỉ định. Phương thức này trả về một mảng mới chứa các phần tử phù hợp.

#### **Cách sử dụng:**

```javascript
let numbers = [5, 12, 8, 130, 44];

let evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});
console.log(evenNumbers); // [12, 8, 130, 44]
```
**Lưu ý:**
- `filter()` trả về một mảng mới, có thể rỗng nếu không có phần tử nào thỏa mãn.