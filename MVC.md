# Mô hình MVC

## I. Mô hình MVC trong Java là gì?

MVC được viết tắt từ Model View Controller. Đây là mô hình phần mềm dùng để tạo lập giao diện người dùng trên máy tính. Mô hình MVC bao gồm ba bộ phận chính là Model, View và Controller. Mỗi thành phần có chức năng, nhiệm vụ khác nhau nhưng giữa chúng có sự tương tác qua lại, hỗ trợ nhau. Trong đó:

- Model có chức năng quản lý và xử lý dữ liệu.
- View có nhiệm vụ hiển thị dữ liệu cho người dùng. 
- Controller có chức năng điều khiển tương tác giữa Model và View.

Mô hình MVC trong Java giúp lập trình viên dễ dàng tách biệt giữa cách thức dữ liệu nội hàm với dữ liệu hiển thị. Sự tương tác qua lại giữa ba thành tố Model, View, Controller tạo nên hiệu quả tốt nhất cho việc lập trình. Chúng ta sẽ tìm hiểu chi tiết hơn về chức năng của từng thành phần trong MVC trong phần tiếp theo để từ đó hiểu và ứng dụng tốt nhất nhé!

![](https://lanit.com.vn/wp-content/uploads/2022/06/mo-hinh-mvc-trong-java-la-gi-02.jpg)

## II. Các thành phần trong mô hình MVC trong Java

### 1. Model

Một trong những thành phần quan trọng nhất của mô hình MVC trong Java. Đây là bộ phận làm nhiệm vụ quản lý dữ liệu. Model có chức năng vận chuyển thông tin từ nội hàm để hiển thị đến người dùng thông qua màn hình và xử lý các thông tin để người dùng dễ dàng tiếp cận nhất.

Model hoàn toàn độc lập với các thành phần còn lại trong MVC và nó chứa các tác vụ cần thiết nhất cho quá trình lập trình

### 2. View

Thành phần tiếp theo chúng ta sẽ nhắc đến ở mô hình MVC trong Java, đó là View. Đối với người dùng thì View có vai trò thiết yếu. Nó thực hiện nhiệm vụ tạo tương tác với người dùng và hiển thị các kết quả từ tầng Controller. Đồng thời, View cũng thực hiện việc tiếp nhận các hoạt động, yêu cầu của người dùng để chuyển đến Controller xử lý.

![](https://lanit.com.vn/wp-content/uploads/2022/06/mo-hinh-mvc-trong-java-la-gi-03.jpg)

### 3. Controller

Khi nhắc tới các thành phần ở mô hình MVC nhất định không thể bỏ qua Controller. Nếu không có thành phần này thì mọi hoạt động của Model hay View đều không còn giá trị.

Controller thực hiện chức năng kết nối tương tác giữa View và Model. Nó định nghĩa các lệnh và thực hiện xử lý các lệnh trong hệ thống. Controller đối chiếu hành động của người dùng từ View và tương tác với Model để chuyển tải thông tin cần thiết đến người dùng.

