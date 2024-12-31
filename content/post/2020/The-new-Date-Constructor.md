---
title: The new Date() Constructor  
date: 2023-12-31  
tags: ["javascript", "date", "constructor", "blog"]  
image: "/img/posts/img-36.png"  
Description: "Hướng dẫn chi tiết về cách sử dụng `new Date()` constructor trong JavaScript để tạo đối tượng `Date` và làm việc với ngày giờ."  
---

### 1. Giới Thiệu về `new Date()` Constructor

Trong JavaScript, Date là một đối tượng tích hợp sẵn dùng để làm việc với ngày và giờ. Bạn có thể sử dụng new Date() constructor để tạo một đối tượng Date mới. Khi gọi new Date(), bạn có thể tạo ra đối tượng Date theo nhiều cách khác nhau, tùy vào đối số được truyền vào.

### 2. Tạo Đối Tượng `Date` Mới

#### **Không truyền đối số**: 

Khi bạn không truyền bất kỳ đối số nào vào `new Date()`, nó sẽ tạo ra một đối tượng `Date` đại diện cho thời gian hiện tại (theo thời gian của hệ thống).

```javascript
let currentDate = new Date();
console.log(currentDate);  // Ví dụ: Thu Dec 31 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

#### **Truyền chuỗi ngày giờ**:

Bạn có thể tạo đối tượng `Date` từ một chuỗi ngày giờ hợp lệ. JavaScript sẽ phân tích chuỗi ngày giờ và trả về một đối tượng `Date` tương ứng.

```javascript
let dateFromString = new Date("2023-12-31T12:00:00");
console.log(dateFromString);  // Ví dụ: Sun Dec 31 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

**Lưu ý** rằng chuỗi ngày giờ phải tuân theo định dạng chuẩn ISO 8601 để đảm bảo tính chính xác khi phân tích.

#### **Truyền giá trị thời gian (timestamp)**:

Bạn cũng có thể truyền một giá trị timestamp (số mili giây kể từ 01/01/1970) vào `new Date()`. Điều này giúp bạn tạo đối tượng `Date` từ một thời điểm xác định trong quá khứ hoặc tương lai.

```javascript
let dateFromTimestamp = new Date(1609459200000);  // Timestamp cho 01/01/2021
console.log(dateFromTimestamp);  // Fri Jan 01 2021 00:00:00 GMT+0000 (Coordinated Universal Time)
```

#### **Truyền ngày, tháng, năm, giờ, phút, giây**:

Bạn cũng có thể truyền từng thành phần ngày, tháng, năm, giờ, phút và giây vào `new Date()`.

```javascript
let specificDate = new Date(2023, 11, 31, 12, 0, 0);  // Lưu ý tháng bắt đầu từ 0
console.log(specificDate);  // Ví dụ: Sun Dec 31 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

Trong đó:
- 2023 là năm.
- 11 là tháng (0 là tháng 1, 1 là tháng 2,...).
- 31 là ngày trong tháng.
- 12 là giờ (theo định dạng 24 giờ).
- 0 là phút.
- 0 là giây.

### 3. Phương Thức và Cách Sử Dụng Đối Tượng Date

Sau khi tạo đối tượng `Date` với `new Date()`, bạn có thể sử dụng các phương thức của đối tượng `Date` để thao tác với thời gian.

#### **Lấy thông tin từ đối tượng Date**:
- **`getFullYear()`**: Trả về năm của đối tượng Date.

```javascript
let date = new Date();
console.log(date.getFullYear());  // Ví dụ: 2023
```

- **`getMonth()`**: Trả về tháng (0-11).

```javascript
let date = new Date();
console.log(date.getMonth());  // Ví dụ: 11 (Tháng 12)
```

- **`getDate()`**: Trả về ngày trong tháng.

```javascript
let date = new Date();
console.log(date.getDate());  // Ví dụ: 31
```

- **`getDay()`**: Trả về ngày trong tuần (0 là Chủ nhật, 6 là Thứ bảy).

```javascript
let date = new Date();
console.log(date.getDay());  // Ví dụ: 0 (Chủ nhật)
```

- **`getHours()`**: Trả về giờ (0-23).

```javascript
let date = new Date();
console.log(date.getHours());  // Ví dụ: 12
```

- **`getMinutes()`**: Trả về phút (0-59).

```javascript
let date = new Date();
console.log(date.getMinutes());  // Ví dụ: 30
```

- **`getSeconds()`**: Trả về giây (0-59).

```javascript
let date = new Date();
console.log(date.getSeconds());  // Ví dụ: 45
```

#### **Cập nhật thông tin trong đối tượng Date**:
- **`setFullYear(year)`**: Cập nhật năm.

```javascript
let date = new Date();
date.setFullYear(2025);
console.log(date);  // Ví dụ: Thu Dec 31 2025 12:00:00 GMT+0000 (Coordinated Universal Time)
```

- **`setMonth(month)`**: Cập nhật tháng.

```javascript
let date = new Date();
date.setMonth(6);  // Tháng 7 (tháng bắt đầu từ 0)
console.log(date);  // Ví dụ: Thu Jul 31 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

- **`setDate(date)`**: Cập nhật ngày trong tháng.

```javascript
let date = new Date();
date.setDate(15);
console.log(date);  // Ví dụ: Wed Dec 15 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```