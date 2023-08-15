# **LEARN JAVA**

## **Cấu trúc một lớp JAVA**

```java

package com.mycompany.java_1;

/**
 *
 * @author kin
 */
public class JAVA_1 {

    public static void main(String[] args) {
        int n = 20;
        int factorial = 1;
        
        // n! = 1*2*3...*n
        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }
        System.out.println("The Factorial of " + n + " is " + factorial);
    }
}

```

## **Cách khai báo biến**

- Tên biến chỉ bắt đầu chữ cái, ký hiệu đô là `$` hoặc ký tự gạch dưới. Tên biến có sự phân biệt viết HOA, viết THƯỜNG.

- Không sử dụng những tên sau làm tên biến:

![](./img_java/Screenshot%202023-08-13%20180530.png)

## **Kiểu dữ liệu trong JAVA**

![](./img_java/Screenshot%202023-08-13%20181002.png)
![](./img_java/Screenshot%202023-08-13%20181118.png)

- Kiểu dữ kiệu đối tượng `Được Viết Hoa chữ cái đầu`

> `Hằng số trong JAVA`

- `Syntax: final kiểu dữ liệu tên biến = giá trị`

```java
package com.mycompany.java_1;

public class JAVA_1 {

    public static void main(String[] args) {
        final int kin = 1;
    }
}

```

## **Cách nhập dữ liệu đầu vào (Input)**

- Lớp Scanner cho phép người dùng nhập giá trị từ bàn phím đối với một kiểu dữ liệu:

```java
public static void main(String[] args){
    Scanner scaner = new Scanner (System.in);
}
```

![](./img_java/Screenshot%202023-08-13%20184706.png)

```java
//Ví dụ:
package com.mycompany.java_1;

import java.util.Scanner;

/**
 *
 * @author kin
 */
public class JAVA_1 {

    public static void main(String[] args) {
        Scanner Nhap = new Scanner(System.in);
        int n = Nhap.nextInt();
        int factorial = 1;
        // n! = 1*2*3...*n
        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }
        System.out.println("The Factorial of " + n + " is " + factorial);
    }
}
```
## **Lớp Math**

- Math có 2 trường tĩnh:
    - `E: Cơ số của logarit tự nhiên`
    - `PI: 3,14..`

- Có các hàm toàn học sin cos, abs, ....

![](./img_java/Screenshot%202023-08-13%20202307.png)


## **Cách bắt lỗi ngoại lệ bằng try catch**

```java
//Cú pháp:

try{
    statement(s); //Khối lệnh có thể ném ngoại lệ
}
catch(exceptiontype name){
    statement(s); // Khối lệnh  sẽ thực hiện nếu ngoại lệ xảy ra
}
catch(exceptiontype name){
    statement(s); // Khối lệnh  sẽ thực hiện nếu ngoại lệ xảy ra
}
finally{
    statement(s); // Khối lệnh sẽ thực hiện bất chấp ngoại lệ xảy ra hay không
}

// Ví dụ:
package com.mycompany.java_1;

import java.util.Scanner;

public class JAVA_1 {

    public static void main(String[] args) {

        Scanner Nhap = new Scanner(System.in);
        int n = 0;
        try {
            n = Nhap.nextInt();

        } catch (Exception e) {
            System.err.println("Nhap du lieu khong dung");
        }
        int factorial = 1;
        // n! = 1*2*3...*n
        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }
        System.out.println("The Factorial of " + n + " is " + factorial);
    }
}

```

## **Từ khóa throw trong java**

- Từ khoá throw trong java được sử dụng để ném ra một ngoại lệ cụ thể.

- Chúng ta có thể ném một trong hai ngoại lệ checked hoặc unchecked trong java bằng từ khóa throw. Từ khóa throw chủ yếu được sử dụng để ném ngoại lệ tùy chỉnh (ngoại lệ do người dùng tự định nghĩa). Chúng ta sẽ học ngoại lệ tùy chỉnh trong bài sau.

![](./img_java/Screenshot%202023-08-14%20232220.png)
![](./img_java/Screenshot%202023-08-14%20232247.png)

## **Từ khóa throws trong java**

- Từ khóa throws trong java được sử dụng để khai báo một ngoại lệ. Nó thể hiện thông tin cho lập trình viên rằng có thể xảy ra một ngoại lệ, vì vậy nó là tốt hơn cho các lập trình viên để cung cấp các mã xử lý ngoại lệ để duy trì luồng bình thường của chương trình.

- Exception Handling chủ yếu được sử dụng để xử lý ngoại lệ checked. Nếu xảy ra bất kỳ ngoại lệ unchecked như NullPointerException, đó là lỗi của lập trình viên mà anh ta không thực hiện kiểm tra trước khi code được sử dụng.

![](./img_java/Screenshot%202023-08-14%20232434.png)
![](./img_java/Screenshot%202023-08-14%20232503.png)

## **Lập trình hướng đối tượng**

![](./img_java/Screenshot%202023-08-13%20213454.png)


> `toString()`

- Nhằm mục địch đưa ra thông tin đối tượng

```java
package com.mycompany.java_1;

public class JAVA_1 {

    public int x = 0;
    public int y = 0;

    public JAVA_1(int x, int y) {
        this.x = x;
        this.y = y;
    }

    @Override
    public String toString() {
        return x + ", " + y; // Generated from nbfs://nbhost/SystemFileSystem/Templates/Classes/Code/OverriddenMethodBody
    }

    public static void main(String[] args) {
        JAVA_1 ori = new JAVA_1(1, 2);
        System.out.println(ori);
    }
}
//Output: 1, 2
```

> `equals()`

- Mục đích so sánh 2 đối tượng.

![](./img_java/Screenshot%202023-08-13%20224758.png)
![](./img_java/Screenshot%202023-08-13%20224945.png)

> `hashCode()`

![](./img_java/Screenshot%202023-08-13%20225525.png)
- Nó sẽ hash ra một giá trị tùy thuộc vào giá trị thuộc tính.


> `Khái niệm kế thừa trong lập trình JAVA`

- **Inheritance (Kế thừa)**

![](./img_java/Screenshot%202023-08-13%20231402.png)

- **extend (Kế thừa)**

```java
public class HocSinh extends ConNguoi{
    private String tenLop, tenTruong;
}

public HocSinh(String hoVaTen, int namSinh, String tenLop, String tenTruong){
    super(hoVaTen, namSinh);
    this.tenLop = tenLop;
    this.tenTruong = tenTruong;
}

```

![](./img_java/Screenshot%202023-08-13%20234011.png)

![](./img_java/Screenshot%202023-08-14%20001058.png)

- Một lớp không bao giờ kế thừa được nhiều lớp.

> `Overriding - Ghi đè phương thưc`

```java
class Vehicle {
    void run() {
        System.out.println("Vehicle is running");
    }
}
 
public class Bike2 extends Vehicle {
    void run() {
        System.out.println("Bike is running safely");
    }
 
    public static void main(String args[]) {
        Bike2 obj = new Bike2();
        obj.run();
    }
}
```

- Phương thức phải có tên giống với lớp cha.
- Phương thức phải có tham số giống với lớp cha.
- Lớp con và lớp cha có mối quan hệ kế thừa.

> ` Nạp chồng phương thức - Overloading trong Java`

![](./img_java/Screenshot%202023-08-14%20093236.png)
![](./img_java/Screenshot%202023-08-14%20093553.png)

> `Lớp abstract trong java - Tính trừu tượng trong JAVA`

- Tính trừu tượng là một tiến trình ẩn các cài đặt chi tiết và chỉ hiển thị tính năng tới người dùng.

- Nói cách khác, nó chỉ hiển thị các thứ quan trọng tới người dùng và ẩn các chi tiết nội tại, ví dụ: để gửi tin nhắn, người dùng chỉ cần soạn text và gửi tin. Bạn không biết tiến trình xử lý nội tại về phân phối tin nhắn.
- Tính trừu tượng giúp bạn trọng tâm hơn vào đối tượng thay vì quan tâm đến cách nó thực hiện.

- Có 2 cách để đạt được sự trừu tượng hóa trong java

    - `Sử dụng lớp abstract`
    - `Sử dụng interface`

- Một phương thức được khai báo là abstract và không có trình triển khai thì đó là phương thức trừu tượng.

- Nếu bạn muốn một lớp chứa một phương thức cụ thể nhưng bạn muốn triển khai thực sự phương thức đó để được quyết định bởi các lớp con, thì bạn có thể khai báo phương thức đó trong lớp cha ở dạng abstract.

- Từ khóa abstract được sử dụng để khai báo một phương thức dạng abstract. Một phương thức abstract không có thân phương thức.

```java
// lop truu tuong Shape
abstract class Shape{  
    abstract void draw();  
}  
//Trong tinh huong nay, trinh trien khai duoc cung cap boi ai do, 
// vi du: nguoi su dung cuoi cung nao do  
class Rectangle extends Shape{  
void draw(){
  System.out.println("Ve hinh chu nhat");
  }  
}  
   
class Circle1 extends Shape{  
void draw(){
   System.out.println("Ve hinh tron");
}  
}  
   
//Trong tinh huong nay, phuong thuc duoc goi boi lap trinh vien hoac nguoi dung  
class TestAbstraction1{  
public static void main(String args[]) {  
   // Trong tinh huong nay, doi tuong duoc cung cap thong qua phuong thuc, 
   // chang han nhu getShape()  
   Shape s=new Circle1();
   s.draw();  
   }  
}  
```

- Bài tập:

```java
public class HangSanXuat {
	private String tenHangSanXuat, tenQuocGia;

	public HangSanXuat(String tenHangSanXuat, String tenQuocGia) {
		this.tenHangSanXuat = tenHangSanXuat;
		this.tenQuocGia = tenQuocGia;
	}

	public String getTenHangSanXuat() {
		return tenHangSanXuat;
	}

	public void setTenHangSanXuat(String tenHangSanXuat) {
		this.tenHangSanXuat = tenHangSanXuat;
	}

	public String getTenQuocGia() {
		return tenQuocGia;
	}

	public void setTenQuocGia(String tenQuocGia) {
		this.tenQuocGia = tenQuocGia;
	}
	
	
}

public abstract class PhuongTienDiChuyen {
	protected String tenLoaiPhuongTien;
	protected HangSanXuat hangSanXuat;
	
	public PhuongTienDiChuyen(String tenLoaiPhuongTien, HangSanXuat hangSanXuat) {
		this.tenLoaiPhuongTien = tenLoaiPhuongTien;
		this.hangSanXuat = hangSanXuat;
	}

	public String getTenLoaiPhuongTien() {
		return tenLoaiPhuongTien;
	}

	public void setTenLoaiPhuongTien(String tenLoaiPhuongTien) {
		this.tenLoaiPhuongTien = tenLoaiPhuongTien;
	}
	
	public String layTenHangSanXuat() {
		return this.hangSanXuat.getTenHangSanXuat();
	}
	
	public void batDau() {
		System.out.println("Bắt đầu ....");
	}

	public void tangToc() {
		System.out.println("Tăng tốc ...");
	}
	
	public void dungLai() {
		System.out.println("Dừng lại ...");
	}
	
	public abstract double layVanToc();
}
```

![](./img_java/Screenshot%202023-08-14%20104841.png)


> `Interface trong java`

- Các trường của Interface là public, static và final theo mặc định và các phương thức là public và abstract.

- Một Interface trong Java là một tập hợp các phương thức trừu tượng (abstract). Một class triển khai một interface, do đó kế thừa các phương thức abstract của interface.

- Một interface không phải là một lớp. Viết một interface giống như viết một lớp, nhưng chúng có 2 định nghĩa khác nhau. Một lớp mô tả các thuộc tính và hành vi của một đối tượng. Một interface chứa các hành vi mà một class triển khai.

- Trừ khi một lớp triển khai interface là lớp trừu tượng abstract, còn lại tất cả các phương thức của interface cần được định nghĩa trong class.

- Một interface tương tự với một class bởi những điểm sau đây:

    - Một interface được viết trong một file với định dạng .java, với tên của interface giống tên của file.
    - Bytecode của interface được lưu trong file có định dạng .class.
    - Khai báo interface trong một package, những file bytecode tương ứng cũng có cấu trúc thư mục có cùng tên package.
- Một interface khác với một class ở một số điểm sau đây:

    - Bạn không thể khởi tạo một interface.
    - Một interface không chứa bất cứ hàm Contructor nào.
    - Tất cả các phương thức của interface đều là abstract.
    - Một interface không thể chứa một trường nào trừ các trường vừa static và final.
    - Một interface không thể kế thừa từ lớp, nó được triển khai bởi một lớp.
    - Một interface có thể kế thừa từ nhiều interface khác.

```java
interface printable {  
void print();  
}  
   
class A6 implements printable {  
    public void print() {
        System.out.println("Hello");
    }  
   
    public static void main(String args[]){  
        A6 obj = new A6();  
        obj.print();  
    }
} 
```

- Khi ghi đè các phương thức được định nghĩa trong interface, có một số qui tắc sau:

    - Các checked exception không nên được khai báo trong phương thức implements, thay vào đó nó nên được khai báo trong phương thức interface hoặc các lớp phụ được khai báo bởi phương thức interface.
    - Signature (ký số) của phương thức interface và kiểu trả về nên được duy trì khi ghi đè phương thức (overriding method).
    - Một lớp triển khai chính nó có thể là abstract và vì thế các phương thức interface không cần được triển khai.
- Khi triển khai interface, có vài quy tắc sau:

    - Một lớp có thể triển khai một hoặc nhiều interface tại một thời điểm.
    - Một lớp chỉ có thể kế thừa một lớp khác, nhưng được triển khai nhiều interface.
    - Một interface có thể kế thừa từ một interface khác, tương tự cách một lớp có thể kế thừa lớp khác.

```java
interface Printable{  
    void print();  
}  
interface Showable{  
    void print();  
}  
   
class TestTnterface1 implements Printable,Showable{  
    public void print() {
        System.out.println("Hello");
    }  
     
    public static void main(String args[]) {  
        TestTnterface1 obj = new TestTnterface1();  
        obj.print();  
    }  
}  
```

- `Kế thừa Interface trong Java`

```java
interface Printable{  
    void print();  
}  
interface Showable extends Printable{  
    void show();  
}  
class Testinterface2 implements Showable{  
   
    public void print() {
        System.out.println("Hello");
    }  
    public void show() {
        System.out.println("Welcome");
    }  
   
    public static void main(String args[]){  
        Testinterface2 obj = new Testinterface2();  
        obj.print();  
        obj.show();  
    }  
}  
```

- `Interface lồng nhau`

```java
interface printable{  
    void print();  
    interface MessagePrintable{  
       void msg();  
    }
}  

```
- Ví dụ điển hình:

```java
public interface MayTinhBoTuiInterface {
	public abstract double cong(double a, double b);
	
	public double tru(double a, double b);
	
	public double nhan(double a, double b);
	
	public double chia(double a, double b);
}

public class MayTinhCasioFX500 implements MayTinhBoTuiInterface{

	@Override
	public double cong(double a, double b) {
		return a+b;
	}

	@Override
	public double tru(double a, double b) {
		return a-b;
	}

	@Override
	public double nhan(double a, double b) {
		return a*b;
	}

	@Override
	public double chia(double a, double b) {
		return a/b;
	}
	
}

public class MayTinhVinacal500 implements MayTinhBoTuiInterface{

	@Override
	public double cong(double a, double b) {
		return a-b;
	}

	@Override
	public double tru(double a, double b) {
		return a-b;
	}

	@Override
	public double nhan(double a, double b) {
		return a*b;
	}

	@Override
	public double chia(double a, double b) {
		return a/b;
	}

}

public interface SapXepInterface {
	public void sapXepTang(double[] arr);
	public void sapXepGiam(double[] arr);
}

public class SapXepChen implements SapXepInterface {

	@Override
	public void sapXepTang(double[] arr) {
		int n = arr.length;
		double key;
		int i, j;
		for (i = 1; i < n; i++) {
			key = arr[i];
			j = i - 1;

			while (j >= 0 && arr[j] > key) {
				arr[j + 1] = arr[j];
				j = j - 1;
			}
			arr[j + 1] = key;
		}
	}

	@Override
	public void sapXepGiam(double[] arr) {
		int n = arr.length;
		double key;
		int i, j;
		for (i = 1; i < n; i++) {
			key = arr[i];
			j = i - 1;

			while (j >= 0 && arr[j] < key) {
				arr[j + 1] = arr[j];
				j = j - 1;
			}
			arr[j + 1] = key;
		}
	}

}

public class SapXepChon implements SapXepInterface {

	@Override
	public void sapXepTang(double[] arr) {
		int n = arr.length;
		int i, j, min_idx;
		for (i = 0; i < n - 1; i++) {
			min_idx = i;
			for (j = i + 1; j < n; j++)
				if (arr[j] < arr[min_idx])
					min_idx = j;
			double temp = arr[min_idx];
			arr[min_idx] = arr[i];
			arr[i] = temp;
		}
	}

	@Override
	public void sapXepGiam(double[] arr) {
		int n = arr.length;
		int i, j, min_idx;
		for (i = 0; i < n - 1; i++) {
			min_idx = i;
			for (j = i + 1; j < n; j++)
				if (arr[j] > arr[min_idx])
					min_idx = j;
			double temp = arr[min_idx];
			arr[min_idx] = arr[i];
			arr[i] = temp;
		}
	}

}

public class PhanMemMayTinh implements MayTinhBoTuiInterface, SapXepInterface{

	@Override
	public double cong(double a, double b) {
		return a+b;
	}

	@Override
	public double tru(double a, double b) {
		return a-b;
	}

	@Override
	public double nhan(double a, double b) {
		return a*b;
	}

	@Override
	public double chia(double a, double b) {
		return a/b;
	}
	
	@Override
	public void sapXepTang(double[] arr) {
		int n = arr.length;
		double key;
		int i, j;
		for (i = 1; i < n; i++) {
			key = arr[i];
			j = i - 1;

			while (j >= 0 && arr[j] > key) {
				arr[j + 1] = arr[j];
				j = j - 1;
			}
			arr[j + 1] = key;
		}
	}

	@Override
	public void sapXepGiam(double[] arr) {
		int n = arr.length;
		double key;
		int i, j;
		for (i = 1; i < n; i++) {
			key = arr[i];
			j = i - 1;

			while (j >= 0 && arr[j] < key) {
				arr[j + 1] = arr[j];
				j = j - 1;
			}
			arr[j + 1] = key;
		}
	}


}

import java.util.Iterator;

public class Test {
	public static void main(String[] args) {
		System.out.println("Test câu a: ");
		MayTinhCasioFX500 mfx500 = new MayTinhCasioFX500();
		MayTinhVinacal500 mvn500 = new MayTinhVinacal500();
		
		System.out.println("5+3="+ mfx500.cong(5, 3));
		System.out.println("4*5="+ mvn500.nhan(4, 5));
		System.out.println("4/0="+ mvn500.chia(4, 0));
		
		System.out.println("Test câu b: ");
		
		double[] arr = new double[] {5,1,3,4,5,8,0};
		double[] arr2 = new double[] {6,2,7,9,2,4,5};
		SapXepChen sxchen = new SapXepChen();
		SapXepChon sxchon = new SapXepChon();
		
		sxchen.sapXepTang(arr);
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i]+" ");
		}
		System.out.println();
		sxchon.sapXepGiam(arr2);
		for (int i = 0; i < arr2.length; i++) {
			System.out.print(arr2[i]+" ");
		}
		System.out.println();
		
		System.out.println("Test câu c:");
		PhanMemMayTinh pmmt =new PhanMemMayTinh();
		System.out.println("3+5=" + pmmt.cong(3, 5));
		double[] arr3 = new double[] {6,2,7,9,2,4,5};
		pmmt.sapXepTang(arr3);
		for (int i = 0; i < arr3.length; i++) {
			System.out.print(arr3[i]+" ");
		}
	}
}
```

## **Package trong java**

- Package trong java có thể được phân loại theo hai hình thức, package được dựng sẵn và package do người dùng định nghĩa.

- Có rất nhiều package được dựng sẵn như java, lang, AWT, javax, swing, net, io, util, sql, ...

> `Lợi thế của việc sử dụng package trong java`

- Package được sử dụng để phân loại lớp và interface giúp dễ dàng bảo trì.
- Package cung cấp bảo vể truy cập
- Package khắc phục được việc đặt trùng tên.

![](./img_java/Screenshot%202023-08-14%20112656.png)

```java
//Save file Simple.java
package mypack;  
public class Simple {  
    public static void main(String args[]) {
        System.out.println("Learn java package");
    }
}  
```

- Có 3 cách để truy cập package từ package bên ngoài:

    - Khai báo import package.*;
    - Khai báo import package.classname;
    - Sử dụng tên đầy đủ.

![](./img_java/Screenshot%202023-08-14%20113250.png)
![](./img_java/Screenshot%202023-08-14%20113327.png)
![](./img_java/Screenshot%202023-08-14%20113417.png)

## **Phân biệt điều khiển public, protected, private**

![](./img_java/Screenshot%202023-08-14%20114419.png)

## **Constructor trong java**

- Constructor trong java là một dạng đặc biệt của phương thức được sử dụng để khởi tạo các đối tượng.

- Java Constructor được gọi tại thời điểm tạo đối tượng. Nó khởi tạo các giá trị để cung cấp dữ liệu cho các đối tượng, đó là lý do tại sao nó được gọi là constructor.

- Có 2 quy tắc cơ bản cho việc tạo constructor:

    - Tên constructor phải giống tên lớp chứa nó.
    - Constructor không có kiểu trả về tường minh.

- Có 2 kiểu Constructor:

![](./img_java/Screenshot%202023-08-14%20130131.png)


## **Từ khóa final trong java**

> `Biến final trong java`

![](./img_java/Screenshot%202023-08-14%20140733.png)


> `Phương thức final trong Java`

![](./img_java/Screenshot%202023-08-14%20141029.png)

> `Lớp final trong Java`

![](./img_java/Screenshot%202023-08-14%20142023.png)

## **Từ khóa Static trong JAVA**

- Trong java, Static có thể là:

    - `Biến static:` Khi bạn khai báo một biến là static, thì biến đó được gọi là biến tĩnh, hay biến static.
    - `Phương thức static:` Khi bạn khai báo một phương thức là static, thì phương thức đó gọi là phương thức static.
    - `Khối static:` Được sử dụng để khởi tạo thành viên dữ liệu static.

`1. Biến static trong Java`

- Khi bạn khai báo một biến là static, thì biến đó được gọi là biến tĩnh, hay biến static.

    - Biến static có thể được sử dụng để tham chiếu thuộc tính chung của tất cả đối tượng (mà không là duy nhất cho mỗi đối tượng), ví dụ như tên công ty của nhân viên, tên trường học của các sinh viên, ...
    - Biến static lấy bộ nhớ chỉ một lần trong Class Area tại thời gian tải lớp đó.

![](./img_java/Screenshot%202023-08-14%20151628.png)
![](./img_java/Screenshot%202023-08-14%20151709.png)

`2. Phương thức static trong Java`

- Nếu bạn áp dụng từ khóa static với bất cứ phương thức nào, thì phương thức đó được gọi là phương thức static.

    - Một phương thức static thuộc lớp chứ không phải đối tượng của lớp.
    - Một phương thức static gọi mà không cần tạo một instance của một lớp.
    - Phương thức static có thể truy cập biến static và có thể thay đổi giá trị của nó.

```java
public class Student9 {
    int rollno;
    String name;
    static String college = "Bưu Chính Viễn Thông";
 
    static void change() {
        // Thay đổi thuộc tính static (thuộc tính chung của tất cả các đối tượng)
        college = "Đại Học Công Nghệ";
    }
 
    Student9(int r, String n) {
        rollno = r;
        name = n;
    }
 
    void display() {
        System.out.println(rollno + " - " + name + " - " + college);
    }
 
    public static void main(String args[]) {
        Student9.change();
 
        Student9 s1 = new Student9(111, "Thông");
        Student9 s2 = new Student9(222, "Minh");
        Student9 s3 = new Student9(333, "Anh");
 
        s1.display();
        s2.display();
        s3.display();
    }
}

//Output:
111 - Thông - Đại Học Công Nghệ
222 - Minh - Đại Học Công Nghệ
333 - Anh - Đại Học Công Nghệ
```

`3. Khối static trong Java`

- Được sử dụng để khởi tạo thành viên dữ liệu static.
- Nó được thực thi trước phương thức main tại lúc tải lớp.

```java
public class A2 {
    static {
        System.out.println("Khối static: hello !");
    }
 
    public static void main(String args[]) {
        System.out.println("Main: hello !");
    }
}
//Output:
Khối static: hello !
Main: hello !
```

## **Truyền giá trị và tham chiếu (pass-by-value và pass-by-reference) trong java**

![](./img_java/Screenshot%202023-08-14%20154558.png)
![](./img_java/Screenshot%202023-08-14%20154636.png)


## **Xử lý chuỗi trong JAVA**

![](./img_java/Screenshot%202023-08-14%20205345.png)
![](./img_java/Screenshot%202023-08-14%20205542.png)

```JAVA
//Phương thức charAt trong Java String
// Phương thức charAt() trả về giá trị Char của chuỗi tại vị trí có chỉ số index được chỉ định được chỉ định. Index bắt đầu từ 0.

public class CharAtExample {
 public static void main(String args[]) {
  String name = "hello java";
  char ch = name.charAt(4);
  System.out.println(ch);
 }
}
//Output: o

---------------------------------------------------------
//Phương thức compareTo trong Java String
//Phương thức compareTo() so sánh các chuỗi cho trước với chuỗi hiện tại theo thứ tự từ điển. Nó trả về số dương, số âm hoặc 0.

//Nếu chuỗi đầu tiên lớn hơn chuỗi thứ hai, nó sẽ trả về số dương (chênh lệch giá trị ký tự). Nếu chuỗi đầu tiên nhỏ hơn chuỗi thứ hai, nó sẽ trả về số âm và nếu chuỗi đầu tiên là bằng chuỗi thứ hai, nó trả về 0.

public class LastIndexOfExample {
 public static void main(String args[]) {
  String s1 = "hello";
  String s2 = "hello";
  String s3 = "meklo";
  String s4 = "hemlo";
  System.out.println(s1.compareTo(s2));
  System.out.println(s1.compareTo(s3));
  System.out.println(s1.compareTo(s4));
 }
}

//Output:
0
-5
-1

---------------------------------------------------------
//Phương thức concat trong Java String
//Phương thức concat() nối thêm chuỗi được chỉ định vào cuối chuỗi đã cho.
public class ConcatExample {
 public static void main(String args[]) {
  String s1 = "java string";
  s1.concat("is immutable");
  System.out.println(s1);
  s1 = s1.concat(" is immutable so assign it explicitly");
  System.out.println(s1);
 }
}
// Output:
java string
java string is immutable so assign it explicitly


---------------------------------------------------------
//Phương thức contains trong Java String
//Phương thức contains() tìm kiếm chuỗi ký tự trong chuỗi này. Nó trả về true nếu chuỗi các giá trị char được tìm thấy trong chuỗi này, nếu không trả về false.
public class ContainsExample {
 public static void main(String args[]) {
  String name = "what do you know about me";
  System.out.println(name.contains("do you know"));
  System.out.println(name.contains("about"));
  System.out.println(name.contains("hello"));
 }
}
//Output:

true
true
false

---------------------------------------------------------

//Phương thức endsWith trong Java String
//Phương thức endsWith() kiểm tra nếu chuỗi này kết thúc với hậu tố nhất định. Nó trả về true nếu chuỗi này kết thúc với hậu tố đã cho, nếu khác thì trả về false.

public class EndsWithExample {
 public static void main(String args[]) {
  String s1 = "hello java";
  System.out.println(s1.endsWith("t"));
  System.out.println(s1.endsWith("java"));
 }
}

//Output:

false
true

---------------------------------------------------------

//Phương thức equals trong Java String
//Phương thức equals() so sánh hai chuỗi đưa ra dựa trên nội dung của chuỗi. Nếu hai chuỗi khác nhau nó trả về false. Nếu hai chuỗi bằng nhau nó trả về true.
//Phương thức equals() của lớp String được ghi đè từ phương thức equals() của lớp Object.

public class EqualsExample {
 public static void main(String args[]) {
  String s1 = "java";
  String s2 = "java";
  String s3 = "JAVA";
  String s4 = "python";
  System.out.println(s1.equals(s2));
  System.out.println(s1.equals(s3));
  System.out.println(s1.equals(s4));
 }
}

//Output:

true
false
false

---------------------------------------------------------

//Phương thức equalsIgnoreCase trong Java String
//Phương thức equalsIgnoreCase() so sánh hai chuỗi đưa ra dựa trên nội dung của chuỗi không phân biệt chữ hoa và chữ thường. Nếu hai chuỗi khác nhau nó trả về false. Nếu hai chuỗi bằng nhau nó trả về true.

public class EqualsExample {
 public static void main(String args[]) {
  String s1 = "java";
  String s2 = "java";
  String s3 = "JAVA";
  String s4 = "python";
  System.out.println(s1.equalsIgnoreCase(s2));
  System.out.println(s1.equalsIgnoreCase(s3));
  System.out.println(s1.equalsIgnoreCase(s4));
 }
}
//Output:

true
true
false

-------------------------------------------------

//Phương thức formart trong Java String
//Phương thức formart() trả về một chuỗi được format theo miền địa phương.
//Nếu bạn không chỉ định miền địa phương trong phương thức String.format(), nó sử dụng miền mặc bằng cách gọi phương thức Locale.getDefault().
//Phương thức format() của ngôn ngữ java là giống như hàm sprintf() trong C và printf() trong Java.

public class FormatExample {
 public static void main(String args[]) {
  String name = "sonoo";
  String sf1 = String.format("name is %s", name);
  String sf2 = String.format("value is %f", 32.33434);
  String sf3 = String.format("value is %32.12f", 32.33434);
 
  System.out.println(sf1);
  System.out.println(sf2);
  System.out.println(sf3);
 }
}
//Output:

name is sonoo
value is 32.334340
value is                  32.334340000000

-----------------------------------------------------
//Phương thức getBytes trong Java String
//Phương thức getBytes() trả về mảng byte của chuỗi.

public class StringGetBytesExample {
 public static void main(String args[]) {
  String s1 = "ABCDEFG";
  byte[] barr = s1.getBytes();
  for (int i = 0; i < barr.length; i++) {
   System.out.println(barr[i]);
  }
 }
}
//Output:

65
66
67
68
69
70
71

---------------------------------------------------------

//Phương thức getChars trong Java String
//Phương thức getChars() sao chép nội dung của chuỗi thành mảng Char cụ thể. Có 4 đối số truyền vào phương thức getChars().

public class StringGetCharsExample {
 public static void main(String args[]) {
  String str = new String("hello Java how are you?");
  char[] ch = new char[4];
  try {
   str.getChars(6, 10, ch, 0);
   System.out.println(ch);
  } catch (Exception ex) {
   System.out.println(ex);
  }
 }
}
//Output:

Java


----------------------------------------------------

//Phương thức indexOf trong Java String
//Phương thức indexOf() trả về chỉ số của giá trị ký tự đã cho hoặc chuỗi con. Nếu không tìm thấy trả lại giá trị -1. Chỉ số (index) được đếm từ 0.

public class IndexOfExample {
 public static void main(String args[]) {
  String s1 = "this is index of example";
   
  //Truyền vào chuỗi con
  int index1 = s1.indexOf("is");
  int index2 = s1.indexOf("index");
  System.out.println(index1 + "  " + index2);//2 8  
 
  //Truyền vào chuỗi con và chỉ số bắt đầu
  int index3 = s1.indexOf("is", 4);
  System.out.println(index3);//5
 
  //Truyền vào giá trị Char
  int index4 = s1.indexOf('s');
  System.out.println(index4);//3  
 }
}
//Output:

2  8
5
3

---------------------------------------------------
//Phương thức isEmpty trong Java String
//Phương thức isEmpty() khi chuỗi trống trả về true, ngược lại trả về false.

public class IsEmptyExample {
 public static void main(String args[]) {
  String s1 = "";
  String s2 = "hello java";
 
  System.out.println(s1.isEmpty());
  System.out.println(s2.isEmpty());
 }
}
//Output:

true
false
----------------------------------------------------

//Phương thức join trong Java String
//Phương thức join() trả về một chuỗi được nối với nhau bởi dấu phân tách. Trong phương thức join chuỗi, dấu phân cách được sử dụng cho mỗi chuỗi được nối. Trong trượng hợp chuỗi = null, giá trị "null" được thêm vào. 

public class StringJoinExample {
 public static void main(String args[]) {
  String joinString1 = String.join("-", "welcome", "to", "java");
  System.out.println(joinString1);
 }
}
//Output:

welcome-to-java

---------------------------------------------------------
//Phương thức lastIndexOf() trả vể chỉ số cuối của ký tự hoặc chuỗi con. Nếu không tìm thấy trả về -1. Giá trị index được tính từ 0.

int lastIndexOf(int ch)
int lastIndexOf(int ch, int fromIndex)
int lastIndexOf(String substring)
int lastIndexOf(String substring, int fromIndex)
//Ví dụ:
public class LastIndexOfExample {
 public static void main(String args[]) {
  String s1 = "this is index of example";
  int index1 = s1.lastIndexOf('s');
  int index2 = s1.lastIndexOf("ex");
  System.out.println(index1);//6 
  System.out.println(index2);//17
 }
}
//Output:

6
17
--------------------------------------------------------

//Phương thức length trong Java String
//Phương thức length () trả về độ dài của chuỗi (tổng số ký tự theo mã unicode).

public class LengthExample {
 public static void main(String args[]) {
  String s1 = "java";
  String s2 = "python";
  System.out.println("string length is: " + s1.length());
  System.out.println("string length is: " + s2.length());
 }
}
//Output:

string length is: 4
string length is: 6

---------------------------------------------------------

//Phương thức replace trong Java String
//Phương thức replace() được sử dụng để thay thế tất cả các ký tự hoặc chuỗi cũ thành ký tự hoặc chuỗi mới.

public class ReplaceExample1 {
 public static void main(String args[]) {
  String s1 = "viettuts is a very good website";
  String replaceString = s1.replace('t', 'j');//thay thế tất cả ký tự 't' thành 'j'  
  System.out.println(replaceString);
 }
}
//Output:

viejjujs is a very good websije

---------------------------------------------------------

//Phương thức replaceAll trong Java String
//Phương thức replaceAll() trả về một chuỗi thay thế tất cả các chuỗi ký tự phù hợp với regex.
	
public String replaceAll(String regex, String replacement) 


public class ReplaceAllExample1 {
 public static void main(String args[]) {
  String s1 = "viettuts is a very good website";
  String replaceString = s1.replaceAll("t", "j"); //thay the "a" thanh "e"  
  System.out.println(replaceString);
 }
}
//Output:

viejjujs is a very good websije

---------------------------------------------------------

//Phương thức split trong Java String
//Phương thức split() tách chuỗi này theo biểu thức chính quy(regular expression) và trả về mảng chuỗi.

//Phương thức:
public String split(String regex)
public String split(String regex, int limit)
/////////////////////////////////////////////////////////////

public class SplitExample {
 public static void main(String args[]) {
  String s1 = "java string split method by viettuts";
  String[] words = s1.split("\\s");//tach chuoi dua tren khoang trang
  //su dung vong lap foreach de in cac element cua mang chuoi thu duoc
  for (String w : words) {
   System.out.println(w);
  }
 }
}
//Output:

java
string
split
method
by
viettuts

---------------------------------------------------------
public class SplitExample2 {
 public static void main(String args[]) {
  String s1 = "welcome to split world";
  System.out.println("returning words 1:");
  for (String w : s1.split("\\s", 0)) {
   System.out.println(w);
  }
  System.out.println("returning words 2:");
  for (String w : s1.split("\\s", 1)) {
   System.out.println(w);
  }
  System.out.println("returning words 3:");
  for (String w : s1.split("\\s", 2)) {
   System.out.println(w);
  }
 }
}
//Output:

returning words 1:
welcome
to
split
world
returning words 2:
welcome to split world
returning words 3:
welcome
to split world


--------------------------------------------------------------
//Phương thức startsWith trong Java String
//Phương thức startsWith() được sử dụng để kiểm tra tiền tố của chuỗi có khớp với giá trị tiền tố đã nhập không, nếu đúng trả về true, sai trả về false.

public class StartsWithExample {
 public static void main(String args[]) {
  String s1 = "java string startsWith() method sample";
  System.out.println(s1.startsWith("ja"));
  System.out.println(s1.startsWith("java string"));
 }
}
//Output:

true
true

--------------------------------------------------------------
//Phương thức subString trong Java String
//Phương thức subString() trả về chuỗi con của một chuỗi.

//Chúng ta truyền chỉ số bắt đầu và chỉ số kết thúc cho phương thức subString(), với chỉ số bắt đầu tính từ 0 và chỉ số kết thúc tính từ 1.

public String substring(int startIndex, int endIndex)

public class SubstringExample {
 public static void main(String args[]) {
  String s1 = "hellojava";
  System.out.println(s1.substring(3, 7));// "loja"  
  System.out.println(s1.substring(3));// "lojava"  
 }
}
//Output:

loja
lojava


--------------------------------------------------------------

//Phương thức toCharArray trong Java String
//Phương thức toCharArray() được sử dụng để chuyển đổi chuỗi thành các mảng ký tự. Nó trả về một mảng ký từ có độ dài tương đương độ dài của chuỗi.

public class StringToCharArrayExample {
 public static void main(String args[]) {
  String s1 = "hello";
  char[] ch = s1.toCharArray();
  for (int i = 0; i < ch.length; i++) {
   System.out.println(ch[i]);
  }
 }
}
//Output:

h
e
l
l
o

--------------------------------------------------------------

//Phương thức toLowerCase trong Java String
//Phương thức toLowerCase() được sử dụng để chuyển chuỗi về dạng chữ thường.
//Phương thức toLowerCase() hoạt động giống y chang phương thức toLowerCase(Locale.getDefault()). Nó sử dụng locale mặc định.

public class StringLowerExample {
 public static void main(String args[]) {
  String s1 = "HELLO stRIng";
  String s1lower = s1.toLowerCase();
  System.out.println(s1lower);
 }
}
//Output:

hello string

--------------------------------------------------------------
//Phương thức toUpperCase trong Java String
//Phương thức toUpperCase() được sử dụng để chuyển chuỗi về dạng chữ hoa.
//Phương thức toUpperCase() hoạt động giống y chang phương thức toUpperCase(Locale.getDefault()). Nó sử dụng locale mặc định.

public class StringLowerExample {
 public static void main(String args[]) {
  String s1 = "HELLO stRIng";
  String s1Upper = s1.toUpperCase();
  System.out.println(s1Upper);
 }
}
//Output:

HELLO STRING

--------------------------------------------------------------
//Phương thức trim trong Java String
//Phương thức trim() được sử dụng để xóa khoảng trẳng ở đầu và cuối chuỗi. Giá trị unicode của khoảng trắng là '\u0020'. Phương thức trim() kiểm tra giá trị unicode trước và sau chuỗi, nếu tồn tại thì xóa bỏ khoảng trắng đi và trả về chuỗi không có khoảng trắng ở đầu và cuối.

public class StringTrimExample {
 public static void main(String args[]) {
  String s1 = "  hello string   ";
  System.out.println(s1 + "java"); 
  System.out.println(s1.trim() + "java");
 }
}
//Output:

  hello string   java
hello stringjava

--------------------------------------------------------------

//Phương thức valueOf trong Java String
//Phương thức valueOf() được sử dụng để chuyển đối kiểu dữ liệu khác thành chuỗi. Bằng việc sử dụng phương thức valueOf(), bạn có thể chuyển int thành chuỗi, long thành chuỗi, boolean thành chuỗi, float thành chuỗi, double thành chuỗi, char thành chuỗi, mảng char thành chuỗi, đối tượng thành chuỗi.

public class StringValueOfExample {
 public static void main(String args[]) {
  int value = 30;
  String s1 = String.valueOf(value);
  System.out.println(s1 + 10);
 }
}
//Output:

3010
```

## **Array-Các hàm có sẵn**

```java
//Tạo một mảng trong Java
//Để khai báo một mảng, khai báo loại biến với dấu ngoặc vuông []:

dataType[] arr;
dataType []arr; 
dataType arr[];  

String[] cars = { "Honda", "BMW", "Ford", "Mazda" };
Để tạo một mảng các số nguyên, bạn có thể viết:
int[] myNum = { 10, 20, 30, 40 };

------------------------------------------------------------------
//Truy cập các phần tử của một mảng trong Java
//Bạn truy cập một phần tử mảng bằng cách sử dụng số chỉ mục (index).

//Ví dụ:


package vn.viettuts.array;
 
public class TruyCapArray1 {
    public static void main(String[] args) {
        String[] cars = { "Honda", "BMW", "Ford", "Mazda" };
        System.out.println(cars[0]);
    }
}
Kết quả:

Honda
----------------------------------------------------
//Duyệt các phần tử của mảng trong Java
//Có 2 các để duyệt các phần tử của mảng:

- Sử dụng vòng lặp for
- Sử dụng foreach




package vn.viettuts.array;
 
public class DuyetArray1 {
    public static void main(String[] args) {
        String[] cars = { "Honda", "BMW", "Ford", "Mazda" };
        for (int i = 0; i < cars.length; i++) {
            System.out.println(cars[i]);
        }
    }
}
Kết quả:

Honda
BMW
Ford
Mazda

//Sử dụng foreach

package vn.viettuts.array;
 
public class DuyetArray2 {
    public static void main(String[] args) {
        String[] cars = { "Honda", "BMW", "Ford", "Mazda" };
        for (String car : cars) {
            System.out.println(car);
        }
    }
}
Kết quả:

Honda
BMW
Ford
Mazda
------------------------------------------------------

//Sắp xếp mảng
//Có nhiều phương thức mảng có sẵn, ví dụ Sort(), sắp xếp một mảng theo thứ tự bảng chữ cái hoặc theo thứ tự tăng dần, ví dụ:


package vn.viettuts.array;
 
import java.util.Arrays;
 
public class DuyetArray2 {
    public static void main(String[] args) {
        String[] cars = { "Honda", "BMW", "Ford", "Mazda" };
        // sap xep mangr cars theo thu tu tang dan
        Arrays.sort(cars);
        System.out.println("Mảng cars sau khi được sắp xếp:");
        for (String car : cars) {
            System.out.println(car);
        }
    }
}
Kết quả:

Mảng cars sau khi được sắp xếp:
BMW
Ford
Honda
-----------------------------------------------------
//Sao chép một mảng trong java
//Chúng ta có thể sao chép một mảng tới mảng khác bởi phương thức arraycopy của lớp System. Cú pháp của phương thức arraycopy:


public static void arraycopy(  
Object src, int srcPos,Object dest, int destPos, int length  
)  
//Ví dụ về sao chép mảng trong java


public class TestArrayCopyDemo {
    public static void main(String[] args) {
        char[] copyFrom = { 'd', 'e', 'c', 'a', 'f', 
                'f', 'e', 'i', 'n', 'a', 't', 'e', 'd' };
        char[] copyTo = new char[7];
 
        System.arraycopy(copyFrom, 2, copyTo, 0, 7);
        System.out.println(new String(copyTo));
    }
}
Kết quả:

caffein

--------------------------------------------------------
//Mảng hai chiều và đa chiều trong Java
//Trong TH này, dữ liệu được lưu trữ theo hàng và cột theo chỉ mục (hay còn gọi là dạng ma trận).

Khai báo mảng đa chiều trong java

dataType[][] arr;
dataType [][]arr;
dataType arr[][];
dataType []arr[];   

//Ví dụ về khởi tạo và gán giá trị cho mảng đa chiều trong java
int[][] arr=new int[3][3]; // 3 hàng 3 cột
arr[0][0]=1;  
arr[0][1]=2;  
arr[0][2]=3;  
arr[1][0]=4;  
arr[1][1]=5;  
arr[1][2]=6;  
arr[2][0]=7;  
arr[2][1]=8;  
arr[2][2]=9;  
//Ví dụ khai báo và khởi tạo mảng đa chiều trong java

public class TestArray3 {
    public static void main(String args[]) {
 
        // khai báo và khởi tạo mảng 2 chiều
        int arr[][] = { { 1, 2, 3 }, { 2, 4, 5 }, { 4, 4, 5 } };
 
        // in mảng 2 chiều r màn hình
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();
        }
 
    }
}
Kết quả:

1 2 3 
2 4 5 
4 4 5 
//Ví dụ cộng 2 ma trận (mảng đa chiều) trong Java

package vn.viettuts.array;
 
public class CongMaTran {
    public static void main(String[] args) {
        // tao hai ma tran
        int a[][] = { { 1, 3, 4 }, { 3, 4, 5 } };
        int b[][] = { { 1, 3, 4 }, { 3, 4, 5 } };
 
        // tao ma tran khac de luu giu ket qua phep cong hai ma tran
        int c[][] = new int[2][3];
 
        // cong va in tong hai ma tran
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                c[i][j] = a[i][j] + b[i][j];
                System.out.print(c[i][j] + " ");
            }
            System.out.println();
        }
    }
}
Kết quả:

2 6 8 
6 8 10 
```

- [**CÁC HÀM CÓ SẴN TRONG ARRAY**](https://www.geeksforgeeks.org/array-class-in-java/?ref=lbp)

## **JAVA Collection Framework**

![](./img_java/Screenshot%202023-08-14%20235943.png)

![](./img_java/Screenshot%202023-08-15%20000052.png)

![](./img_java/Screenshot%202023-08-15%20000132.png)

![](./img_java/Screenshot%202023-08-15%20000153.png)

- [**Tài liệu JAVA Collection**](https://www.geeksforgeeks.org/java-collection-tutorial/?ref=lbp)

## **[JAVA-I/O](https://viettuts.vn/java-io)**

![](./img_java/Screenshot%202023-08-15%20002753.png)

## **Tìm hiểu về cửa sổ chương trình JFrame**


- Trục tọa độ: 

![](./img_java/Screenshot%202023-08-15%20091227.png)

- Những phương thức cơ bản:

![](./img_java/Screenshot%202023-08-15%20091436.png)

```java
package com.mycompany.view;

import javax.swing.JFrame;
import jdk.jshell.JShell;

public class View {
    
    public static void main(String[] args) {
        JFrame jf = new JFrame();
        jf.setVisible(true);
        jf.setTitle("LẬP TRÌNH JAVA");
        jf.setSize(600, 400);
        jf.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```

> `Các thành phần và bố cục của chương trình giao diện`

![](./img_java/Screenshot%202023-08-15%20093114.png)

![](./img_java/Screenshot%202023-08-15%20093723.png)
![](./img_java/Screenshot%202023-08-15%20093802.png)
![](./img_java/Screenshot%202023-08-15%20103342.png)
![](./img_java/Screenshot%202023-08-15%20103509.png)
![](./img_java/Screenshot%202023-08-15%20103524.png)
![](./img_java/Screenshot%202023-08-15%20103547.png)

> `Cách sử dụng JPanel và cấu hình Look and Feel cho giao diện chương trình Java`

![](./img_java/Screenshot%202023-08-15%20132132.png)

```java
package com.mycompany.view;

import java.awt.BorderLayout;
import java.awt.FlowLayout;
import java.awt.GridLayout;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.JTextField;

public class View {

    public static void main(String[] args) {
        JFrame jf = new JFrame();
        jf.setTitle("LẬP TRÌNH JAVA");
        jf.setSize(300, 300);
        jf.setLocationRelativeTo(null);
        jf.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JTextField jTextField = new JTextField(20);

        JPanel jPanel_head = new JPanel();
        jPanel_head.add(jTextField);

        JButton jButton_0 = new JButton("0");
        JButton jButton_1 = new JButton("1");
        JButton jButton_2 = new JButton("2");
        JButton jButton_3 = new JButton("3");
        JButton jButton_4 = new JButton("4");
        JButton jButton_5 = new JButton("5");
        JButton jButton_6 = new JButton("6");
        JButton jButton_7 = new JButton("7");
        JButton jButton_8 = new JButton("8");
        JButton jButton_9 = new JButton("9");
        JButton jButton_cong = new JButton("+");
        JButton jButton_tru = new JButton("-");
        JButton jButton_nhan = new JButton("*");
        JButton jButton_chia = new JButton("/");
        JButton jButton_bang = new JButton("=");

        JPanel jPanel_button = new JPanel();
        jPanel_button.setLayout(new GridLayout(5, 3));

        jPanel_button.add(jButton_0);
        jPanel_button.add(jButton_1);
        jPanel_button.add(jButton_2);
        jPanel_button.add(jButton_3);
        jPanel_button.add(jButton_4);
        jPanel_button.add(jButton_5);
        jPanel_button.add(jButton_6);
        jPanel_button.add(jButton_7);
        jPanel_button.add(jButton_8);
        jPanel_button.add(jButton_9);
        jPanel_button.add(jButton_cong);
        jPanel_button.add(jButton_tru);
        jPanel_button.add(jButton_nhan);
        jPanel_button.add(jButton_chia);
        jPanel_button.add(jButton_bang);

        jf.setLayout(new BorderLayout());
        jf.add(jPanel_head, BorderLayout.NORTH);
        jf.add(jPanel_button, BorderLayout.CENTER);
        jf.setVisible(true);
    }
}
```

> `Áp dụng mô hình MVC trong xây dựng chương trình và cách xử lý sự kiện - Trong CODE`

> `Cách sử dụng JRadioButton và JCheckbox để lựa chọn trong Java Swing`

> `Cách sử dụng JCombobox và JList trong Java Swing`
 