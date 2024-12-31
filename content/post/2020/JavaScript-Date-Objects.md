---
title: JavaScript Date Objects  
date: 2023-12-31  
tags: ["javascript", "date", "objects", "blog"]  
image: "/img/posts/img-24.png"  
Description: "Hướng dẫn sử dụng đối tượng Date trong JavaScript để làm việc với ngày giờ, bao gồm các phương thức và cách thức tạo đối tượng Date."  
---

### 1. Giới Thiệu về JavaScript Date Objects

Trong JavaScript, `Date` là một đối tượng tích hợp sẵn giúp bạn làm việc với ngày và giờ. Bạn có thể tạo và thao tác với các đối tượng `Date` để lấy thông tin về thời gian hiện tại, so sánh ngày tháng, cũng như chuyển đổi giữa các định dạng ngày giờ khác nhau.

Đối tượng `Date` trong JavaScript được tạo ra để làm việc với thời gian và có thể đại diện cho một thời điểm trong quá khứ, hiện tại hoặc tương lai.

### 2. Tạo Đối Tượng `Date`

Để tạo một đối tượng `Date`, bạn có thể sử dụng cú pháp sau:

```javascript
let currentDate = new Date();  // Tạo đối tượng Date với thời gian hiện tại
console.log(currentDate);  // Ví dụ: Thu Dec 31 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

Ngoài ra, bạn có thể tạo `Date` từ một chuỗi ngày giờ hoặc một giá trị thời gian (timestamp):

```javascript
let specificDate = new Date("2023-12-31");  // Tạo Date từ chuỗi
console.log(specificDate);  // Sun Dec 31 2023 00:00:00 GMT+0000 (Coordinated Universal Time)
```

Hoặc từ timestamp (số mili giây kể từ 01/01/1970):

```javascript
let timestampDate = new Date(1609459200000);  // Tạo Date từ timestamp
console.log(timestampDate);  // Fri Jan 01 2021 00:00:00 GMT+0000 (Coordinated Universal Time)
```

### 3. Phương Thức Của Đối Tượng Date

Dưới đây là một số phương thức phổ biến của đối tượng `Date`:

- **`getFullYear()`**: Trả về năm của đối tượng Date.

```javascript
let date = new Date();
console.log(date.getFullYear());  // Ví dụ: 2023
```

- **`getMonth()`**: Trả về tháng của đối tượng Date, với tháng bắt đầu từ 0 (Tháng 0 là tháng 1).

```javascript
let date = new Date();
console.log(date.getMonth());  // Ví dụ: 11 (Tháng 12)
```

- **`getDate()`**: Trả về ngày trong tháng của đối tượng Date.

```javascript
let date = new Date();
console.log(date.getDate());  // Ví dụ: 31
```

- **`getHours()`**: Trả về giờ của đối tượng Date (0-23).

```javascript
let date = new Date();
console.log(date.getHours());  // Ví dụ: 12
```

- **`getMinutes()`**: Trả về phút của đối tượng Date (0-59).

```javascript
let date = new Date();
console.log(date.getMinutes());  // Ví dụ: 30
```

- **`getSeconds()`**: Trả về giây của đối tượng Date (0-59).

```javascript
let date = new Date();
console.log(date.getSeconds());  // Ví dụ: 45
```

- **`getMilliseconds()`**: Trả về mili giây của đối tượng Date (0-999).

```javascript
let date = new Date();
console.log(date.getMilliseconds());  // Ví dụ: 500
```

- **`getDay()`**: Trả về ngày trong tuần (0 là Chủ nhật, 6 là Thứ bảy).

```javascript
let date = new Date();
console.log(date.getDay());  // Ví dụ: 0 (Chủ nhật)
```

- **`getTime()`**: Trả về số mili giây kể từ 01/01/1970.

```javascript
let date = new Date();
console.log(date.getTime());  // Ví dụ: 1636345790000
```

### 4. Các Phương Thức Cập Nhật Ngày Giờ

Đối tượng `Date` cũng cung cấp các phương thức để cập nhật ngày giờ của đối tượng:

- **`setFullYear(year)`**: Cập nhật năm cho đối tượng Date.

```javascript
let date = new Date();
date.setFullYear(2025);
console.log(date);  // Ví dụ: Thu Dec 31 2025 12:00:00 GMT+0000 (Coordinated Universal Time)
```

- **`setMonth(month)`**: Cập nhật tháng cho đối tượng Date.

```javascript
let date = new Date();
date.setMonth(6);  // Tháng 7 (nhớ là tháng bắt đầu từ 0)
console.log(date);  // Ví dụ: Thu Jul 31 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

- **`setDate(date)`**: Cập nhật ngày cho đối tượng Date.

```javascript
let date = new Date();
date.setDate(15);
console.log(date);  // Ví dụ: Wed Dec 15 2023 12:00:00 GMT+0000 (Coordinated Universal Time)
```

- **`setHours(hours)`**: Cập nhật giờ cho đối tượng Date.

```javascript
let date = new Date();
date.setHours(18);
console.log(date);  // Ví dụ: Thu Dec 31 2023 18:00:00 GMT+0000 (Coordinated Universal Time)
```

- **`setMinutes(minutes)`**: Cập nhật phút cho đối tượng Date.

```javascript
let date = new Date();
date.setMinutes(45);
console.log(date);  // Ví dụ: Thu Dec 31 2023 12:45:00 GMT+0000 (Coordinated Universal Time)
```

### 5. Phương Thức `toLocaleString()`

Phương thức `toLocaleString()` giúp bạn định dạng ngày giờ theo múi giờ và ngôn ngữ cụ thể.

```javascript
let date = new Date();
console.log(date.toLocaleString('en-US'));  // Ví dụ: 12/31/2023, 12:00:00 PM
console.log(date.toLocaleString('en-GB'));  // Ví dụ: 31/12/2023, 12:00:00
```