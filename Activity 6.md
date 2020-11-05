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

* Binary number conversion:-

  1. Take the number modulo base i.e. number % base

  2. Write down the result. i.e. remainder

  3. Divide the number by base i.e. number / base

  4. repeat the process untill the number greater than 0. (number > 0)

* Positive number in binary format:-

  +58 as 8-bit number = (00111010) 
  
  +134 as 9-bit number =(010000110) 
  
  +1122 as 12-bit number =(010001100010) 
  
* Negative number in binary format:-

  -55 as 8-bit number = (10110111) [Signed magnitude]  , (11001000)[Signed 1s complement] ,(11001001)[Signed 2s complement]
  
  -324 as  10-bit number = (1101000100) [Signed magnitude]  ,(1010111011)[Signed 1s complement] ,(1010111100)[Signed 2s complement]
  
  -1001 as 12-bit number = (101111101001) [Signed magnitude]  , (110000010110  )[Signed 1s complement] ,(110000010111)[Signed 2s complement]
  
* Floating number in binary format:-


  

# Question:4

convert between primtiive type and wrapper types.

***Answer:***



# Question:5

convert string(decimal value) to long, int, short, byte.

***Answer:***



# Question:6

Understand the wrapper class hierachy. Explain the wrapper child classes for Number class.

***Answer:***



# Question:7

Define auto boxing & auto unboxing with example.

***Answer:***

Autoboxing: Automatic conversion of primitive types to the object of their corresponding wrapper classes is known as autoboxing.
For example – conversion of int to Integer,char to Character, long to Long, double to Double etc.

Unboxing: It is just the reverse process of autoboxing. Automatically converting an object of a wrapper class to its corresponding primitive type is known as unboxing.
For example – conversion of Integer to int,Character to char,Long to long, Double to double etc.

# Question:8

Convert a string ("105") to integer. and print the doubleValue(), longValue(), byteValue(), floatValue(), shortValue(), toString()

***Answer:***




# Question:9

Mention the fully qualified name of each wrapper class.

***Answer:***



# Question:10


Write the class definition for all wrapper class types. Find out the abstract methods peresent in the implemented interface.
(Ex: public final class Float extends Number implements Comparable, Comparable: public int compareTo(T o); ).

***Answer:***







