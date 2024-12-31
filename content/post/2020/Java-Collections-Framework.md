---
title: Giới Thiệu Java Collections Framework  
date: 2023-12-28  
tags: ["java", "collections", "programming", "blog"]  
image: "/img/posts/img-12.png"  
Description: "Tìm hiểu về Java Collections Framework, một phần không thể thiếu trong việc quản lý dữ liệu và cải thiện hiệu suất của các ứng dụng Java. Hãy cùng khám phá các loại Collection và cách sử dụng chúng."  
---

### 1. Java Collections Framework là gì?  

Java Collections Framework (JCF) là một tập hợp các lớp và giao diện trong Java, được sử dụng để lưu trữ và quản lý dữ liệu theo cách hiệu quả. Nó hỗ trợ các cấu trúc dữ liệu như List, Set, Map và Queue, giúp đơn giản hóa việc thao tác trên dữ liệu.

#### **Các loại Collection chính:**  
- **List**: Lưu trữ các phần tử có thứ tự và cho phép trùng lặp (ArrayList, LinkedList).  
- **Set**: Không cho phép phần tử trùng lặp (HashSet, TreeSet).  
- **Map**: Lưu trữ dữ liệu theo cặp Key-Value (HashMap, TreeMap).  

#### **Ví dụ mã Java:**  
```java
import java.util.*;

public class CollectionsExample {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("Java");
        list.add("Python");
        list.add("C++");

        for (String lang : list) {
            System.out.println(lang);
        }
    }
}
```
### 2. Ưu Điểm của Java Collections Framework
- **Hiệu quả**: Cung cấp các thuật toán tối ưu cho việc tìm kiếm, sắp xếp và xử lý dữ liệu.
- **Tái sử dụng**: Sử dụng lại mã nguồn qua các lớp và giao diện chuẩn.
- **Đồng bộ hóa**: Hỗ trợ môi trường đa luồng với các lớp như Vector và Hashtable.