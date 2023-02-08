# Collection và Collections

## I. Collection và Collections

"Collection" và "Collections" trong java là hai khái niệm khác nhau.

Collections trong java là một khuôn khổ cung cấp một kiến trúc để lưu trữ và thao tác tới nhóm các đối tượng. Tất cả các hoạt động mà bạn thực hiện trên một dữ liệu như tìm kiếm, phân loại, chèn, xóa,... có thể được thực hiện bởi Java Collections.

Collection trong java là một root interface trong hệ thống cấp bậc Collection. Java Collection cung cấp nhiều interface (Set, List, Queue, Deque vv) và các lớp (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet vv).

*Note :* 
> Sự khác nhau giữa Collection và Collections là Collection là một root interface trong hệ thống cấp bậc Collection trong Java, trong khi Collections là một lớp trong java.util package.

### 1. Collection

Collection là một root interface trong hệ thống cấp bậc Collection. Java Collection cung cấp nhiều interface (Set, List, Queue, Deque vv) và các lớp (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet vv).

### 2. Hệ thống cấp bậc Collection

![](https://viettuts.vn/images/java/java-collection/he-thong-cap-bac-colection-trong-java.png)

## II. Các interface trong Collection

### 1. List

List là một interface trong Collection. List là một danh sách các phần tử được sắp xếp theo thứ tự. List cho phép các phần tử trùng lặp và cho phép các phần tử null. List cung cấp các phương thức để truy cập các phần tử theo chỉ số và cho phép thay đổi các phần tử.

Cú pháp khai báo List:

`List<E> list = new ArrayList<E>();`

Các phương thức của interface List trong java :

| Phương thức | Mô tả |
| --- | --- |
| void add(int index, E element) | Thêm một phần tử vào danh sách tại vị trí chỉ định |
| boolean addAll(int index, Collection<? extends E> c) | Thêm tất cả các phần tử của một Collection vào danh sách tại vị trí chỉ định |
| E get(int index) | Trả về phần tử tại vị trí chỉ định |
| E set(int index, E element) | Thay thế phần tử tại vị trí chỉ định bằng phần tử mới |
| E remove(int index) | Xóa phần tử tại vị trí chỉ định |

Ví dụ : 
``` java
    import java.util.ArrayList;  
    import java.util.List;  
      
    public class ListExample {  
        public static void main(String[] args) {  
            List<String> list = new ArrayList<String>();  
            list.add("Java");  
            list.add("C++");  
            list.add("PHP");  
            list.add("Java");  
            list.add("Python");  
            System.out.println("Các phần tử của list: ");  
            for (String str : list) {  
                System.out.println(str);  
            }  
        }  
    }
```

### 2. ArrayList

Những điểm cần ghi nhớ về ArrayList:

    * ArrayList là một lớp kế thừa lớp List nên nó sẽ có một vài đặc điểm và phương thức tương đồng với List.
    * ArrayList được sử dụng như một mảng động để lưu trữ các phần tử.
    * ArrayList có thể chứa các phần tử trùng lặp.
    * ArrayList có thể chứa các phần tử null.
    * ArrayList không đồng bộ, nó không là thread-safe và không đảm bảo sự đồng bộ.
    * ArrayList là một lớp có thể thay đổi kích thước.
    * ArrayList duy trì thứ tự của phần tử được thêm vào.

Cú pháp khai báo ArrayList:

`ArrayList<E> arr = new ArrayList<E>();`

Các phương thức của ArrayList trong java :

| Phương thức | Mô tả |
| --- | --- |
| void add(int index, E element) | Thêm một phần tử vào danh sách tại vị trí chỉ định |
| boolean addAll(int index, Collection<? extends E> c) | Thêm tất cả các phần tử của một Collection vào danh sách tại vị trí chỉ định |
| E get(int index) | Trả về phần tử tại vị trí chỉ định |
| E set(int index, E element) | Thay thế phần tử tại vị trí chỉ định bằng phần tử mới |
| E remove(int index) | Xóa phần tử tại vị trí chỉ định |


Ví dụ : 
``` java
    import java.util.ArrayList;  
    import java.util.List;  
      
    public class ArrayListExample {  
        public static void main(String[] args) {  
            ArrayList<String> list = new ArrayList<String>();
            list.add("Java");
            list.add("C++");
            list.add("PHP");
            list.add("Java");
            list.add("Python");
            System.out.println("Các phần tử của list: ");
            for (String str : list) {
                System.out.println(str);
            }
        }  
    }
```

### 3. Map

Trong java, map được sử dụng để lưu trữ và truy xuất dữ liệu theo cặp key và value. Mỗi cặp key và value được gọi là mục nhập (entry). Map trong java chỉ chứa các giá trị key duy nhất. Map rất hữu ích nếu bạn phải tìm kiếm, cập nhật hoặc xóa các phần tử trên dựa vào các key.

Những điểm cần ghi nhớ về Map:

    * Map là một lớp kế thừa lớp Collection nên nó sẽ có một vài đặc điểm và phương thức tương đồng với Collection.
    * Map không chứa các phần tử trùng lặp.
    * Map không chứa các phần tử null.
    * Map không đồng bộ, nó không là thread-safe và không đảm bảo sự đồng bộ.
    * Map là một lớp không có thứ tự.

Cú pháp khai báo Map:

`Map<K, V> map = new HashMap<K, V>();`

Các phương thức của Map trong java :

| Phương thức | Mô tả |
| --- | --- |
| void clear() | Xóa tất cả các mục nhập của Map |
| boolean containsKey(Object key) | Kiểm tra xem Map có chứa một key cụ thể hay không |
| boolean containsValue(Object value) | Kiểm tra xem Map có chứa một value cụ thể hay không |
| Set<Map.Entry<K,V>> entrySet() | Trả về một Set chứa tất cả các mục nhập của Map |
| V get(Object key) | Trả về value của một key cụ thể |
| boolean isEmpty() | Kiểm tra xem Map có rỗng hay không |
| Set<K> keySet() | Trả về một Set chứa tất cả các key của Map |
| V put(K key, V value) | Thêm một mục nhập vào Map |
| void putAll(Map<? extends K,? extends V> m) | Thêm tất cả các mục nhập của một Map khác vào Map hiện tại |
| V remove(Object key) | Xóa một mục nhập khỏi Map |
| int size() | Trả về số lượng mục nhập của Map |
| Collection<V> values() | Trả về một Collection chứa tất cả các value của Map |

Ví dụ : 
``` java
    import java.util.HashMap;  
    import java.util.Map;  
      
    public class HashMapExample {  
        public static void main(String[] args) {  
            HashMap<Integer, String> map = new HashMap<Integer, String>();
            map.put(1, "Java");
            map.put(2, "C++");
            map.put(3, "PHP");
            map.put(4, "Java");
            map.put(5, "Python");
            System.out.println("Các phần tử của map: ");
            for (Map.Entry<Integer, String> entry : map.entrySet()) {
                System.out.println(entry.getKey() + " " + entry.getValue());
            }
        }  
    }
```

### 4. Các Collection khác trong java

Các Collection khác trong java :

| Collection | Mô tả |
| --- | --- |
| LinkedList |   |
| PriorityQueue | Là một lớp kế thừa lớp AbstractQueue và triển khai các interface Queue. |
| ArrayDeque | Là một lớp kế thừa lớp AbstractCollection và triển khai các interface Deque và Queue. |
| HashSet | Là một lớp kế thừa lớp AbstractSet và triển khai các interface Set. |
| LinkedHashSet | Là một lớp kế thừa lớp HashSet và triển khai các interface Set. |
| TreeSet | Là một lớp kế thừa lớp AbstractSet và triển khai các interface Set. |
| HashMap | Là một lớp kế thừa lớp AbstractMap và triển khai các interface Map. |
| LinkedHashMap | Là một lớp kế thừa lớp HashMap và triển khai các interface Map. |
| TreeMap | Là một lớp kế thừa lớp AbstractMap và triển khai các interface Map. |

### 5. Phân biêt giữa ArrayList và List

#### 5.1. Điểm khác nhau giữa ArrayList và List

| ArrayList | List |
| --- | --- |
| ArrayList là một lớp cụ thể trong java.util.ArrayList | List là một interface trong java.util.List |
| 

#### 5.2. Lúc nào cần dùng List, lúc nào cần dùng ArrayList

> Nếu dùng `List` (`List a = new ArrayList(); `)sẽ có ưu điểm là bạn có thể chuyển đổi `ArrayList` sang `Vector`, `LinkedList` dễ dàng thông qua các method có trong `List` interface, còn nếu dùng kiểu: `ArrayList a = new ArrayList();` thì bạn sẽ khó làm được điều này, bạn sẽ chỉ dùng được những method trong `ArrayList`.

### 6. Một số method trong Collections

| Method | Mô tả | Ví dụ |
| --- | --- | --- |
| sort() | Sắp xếp các phần tử trong Collection theo thứ tự tăng dần | Collections.sort(list); |
| reverse() | Đảo ngược thứ tự các phần tử trong Collection | Collections.reverse(list); |
| shuffle() | Xáo trộn các phần tử trong Collection | Collections.shuffle(list); |
| swap() | Hoán đổi vị trí của 2 phần tử trong Collection | Collections.swap(list, 0, 1); |
| rotate() | Xoay vòng các phần tử trong Collection | Collections.rotate(list, 2); |
| binarySearch() | Tìm kiếm một phần tử trong Collection | Collections.binarySearch(list, 2); |
| max() | Tìm phần tử có giá trị lớn nhất trong Collection | Collections.max(list); |
| min() | Tìm phần tử có giá trị nhỏ nhất trong Collection | Collections.min(list); |
| frequency() | Đếm số lần xuất hiện của một phần tử trong Collection | Collections.frequency(list, 2); |
| copy() | Sao chép các phần tử từ Collection này sang Collection khác | Collections.copy(list, list2); |
| fill() | Điền giá trị cho tất cả các phần tử trong Collection | Collections.fill(list, 2); |
| disjoint() | Kiểm tra xem 2 Collection có phần tử chung hay không | Collections.disjoint(list, list2); |
| replaceAll() | Thay thế tất cả các phần tử trong Collection bằng một giá trị khác | Collections.replaceAll(list, 2, 3); |
