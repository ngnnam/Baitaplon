# Kiểm thử Website Fahasa bằng Selenium WebDriver

## Giới thiệu

Đây là dự án kiểm thử tự động Website Fahasa bằng Selenium WebDriver và Java.

Mục tiêu của dự án là mô phỏng quy trình mua hàng thực tế của người dùng trên Fahasa và kiểm tra các chức năng quan trọng của hệ thống.

Các chức năng được kiểm thử:

* Đăng nhập
* Tìm kiếm sản phẩm
* Thêm sản phẩm vào giỏ hàng
* Cập nhật số lượng sản phẩm trong giỏ hàng
* Thanh toán
* Xác nhận thanh toán

Dự án được xây dựng theo mô hình kiểm thử End-to-End (E2E Testing).

---

# Công nghệ sử dụng

* Java
* Selenium WebDriver
* Maven
* IntelliJ IDEA
* ChromeDriver
* TestNG

---

# Cấu trúc dự án

```text
src
│
├── Main.java
├── LoginTest.java
├── SearchTest.java
├── CartTest.java
└── PaymentTest.java
```

## Main.java

Là file điều khiển luồng kiểm thử chính.

Thứ tự thực hiện:

```text
Đăng nhập
↓
Tìm kiếm sản phẩm
↓
Thêm vào giỏ hàng
↓
Thanh toán
```

Toàn bộ các chức năng sử dụng chung một phiên làm việc (WebDriver) nhằm mô phỏng chính xác hành vi của người dùng thực tế.

---

## LoginTest.java

Kiểm thử chức năng đăng nhập.

Các bước thực hiện:

1. Truy cập trang đăng nhập.
2. Nhập tên đăng nhập.
3. Nhập mật khẩu.
4. Nhấn nút đăng nhập.
5. Kiểm tra đăng nhập thành công.

Kết quả mong đợi:

* Hệ thống chuyển sang trạng thái đăng nhập thành công.

---

## SearchTest.java

Kiểm thử chức năng tìm kiếm sản phẩm.

Các bước thực hiện:

1. Nhập từ khóa tìm kiếm.
2. Thực hiện tìm kiếm.
3. Kiểm tra kết quả tìm kiếm.

Ví dụ từ khóa:

```text
Đắc nhân tâm
```

Kết quả mong đợi:

* Hiển thị danh sách sản phẩm phù hợp.

---

## CartTest.java

Kiểm thử chức năng giỏ hàng.

Các bước thực hiện:

1. Chọn sản phẩm đầu tiên từ kết quả tìm kiếm.
2. Mở trang chi tiết sản phẩm.
3. Thêm sản phẩm vào giỏ hàng.
4. Kiểm tra giỏ hàng.
5. Tăng số lượng sản phẩm.
6. Giảm số lượng sản phẩm.
7. Xóa sản phẩm khỏi giỏ hàng.

Kết quả mong đợi:

* Các thao tác trên giỏ hàng hoạt động chính xác.

---

## PaymentTest.java

Kiểm thử chức năng thanh toán.

Các bước thực hiện:

1. Chọn sản phẩm trong giỏ hàng.
2. Nhấn nút Thanh toán.
3. Nhấn nút Xác nhận thanh toán.
4. Kiểm tra chuyển sang trang thanh toán.

Kết quả mong đợi:

* Người dùng được chuyển đến quy trình thanh toán thành công.

---

# Luồng kiểm thử

```text
Login
↓
Search Product
↓
Open Product Detail
↓
Add To Cart
↓
Increase Quantity
↓
Decrease Quantity
↓
Select Product
↓
Checkout
↓
Confirm Payment
```

---

# Cách chạy chương trình

## Bước 1

Clone dự án:

```bash
git clone https://github.com/your-username/FahasaTesting.git
```

## Bước 2

Mở dự án bằng IntelliJ IDEA.

## Bước 3

Cài đặt các thư viện Maven.

## Bước 4

Chạy file:

```text
Main.java
```

---

# Kết quả đầu ra mẫu

```text
===== START FAHASA TEST =====

LOGIN SUCCESS

SEARCH TEST PASSED

CART TEST PASSED

PAYMENT TEST PASSED

===== END FAHASA TEST =====
```

---

# Hướng phát triển

Trong tương lai có thể mở rộng thêm:

* Kiểm thử dữ liệu (Data Driven Testing)
* TestNG Report
* Extent Report
* Tự động chụp màn hình khi lỗi
* Kiểm thử đa trình duyệt
* Tích hợp GitHub Actions
* Kiểm thử hiệu năng bằng JMeter
* Kiểm thử API bằng Postman

---

Đồ án môn Kiểm thử và Đảm bảo chất lượng phần mềm

