# Java Primitives & Objects

+ java has a two-fold type system :

1- primitives  : such as int, boolean.  

2- reference types : such as Integer, Boolean.

+ Every object contains a single value of the corresponding primitive type.

+ The wrapper classes are immutable (so that their state can't change once the object is constructed)and we can't inherit from them.

+ autoboxing : The process of converting a primitive type to a reference one ,  the opposite process is called unboxing.

![](https://slidetodoc.com/presentation_image_h/fd9321f202c149c6e18ef1332434e4f9/image-11.jpg)

### **Performance** :

+ performance of a Java code depends very much on the hardware on which the code runs (the compiler , the virtual machine , the operating system).

+ the primitive types live in the stack while the reference types live in the heap. This is a dominant factor that determines how fast the objects get be accessed.

### **Default Values** :

+ Default values of the primitive types :

 1- zeros for numeric types.

 2- false for the boolean type.

 3- \u0000 for the char type. 
 
 + For the wrapper classes, the default value is null. 

## **Usage** :

+ The primitive types are much faster and require much less memory.

+  Java language specification doesn't allow usage of primitive types in the parametrized types (generics).

---

## Exceptions

+ we use exceptions to handle errors and other exceptional events.
 + exceptions is an event that occurs during the execution of a program that disrupts the normal flow of instructions.

 ### The Catch or Specify Requirement :

 Valid Java programming language code must honor the Catch or Specify Requirement. This means that code that might throw certain exceptions must be enclosed by either of the following:

 1- A try statement that catches the exception. 
 
 2- A method that specifies that it can throw the exception.

+  **The try Block** :

![](https://image.slidesharecdn.com/exceptionhandling-180813200205/95/exception-handling-21-638.jpg?cb=1534190573)

+ **The catch Blocks** :

![](https://image.slidesharecdn.com/5-exceptionhandling-190701213934/95/exception-handling-10-638.jpg?cb=1562017200)


+ **The finally Block** :

1- It always executes when the try block exits. This ensures that the finally block is executed even if an unexpected exception occurs.

2- it allows the programmer to avoid having cleanup code accidentally bypassed by a return, continue, or break. Putting cleanup code in a finally block is always a good practice, even when no exceptions are anticipated.

---
## Scanning
Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.




![](https://media.cheggcdn.com/media/243/243a193c-2d95-4084-8ab2-b8b602595db9/phpP7REo4.png)
