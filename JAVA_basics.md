# JAVA Fundamentals
The main() method is the entry point into the application
Basic Structure of a JAVA program
- Functions - methods that execute a job
- Classes - Class is a template, through which object is created
- Static - helps to run a function without creating an object of a class
- Void - does not expect anything in return
- String[] args - arguments that main function receives from input

Naming Conventions
- For classes we use PascalConvention
- For functions we use camelCaseConvention

### Anatomy of a JAVA Program
- #### Document Section (Optional):
  - contains basic information about a JAVA program
  - The information includes the author's name, version, company name, and description of the program written in the form of comments

- #### Package Declaration (Optional)
  - Decalare package name where the class is placed. There can only be one package per JAVA class

- #### Import Statements
  - The package contains the many predefined classes and interfaces. 
  - If we want to use any class of a particular package, we need to import that class. 
  - The import statement represents the class stored in the other package. We use the import keyword to import the class.

- #### Interface Section (Optional)
  - We use the interface keyword to create an interface. An interface is a slightly different from the class. 
  - It contains only constants and method declarations. 
  - Another difference is that it cannot be instantiated. 
  - We can use interface in classes by using the implements keyword. An interface can also be used with other interfaces by using the extends keyword.

- #### Class Definition
  - It is vital part of a Java program. Without the class, we cannot create any Java program. A Java program may contain more than one class definition. 
  - We use the class keyword to define the class. The class is a blueprint of a Java program. It contains information about user-defined methods, variables, and constants. 
  - Every Java program has at least one class that contains the main() method.

- #### Class Variables and Constants
  - We define variables and constants that are to be used later in the program. 
  - In a Java program, the variables and constants are defined just after the class definition. 
  - The variables and constants store values of the parameters. It is used during the execution of the program. 
  - We can also decide and define the scope of variables by using the modifiers.

- #### Main Method Class
  - The execution of all Java programs starts from the main() method. In other words, it is an entry point of the class.
  - It must be inside the class. Inside the main method, we create objects and call the methods.

- #### Methods and Behavior
  - We define the functionality of the program by using the methods. 
  - The methods are the set of instructions that we want to perform. 
  - These instructions execute at runtime and perform the specified task.

### Data Types in JAVA
Variable are of some specific types and that is determined by Data Types. There are 2 different type of data types
- #### Primitive Data Types (8)
  - byte: 
    - takes -128 to 127 values
    - Takes one byte
    - default value is 0
  - short
    - Value ranges from -(2^16)/2 to (2^16)/2 - 1
    - Takes 2 bytes
    - default is 0
  - int
    - Value ranges from -(2^32)/2 to (2^32)/2 - 1
    - Takes 4 bytes
    - default is 0
  - float
    - See in documentation (https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)
    - Takes 8 bytes
    - default is 0.0f
  - long
    - Value ranges from -(2^64)/2 to (2^64)/2 - 1
    - Takes 8 bytes
    - default is 0
  - char
    - Value ranges from 0 to 65,535
    - Takes 2 bytes
    - default is '\u0000'
  - double
    - See in documentation (https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)
    - Takes 8 bytes
    - default is 0.0d
  - bool
    - True or False

- #### Non Primitive Data Types
  - TODO

### Literals
- In order to chose the data type we first need to find the type of data we want to store. After that we need to analyze the MIN & MAX value we might use.
- A constant value which can be assigned to the variable is literal
- the value on the right side of equal to while declaration is literal
- A constant value that can be assigned to the variable is called a literal. 
  - 101 – Integer literal 
  - 10.1f – float literal 
  - 10.1 – double literal (default type for decimals)
  - ‘A’ – character literal 
  - true – Boolean literal 
  - “Kalra” – String literal

### Keywords
- Words that are reserved and used by the Java compiler. They cannot be used as an Identifier.

### Scanner Class
- Scanner class of java.util package is used to take input from the user's keyboard.
- The Scanner class has many methods for taking input from the user depending upon the type of input. 
- To use any of the methods of the Scanner class, first, we need to create an object of the Scanner class
```
import java.util.Scanner;  // Importing  the Scanner class
Scanner sc = new Scanner(System.in);  //Creating an object named "sc" of the Scanner class.

Scanner S = new Scanner(System.in);  //(Read from the keyboard)
int a = S.nextInt();  //(Method to read from the keyboard)
```

### Operators
An operator is a symbol that the compiler to perform a specific operation on operands.
- #### Arithmetic Operators:
  - Arithmetic operators are used to perform mathematical operations such as addition, division, etc on expressions. 
  - Arithmetic operators cannot work with Booleans. 
  - % operator can work on floats and doubles.
  - +,-,*,/,%,++,--

- #### Comparison Operators:
  - these operators are used to compare two operands.
  - ==, !=, >, <, >=, <=

- #### Logical Operators:
  - These operators determine the logic in an expression containing two or more values or variables.
  - &&, ||, !

- #### Bitwise Operators:
  - These operators perform the operations on every bit of a number.
  - &,|,^,<<,>>

#### Resulting data type after arithmetic operation
- Result = byte + short -> integer 
- Result = short + integer -> integer 
- Result = long + float -> float 
- Result = integer + float -> float 
- Result = character + integer -> integer 
- Result = character + short -> integer 
- Result = long + double -> double 
- Result = float + double -> double

### Strings
- A string is a sequence of characters. Strings are objects that represent a char array.
- ```
  char[] str = {'K','A','L','R','A'};
  String s = new String(str);
  // We can also do
  String s = "KALRA";
- Strings are immutable and cannot be changed. 
- java.lang.String class is used to create a String object.
- The string is a class but can be used as a data type.

#### Different ways to create a string in Java:
- <b>By using string literal</b>
  - use double quotes("") to create string using string literal. 
  - Before creating a new string instance, JVM verifies if the same string is already present in the string pool or not. If it is already present, then JVM returns a reference to the pooled instance otherwise, a new string instance is created.
- <b>By using the new</b>
  - When we create a string using "new", a new object is always created in the heap memory.
```
String str1 = "CodeWithHarry";
String str2 = "CodeWithHarry"
System.out.println(str1 == str2); // True

String str1 = new String("Keep coding"); 
String str2 = new String("Keep coding""); 
System.out.println(str1 == str2); // False

```
Although the value of both the string object is the same, still false is displayed as output because str1 and str2 are two different string objects created in the heap. That's why it is not considered a good practice two compare two strings using the == operator. <i>Always use the equals() method to compare two strings in Java.</i>

#### String Methods
Method	Description
1. length(): Returns the length of String name. (5 in this case)
2. toLowerCase(): Converts all the characters of the string to the lower case letters.
3. toUpperCase(): Converts all the characters of the string to the upper case letters.
4. trim(): Returns a new String after removing all the leading and trailing spaces from the original string.
5. substring(int start): Returns a substring from start to the end. Substring(3) returns “ra”. [Note that indexing starts from 0]
6. substring(int start, int end): Returns a substring from the start index to the end index. The start index is included, and the end is excluded.
7. replace(‘r’, ‘p’): Returns a new string after replacing r with p. Kalpa is returned in this case. (This method takes char as argument)
8. startsWith(“Ka”): Returns true if the name starts with the string “Ka”. (True in this case)
9. endsWith(“ra”): Returns true if the name ends with the string “ra”. (True in this case)
10. charAt(2): Returns the character at a given index position. (r in this case)
11. indexOf(“s”): Returns the index of the first occurrence of the specified character in the given string.
12. lastIndexOf(“r”): Returns the last index of the specified character from the given string. (3 in this case)
13. equals(“Kalra”): Returns true if the given string is equal to “Kalra” false otherwise [Case sensitive]
14.equalsIgnoreCase(“kalra”): Returns true if two strings are equal, ignoring the case of characters.

### If-else Statements
If-else block is used to check conditions and execute a particular section of code for a specific condition.

### Switch Case Statements
- Switch-Case is used when we have to make a choice between the number of alternatives for a given variable.
- Variable can be an integer, character, or string in Java.
- Every switch case must contain a default case. The default case is executed when all the other cases are false.
- Never forget to include the <strong>break</strong> statement after every switch case otherwise the switch case will not terminate.

### Loops
- #### while loop
- #### do-while Loop
  - Do- while loop is similar to a while loop except for the fact that it is guaranteed to execute at least once. 
  - Use a do-while loop when the exact number of iterations is unknown, but you need to execute a code block at least once. 
  - After executing a part of a program for once, the rest of the code gets executed on the basis of a given boolean condition.
  - ```
    int i=1;  
    do{  
      System.out.println(i);  
      i++;  
    }while(i<=10);
    
  - <strong>Difference Between while loop and do-while loop:</strong>
    - while – checks the condition & executes the code. 
    - do-while – executes the code at least once and then checks the condition. Because of this reason, the code in the do-while loop executes at least once, even if the condition fails.
- #### for loop

#### Break and Continue in Java
- #### Break statement:
  - The break statement is used to exit the loop irrespective of whether the condition is true or false. 
  - Whenever a ‘break’ is encountered inside the loop, the control is sent outside the loop.
- #### Continue statement:
  - The continue statement is used to immediately move to the next iteration of the loop. 
  - The control is taken to the next iteration thus skipping everything below ‘continue’ inside the loop for that iteration.

### Arrays
- An array is a collection of similar types of data having contiguous memory allocation.
- The size of the array can not be increased at run time therefore we can store only a fixed size of elements in array.
- Why to use Array? Accessing is faster!!
```
int[] marks; //Declaration
marks = new int[5]; //
```
#### For Each loop
- same like for loop
```
for (int element:Arr) {
    System.out.println(element);    //Prints all the elements
}
```
#### Multidimensional Arrays
- Array of Arrays
```
int[][] arr = new int[n][n]; //2-D array
int[][][] arr1 = new int[n][n][n]; //3-D array
```

### Methods
- Sometimes our program grows in size, and we want to separate the logic of the main method from the other methods.
- DRY: Don't repeat yourself
```
returnType nameOfMethod() {
//Method body
}
```
<strong>Calling a Method : </strong>
A method can be called by creating an object of the class in which the method exists followed by the method call:
```
Calc obj = new Calc(); //Object Creation

obj.mySum(a , b); //Method call upon an object
```
<strong>Void return type:</strong>
When we don’t want our method to return anything, we use void as the return type.

<strong>Static keyword:</strong>
- The static keyword is used to associate a method of a given class with the class rather than the object. 
- You can call a static method without creating an instance of the class. 
- In Java, the main() method is static, so that JVM can call the main() method directly without allocating any extra memory for object creation.
- All the objects share the static method in a class.

#### Method Overloading
- In Java, it is possible for a class to contain two or more methods with the same name but with different parameters. Such methods are called Overloaded methods. 
- Method overloading is used to increase the readability of the program.
#### Ways to perform method overloading:
- By changing the return type of the different methods 
- By changing the number of arguments accepted by the method

### Variable Arguments (VarArgs)
- let's suppose you want to overload an "add" method. The "add" method will accept one argument for the first time and every time the number of arguments passed will be incremented by 1 till the number of arguments is equaled to 10. 
- One approach to solve this problem is to overload the "add" method 10 times. But is it the optimal approach? What if I say that the number of arguments passed will be incremented by 1 till the number of arguments is equaled to 1000. Do you think that it is good practice to overload a method 1000 times? 
- To solve this problem of method overloading, Variable Arguments(Varargs) were introduced with the release of JDK 5. 
- With the help of Varargs, we do not need to overload the methods.
```
public static void foo(int …arr)
{
// arr is available here as int[] arr
}
```

### Recursion
- In programming, recursion is a technique through which a function calls itself. 
- With the help of recursion, we can break down complex problems into simple problems.
```
//factorial(n) = n*factorial(n-1)                 [n >= 1]
```

## Object Oriented Programming
Solving a problem by creating objects
### Class
A class is a blueprint for creating objects
### Object
### Four pillars of Object-Oriented-Programming Language :
- #### Abstraction
- 
