# Chapter 1 Kickstarter for Beginners

## Key points of OOP
### Type, class, enum, and interface
* Type is a nane given to a bahavior.
* A class, an enum, and an interface are types of types
	* A class allows you to combine the description of a behavior and the implementation that is used to realized this behavior
	* An enum allows you to combine the description of a behavior and the implementation that is used to realize this behavior, but in addition provides a fixed number of instancesof this type. You cannot create more  instances of this type.
	* And interface allows you to dfine just the behavior without any implementation. You cannot create instances of an interface.
	* Abstract class, like a class it defeines behavior as well as implementation but the implementation is not complete enough for you to create instances. Like an interface it cannot live as its own.
### Why is something so?
* To help componentize the code: A well-developed software commponent is as generic as possible.
* To eliminate the scope for bugs: Java designers have tried to limit or eliminate features that increase the possibility of bugs in a piece of code. 
* Make life easier for the programmer: having more and more features is not necessarily a good thing. Instead of  focusing on mastering complicated features, the proframmers hsould be spending mmore time in develping business logic.
* To become commercially successful: Java was designed by pragmatic folks rather than idealistic ones. Dome things may not make complete sense from a purely logical or technical perspective but that's how they designed those things anyway.
## Declaration and Definition
Declaration just means that something exists, a definition describes exactly waht it is
```
class SomeClass //class declaration
// class definition starts
{
	public void mi() // method declaration
	// method definition starts
	{
	}
	// method definition ends
}
// class definition ends
```
## 1.4 Object and Reference
### 1.4.1 Relation between a class, an object and a reference
* Object is an instance of a class
* Class defines what the actual object will contain
* To access an object, you need to know exactly wherethat object resides in memory. You need to know the address of an object.a It is this address that is stored in a reference variable
* Primitive variable are the unique variable which store the value of the content and not the reference to it. For example a string variable point to a address direction. The variable just have the address, but not he content of this space of memory. Primary variables as an int stores directly the content of the variable and not point to any other address.
* You cannot make a reference variable point toa memory location directly. You can do that in C/C++ but not in Java.
* You can have as many refeerences to an object as you want.
* A variable which is not pointing at any object is said to be null.

![](image.png)

## Static and instance
### Static and Instance
* **Static** for java is not a variable which doesn't move. For that there is **Final**
* **Static** means something that belogs to a class instead of belonging to an instance of that class
* **Static** is considered a non object-oriented feature.
* **Static** it is not an error that you access through a variable of that class, but this is strongly discouraged.
* There are static methods

## Stack and Heap
### Stach and Heap
* When you executea program, the OS allocates and gives memory toa that program
* Once the program the OS gives out a chunk of memory, it is responsability of the program to manage it/
* Once the program ends, this memory is released and goes back to the OS.
* The space for storing the temporary stuff is called **Stack space**
* The space for storing all other stuff is called **Heap space**
* In the stack space variable are store as a stack, when its thread dies its stack space is reverted back to the JVM.
* In the heap space, objects lie in a heap just as they please.
* Whenever any object is crated any where in the code, the JVM allocates space for that object on the heap and puts its contents in the space.
* If there is no reference on any stack space through which an object can be access, that object is considered garbage, and it is cleaned up automatically by the JVM using a garbage collector.
* If you create a variable in a method, whether a reference variable or a primitive variable, it is kept on the stack but when you create an object, that object is stored on the heap.
* Local variablesa re always  kept on the slack. Objects are always stored in the heap
* JVM may have several threads. Each threis given a fixed amount of stack space.
* Heap space is shared among all threads.
* Stack space is limited for a program. To increase to more than 64KB use -Xss.
* Heap space is unlimited from the program's perspective.
* Only temporary varialbles are created on the stack space.
* When a method is invoked by a thread, it uses the thread's stack space to keep its temporary varialbes.
* Variables added to the stack space by a method  are removed from the stack when that method ends.

## 1.7 Conventions
### 1.7.1 Conventions in Java
1. Cases
	* CamelCase for class names
	* lowercar for package names
1. Naming: meaningful
1. Package names: reverse domain name. E.g. com.something.appname

## 1.8 Compilation and Execution
### 1.8.1 Compilation and Execution

* Java sourcefile is compiled into a Java class file an a class file is what isexecuted by the JVM.
* You can organie your Java classes into packages by putting a package statement at the top of a Java source file.
* The package name plus the class name is calle **Fully Qualified Class Name FQCN**
* To compile a class generiting the packages use `javac -d . ClassName.java`
	* -d directs the compiler to create the didrectory structure as per the package name of the class and put the class file in the right place.
	* . tells the ocmpiler that the current directory is the target directory for the resulting output.
* To run you can use `java -classpath . packagename.ClassName`
	* classpath specify where your classes are located. You can specify may locations. 
* Location  is the location of the directory structure of teh class file. 

