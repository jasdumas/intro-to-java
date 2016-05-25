# intro-to-java
I'm learning Java for my MS-CS Program at Johns Hopkins Engineering for Professionals

## Topics to cover:

### History of Java

Java is a general-purpose computer programming language that is concurrent, class-based, object-oriented, and specifically designed to have as few implementation dependencies as possible. It is intended to let application developers "write once, run anywhere" (WORA), meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.[15] Java applications are typically compiled to bytecode that can run on any Java virtual machine (JVM) regardless of computer architecture. As of 2016, Java is one of the most popular programming languages in use, particularly for client-server web applications, with a reported 9 million developers. Java was originally developed by James Gosling at Sun Microsystems (which has since been acquired by Oracle Corporation) and released in 1995 as a core component of Sun Microsystems' Java platform. The language derives much of its syntax from C and C++, but it has fewer low-level facilities than either of them. Source: https://en.wikipedia.org/wiki/Java_(programming_language) 

### Why Use Java

Java is: platform independent, compiler catches the errors, industry standard, universal language for programmers, many libraries, structured language. Java is analogous to a manual car versus a automatic. Java teaches the basics of fundamental programming.

### Tools, Compilers, Terminal Commands

* on MacOS: http://www.cs.princeton.edu/courses/archive/spr04/cos126/hello/mac.html
  * To check that you have the right version of Java installed  `[username:] ~> java -version`

  * Check that the Java Compiler is accesible  `[username:] ~> which javac`

  * Write the program in a vim text editor  `vim HelloWorld.java`

  * Compile the program `[username:] ~> javac HelloWorld.java` (if everything went well you should see _nothing_ in the Terminal.

  * Execute the program  `[username:] ~> java HelloWorld`
  * Desired output: `Hello, World`

### Data types (int, boolean, char)
  
```java
public class DataTypes {
	public static void main(String[] args) {

		System.out.println(26);
		System.out.println("hi");
		System.out.println(true);

	}
}
```

### Variables

```java
public class Variables {
	public static void main(String[] args) {

		int myNumber = 42;
		boolean isFun = true; 
		char movieRating = 'A'; 

	}
}
```

### Boolean Operators (&&, ||, !)

The precedence of each Boolean operator is as follows:

1. ! is evaluated first
2. && is evaluated second
3. || is evaluated third

```java
public class And {
	public static void main(String[] args) {

		System.out.println(2 == 2 && 5 > 3);
    System.out.println(2 != 3 || 5 > 3);
		
	}
}
```

### Relational Operators (<, <=, >, and >=)

```java
public class RelationalOperators {
	public static void main(String[] args) {

		System.out.println(35 >= 6);

	}
}
```
### Equality Operators (==, !=)

```java
public class EqualityOperators {
	public static void main(String[] args) {

		System.out.println(true != true);
    System.out.println(true == false);

	}
}
```

### Arithmetic Operators (+, -, *, /, and %)

```java
public class Arithmetic {
	public static void main(String[] args) {

		int myNumber = 26 * 546;
		System.out.println(myNumber);

	}
}
```

### if statements

```java
public class If {
	public static void main(String[] args) {

		if ( 26 < 27 ) {

			System.out.println("Access granted.");

		}
		
	}
}
```

### if-else statements

```java
public class IfElse {
	public static void main(String[] args) {

		if (5 > 7) {

			System.out.println("Try again...");

		} else {

			System.out.println("Success!");

		}
		
	}
}
```

### if-elseif-else statements

```java
public class IfElseIf {
	public static void main(String[] args) {

		int round = 10;

		if (round > 12) {

			System.out.println("The match is over!");

		} else if (round > 0) {

			System.out.println("The match is underway!");

		}	else {

			System.out.println("The boxing match hasn't started yet.");

		}	
	}
}
```

### ternary conditional statement

The term ternary comes from a Latin word that means "composed of three parts".

```java
public class Ternary {
	public static void main(String[] args) {
		
		int kweenLevel = 3;
    // have to be single character output (i.e 'Y' and not 'Yes')
		char canDrive = (kweenLevel > 0) ? 'Y' : 'N';
		System.out.println(canDrive);

	}
}
```

### Switch Statement

```java
public class Switch {
	public static void main(String[] args) {
		
		char penaltyKick = 'R';

		switch (penaltyKick) {

			case 'L': System.out.println("Messi shoots to the left and scores!");
								break; 
			case 'R': System.out.println("Messi shoots to the right and misses the goal!");
								break;
			case 'C': System.out.println("Messi shoots down the center, but the keeper blocks it!");
								break;
			default:
				System.out.println("Messi is in position...");

		}

	}
}
```

### OOP in Java / Syntax:

### Classes

* A class is a set of instructions that describe how a data structure should behave.

* Java provides us with its own set of pre-defined classes, but we are also free to create our own custom classes.

```java
class Dog {

	public static void main(String[] args) {

	}
}
```
* **Class contructor**: describe the behavior of the class for it to be useful. A class constructor will allow us to create `Dog` instances. With a class constructor, we can set some information about the `Dog`. If we do not create a class constructor, Java provides one that does not allow you to set initial information.

```java
class Dog {

public Dog() {

}
	public static void main(String[] args) {

	}
}
```
* **Instance Variables**: When we create a new class, we probably have specific details that we want the class to include. We save those specific details into instance variables.

```java
class Dog {

	int age;  
	public Dog() {

}
	public static void main(String[] args) {

	}
}
```

* **Constructor parameters**: By adding a class constructor and creating instance variables, we will soon be able to use the Dog class. However, the class constructor Dog is still empty. Let's modify this by adding parameters to the Dog constructor. Parameters allow data types to be created with specified attributes.

```java
class Dog {

	int age;  
	public Dog(int dogsAge) {
					age = dogsAge;
}
// This is Java's built-in main method. When Java runs your program, the code inside of the main method is executed.

	public static void main(String[] args) {

	}
}
```

* **Objects**: To use the Dog class, we must create an instance of the Dog class. An instance of a class is known as an object in Java.

```java
class Dog {

	int age;  
	public Dog(int dogsAge) {
    age = dogsAge;

}
	public static void main(String[] args) {
			Dog fiona = new Dog(3);
	}
}
```

### Methods

Although we created an object inside of main method, we did not print out anything about the fiona object itself, nor did we instruct the class to perform any actions. Let's learn about how methods in Java are used to define actions.

A method is a pre-defined set of instructions. Methods are declared within a class. Java provides some pre-defined methods available to all classes, but we can create our own as well.

```java
class Dog {

	int age;  
	public Dog(int dogsAge) {
    age = dogsAge;

}
	public void bark() {
  	   System.out.println("Woof!");
	}

	public static void main(String[] args) {
			Dog fiona = new Dog(3);
	}
}

```


* Calling a method `bark()` on a object `fiona` to print out **"Woof!"**

```java
class Dog {

	int age;  
  
	public Dog(int dogsAge) {
    	
    	age = dogsAge;

}
	public void bark() {
  		System.out.println("Woof!");
	}

	public static void main(String[] args) {
		Dog fiona = new Dog(3);
    
    		fiona.bark();
	}
}
```
* creating another method to call on the object `feet`
```java
class Dog {

	int age;  
  
	public Dog(int dogsAge) {
    age = dogsAge;

}
	public void bark() {
  System.out.println("Woof!");
	}

  public void run(int feet) {
    System.out.println("Your dog ran " + feet + " feet!");
    
  }
	public static void main(String[] args) {
			Dog fiona = new Dog(3);
    
    	fiona.bark();
    	fiona.run(150);
	}
}
```
* The `void` keyword: The void keyword indicates that no value should be returned by the method after it executes all the logic in the method. If we do want the method to return a value after it finishes running, we can specify the return type.

	* The void keyword (which means "completely empty") indicates to the method that no value is returned after calling that method.
	
	* Alternatively, we can use data type keywords (such as int, char, etc.) to specify that a method should return a value of that type.

* we use the `return` keyword in the method to return something.

```java
class Dog {
  
  int age;

	public Dog(int dogsAge) {
    
  	age = dogsAge;
    
  }
  
  public void bark() {
		
    System.out.println("Woof!");
    
	}
	
  public void run(int feet) {
    
    System.out.println("Your dog ran " + feet + " feet!");

	}
  
  public int getAge() {

    return age;
    
	}
  
	public static void main(String[] args) {
    
    Dog fiona = new Dog(5);
    fiona.bark();
    fiona.run(40);
    int fionaAge = fiona.getAge();
    System.out.println(fionaAge);

	}

}

```
	
* One of the object-oriented programming concepts that allows us to reuse and maintain code more efficiently is called inheritance. It is used to share or inherit behavior from another class.

* See **Dog.java** and how it inherits from **Animal.java** files


### Data Structures 

* a data structure is a particular way of organizing data in a computer so that it can be used efficiently.

* **For loops**: run a task repeatedly until a certain condition is met as opposed to manipulating an entire set of data

```java
public class For {
	public static void main(String[] args) {

		for (int waterLevel = 0; waterLevel < 7; waterLevel++) {

			System.out.println("The pool's water level is at " + waterLevel + " feet.");

		}
		
	}

}
```

* **ArrayList**: The ArrayList stores a list of data of a specified type (homogeneous). ArrayLists are **zero indexed**. The `add` method passes the pre-defined instructions to the ArrayList named weeklyTemperatures for initial population.

```java
import java.util.ArrayList;

public class Temperatures {
	
	public static void main(String[] args) {
    // create a ArrayList
    ArrayList<Integer> weeklyTemperatures = new
    ArrayList<Integer>();
    
    // add values to the ArrayList
    weeklyTemperatures.add(78);
	weeklyTemperatures.add(67);
    weeklyTemperatures.add(89);
	weeklyTemperatures.add(94);
    // print out the lowest value
    System.out.println(weeklyTemperatures.get(1));
	}
}

```

* **Accessing the ArrayList**: The `get` method access the ArrayList while the second add method provides the 111 value into the 2nd index position in the ArrayList.

```java
import java.util.ArrayList;

public class TemperaturesB {
	
	public static void main(String[] args) {

	ArrayList<Integer> weeklyTemperatures = new 
    ArrayList<Integer>();
	weeklyTemperatures.add(78);
	weeklyTemperatures.add(67);
	weeklyTemperatures.add(89);
	weeklyTemperatures.add(94);
	
	// add a new value to the ArrayList in the second index
	weeklyTemperatures.add(2, 111);
		
    // printout the 3rd index temp value
    System.out.println(weeklyTemperatures.get(3));
	}
}
```

### String Manipulation
### Prompting users for input
### Loop Control
### Writing Functions
### File I/O 

## Learning Resources:

https://www.coursera.org/learn/java-programming/
https://www.codecademy.com/en/courses/learn-java    **(where the notes are based off of)**     
http://introcs.cs.princeton.edu/java/10elements/            
http://www.cs.princeton.edu/courses/archive/spr04/cos126/hello/mac.html    
https://en.wikipedia.org/wiki/Java_(programming_language)       
https://en.wikibooks.org/wiki/Java_Programming/Topics
