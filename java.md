# Java

## I. Giới thiệu về Java

Java là một ngôn ngữ lập trình hướng đối tượng, được phát triển bởi Sun Microsystems (nay là Oracle) vào năm 1995. Java được thiết kế để có thể chạy trên nhiều nền tảng máy tính khác nhau (Windows, Mac OS, Linux, Solaris, ...), và được thiết kế để có thể chạy trên các thiết bị di động (điện thoại di động, máy tính bảng, ...).

## II. Các syntax cơ bản trong Java

## 1. Nhập, xuất dữ liệu

Một đoạn code mẫu về nhập xuất trong Java

```java

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt(); // Nhập số nguyên
        System.out.println(a); // Xuất ra màn hình
    }
}

```

### 1.1. Nhập dữ liệu

Để nhập dữ liệu từ bàn phím, ta sử dụng lớp Scanner. Lớp Scanner có thể được khởi tạo bằng cách truyền vào một đối tượng InputStream. Đối tượng InputStream có thể được khởi tạo bằng cách sử dụng System.in.

Cú pháp:

(data-type) (variable-name) = scan.next...();

Ta cần thay trong dấu "..." bằng phương thức ta muốn:

| Phương thức | Kiểu dữ liệu | Mô tả |
|-------------|--------------|-------|
| nextByte() | byte | Nhập số nguyên có dấu |
| nextShort() | short | Nhập số nguyên có dấu |
| nextInt() | int | Nhập số nguyên có dấu |
| nextLong() | long | Nhập số nguyên có dấu |
| nextFloat() | float | Nhập số thực |
| nextDouble() | double | Nhập số thực |
| nextBoolean() | boolean | Nhập giá trị true hoặc false |
| nextLine() | String | Nhập chuỗi ký tự |
| next() | String | Nhập chuỗi ký tự (không nhập dấu xuống dòng tương tự với cin trong C++)|


### 1.2. Xuất dữ liệu

Để xuất dữ liệu ra màn hình, ta sử dụng lớp System.out.println(). Lớp này có thể được sử dụng để xuất ra màn hình các kiểu dữ liệu cơ bản như int, float, double, char, String, boolean.

Cú pháp :

System.out.println() : xuất ra màn hình và xuống dòng

System.out.print() : xuất ra màn hình và không xuống dòng

System.out.printf() : xuất ra màn hình theo định dạng 
được kết quả đó nhờ vào các đối số thích hợp.(giống với đặc tả trong C/C++)

## 2. Biến

### 2.1. Khai báo biến

Cú pháp:

(data-type) (variable-name);

### 2.2. Khởi tạo biến

Cú pháp:

(data-type) (variable-name) = (value);

### 2.3. Các loại biến trong java

- Biến cục bộ: Biến được khai báo trong một phương thức, không có từ khóa static.

- Biến toàn cục: Biến được khai báo bên ngoài phương thức, có từ khóa static.

- Biến tham chiếu: Biến tham chiếu là biến tham chiếu đến một đối tượng. Biến tham chiếu được khai báo bằng cách sử dụng từ khóa new.

- Biến hằng: Biến hằng là biến không thể thay đổi giá trị sau khi được khởi tạo. Biến hằng được khai báo bằng cách sử dụng từ khóa final.

## 3. Toán tử

### 3.1. Toán tử số học

| Toán tử | Ý nghĩa |
| --- | --- |
| + | Cộng |
| - | Trừ |
| * | Nhân |
| / | Chia |
| % | Chia lấy dư |
| ++ | Tăng 1 đơn vị |
| -- | Giảm 1 đơn vị |

### 3.2. Toán tử so sánh

| Toán tử | Ý nghĩa |
| --- | --- |
| == | So sánh bằng |
| != | So sánh không bằng |
| > | So sánh lớn hơn |
| < | So sánh nhỏ hơn |
| >= | So sánh lớn hơn hoặc bằng |
| <= | So sánh nhỏ hơn hoặc bằng |

### 3.3. Toán tử gán

| Toán tử | Ý nghĩa |
| --- | --- |  
| = | Gán giá trị |
| += | Cộng và gán |
| -= | Trừ và gán |
| *= | Nhân và gán |
| /= | Chia và gán |
| %= | Chia lấy phần dư và gán |

### 3.4. Toán tử logic

| Toán tử | Ý nghĩa |
| --- | --- |
| && | AND |
| \|\| | OR |
| ! | NOT |

### 3.5. Toán tử bit

| Toán tử | Ý nghĩa |
| --- | --- |
| & | AND |
| \| | OR |
| ^ | XOR |
| ~ | NOT |
| << | Dịch trái |
| >> | Dịch phải |
| >>> | Dịch phải không dấu |

## 4. Câu lệnh điều kiện (If - else)

### 4.1. Cú pháp

``` java

if (<dieu kien>) {
    //code
} else{
    //code
}
```

### 4.2. Ví dụ

``` java

public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        if (a > b) {
            System.out.println("a > b");
        } else {
            System.out.println("a < b");
        }
    }
}
```

## 5. Câu lệnh lặp (For - while)

### 5.1. Câu lệnh lặp for

Cú pháp:

``` java
for (<khoi tao>; <dieu kien>; <tang bien dem>) {
    //code
}
```

Ví dụ:

``` java
public class Main {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            System.out.println(i);
        }
    }
}
```

### 5.2. Câu lệnh lặp while

Cú pháp:

``` java
while (<dieu kien>) {
    //code
}
```

Ví dụ:

``` java
public class Main {
    public static void main(String[] args) {
        int i = 0;
        while (i < 10) {
            System.out.println(i);
            i++;
        }
    }
}
```

### 5.3. Câu lệnh nhảy (break - continue)

- Câu lệnh break: Dùng để thoát khỏi vòng lặp.

- Câu lệnh continue: Dùng để bỏ qua các lệnh phía sau câu lệnh continue và chuyển sang lần lặp tiếp theo.

## 6. Mảng

### 6.1. Cú pháp

``` java
<kiểu dữ liệu>[] <tên mảng> = new <kiểu dữ liệu>[<số phần tử>];
```

Ví dụ:

``` java

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = sc.nextInt();
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
    }
}
```

## 7. Wrapper class

Wrapper class là một lớp bao bọc (wrapper) cho các kiểu dữ liệu nguyên thủy. Nó được sử dụng để chuyển đổi các kiểu dữ liệu nguyên thủy thành đối tượng và ngược lại. Nó cũng được sử dụng để chuyển đổi các đối tượng thành các kiểu dữ liệu nguyên thủy.

| Kiểu dữ liệu nguyên thủy | Kiểu dữ liệu Wrapper class |
| --- | --- |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| double | Double |
| char | Character |
| boolean | Boolean |

Ví dụ :

``` java

public class Main {
    public static void main(String[] args) {
        int a = 10;
        Integer b = new Integer(a);
        System.out.println(b);
    }
}
```

## 8. String classes

### 8.1. Các phương thức của String

| Phương thức | Mô tả |
| --- | --- |
| length() |  Trả về độ dài của chuỗi |
| charAt(int index) | Trả về ký tự tại vị trí index |
| indexOf(String str) | Trả về vị trí xuất hiện đầu tiên của chuỗi str |
| lastIndexOf(String str) | Trả về vị trí xuất hiện cuối cùng của chuỗi str |
| substring(int beginIndex) | Trả về chuỗi con bắt đầu từ vị trí beginIndex |
| substring(int beginIndex, int endIndex) | Trả về chuỗi con bắt đầu từ vị trí beginIndex và kết thúc tại vị trí endIndex |
| toLowerCase() | Chuyển chuỗi thành chữ thường |
| toUpperCase() | Chuyển chuỗi thành chữ hoa |
| trim() | Xóa các khoảng trắng ở đầu và cuối chuỗi |
| split(String regex) | Tách chuỗi thành mảng các chuỗi con bằng regex |
| isEmpty() | Kiểm tra xem chuỗi hiện tại có rỗng hay không |

Lưu ý : 

- Các phương thức trên không thay đổi chuỗi hiện tại mà trả về chuỗi mới.


### 8.2. Các phương thức của StringBuilder

| Phương thức | Mô tả |
| --- | --- |
| append(String str) | Thêm chuỗi str vào cuối chuỗi hiện tại |
| insert(int offset, String str) | Chèn chuỗi str vào vị trí offset |
| delete(int start, int end) | Xóa chuỗi con bắt đầu từ vị trí start và kết thúc tại vị trí end |
| reverse() | Đảo ngược chuỗi hiện tại |
| toString() | Chuyển đổi StringBuilder thành String |

Lưu ý : 
- Các phương thức trên thay đổi chuỗi hiện tại.

## 9. Regex

Regex là viết tắt của Regular Expression. Nó là một chuỗi ký tự đặc biệt được sử dụng để tìm kiếm, so sánh và thay thế các chuỗi khác.

### 9.1. Các ký tự đặc biệt

| Ký tự | Mô tả |
| --- | --- |
| . | Tương đương với một ký tự bất kỳ |
| \d | Tương đương với một ký tự số |
| \D | Tương đương với một ký tự không phải số |
| \w | Tương đương với một ký tự chữ cái hoặc số |
| \W | Tương đương với một ký tự không phải chữ cái hoặc số |
| \s | Tương đương với một ký tự khoảng trắng |
| \S | Tương đương với một ký tự không phải khoảng trắng |
| \b | Tương đương với một ký tự giới hạn từ |
| \B | Tương đương với một ký tự không phải giới hạn từ |
| ^ | Tương đương với một ký tự bắt đầu chuỗi |
| $ | Tương đương với một ký tự kết thúc chuỗi |
| * | Tương đương với một chuỗi bất kỳ |
| + | Tương đương với một chuỗi có ít nhất một ký tự |
| ? | Tương đương với một chuỗi có 0 hoặc 1 ký tự |
| {n} | Tương đương với một chuỗi có n ký tự |
| {n,} | Tương đương với một chuỗi có ít nhất n ký tự |
| {n,m} | Tương đương với một chuỗi có ít nhất n ký tự và nhiều nhất m ký tự |
| [abc] | Tương đương với một ký tự trong tập hợp abc |
| [^abc] | Tương đương với một ký tự không nằm trong tập hợp abc |
| [a-z] | Tương đương với một ký tự trong khoảng từ a đến z |
| [^a-z] | Tương đương với một ký tự không nằm trong khoảng từ a đến z |
| (x) | Tương đương với một chuỗi x |
| (x|y) | Tương đương với một chuỗi x hoặc y |
| (x)? | Tương đương với một chuỗi x hoặc rỗng |
| (x)* | Tương đương với một chuỗi x hoặc rỗng |
| (x)+ | Tương đương với một chuỗi x có ít nhất một ký tự |
| (x){n} | Tương đương với một chuỗi x có n ký tự |
| (x){n,} | Tương đương với một chuỗi x có ít nhất n ký tự |
| (x){n,m} | Tương đương với một chuỗi x có ít nhất n ký tự và nhiều nhất m ký tự |

### 9.2. Pattern và Matcher

Pattern và Matcher là hai lớp cung cấp các phương thức để thực hiện các phép toán trên biểu thức chính quy. Pattern là một lớp không thể thay đổi, nó được sử dụng để tạo ra một Matcher. Matcher là một lớp có thể thay đổi, nó được sử dụng để thực hiện các phép toán trên biểu thức chính quy.

#### 9.2.1. Pattern

Pattern là một lớp không thể thay đổi, nó được sử dụng để tạo ra một Matcher. Pattern cung cấp các phương thức sau:

  * `public static Pattern compile(String regex)`

    Tạo ra một Pattern từ một biểu thức chính quy.

    * `public Matcher matcher(CharSequence input)`
    * `public String pattern()`
    * `public String toString()`

#### 9.2.2. Matcher

Matcher là một lớp có thể thay đổi, nó được sử dụng để thực hiện các phép toán trên biểu thức chính quy. Matcher cung cấp các phương thức sau:

  * `public boolean matches()`

    Kiểm tra xem biểu thức chính quy có khớp với chuỗi đầu vào hay không.

  * `public boolean find()`

    Tìm kiếm chuỗi đầu vào có khớp với biểu thức chính quy hay không.

  * `public boolean find(int start)`

    Tìm kiếm chuỗi đầu vào có khớp với biểu thức chính quy từ vị trí start.

  * `public boolean lookingAt()`

    Kiểm tra xem biểu thức chính quy có khớp với chuỗi đầu vào từ vị trí đầu tiên hay không.

  * `public String group()`

    Trả về chuỗi khớp với biểu thức chính quy.

  * `public String group(int group)`

    Trả về chuỗi khớp với biểu thức chính quy tại nhóm group.

  * `public int start()`

    Trả về vị trí bắt đầu của chuỗi khớp với biểu thức chính quy.

  * `public int start(int group)`

    Trả về vị trí bắt đầu của chuỗi khớp với biểu thức chính quy tại nhóm group.

  * `public int end()`

    Trả về vị trí kết thúc của chuỗi khớp với biểu thức chính quy.

  * `public int end(int group)`

    Trả về vị trí kết thúc của chuỗi khớp với biểu thức chính quy tại nhóm group.

  * `public int groupCount()`

    Trả về số lượng nhóm trong biểu thức chính quy.

## III. OOP trong Java

### 1. Đặc điểm của OOP

  * Đóng gói (Encapsulation)

  * Kế thừa (Inheritance)

  * Đa hình (Polymorphism)

  * Trừu tượng (Abstraction)

### 2. Đóng gói 

Đóng gói là một trong những tính chất quan trọng của OOP. Đóng gói cho phép các đối tượng ẩn các thông tin bên trong nó, chỉ cho phép truy cập thông qua các phương thức công khai (public). Điều này giúp cho việc thay đổi cấu trúc bên trong của đối tượng không ảnh hưởng đến các đối tượng khác.

Ví dụ:

``` Java
    public class Student {
        private String name;
        private int age;
        private String address;
    
        public Student(String name, int age, String address) {
            this.name = name;
            this.age = age;
            this.address = address;
        }
    
        public String getName() {
            return name;
        }
    
        public void setName(String name) {
            this.name = name;
        }
    
        public int getAge() {
            return age;
        }
    
        public void setAge(int age) {
            this.age = age;
        }
    
        public String getAddress() {
            return address;
        }
    
        public void setAddress(String address) {
            this.address = address;
        }
    }
```

### 3. Kế thừa

Kế thừa là một trong những tính chất quan trọng của OOP. Kế thừa cho phép một lớp kế thừa các thuộc tính và phương thức của lớp khác. Lớp kế thừa được gọi là lớp con, lớp được kế thừa được gọi là lớp cha.

Các từ khóa trong kế thừa :

    * `extends` : dùng để kế thừa lớp cha.
    
    * `super` : dùng để gọi phương thức của lớp cha.


Ví dụ:

``` Java
    public class Animal {
        private String name;
        private int age;
    
        public Animal(String name, int age) {
            this.name = name;
            this.age = age;
        }
    
        public void eat() {
            System.out.println("Animal is eating");
        }
    
        public void sleep() {
            System.out.println("Animal is sleeping");
        }
    }
    
    public class Dog extends Animal {
        public Dog(String name, int age) {
            super(name, age);
        }
    
        @Override
        public void eat() {
            System.out.println("Dog is eating");
        }
    
        @Override
        public void sleep() {
            System.out.println("Dog is sleeping");
        }
    }
```

### 4. Đa hình

Đa hình là một trong những tính chất quan trọng của OOP. Đa hình cho phép một phương thức có nhiều hình thức khác nhau. Đa hình được thực hiện thông qua việc ghi đè phương thức (override method).

Từ khóa trong đa hình:

    * `@Override` : dùng để ghi đè phương thức.

Ví dụ:

``` Java
    public class Animal {
        private String name;
        private int age;
    
        public Animal(String name, int age) {
            this.name = name;
            this.age = age;
        }
    
        public void eat() {
            System.out.println("Animal is eating");
        }
    
        public void sleep() {
            System.out.println("Animal is sleeping");
        }
    }
    
    public class Dog extends Animal {
        public Dog(String name, int age) {
            super(name, age);
        }
    
        @Override
        public void eat() {
            System.out.println("Dog is eating");
        }
    
        @Override
        public void sleep() {
            System.out.println("Dog is sleeping");
        }
    }
```

### 5. Trừu tượng

Trừu tượng là một trong những tính chất quan trọng của OOP. Trừu tượng cho phép lập trình viên tập trung vào những đặc điểm chung của đối tượng mà không cần quan tâm đến chi tiết cụ thể. Trừu tượng được thực hiện thông qua việc khai báo lớp trừu tượng (abstract class) và phương thức trừu tượng (abstract method).

Từ khóa trong trừu tượng:

    * `abstract` : dùng để khai báo lớp trừu tượng và phương thức trừu tượng.

Ví dụ:

``` Java
    public abstract class Animal {
        private String name;
        private int age;
    
        public Animal(String name, int age) {
            this.name = name;
            this.age = age;
        }
    
        public abstract void eat();
    
        public abstract void sleep();
    }
    
    public class Dog extends Animal {
        public Dog(String name, int age) {
            super(name, age);
        }
    
        @Override
        public void eat() {
            System.out.println("Dog is eating");
        }
    
        @Override
        public void sleep() {
            System.out.println("Dog is sleeping");
        }
    }
```