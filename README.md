## Basic Dart 

### 1. Cài đặt Dart trên Ubuntu 
- Tham khảo: [Cài đặt Dart](https://dart.dev/get-dart)
- Follow chính xác các bước sau đây, **không bỏ 1 lệnh nào**: 
```
81: $ sudo apt-get update

81: $ sudo apt-get install apt-transport-https
 
81: $ wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo gpg --dearmor -o /usr/share/keyrings/dart.gpg
 
81: $ echo 'deb [signed-by=/usr/share/keyrings/dart.gpg arch=amd64] https://storage.googleapis.com/download.dartlang.org/linux/debian stable main' | sudo tee /etc/apt/sources.list.d/dart_stable.list
```

```
81: $ sudo apt-get update
81: $ sudo apt-get install dart
```

```
81: $ export PATH="$PATH:/usr/lib/dart/bin"
```

- Thay đổi PATH cho future terminal sessions
```
81: $ echo 'export PATH="$PATH:/usr/lib/dart/bin"' >> ~/.profile
```

### 2. Viết code với Dart
- **Khi viết code, câu lệnh phải kết thúc bằng dấu chấm phẩy (;)**
- Tham khảo: [Dart basic syntax](https://www.raywenderlich.com/books/dart-apprentice/v1.0/chapters/1-hello-dart)

### 3. Biên dịch và chạy file dart 
- Mở termial và chạy câu lệnh 
```
81: $ dart run <file_path>
```
- Ví dụ: 
```
81: $ dart run hello.dart 
--> Hello, Dart!
```

### 4. Note
- **Từ khóa var: Chỉ được gán biến cho giá trị cùng kiểu**
- **Từ khóa dynamic: Gán thoải mái**
- [Label to break loop more accurately](https://www.tutorialspoint.com/dart_programming/dart_programming_loops.htm)

- [Final và const trong dart](https://linhta.dev/blog/final-va-const-trong-dart/#update)

- **mixin** khác class thông thường ở chỗ:
    - mixin không có constructor nên không thể tạo đối tượng.
    - mixin chỉ có thể sử dụng để implements hoặc with chứ không thể extends
    - mixin có thể giới hạn những class nào được phép sử dụng code của mình bằng từ khóa mixin on

- **import 'dart:collection';** to use **HashMap, HashSet, LinkedList ...**