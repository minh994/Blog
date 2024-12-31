---
title: JavaScript Operators  
date: 2023-12-30  
tags: ["javascript", "operators", "programming", "blog"]  
image: "/img/posts/img-29.png"  
Description: "Tìm hiểu các toán tử trong JavaScript, cách sử dụng chúng và phân loại các toán tử cơ bản trong ngôn ngữ này."  
---

### 1. JavaScript Operators: Khái Niệm Cơ Bản

Trong JavaScript, **toán tử (operators)** là các ký hiệu hoặc từ khóa dùng để thực hiện các phép toán hoặc các thao tác trên dữ liệu. JavaScript cung cấp nhiều loại toán tử khác nhau, bao gồm các toán tử số học, so sánh, gán, logic, và nhiều loại khác.

---

### 2. Các Loại Toán Tử Trong JavaScript

#### **Toán tử số học (Arithmetic Operators)**

Các toán tử này được sử dụng để thực hiện các phép toán số học trên các giá trị số.

| Toán Tử | Mô Tả            | Ví Dụ    |
|---------|-------------------|----------|
| `+`     | Cộng              | `5 + 3`  // 8  |
| `-`     | Trừ               | `5 - 3`  // 2  |
| `*`     | Nhân              | `5 * 3`  // 15 |
| `/`     | Chia              | `5 / 3`  // 1.6667|
| `%`     | Lấy phần dư       | `5 % 3`  // 2  |
| `++`    | Tăng giá trị lên 1 | `x++`    // x = x + 1 |
| `--`    | Giảm giá trị đi 1  | `x--`    // x = x - 1 |

Ví dụ:
```javascript
let a = 5;
let b = 3;
console.log(a + b);  // In ra 8
console.log(a - b);  // In ra 2
```

#### **Toán tử so sánh (Comparison Operators)**

Các toán tử này được sử dụng để so sánh hai giá trị và trả về true hoặc false.

| Toán Tử | Mô Tả                          | Ví Dụ                  |
|---------|---------------------------------|------------------------|
| `==`    | Bằng (loại không quan trọng)   | `5 == '5'` // true     |
| `===`   | Bằng (loại quan trọng)         | `5 === '5'` // false   |
| `!=`    | Khác (loại không quan trọng)   | `5 != 3` // true       |
| `!==`   | Khác (loại quan trọng)         | `5 !== '5'` // true    |
| `>`     | Lớn hơn                        | `5 > 3` // true        |
| `<`     | Nhỏ hơn                        | `5 < 3` // false       |
| `>=`    | Lớn hơn hoặc bằng             | `5 >= 5` // true       |
| `<=`    | Nhỏ hơn hoặc bằng             | `5 <= 3` // false      |

Ví dụ:
```javascript
let x = 5;
let y = 10;
console.log(x == y);  // In ra false
console.log(x < y);   // In ra true
```

#### **Toán tử gán (Assignment Operators)**

Toán tử gán được sử dụng để gán giá trị cho biến.

| Toán Tử | Mô Tả            | Ví Dụ                  |
|---------|-------------------|------------------------|
| `=`     | Gán giá trị       | `x = 5`                |
| `+=`    | Gán và cộng      | `x += 5` // x = x + 5  |
| `-=`    | Gán và trừ       | `x -= 3` // x = x - 3  |
| `*=`    | Gán và nhân      | `x *= 2` // x = x * 2  |
| `/=`    | Gán và chia       | `x /= 2` // x = x / 2  |
| `%=`    | Gán và lấy phần dư| `x %= 2` // x = x % 2  |

Ví dụ:
```javascript
let a = 10;
a += 5;  // a = 10 + 5
console.log(a);  // In ra 15
```

#### **Toán tử logic (Logical Operators)**

Các toán tử logic được sử dụng để kết hợp các biểu thức boolean.

| Toán Tử | Mô Tả            | Ví Dụ                  |
|---------|-------------------|------------------------|
| `&&`    | Và (AND)          | `true && false` // false|
| `||`    | Hoặc (OR)        | `true || false` // true |
| `!`     | Không (NOT)      | `!true` // false       |

Ví dụ:
```javascript
let a = true;
let b = false;
console.log(a && b);  // In ra false
console.log(a || b);  // In ra true
```

#### **Toán tử điều kiện (Ternary Operator)**

Toán tử điều kiện là một cách ngắn gọn để viết câu lệnh if-else.

Cú pháp:
```javascript
condition ? expr1 : expr2;
```

Ví dụ:
```javascript
let age = 20;
let result = (age >= 18) ? "Adult" : "Minor";
console.log(result);  // In ra "Adult"
```

#### **Toán tử typeof và instanceof**

- `typeof` được sử dụng để kiểm tra kiểu dữ liệu của một biến.
- `instanceof` được sử dụng để kiểm tra đối tượng có phải là thể hiện của một lớp hay không.

Ví dụ:
```javascript
let a = "Hello";
console.log(typeof a);  // In ra "string"

let obj = {};
console.log(obj instanceof Object);  // In ra true
```

### 3. Khi Nào Sử Dụng Các Toán Tử

- Sử dụng toán tử số học khi bạn cần thực hiện các phép toán với giá trị số.
- Sử dụng toán tử so sánh khi bạn muốn so sánh hai giá trị.
- Sử dụng toán tử gán để gán giá trị cho biến hoặc thực hiện các phép toán và gán kết quả cho biến.
- Sử dụng toán tử logic khi bạn cần kết hợp hoặc đảo ngược các điều kiện.
- Sử dụng toán tử điều kiện để thay thế câu lệnh if-else đơn giản.