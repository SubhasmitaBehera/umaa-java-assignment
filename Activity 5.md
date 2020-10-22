# Qyestion 1

Code example of inheritance. Reuse static/non-static method(s) & static/non-static variable(s).

***Program:***

```java

```

***Output:***


# Qusetion 2

Code example of instance of operator using classes as BaseParent->Parent->Child.

***Program:***

```java

```

***Output:***


# Qusetion 3

Code example of super constructor.

***Program:***

```java

```

***Output:***



# Qusetion 4

Does multiple object created in inheritance hierarchy.

***Answer:***


# Qusetion 5

Does super constructor invocation creates one more object.

***Answer:***


# Qusetion 6

Code example of method hiding.

***Program:***

```java

```

***Output:***


# Qusetion 7

Code example of variable hiding.

***Program:***

```java

```

***Output:***


# Qusetion 8

Does static methods overridden.

***Answer:***


# Qusetion 9

Deos private methods overriden.

***Answer:***


# Qusetion 10

By default any class extends which class.

***Answer:***


# Qusetion 11

List down the public/protected (inherited) methods present in java.lag.Object class.

***Answer:***


# Qusetion 12

Find the output:

```java
class A
{
  public int i = 10;
  public int j = 20;
}
class B extends A
{
   public int i = 100;
   public int sumValue(int x)
   {
      return x + this.i + this.j +  super.i + super.j;
   }
}

class Test
{
  public static void main(String[] args)
  {
    A a = new B();
    int result = a.sumValue(a.i);
    System.out.println(result);
  }

}
```

***Output:***


***Explanation:***


# Qusetion 13

Fix the code with all the approaches you know.

```java
class A
{
  private int i;
  public A(int i)
  {
     this.i = i;
  }
}

class B extends A
{
   public B()
   {
   
   }
}
```
***Fixed program:***

```java

```
***Output:***

