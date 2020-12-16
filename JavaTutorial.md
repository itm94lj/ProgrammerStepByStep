# Professional Programmer Java Tutorial
  Once i was a C programmer, recent times i'm trying to be a Java programmer. Try to record the path i go through.
## Step 1: [Java se tutorial from oracle](https://docs.oracle.com/javase/tutorial/)
  On the page above, there are all essential information we need to know. Beyond this to be able to solve problems,
some practices is need. I'm going to pass through all the sections in order, output a mind map if possible and
do some practice. 
  First part is tutorial about the [Java Language](https://docs.oracle.com/javase/tutorial/java/index.html), this trail covers the fundamentals 
of programming in the Java programming language. Pass through it.
### Language Basics
  #### Variables
  Try to answer Questions and Exercises of Variables
  ##### Questions:
  1. The term "instance variable" is another name for **Non-static fields**
  2. The term "class variable" is another name for **Static fields**
  3. A local variable stores temporary state; it is declared inside a **method**
  4. A variable declared within the opening and clossing parenthesis of a method signature is called a **parameter**
  5. What are the eight primitive data types supported by the Java programming language?
     **byte short int long float double boolean char**
  6. Character strings are represented by the class **String**
  7. An **array** is a container object that holds a fixed number of values of a single type.
  ##### Exercises:
  1. Create a small program that defines some fields. Try creating some illegal field names and see what kind of error the compiler produces. Use the naming rules and conventions as a guide.
  According to the **Naming** section of variables there are several rules:
  Only begin with letter '$' or '_', if begin with digits it will show error:
  ```
  > Variable.java:3: 错误: 需要<标识符>\n
  > byte 0myByte;\n
  > Variable.java:3: 错误: 非法下划线\n
  >  byte 0_myByte;\n
  >       ^\n
  ```
  2. In the program you created in Exercise 1, try leaving the fields uninitialized and print out their values. Try the same with a local variable and see what kind of compiler errors you can produce. Becoming familiar with common compiler errors will make it easier to recognize bugs in your code.
  Write a class named **Variable.java** with code below:
 ```
 public class Variable
{
    byte myByte;

    void out()
    {
        System.out.println("myByte:" + myByte);
    }

    public static void main(String[] args)
    {
        Variable a = new Variable();
        a.out();
    }
}
```
After compile and run you may get result:
```
$ java Variable
myByte:0
```
It shows that instance variables will be initialized automatically.
Add below code after a.out() 
```
byte b;
System.out.println("Local variable:" + b);
```
You may get compile error show below:
```
$ javac Variable.java
Variable.java:15: 错误: 可能尚未初始化变量b
        System.out.println("Local variable:" + b);
                                                  ^
1 个错误
```
It shows that local variable is not initialized automatically.
