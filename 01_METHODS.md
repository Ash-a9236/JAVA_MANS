<!--@ash-a9236 2025 : please see license for -->

<!--VARIABLES-->

<style>
  :root {
    --text: #F7E0CD;
    --title: #708C69;
    --highlight: #D69992;
    --link: #B15A43;
  }
</style>

<span style="color: var(--text)">

# <span style="color: var(--title)">CODING IN JAVA 01
## <span style="color: var(--title)">METHODS

<br>
TABLE OF CONTENTS <br> <br>

[<span style="color: var(--link)">01 . . Base Concepts</span>](#base-concepts) <br>
    &emsp; [<span style="color: var(--link)">01 . . Main</span>](#base-concepts-main) <br>
[<span style="color: var(--link)">02 . . Console</span>](#console) <br>
    &emsp; [<span style="color: var(--link)">01 . . Console Print</span>](#console-print) <br>
    &emsp; [<span style="color: var(--link)">02 . . Console Output</span>](#console-output) <br>
    &emsp; [<span style="color: var(--link)">03 . . Console Input</span>](#console-input) <br>
    &emsp; [<span style="color: var(--link)">04 . . Console Errors</span>](#console-errors) <br>
[<span style="color: var(--link)">03 . . Access Modifiers</span>](#access-modifiers) <br>
[<span style="color: var(--link)">04 . . Static vs Non-Static</span>](#static-vs-nonstatic) <br>
[<span style="color: var(--link)">05 . . Return Types</span>](#return-types) <br> 
[<span style="color: var(--link)">06 . . Naming</span>](#naming) <br> 
[<span style="color: var(--link)">07 . . Input</span>](#input) <br>
[<span style="color: var(--link)">07 . . Documentation</span>](#documentation) <br>

<br> <br>

________
### <a name="base-concepts"><span style="color: var(--title)">01.00 BASE CONCEPTS</span></a>
________________

<br>

Methods are little pieces of code that can be reused throughout the code. Each method is meant to <span style="color: var(--highlight)">perform an action</span> or a set of actions which will manipulate variables and objects to <span style="color: var(--highlight)">product an output</span>.
You can see them as actions that can be done by your objects.
<br>

To use a method, you need to <span style="color: var(--highlight)">call</span> it. It is called a <span style="color: var(--highlight)">method call</span>. Those method calls are made through the <span style="color: var(--highlight)">dot operator (.)</span>, which you add to the appropriate object.

*If the method is in the same class, you can call the method simply by writing <span style="color: var(--highlight)">name(input 1, input 2);</span>

```java
package asha9236.example;

public class Main {
    public static void main (String[] args) {
        makeSound();
        addNums(5, 7); //same class method call

        String name = "hello";
        name.toUpperCase(); //calling the toUpperCase method
        //name = "HELLO" now
    }

    public static void makeSound () {
        System.out.println("Bing!");
    }

    public int addNums (int a, int b) {
        return a + b;
    }

}
```

<br>

In Java, methods contain a lot of information that tell the compiler how to handle that method, who can 'see' that method, and how it can be used. Methods follow this blueprint :

* <span style="color: var(--highlight)">header</span> : where you define how the method will work
* <span style="color: var(--highlight)">body</span> : where you define the actions
* <span style="color: var(--highlight)">return</span> : what the method will give you back (the output)

```java
package asha9236.example;

public class Main {

/*
    access modifier - static/not - return type - nameInCamelCase - (input parameter1, input parameter2, ...) {
        actual code
        .
        .
        .
        return paramenter (! has to be the same as the return type in the header);
    }
*/
    public static void main (String[] args) {
        //main method
    }

    public static void makeSound () {
        System.out.println("Bing!");
    }

    public int addNums (int a, int b) {
        return a + b;
    }

}
```

As you might have noticed, all methods and classes are enclosed in curly brackets ({}). Those brackets define the method's start and end as well as <span style="color: var(--highlight)">scope</span> of the variables.

Variables all have scopes in which you can use them, and after the scope, they are automatically deleted by Java. You, as the programmer, needs to know and define the scope of each variable you use in your program.


```java
package asha9236.example;

public class Main {
    public static void main (String[] args) {
        /*1*/int num1 = 5; //scope start of num1
        /*2*/int num2 = 7; //scope start of num2
        /*3*/
        /*4*/int num3 = add (num1, num2); //a is now num1, b is now num2, c is now num3
        /*8*/System.out.println(num3); //will print 14 (5 + 7 + 2)
    } //scope end of : num1, num2, num3

    public static int add (int a, int b) { //scope start of a, b
        /*5*/int c = 2; //scope start of c
        /*6*/c += a + b; //+= means c = c + a + b
        /*7*/return c;
    } //scope end of c
}
```

<br>

#### <a id="base-concepts-main"><span style="color: var(--title)">01.01 MAIN</span></a>
________________

<br>

In my previous examples you might have seen this : 

```java
package asha9236.example;

public class Main {
    public static void main (String[] args) {
    
    }
}
```

This is called the <span style="color: var(--highlight)">main</span> class and method. For now, you do not need to worry about the class, but the method is what we are looking for. 

A Java program cannot run without a main method since it is the entry point of the program. You can see the entire program as a list of steps to do, and the main method would be step 0. You can add a main method to any class, but know that if you delete the main class, you need to define which is the entry point.

To add a main method to a class, you can simply write it (public static void main (String[] args) {} OR psvm + tab on IntelliJ) and the compiler will recognize it.


<br> <br>

________
### <a name="console"><span style="color: var(--title)">02.00 CONSOLE</span></a>
________________

<br>

The terminal or console is the origin of what computers where before GUI (Graphical User Interface). They are called CLI (Command Line Interface) because to interact with them you need to write commands.

When you compile and run the code, a new window will open either in the IDE's built-in terminal, or in your computer's terminal itself. The console will contain the output of the code as a process exit. 

You can print on the console as we have done it with <span style="color: var(--highlight)">System.out.println();</span> (System Class -> Output field -> Print + new line method), or write the shortcut <span style="color: var(--highlight)">sout + tab</span>.

<br>

#### <a id="console-print"><span style="color: var(--title)">02.01 CONSOLE PRINT</span></a>
________________

<br>

Printing on the console has different means, most of the time, it is to print values or steps of your code for you to be able to follow it more easely.

It might seem useless at first, but printing will make abstract calculations a bit more easy to understand, especially when debugging.

You can print with different methods in Java : 
* <span style="color: var(--highlight)">System.out.println();</span> - sout : base printing with a new line added 
* <span style="color: var(--highlight)">System.out.print();</span> - none : the base printing, no new line
* <span style="color: var(--highlight)">System.out.printf();</span> - souf : format printing

The most difficult print to handle is <span style="color: var(--highlight)">System.out.printf();</span> because it uses <span style="color: var(--highlight)">placeholders</span> to hold values. They take the form <span style="color: var(--highlight)">%[arg$][flags][width][.precision]conversion</span>. While it is difficult to use at first, it is better for long printing with a lot of values.

| CODE | MEANING |
|------|---------|
|  \n  | will return to the next line <br> effective equivalent to an empty System.out.println(); |
|  \t  | horizontal tab |
|  \"  | inserting double quotes |
|  \\  | inserting a backslash |
|      |            |
| %b   | Boolean |
| %d   | int placeholder |
| %s   | String |
| %c   | char |
| %f   | double of float |

For example :

```Java
package asha9236.example;

public class Main {
    public static void main (String[] args) {
        System.out.println("Hello !");

        String name = "test";
        int num = 4;
        double decimalNum = 4.123456789;

        System.out.printf("Hello ! \nMy name is %s\nMy favourite number is : %d \nThis is a decimal number : %f \nAnd this is a decimal number rounded : %f.2\n\n", name, num, decimalNum, decimalNum);

        //If you use the regular System.out.println() :
        System.out.println("Hello ! \nMy name is " + name + "\nMy favourite number is : " + num + "\nThis is a decimal number : " + decimalNum);
    }
}
```

Output

```console
Hello !
Hello !
My name is test
My favourite number is 4
This is a decimal number : 4.123456789
And this is a decimal number rounded : 4.12

My name is test
My favourite number is 4
This is a decimal number : 4.123456789

Process finished with exit code 0
```

<br>

#### <a id="console-output"><span style="color: var(--title)">02.02 CONSOLE OUTPUT</span></a>
________________

<br>

As mentionned earlier, you can use the console to print values through your code to check if everything is working correctly. For example :

```Java
package asha9236.example;

public class Main {
    public static void main(String[] args) {
        System.out.println("Hello !");

        double num = 4.123456789;
        System.out.printf("Line : 8 - %f\n", num);

        num += 15.47428943;
        System.out.printf("Line : 11 - %f\n", num);

        num += 'a';
        System.out.printf("Line : 14 - %f\n", num);
    }
}

```

```Console
Hello !
Line : 8 - 4.123457
Line : 11 - 19.597746
Line : 14 - 116.597746

Process finished with exit code 0
```

<br>

#### <a id="console-input"><span style="color: var(--title)">02.03 CONSOLE INPUT</span></a>
________________

<br>

The console can also be use to make applications and to therfore get external information into your code.
It is made through the <span style="color: var(--highlight)">Scanner</span> class.

```Java
package asha9236.example;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner console = new Scanner(System.in); //creating the scanner with the name 'console' & telling it to look at the console through 'System.in'

        System.out.println("Hello !");
        System.out.print("Please input your name => "); 
        String name = console.nextLine(); //will never go further than here until something is inputted though the console
        System.out.printf("Hello %s! ", name);
    }
}


```

Console until line 11 : 

```Console
Hello !
Please input your name => 
```

Console after input :

```Console
Hello !
Please input your name => ash-a9236
Hello ash-a9236! 

Process finished with exit code 0
```

The <span style="color: var(--highlight)">Scanner class</span> has multiple methods that can be used to get multiple types of input.
They include : 

| METHOD        | INPUT REQUIRED |
| --------------| ---------------|
| .next()       | String until a space is encountered|
| .nextLine()   | String until a next line (enter) is encountered |
| .nextInt()    | int |
| .nextDouble() | double |
| .nextFloat()  | float |

BUT! Be careful : if you request an int through .nextInt() and you try to pass a String it will return an error and exit the code completly : 

```java
package asha9236.example;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner console = new Scanner(System.in);

        System.out.println("Hello !");
        System.out.print("Please input your name => ");
        int name = console.nextInt(); //change the input type to int

        System.out.printf("Hello %d! ", name);
    }
}
```

```Console
Hello !
Please input your name => ash-a9236

Exception in thread "main" java.util.InputMismatchException
	at java.base/java.util.Scanner.throwFor(Scanner.java:964)
	at java.base/java.util.Scanner.next(Scanner.java:1619)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2284)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2238)
	at asha9236.example.Main.main(Main.java:11)

Process finished with exit code 1
```


<br>

#### <a id="console-errors"><span style="color: var(--title)">02.04 CONSOLE ERRORS</span></a>
________________

<br>

As you could see in the last example, when something goes wrong with your code during <span style="color: var(--highlight)">runtime</span>, <span style="color: var(--highlight)">the code will complelty stop and throw an exception</span>.

Console errors are informations about how, where and why the error happen.

<span style="color: var(--highlight)">Exception</span> are the way that your IDE shows you an error. They show : 
* the <span style="color: var(--highlight)">type</span> of error
* <span style="color: var(--highlight)">where</span> the error happen
and sometimes 
* <span style="color: var(--highlight)">how to fix it</span>

This allows you to debug your code more efficiently, as long as you read the exception correctly.

In last example, the error was : 

```Console
Exception in thread "main" java.util.InputMismatchException
	at java.base/java.util.Scanner.throwFor(Scanner.java:964)
	at java.base/java.util.Scanner.next(Scanner.java:1619)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2284)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2238)
	at asha9236.example.Main.main(Main.java:11)

Process finished with exit code 1
```

In this, the IDE tells you :
1. the exception is an <span style="color: var(--highlight)">InputMismatchException</span>, therefore there is a mismatch between what the IDE expected the user to input, and what the user actually inputed
2. it happened at the <span style="color: var(--highlight)">line 11</span> of the main method in the Main class : all the line at first don't matter, only the last line with your groupId (in my case asha9236), matters because up until then it is not your code but rather the code that makes Java. The way to recognize it is if it starts with java.[something...].[the class you are using], which in our case is 'java.base./java.util.Scanner'
3. The <span style="color: var(--highlight)">process exit</span>, which indicated <span style="color: var(--highlight)">1</span>, AKA, an <span style="color: var(--highlight)">expected potential error</span>

The <span style="color: var(--highlight)">process exit</span> has 3 main values : 

| VALUE | MEANING |
|-------|---------|
| 0     | good termination <br> everything went well |
| Positive | wrongfull termination but known exception <br> Something went wrong but we know what and why |
| Negative | completly wrongfull and unclean termination <br> worst exit code : something went wrong and we don't know what, where or how <br> with this termination you need to be careful (later on with more advanced code) : the code exited unsafely so some 'code stuff' like threads might still be active or unclosed |



Sometimes, there is an error but the IDE <span style="color: var(--highlight)">doesn't catch it</span>. Those are called <span style="color: var(--highlight)">logical errors</span> and cannot be caught unless you manually go through your code. An example of this would be doing 2+2 and expecting 4, but the IDE gives you back 22 : there is no error for the IDE but clearly one in the logic.

Basically, there are 3 types of errors : 

| TYPE      | ERROR |
|-----------|-------|
| Compile-time | Small errors that will be caught by the IDE. They are often called syntax errors <br> i.e. int a = 6  -> ';' expected 1:9 <br> => missing semicolon at the end of the statement |
| Runtime   | Errors that happen when the code runs, they sometime get caught by the IDE before compilation, but they often do not <br> i.e. int a = 6 / 0; ->  Exception in thread "main" java.lang.ArithmeticException: / by zero at asha9236.example.Main.main(File.java:14) <br> => impossible division since it was by 0 |
| Logic     | Errors that happen when you expect a certain result and the computer gives you another <br> (examples are too long)|


<br> <br>

________
### <a name="access-modifiers"><span style="color: var(--title)">03.00 ACCESS MODIFIERS</span></a>
________________

<br>

As you might have caught in code examples before, the keyword 'public' appears quite often in <span style="color: var(--highlight)">method definitions (headers)</span>. <span style="color: var(--highlight)">public</span> is an <span style="color: var(--highlight)">access modifier</span>, which allows everyone to see what is inside the method.

<span style="color: var(--highlight)">Access modifiers</span> are keywords which determine <span style="color: var(--highlight)">who</span> can 'see' and 'use' the method. 

The best way to write your code is to give as little access as necessary (to enfore the black box). Basically, if a method doesn't need to be public, make it protected. If it doesn't need to be protected, make it private.

| MODIFIER  | UML SIGN | NOTE |
|-----------|----------|------|
| public    | +        | the <span style="color: var(--highlight)">most permissive</span> access modifier. Everyone can have access to those methods |
| protected | #        | a small step over private : allows all the subclasses to see the methods as well <br> it is mostly used in the case of inheritance (parent-child relationships) |
| default   |          | It allows only those of the same package to see each other. <br>Note that no keyword is needed to implement it |
| private   | -        | The <span style="color: var(--highlight)">less permisive</span> access modifier. Only those in the same class can see and use the methods. <br>It is often used for data fields |

<br>

Access modifiers can be seen by : 

| MODIFIER  | UML SIGN | SAME CLASS | PACKAGE SUBCLASS | PACKAGE NON-SUBCLASS | DIFF PACK SUBCLASS | DIFF PACK NON-SUBCLASS |
|-----------|----------|------------|------------------|----------------------|--------------------|------------------------|
| public    | +        | Y          | Y                | Y                    | Y                  | Y                      |
| protected | #        | Y          | Y                | Y                    | Y                  | N                      |
| default   |          | Y          | Y                | Y                    | N                  | N                      |
| private   | -        | Y          | N                | N                    | N                  | N                      |



<br> <br>

________
### <a name="static-vs-nonstatic"><span style="color: var(--title)">04.00 STATIC VS NON-STATIC</span></a>
________________

<br>

On the main method header there is the keyword 'static'. Static, or the absence of it (no keyword) is simply there to define <span style="color: var(--highlight)">to who does this method belongs</span>.

When you create a class (or an object), you want to create methods that either <span style="color: var(--highlight)">belong to the class itself</span> OR <span style="color: var(--highlight)">belong to an instance of the class</span>, AKA an object.

To put it more simply, you can create a class 'Cat' and have methods, that are 'owned' by the Cat class but can be used by whoever wants it, while on the opposite you can have methods that only belong to specific cats (i.e. orangeCat, blackCat, etc.) and that can only be used by those cats separately.

| -          | BELONGS TO | CAN USE | USED BY | NOTE |
|------------|------------|---------|---------|------|
| static     | An instance of a class (object)  | static | static <br>non static| - the method is always in the RAM <br><br>- less memory used (since its fixed 1 time) <br><br>- to call you need Class.methodName(); <br><br>- Compile time / early binding <br>no overriding (since early binding) |
| non static | The class itself | static <br>non static | non static | - the method is not fixed in the RAM <br><br>- more memory used <br><br>- to call you need object.methodName(); <br><br>- Runtime / dynamic binding <br><br>- can be overriden









</span>
