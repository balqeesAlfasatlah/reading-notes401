# Object-Oriented Programming Concepts

## Object & Class

+ Everything in Java is associated with classes and objects.

+ **object** is a software bundle of related state and behavior.

+  **Class** is like an object constructor, or a "blueprint" for creating objects.

+ For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.


![](https://1.bp.blogspot.com/-pFHJTng93q4/XU-utsYfSjI/AAAAAAAAEno/43JhWi3SrVAVmXc3UyKmhyXKH74esCKHACLcBGAs/s1600/object-class-diagrame-1.png)

+ Declaring Classes :

![](https://image2.slideserve.com/4996496/defining-a-class-in-java-l.jpg)

![](https://java2blog.com/wp-content/webpc-passthru.php?src=https://java2blog.com/wp-content/uploads/2017/05/classStructure-2-1.png&nocache=1)

## Inheritance

Inheritance in Java is a mechanism in which one object acquires all the properties and behaviors of a parent object.

![](https://cdn.techbeamers.com/wp-content/uploads/2019/04/Java-Inheritance.png)

+ The **extends** keyword indicates that you are making a new class that derives from an existing class.

+ **Overriding and Hiding Methods** :

  + instance method in a subclass with the same signature (name, plus the number and the type of its parameters) and return type as an instance method in the superclass overrides the superclass's method.


  ![](https://astikanand.github.io/techblogs/java/assets/method_overriding_hiding.png)


+ **Polymorphism :**  the ability of an object to take many forms

![](https://study.com/cimages/multimages/16/java_inherit_poly_inheritance.png)

## interface

 An interface is a completely "abstract class" that is used to group related methods with empty bodies:

 ![](https://slidetodoc.com/presentation_image_h/0d1257fa2a9daedba90a6015675902fc/image-2.jpg)

 ![](https://www.pixeltrice.com/wp-content/uploads/2020/07/in-1.png)


+ **Using an Interface as a Type** :
When you define a new interface, you are defining a new reference data type. You can use interface names anywhere you can use any other data type name.

**example** :

public Object findLargest(Object object1, Object object2) {

   Relatable obj1 = (Relatable)object1;

   Relatable obj2 = (Relatable)object2;

   if ((obj1).isLargerThan(obj2) > 0)

return object1;

   else 

 return object2;

}

+ **Default Methods** : enable you to add new functionality to the interfaces of your libraries and ensure binary compatibility with code written for older versions of those interfaces.

   + When you extend an interface that contains a default method, you can do the following:

      + Not mention the default method at all, which lets your extended interface inherit the default method.

      + Redeclare the default method, which makes it abstract.

     + Redefine the default method, which overrides it.


 ## Package

 A package is a namespace that organizes a set of related classes and interfaces.