---
title: JavaScript Variables Khai Báo và Sử Dụng  
date: 2024-12-30  
tags: ["javascript", "variables", "programming", "blog"]  
image: "/img/posts/img-35.png"  
Description: "Khám phá cách khai báo và sử dụng biến trong JavaScript. Bài viết này sẽ giúp bạn hiểu về các cách khai báo biến, phạm vi và các quy tắc liên quan đến biến trong JavaScript."  
---

### 1. JavaScript Variables: Khái Niệm Cơ Bản

Biến trong JavaScript là một không gian lưu trữ dữ liệu có thể thay đổi trong suốt quá trình thực thi chương trình. JavaScript cho phép khai báo biến bằng ba từ khóa chính: `var`, `let`, và `const`.

---

### 2. Cách Khai Báo Biến trong JavaScript

#### 2.1. `var`: Biến Toàn Cục và Phạm Vi Hàm

Trước đây, `var` được sử dụng rộng rãi để khai báo biến trong JavaScript. Biến khai báo bằng `var` có phạm vi toàn cục hoặc phạm vi hàm, điều này có thể gây ra một số vấn đề về quản lý phạm vi biến.

Cách sử dụng:
```javascript
var x = 10;  // Biến x được khai báo với phạm vi toàn cục hoặc hàm
```

**Khi nào sử dụng `var`:**
`var` hiện nay ít được sử dụng trong mã JavaScript hiện đại vì phạm vi của nó không rõ ràng. Tuy nhiên, bạn vẫn có thể sử dụng `var` nếu bạn cần hỗ trợ các trình duyệt cũ hoặc nếu bạn làm việc với mã cũ đã sử dụng `var`.

#### 2.2. `let`: Biến Phạm Vi Khối

`let` được giới thiệu trong ES6 và được sử dụng để khai báo biến với phạm vi khối (block-scoped). Điều này giúp kiểm soát phạm vi biến tốt hơn và tránh được các lỗi trong mã nguồn.

Cách sử dụng:
```javascript
let y = 20;  // Biến y có phạm vi trong khối mã (block-scoped)
```

**Khi nào sử dụng `let`:**
Sử dụng `let` khi bạn muốn khai báo biến có thể thay đổi giá trị trong suốt vòng đời của nó. Điều này đặc biệt hữu ích khi làm việc với các biến cần thay đổi giá trị trong các vòng lặp hoặc điều kiện.

#### 2.3. `const`: Biến Hằng Số

`const` được sử dụng để khai báo biến hằng số, nghĩa là giá trị của biến không thể thay đổi sau khi đã được gán.

Cách sử dụng:
```javascript
const z = 30;  // Biến hằng số z, không thể thay đổi giá trị
```

**Khi nào sử dụng `const`:**
Sử dụng `const` khi bạn muốn khai báo một biến mà giá trị của nó không bao giờ thay đổi trong suốt vòng đời của chương trình. Điều này giúp bảo vệ giá trị của biến khỏi bị thay đổi và tạo ra mã an toàn hơn.

### 3. Phạm Vi Của Biến

Phạm vi của biến trong JavaScript phụ thuộc vào cách khai báo biến:

- **Phạm vi toàn cục**: Biến được khai báo ngoài hàm hoặc khối mã có thể truy cập ở mọi nơi trong mã.
- **Phạm vi hàm**: Biến khai báo với `var` trong một hàm chỉ có thể truy cập trong hàm đó.
- **Phạm vi khối**: Biến khai báo với `let` và `const` trong một khối (ví dụ: trong `if` hoặc vòng lặp) chỉ có thể truy cập trong khối đó.

Cách sử dụng phạm vi khối:
```javascript
if (true) {
    let blockScoped = "I am block scoped";
    console.log(blockScoped);  // In ra "I am block scoped"
}
console.log(blockScoped);  // Lỗi: blockScoped không được định nghĩa ngoài khối
```

### 4. Gán Giá Trị Cho Biến

JavaScript cho phép bạn gán giá trị cho biến bất kỳ lúc nào trong chương trình. Bạn có thể gán một giá trị cho biến khi khai báo hoặc sau đó.

Cách gán giá trị:
```javascript
let a = 10;  // Khai báo và gán giá trị cho biến
a = 20;  // Gán giá trị mới cho biến a
console.log(a);  // In ra 20
```

### 5. Biến Trong Các Loại Dữ Liệu

JavaScript là ngôn ngữ động, nghĩa là bạn có thể thay đổi kiểu dữ liệu của biến trong suốt quá trình thực thi.

Cách sử dụng:
```javascript
let number = 10;  // number là kiểu số
number = "Hello";  // number giờ là kiểu chuỗi
console.log(number);  // In ra "Hello"
```

### 6. Kết Luận

Biến là một phần quan trọng trong JavaScript, giúp lưu trữ và quản lý dữ liệu trong suốt quá trình thực thi chương trình. Bạn có thể khai báo biến bằng `var`, `let`, hoặc `const`, tùy thuộc vào phạm vi và yêu cầu của chương trình. Hiểu rõ cách khai báo và sử dụng biến giúp bạn viết mã hiệu quả và tránh được các lỗi phổ biến.

**Khi nào sử dụng `var`, `let`, và `const`:**

- **`var`**: Chỉ sử dụng trong các trường hợp cần hỗ trợ trình duyệt cũ hoặc mã cũ. Tránh sử dụng trong mã mới vì phạm vi của nó có thể gây ra lỗi khó phát hiện.
- **`let`**: Sử dụng khi cần thay đổi giá trị của biến trong suốt vòng đời chương trình, đặc biệt là trong các vòng lặp và điều kiện.
- **`const`**: Sử dụng khi giá trị của biến không bao giờ thay đổi trong suốt chương trình, giúp bảo vệ dữ liệu và tạo ra mã an toàn hơn.