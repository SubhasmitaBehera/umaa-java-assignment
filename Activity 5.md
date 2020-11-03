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
public class Test {
    public static void main(String[] args) {
        Child c = new Child();
        Child a = new Child(8);
    }
    public static class Parent {

        public Parent(int age) {
            System.out.println("My(parent) age is "+age);
        }

        public Parent() {
            System.out.println("I am parent...");
        }
    }

    public static class Child extends Parent {
        public Child() {
//            super();
            System.out.println("I am child...");
        }
        public Child(int age){
            super(30);
            System.out.println("My(child) age is "+age);
        }
    }
}

```

***Output:***

* I am parent...
* I am child...
* My(parent) age is 30
* My(child) age is 8



# Qusetion 4

Does multiple object created in inheritance hierarchy.

***Answer:***

No, a single object is created in inheritance hierarchy.

# Qusetion 5

Does super constructor invocation creates one more object.

***Answer:***

No, super constructor invocation does not create one more object.

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

No, static method does not override.

# Qusetion 9

Does private methods overriden.

***Answer:***

No, private method does not override.

# Qusetion 10

By default any class extends which class.

***Answer:***

By default any class extends object class.

# Qusetion 11

List down the public/protected (inherited) methods present in java.lang.Object class.

***Answer:***

## Public:-

* Object()
* equals(Object obj)
* Class<?> getClass()
* hashCode()
* notify()
* notifyAll()
* toString()
* wait()
* wait(long var1) 
* wait(long timeoutMillis, int nanos)

## Protected:-

* clone()
* finalize()

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

