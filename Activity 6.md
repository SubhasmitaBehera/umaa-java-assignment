# Question:1

1s complement

***Answer:***

To get 1's complement of a binary number, simply invert the given number. For example, 1's complement of binary number 0110100 is 1001011.

# Question:2

2s complement

***Answer:***

To get 2's complement of binary number is 1's complement of given number plus 1 to the least significant bit (LSB).
For example 2's complement of binary number 10100 is (01011) + 1 = 01100.

# Question:3

Represent whole numbers (+ve / -ve ) or float point numbers (+ve / -ve) in binary format.

***Answer:***

* Binary number conversion (positive number):-

  1. Take the number modulo base i.e. number % base

  2. Write down the result. i.e. remainder

  3. Divide the number by base i.e. number / base

  4. repeat the process untill the number greater than 0. (number > 0)

* Positive number in binary format:-

  +58 as 8-bit number = (00111010) 
  
  +134 as 9-bit number =(010000110) 
  
  +1122 as 12-bit number =(010001100010) 
  
* Binary number conversion (negative number):-
  
  1. Fisrt find the binary no of the given number in positive.
  2. Then take 1's complement as discussed above
  3. Then add 1 to it.
  
* Negative number in binary format:-

  -55 as 8-bit number = (10110111) [Signed magnitude]  , (11001000)[Signed 1s complement] ,(11001001)[Signed 2s complement]
  
  -324 as  10-bit number = (1101000100) [Signed magnitude]  ,(1010111011)[Signed 1s complement] ,(1010111100)[Signed 2s complement]
  
  -1001 as 12-bit number = (101111101001) [Signed magnitude]  , (110000010110  )[Signed 1s complement] ,(110000010111)[Signed 2s complement]
  
* Binary number conversion (floating number):-

 1. A floating point number has two parts one is integral part and another one is decimal part.
 
 2. The Conversion of integral part will be the same as discussed above.

 3. To convert the decimal part to binary, multiply fractional part with 2 and take the one bit which appears before the decimal point.
 
 4. Follow the same procedure until it becomes 1.0. alt image

* Floating number in binary format:-

  ***10.75 :-***

  Integral Part:
  10 = (1010) 2

   Fractional Part:

   0.75 * 2 =>1.50 // take 1 and move .50 to next step

   0.50 * 2 =>1.00 // take 1 and stop the process because no remainder

   0.75 = (11) 2


   Combining both integral and fractional:

   10.75 = (1010.11) 2
  

# Question:4

Convert between primtiive type and wrapper types.

***Answer:***

### Primitive Types and	Wrapper Types:-

* int	-> Integer

* char ->	Character

* float ->	Float

* boolean	-> Boolean

* double -> Double

* long	-> Long

* short ->	Short

* byte	-> Byte

# Question:5

convert string(decimal value) to long, int, short, byte.

***Answer:***

```java
public class Test{
    public static void main(String[] args) {
        String str = "105";

        long l = Long.parseLong(str);
        System.out.println("long : "+ l);

        int i =Integer.parseInt(str);
        System.out.println("int :" +i);

        short s = Short.parseShort(str);
        System.out.println("short : " + s);

        byte b = Byte.parseByte(str);
        System.out.println("byte : " +b);

    }
}
```

***Output:***

* long : 105
* int :105
* short : 105
* byte : 105

# Question:6

Understand the wrapper class hierachy. Explain the wrapper child classes for Number class.

***Answer:***

* All primitive wrapper class (Integer , Float , Long , Double , Short , Byte ) extends Number class and implements Comparable, Constable, ConstantDesc.

*  Character  class extends Character class and implements java.io.Serializable, Comparable .

*  Boolean class extends Boolean class and implements java.io.Serializable, Comparable .

* The wrapper child classes of Number class are Integer ,Float , Long , Double , Short and  Byte .

# Question:7

Define auto boxing & auto unboxing with example.

***Answer:***

Autoboxing: Automatic conversion of primitive types to the object of their corresponding wrapper classes is known as autoboxing.
For example – conversion of int to Integer,char to Character, long to Long, double to Double etc.

Unboxing: It is just the reverse process of autoboxing. Automatically converting an object of a wrapper class to its corresponding primitive type is known as unboxing.
For example – conversion of Integer to int,Character to char,Long to long, Double to double etc.

```java
public class Test{
    public static void main(String args[]){
        int a=50;
        Integer a2=new Integer(a);//autoboxing

        Integer a3=5;//autoboxing

        System.out.println(a2+" "+a3);

        Integer i=new Integer(50);
        int b=i;//unboxing

        System.out.println(a);
    }
}
```

***Output:***

* 50 5
* 50

# Question:8

Convert a string ("105") to integer. and print the doubleValue(), longValue(), byteValue(), floatValue(), shortValue(), toString()

***Answer:***

```java
public class Test{
    public static void main(String[] args) {
        String str = "105";

        int i =Integer.parseInt(str);
        System.out.println(i);

        double d = Double.parseDouble(str);
        System.out.println(d);

        long l = Long.parseLong(str);
        System.out.println(l);

        byte b = Byte.parseByte(str);
        System.out.println(b);

        float f = Float.parseFloat(str);
        System.out.println(f);

        short s = Short.parseShort(str);
        System.out.println(s);

        System.out.println(str.toString());
    }
}
```

***Output:***

* 105
* 105.0
* 105
* 105
* 105.0
* 105
* 105


# Question:9

Mention the fully qualified name of each wrapper class.

***Answer:***

*  Numbers : java.lang.Number

*  Boolean : java .lang.Boolean

*  Character : java.lang.Character


# Question:10


Write the class definition for all wrapper class types. Find out the abstract methods peresent in the implemented interface.
(Ex: public final class Float extends Number implements Comparable, Comparable: public int compareTo(T o); ).

***Answer:***

* Integer : public final class Integer extends Number implements Comparable, Constable, ConstantDesc .

* Float : public final class Float extends Number implements Comparable, Constable, ConstantDesc .

* Double : public final class Double extends Number implements Comparable, Constable, ConstantDesc .

* Short : public final class Short extends Number implements Comparable, Constable, ConstantDesc .

* Long : public final class Long extends Number implements Comparable, Constable, ConstantDesc .

* Byte : public final class Byte extends Number implements Comparable, Constable, ConstantDesc .

* Character : public final class extends Character implements java.io.Serializable, Comparable .

* Boolean : public final class extends Boolean implements java.io.Serializable,Comparable .





