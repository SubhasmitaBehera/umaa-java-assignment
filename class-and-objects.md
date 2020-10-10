# Question:1

* Example with code to show state and behaviour of an object where behaviour depends upon the state of object?

***Answer:***

```java
class Student {
    int rollno;
    String name;
    String course;
    String address;

    Student(int rollno, String name, String course) {
        this.rollno = rollno;
        this.name = name;
        this.course = course;
        this.studentAdd(this);
    }

    void studentAdd(Student stu) {
        stu.name = this.name;
        this.address = "Bhubaneswar";
        System.out.println("Student name is : " + stu.name);
        System.out.println("Student rollno is : " + this.rollno);
        System.out.println("Student course is : " + this.course);
        System.out.println("Student address is : " + this.address);

    }
}

class StudentID {
    public static void main(String args[]) {
        Student s1 = new Student(111, "Ankit", "MCA");
        Student s2 = new Student(112, "Sumit", "CS");
        s1.studentAdd(s1);
    }
}
```

***Output:***

* Student name is : Ankit
* Student rollno is : 111
* Student course is : MCA
* Student address is : Bhubaneswar
* Student name is : Sumit
* Student rollno is : 112
* Student course is : CS
* Student address is : Bhubaneswar
* Student name is : Ankit
* Student rollno is : 111
* Student course is : MCA
* Student address is : Bhubaneswar

# Question:2

* What is the definition of hashcode as per java 8 document?

***Answer:***

## public int hashCode()

* This method is supported for the benefit of hash tables such as those provided by HashMap.
* If two objects are equal according to the equals(Object) method, then calling the hashCode method on each of the two objects must produce the same integer result.
* Whenever it is invoked on the same object more than once during an execution of a Java application, the hashCode method must consistently return the same integer, provided no information used in equals comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
* It is not required that if two objects are unequal according to the equals(java.lang.Object) method, then calling the hashCode method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.
* As much as is reasonably practical, the hashCode method defined by class Object does return distinct integers for distinct objects.
* Returns a hash code value for the object.
 
# Question:3

* What is the fully qualified name of Object class in java ?

***Answer:***

The fully qualifued class name of Object Class in java is ( java.lang.Object ).

# Question:4

* Object class is in which package ?

***Answer:***

Object class is in (java.lang) package.

# Question:5

Find the output?

```java
public class Test
{
  public static void main(String[] args)
  {
    Object obj1 = new Object();
    Object obj2 = new Object();
    System.out.println(obj1.hashCode() == obj2.hashCode());
    System.out.println(obj1.getClass());
    System.out.println(obj1 == obj2);
  }
}
```
***Output:***

* false
* class java.lang.Object
* false

***Explanation:***

* Two different objects have different hashcode , so that output comes false.
* getClass() method returns the native class of the object.Here native class name of obj1 is class java.lang.Object.
* == operation compare the memory location of objects.Here the memory locations of obj1 and obj2 are different.So that the output comes false.

# Question:6

Find the output?

```java
public class Test {
    int x;
    public Test(int x){
        this.x = x;
    }
    public static void main(String[] args) {
        Test t = new Test(10);
        System.out.println(t.x);
    }
}
```

***Output:***

* 10

***Explanation:***

* Here the one argument constuctor is automatically called ,when we create an object and the argument is given 10. So 10 assigned to x and the output comes 10.

# Question:7

Why below code will not compile? What is the fix we have to do so that the code will compile.

```java
public class Test {
    int x;
    public Test(int x){
        this.x = x;
    }
    public static void main(String[] args) {
        Test t = new Test();
        System.out.println(t.x);
    }
}
```

***Answer:***
* The above code won't compile cause the user defined constructor has one argument where as there is no argument passed when we called the constructor.
* If we pass one integer argument in the constructor invoking part, the code will compile.

# Question:8

Will below code will compile?

```java
public class Test {
    int x;
    public Test(int x){
        this.x = x;
    }
    public Test()
    {
        
    }
    public static void main(String[] args) {
        Test t = new Test();
        System.out.println(t.x);
    }
}
```

***Answer:***
* Yes, the above code will compile .The output will be 0 cause we haven't assign x in non-parameterized constructor and the default value of x will be 0.

# Question:9

Find the output?

```java
public class Test {
    int x;
    String y;
    public static void main(String[] args) {
        Test t = new Test();
        System.out.println(t.x);
        System.out.println(t.y);
    }
}
```

***Output:***

* 0
* null

***Explanation:***

* We haven't assign to x and y. The default value of x will be 0 cause x is int type and y will be null cause y is String type.

# Question:10

What is the default value of int , String variables ?

***Answer:***

Default value of int is 0 and default value of String is null.

# Question:11

Find the output?

```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        this.x = x;
        this.y = y;
        Test tVar = this;
        System.out.println(tVar.hashCode() == this.hashCode());
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }
}
```

***Output:***

* true
* 10
* john

***Explanation:***

* Here 'this' is assigned to tVar, so both will share same hashCode.So that output will come true.
* In the constructor invoking part 10 is passed for x so the value of t.x will be 10 and john is passed for y so the value of t.y will be john.
* Here x and y are non-static variable, so we call them through object t.

# Question:12

Find the output?

```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        this.x = x;
        this.y = y;
        m1(this);
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }
    
    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```

***Output:***

* 100
* Doe

***Explanation:***

* Here [m1(this);] invoked m1 method and the field value x updated '10' to '100' and field value of y updated "john" to "Deo".


# Question:13

Find the output?

```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        this.x = x;
        this.y = y;
        this.m1(this);
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x == 10);
        System.out.println(t.y == "john");
    }

    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```

***Output:***

* false
* false

***Explanation:***

* The value of t.x is '100' so t.x==10 is false and the value of t.y is "Doe" so t.y=="john" is also false.

# Question:14

Find the output?

```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        x = x;
        y = y;
        this.m1(this);
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }

    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```

***Output:***

* 100
* Doe

***Explanation:***

* Here, x = x and y = y won't modify the field value but m1(this) will update the field value x and y to '100' and "Doe" respectively.

# Question:15

Find the output?

```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        x = x;
        y = y;
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }

    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```

***Output:***

* 0
* null

***Explanation:***

* Here, x = x and y = y won't modify the field value, so the value of fields will be default.

# Question:16

Find the output?

```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        x = x;
        y = y;
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        Test t1 = t;
        System.out.println(t1 == t);
        t1.x = 300;
        t1.y = "alex";
        System.out.println(t.x);
        System.out.println(t.y);
    }
}
```

***Output:***

* true
* 300
* alex

***Explanation:***

*  Here, object 't' is assigned to 't1' so both share same memory location and field. So the output is true.
* 300 and "alex" is assigned to t1.x and t1.y respecively . Because of t1 and t share same field value so the value of t.x and t.y will be 300 and alex respectively.

# Question:17

Identify State & Behaviour. Find where the state is used. Does behavour depends on the state?

```java
public class Calculator
{
   private int i;
   private int j;
   
   public Calculator(int i, int j)
   {
     this.i = i;
     this.j = j;
   }
   
   public int sum()
   {
     return i + j;
   }
}
```

***Answer:***

* Here i and j are State.
* int sum() is Behaviour .
* State is used in int sum() method and returns the sum of i and j but the return value is not used.
* Yes Behaviour depends on the State.

# Question:18

Find the output? Identify the static method & variables.

```java
public class Test
{
  static int x;
  int y;
  static{
    x = 10;
  }
  
  static{
    x = x + 20;
  }
  
  {
    y = 100;
  }
  
  {
    y = y + 20;
  }
  
  public static void main(String[] args)
  {
    Test t = null;
    t.x = t.x + 40;
    x = x + 50;
    
    t = new Test();
    t.y = t.y + 200;
    
    Test t1 = new Test();
    System.out.println(t.x);
    System.out.println(t1.x);
    System.out.println(Test.x);
    
    System.out.println(t.y);
    System.out.println(t1.y);
   
   System.out.println(t.getX());
   System.out.println(t1.getX());
   System.out.println(Test.getX());
   
   System.out.println(t.getSum());
   System.out.println(t1.getSum());
   
  }
  
  public static int getX()
  {
    return x;
  }
  
  public int getSum()
  {
    return  x + y;
  }
}
```

***Output***

* 120
* 120
* 120
* 320
* 120
* 120
* 120
* 120
* 440
* 240

***Explanation:***

If a field is static then any change to the field value will update the value to the last modified value. As static does not depend on the instance of the class so for any object the value will be the same

***Answer:***

Here, static methods are getX and main method. Static variable is x.

# Question:19

Write some code to create Null Pointer Exception.

***Program:***

```java
public class Test {
    void m1(){
        System.out.println("Statement inside method m1...");
    }
    public static void main(String[] args) {
        Test obj = null;
        obj.m1(); // In this line nullPointerException of  java.lang.NullPointerException class occurs.
    }
}
```



