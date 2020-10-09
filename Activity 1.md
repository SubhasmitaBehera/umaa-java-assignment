# Activity 1 : Blocks
***Qustion:***
* Define a class called Test.java
* Add main method.
* Write System.out.println statement inside method with some message.
* Define 2 static blocks with some statements inside it.
* Define 2 static blocks with some staement inside it.
* Create object of Test class inside main method using new. Run the Test class. See the output.

***Program:***

```java

public class Test {
    static {
        System.out.println("Statement inside 1st Static block...");
    }

    static {
        System.out.println("Statement inside 2nd Static block...");
    }

    {
        System.out.println("Statement inside 1st Non-Static block...");
    }

    {
        System.out.println("Statement inside 2nd Non-Static block...");
    }

    public static void main(String[] args) {
        System.out.println("Statement inside the Main Method...");
        new Test();
    }
}
```
***Output:***

* Statement inside 1st Static block...
* Statement inside 2nd Static block...
* Statement inside the Main Method...
* Statement inside 1st Non-Static block...
* Statement inside 2nd Non-Static block...

# Activity 2 : Static Methods

***Question:***
* Define a class called Test.java
* Define main method.
* Define 2 static methods called as m1() and m2() with both having void return type. Add some statements in both of the methods.
* Call m1() from m2()
* From main method call m1() without creating object.
* Add a static block. call m1() from static block without using object. verify the output.

***Program:***

```java

public class Test {
    static{
        System.out.println("This is Static block...");
        m1();
    }

    static void  m1(){
        System.out.println("Statement inside Static method m1()...");
    }
    static void m2(){
        System.out.println("Statement inside Static method m2()...");
        m1();
    }
    public static void main(String[] args) {
        System.out.println("This is Main method...");
        m1();
    }
}
```

***Output:***
* This is Static block...
* Statement inside Static method m1()...
* This is Main method...
* Statement inside Static method m1()...

# Activity 3 : Non Static Methods

***Question:***
* Define a class called Test.java
* Define main method.
* Define 2 non-static methods called as m1() and m2() with both having void retunr type. Ass some statements in both of the methods.
* Call m1() from m2().
* Inside main method create object of Test using new. Test var = new Test().
* Using above reference variable of Test call m1()
* Add a non static block. call m1() from non static block. verify the outout.

***Program:***
```java
public class Test {
    {
        System.out.println("This is Non-Static block...");
        m1();
    }

    void  m1(){
        System.out.println("Statement inside method m1()...");
    }
    void m2(){
        System.out.println("Statement inside method m2()...");
        m1();
    }
    public static void main(String[] args) {
        System.out.println("This is Main method...");
        Test var = new Test();
        var.m1();

    }
}
```
***Output:***

* This is Main method...
* This is Non-Static block...
* Statement inside method m1()...
* Statement inside method m1()...

# Activity 4 : Parameterized Methods

***Question:***

* Define a class called Test.java
* Define a main method.
* Create a static method sum(int x, int y) and having return type as int. This should give sum of x + y
* Call sum(10, 20) from main method and print the result inside main method

***Program:***

```java
public class Test {
    static int sum(int x, int y) {
        return x + y;
    }
    
    public static void main(String[] args) {
        System.out.println("This is Main method...");
        int res = sum(10, 20);
        System.out.println("Sum of 10 and 20 is " + res);
    }
}
```
***Output:***
* This is Main method...
* Sum of 10 and 20 is 30

# Activity 5 : Variable Declaration

***Question:***
* You may see compilation error with this activity. Define a class called Test.java
* Define a main method.
* Declare a static variable x of type int at the class level. Declare a non static varaible y of type String at the class level. Run the class. Verify output.
* Define a static block. print the value of x & y inside static block. Run the class. Verify output.
* Define a non-static block. print the value of x & y inside non-static block. Run the class. Verify output.
* Define a static method m1() with void return type. print the value of x & y inside static method. Run the class. Verify output.
* Define a non-static method m2() with void return type. print the value of x & y inside non-static method. Run the class. Verify output.
* print the value of x & y inside main method. Run the class. Verify output.
* Inside main method create object of Test class using new. Test var = new Test();
* call m2() using the reference variable var. Run the class. Verify output.
* Inside main method call m1() without object. Run the class. Verify output.
* What is the default value for x and y you are getting here?

***Program:***

```java
public class Test {
    static int x;
    public String y;

    static {
        System.out.println("Inside static block x = " + x);
//        System.out.println("Inside static block y = " +y);    //Compile time error :- Non-static field 'y' cann't be referenced from a static context
    }

    {
        System.out.println("Inside non-static block x = " + x);
        System.out.println("Inside non-static block y = " + y);

    }

    static void m1() {
        System.out.println("Inside static method m1 x = " + x);
//        System.out.println("Inside static method m1 y = " +y);  //Compile time error :- Non-static field 'y' cann't be referenced from a static context
    }

    void m2() {
        System.out.println("Inside non-static method m2 x = " + x);
        System.out.println("Inside non-static method m2 y = " + y);
    }


    public static void main(String[] args) {
        System.out.println("This is Main method...");
        System.out.println("Inside Main method x = " + x);
//        System.out.println("Inside Main method y = " +y);   //Compile time error :- Non-static field 'y' cann't be referenced from a static context
        Test var = new Test();
        var.m2();
        m1();

    }
 }
  ```
 ***Output:***
* Inside static block x = 0
* This is Main method...
* Inside Main method x = 0
* Inside non-static block x = 0
* Inside non-static block y = null
* Inside non-static method m2 x = 0
* Inside non-static method m2 y = null
* Inside static method m1 x = 0

# Activity 6 : Variable Declaration & Intialization

***Question:***
* You may see compilation error with this activity. Define a class called Test.java
* Define a main method.
* Declare a static variable x of type int at the class level. Declare a non static varaible y of type String at the class level. Run the class. Verify output.
* Define a static block. Initialize x = 20; and print x. Run the class. Verify output.
* Define a static method m1(). Initialize x = 30; and print x. Run the class. Verify output.
* From the main method call m1() without object. Run the class. Verify output.
* Define a non static block. Initialize y = "hello"; and print y. Run the class. Verify output.
* Define a non static method m2(). Initialize y = "bye"; and print y. Run the class. Verify output.
* Inside main method create object of Test using new. Test var = new Test(); From the main method call var.m2(). Run the class. Verify output.

***Program:***

```java
public class Test {
    static int x;
    public String y;

    static {
        x = 20;
        System.out.println("Inside static block, x = " + x);
    }

    {
        y = "hello";
        System.out.println("Inside non-static block, y = " + y);
    }

    static void m1() {
        x = 30;
        System.out.println("Inside static method m1, x = " + x);
    }

    void m2() {
        y = "bye";
        System.out.println("Inside non-static method m2, y = " + y);
    }

    public static void main(String[] args) {
        m1();
        Test var = new Test();
        var.m2();
    }
}
```
***Output:***
* Inside static block, x = 20
* Inside static method m1, x = 30
* Inside non-static block, y = hello
* Inside non-static method m2, y = bye

# Activity 7 : Final Variables or Constants

***Questions:***
* Define a class called Test.java
* Define a main method.
* Declare a final static variable x of int type. Try to initialize this 2 times.
* Declare a final non static variable y of int type. Try to initialize this 2 times.

***Programs:***

```java
public class Test {
    static final int x = 10;
    public final int y = 20;

    static {
        System.out.println(x);
        Test var = new Test();
        System.out.println(var.y);
    }

    public static void main(String[] args) {
        final int x = 100;
        final int y = 200;
        System.out.println(x);
        System.out.println(y);
    }
}
```
***Output:***
* 10
* 20
* 100
* 200
