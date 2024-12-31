---
title: JavaScript Object Methods  
date: 2023-12-30  
tags: ["javascript", "object", "methods", "programming", "blog"]  
image: "/img/posts/img-28.png"  
Description: "Khám phá các phương thức của đối tượng trong JavaScript, từ các phương thức cơ bản đến các phương thức mạnh mẽ giúp thao tác và quản lý dữ liệu trong đối tượng."  
---

### 1. JavaScript Object Methods: Khái Niệm

Trong JavaScript, **Object methods** là các phương thức được định nghĩa trong một đối tượng. Những phương thức này cho phép bạn thực hiện các hành động hoặc thao tác liên quan đến dữ liệu trong đối tượng. Một đối tượng trong JavaScript có thể chứa các thuộc tính (properties) và các phương thức (methods).

---

### 2. Định Nghĩa và Cách Sử Dụng Object Methods

#### **1. Định nghĩa một Object Method**

Phương thức của đối tượng là một hàm được định nghĩa bên trong đối tượng đó. Dưới đây là một ví dụ về cách định nghĩa phương thức trong đối tượng:

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log("Hello, " + this.name);
  }
};

person.greet();  // In ra "Hello, John"
```
Trong ví dụ này, `greet` là một phương thức trong đối tượng `person`. Khi gọi `person.greet()`, phương thức này sẽ hiển thị thông điệp chào mừng.

---

### 3. Các Phương Thức Của Đối Tượng JavaScript Thường Gặp

#### **1. Object.keys()**

Phương thức `Object.keys()` trả về một mảng chứa tất cả các thuộc tính (keys) của đối tượng.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

let keys = Object.keys(person);
console.log(keys);  // In ra ["name", "age"]
```

#### **2. Object.values()**

Phương thức `Object.values()` trả về một mảng chứa tất cả các giá trị (values) của đối tượng.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

let values = Object.values(person);
console.log(values);  // In ra ["John", 30]
```

#### **3. Object.entries()**

Phương thức `Object.entries()` trả về một mảng chứa tất cả các cặp [key, value] của đối tượng dưới dạng các mảng con.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

let entries = Object.entries(person);
console.log(entries);  // In ra [["name", "John"], ["age", 30]]
```

#### **4. Object.hasOwnProperty()**

Phương thức `hasOwnProperty()` kiểm tra xem đối tượng có thuộc tính (key) cụ thể hay không. Phương thức này chỉ kiểm tra các thuộc tính trực tiếp của đối tượng, không kiểm tra qua chuỗi kế thừa.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

console.log(person.hasOwnProperty("name"));  // In ra true
console.log(person.hasOwnProperty("gender"));  // In ra false
```

#### **5. Object.assign()**

Phương thức `Object.assign()` sao chép tất cả các thuộc tính từ các đối tượng nguồn vào đối tượng đích. Phương thức này thực hiện sao chép theo kiểu "shallow" (nông), tức là chỉ sao chép các giá trị của các thuộc tính ở cấp độ 1.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

let address = {
  city: "New York",
  country: "USA"
};

let mergedObject = Object.assign({}, person, address);
console.log(mergedObject);  
// In ra { name: "John", age: 30, city: "New York", country: "USA" }
```

#### **6. Object.freeze()**

Phương thức `Object.freeze()` đóng băng một đối tượng, ngăn không cho thay đổi thuộc tính của nó. Sau khi đóng băng, bạn không thể thay đổi, thêm mới hoặc xóa thuộc tính của đối tượng.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

Object.freeze(person);
person.age = 35;  // Thay đổi sẽ không có hiệu lực
console.log(person.age);  // In ra 30
```

#### **7. Object.seal()**

Phương thức `Object.seal()` niêm phong một đối tượng, cho phép bạn thay đổi các giá trị của thuộc tính đã tồn tại nhưng không thể thêm mới hoặc xóa thuộc tính.

- **Ví dụ**:
```javascript
let person = {
  name: "John",
  age: 30
};

Object.seal(person);
person.age = 35;  // Thay đổi giá trị có thể
delete person.name;  // Không thể xóa thuộc tính
console.log(person);  // In ra { name: "John", age: 35 }
```

---

### 4. Khi Nào Sử Dụng Object Methods

- **Object.keys()**: Khi bạn cần lấy tất cả các khóa của đối tượng dưới dạng mảng.
- **Object.values()**: Khi bạn cần lấy tất cả các giá trị của đối tượng dưới dạng mảng.
- **Object.entries()**: Khi bạn cần lấy cả khóa và giá trị của đối tượng dưới dạng mảng con.
- **Object.hasOwnProperty()**: Khi bạn muốn kiểm tra sự tồn tại của thuộc tính trong đối tượng mà không cần phải kiểm tra qua chuỗi kế thừa.
- **Object.assign()**: Khi bạn cần sao chép các thuộc tính từ đối tượng này sang đối tượng khác.
- **Object.freeze()**: Khi bạn muốn đóng băng đối tượng và ngăn không cho thay đổi.
- **Object.seal()**: Khi bạn muốn ngăn cản việc xóa thuộc tính mà vẫn cho phép thay đổi giá trị của thuộc tính hiện tại.