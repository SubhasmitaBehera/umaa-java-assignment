# Question:1
Write a simple example of a Product class where it uses this constructor with paremeterized constructor.

***Program:***

```java

```

# Question:2
Does toString() method present in java.lang.Object class? If yes what the implementaion for toString() method given by java.lang.Object class.

***Answer:***



# Question:3
Override toString() method in the class A (as given below) such that it will print the value of i, j, k.
```java
public class Test {
    public static void main(String[] args) {
        A a = new A(10, 20);
        a.setK(400);
        System.out.println(a);
    }
}

class A {
    private int i;
    private int j;
    private int k;

    public A(int i, int j) {
        this.i = i;
        this.j = j;
    }

    public int getI() {
        return i;
    }

    public void setI(int i) {
        this.i = i;
    }

    public int getJ() {
        return j;
    }

    public void setJ(int j) {
        this.j = j;
    }

    public int getK() {
        return k;
    }

    public void setK(int k) {
        this.k = k;
    }
}
```

***Modified Program:***
```java

```
***Output:***



***Explanation:***



# Question:4

What is StackOverflowError. When it occurs. It comes under which package in java library.

***Answer:***


# Question:5

Will the below code compile? Find the output of the below code.
```java
public class Test {
    public static void main(String[] args) {
        A a = new A();
    }
}

class A
{
    private int x =11;
    public A()
    {
        new A(10);
    }

    public A(int x)
    {
        this();
        this.x = x;
    }
}
```

***Answer:***



***Output:***




***Explanation:***


# Question:6

Will the below code compile. If not why?
```java
class A
{
    private int x =11;
    public A()
    {
        this(10);
    }

    public A(int x)
    {
        this();
        this.x = x;
    }
}
```

***Answer:***



# Question:7

Find the output with explanation.
```java
public class Test {
    public static void main(String[] args) {
        A a = new A();
    }
}

class A
{
    private int x =11;
    public A()
    {
        this(10);
        if(x % 2 == 0)
        {
            System.out.println("even");
        }
        else
        {
            System.out.println("odd");
        }
    }
    
    public A(int x)
    {
        this.x = x;
    }
}
```
***Output:***



***Explanation:***



# Question:8

Will the below code compile?
```java
class A
{
    public A()
    {
        new A();
    }
}
```
***Answer:***



# Question:9

Why the below code won't compile?
```java
class A
{
    public A()
    {
        this();
    }
}
```
***Answer:***



# Question:10

Find the output with explanation?
```java
public class Test {
    public static void main(String[] args) {
        A a = new A();
        System.out.println(a.hashValue == a.hashCode());
    }
}

class A
{
    public int i;
    public int hashValue;
    public A()
    {
        new A(10);
    }

    public A(int x)
    {
        this.i = x;
        this.hashValue = this.hashCode();
    }
}
```
***Output:***



***Explanation:***



# Question:11

Find the output with explanation?
```java
public class Test {
    public static void main(String[] args) {
        A a = new A();
        System.out.println(a.hashValue == a.hashCode());
    }
}

class A
{
    public int i;
    public int hashValue;
    public A()
    {
        this(10);
    }
    
    public A(int x)
    {
        this.i = x;
        this.hashValue = this.hashCode();
    }
}
```
***Output:***



***Explanation:***



# Question:12

Access Modifiers & Packages. Find the compilation errors & why? Find the output also by fixing them.
```java
package com.pkg1;

class A
{
  private int i = 10;
  public int j = 100;
  int k = 50;
}

package com.pkg1;
class B
{
  public static void main(String[] args)
  {
    A a = new A();
	System.out.println(a.i);
	System.out.println(a.j);
	System.out.println(a.k); // why this is accessible?
  }
}

package com.pkg2;
class B
{
  public static void main(String[] args)
  {
    A a = new A();
	System.out.println(a.i);
	System.out.println(a.j);
	System.out.println(a.k); // why this is not accessible?
  }
}
```
***Answer:***



***Modified Program:***
```java

```
***Output:***



***Explanation:***



# Question:13

Why we use getters and setters for a class. Give an example.

***Answer:***



***Example:***
```java

```
***Output:***



***Explanation:***



# Question:14

Why it is good to have private fields with public getters & setters?

***Answer:***





