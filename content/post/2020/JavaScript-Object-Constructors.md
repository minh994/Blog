---
title: JavaScript Object Constructors  
date: 2023-12-30  
tags: ["javascript", "objects", "constructors", "programming", "blog"]  
image: "/img/posts/img-27.png"  
Description: "Khám phá cách tạo đối tượng trong JavaScript bằng cách sử dụng constructors. Bài viết này hướng dẫn cách sử dụng các constructors để khởi tạo đối tượng và cách tùy chỉnh chúng."  
---

### 1. Giới Thiệu về JavaScript Object Constructors

Trong JavaScript, một **Object Constructor** là một hàm đặc biệt dùng để tạo đối tượng. Constructors cho phép bạn tạo ra các đối tượng với các thuộc tính và phương thức chung. Bạn có thể tạo ra nhiều đối tượng cùng loại mà không cần phải viết lại mã cho mỗi đối tượng.

---

### 2. Cách Tạo Một Object Constructor

#### **1. Sử Dụng Hàm Constructor**

Bạn có thể tạo một constructor bằng cách sử dụng hàm (function). Khi bạn sử dụng hàm với từ khóa `new`, một đối tượng mới sẽ được tạo và gán các thuộc tính và phương thức từ constructor.

- **Ví dụ**:
```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.greet = function() {
    console.log("Hello, my name is " + this.name);
  };
}

const person1 = new Person("John", 30);
const person2 = new Person("Alice", 25);

person1.greet(); // Output: Hello, my name is John
person2.greet(); // Output: Hello, my name is Alice
```
Trong ví dụ trên, hàm `Person` là một constructor. Mỗi khi bạn tạo một đối tượng mới với `new Person()`, đối tượng đó sẽ có các thuộc tính `name`, `age`, và phương thức `greet`.

#### **2. Sử Dụng Constructor với Class (ES6)**

Từ phiên bản ES6, JavaScript hỗ trợ cú pháp `class` để định nghĩa constructors, giúp việc tạo đối tượng trở nên dễ dàng và dễ hiểu hơn.

- **Ví dụ**:
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  
  greet() {
    console.log("Hello, my name is " + this.name);
  }
}

const person1 = new Person("John", 30);
const person2 = new Person("Alice", 25);

person1.greet(); // Output: Hello, my name is John
person2.greet(); // Output: Hello, my name is Alice
```
Ở đây, `Person` là một lớp với phương thức constructor để khởi tạo các thuộc tính cho đối tượng. Các đối tượng được tạo ra từ lớp `Person` sẽ có các thuộc tính và phương thức giống nhau.

---

### 3. Khi Nào Sử Dụng Object Constructors

Bạn nên sử dụng constructors khi bạn cần tạo ra nhiều đối tượng có chung thuộc tính và phương thức. Một số tình huống điển hình bao gồm:

- Khi bạn cần tạo các đối tượng có cùng cấu trúc nhưng giá trị khác nhau: Ví dụ, tạo đối tượng sinh viên, nhân viên, sản phẩm trong một cửa hàng.
- Khi bạn muốn quản lý mã nguồn một cách có tổ chức và tái sử dụng được: Constructors cho phép bạn giảm thiểu mã nguồn trùng lặp và dễ dàng quản lý các đối tượng của mình.

---

### 4. Phương Thức Trong Object Constructors

Các phương thức có thể được định nghĩa trong constructor để cung cấp hành vi cho đối tượng. Các phương thức này có thể được gọi từ các đối tượng được tạo ra từ constructor.

- **Ví dụ với phương thức**:
```javascript
function Car(make, model) {
  this.make = make;
  this.model = model;
  this.displayInfo = function() {
    console.log("Car make: " + this.make + ", Model: " + this.model);
  };
}

const car1 = new Car("Toyota", "Corolla");
const car2 = new Car("Honda", "Civic");

car1.displayInfo(); // Output: Car make: Toyota, Model: Corolla
car2.displayInfo(); // Output: Car make: Honda, Model: Civic
```
Ở đây, phương thức `displayInfo` được sử dụng để hiển thị thông tin về chiếc xe.