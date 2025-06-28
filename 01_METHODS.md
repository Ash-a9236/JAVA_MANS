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
    &emsp; [<span style="color: var(--link)">01 . . Console Errors</span>](#console-errors) <br>
    &emsp; [<span style="color: var(--link)">02 . . Console Output</span>](#console-output) <br>
[<span style="color: var(--link)">03 . . Access Modifiers</span>](#access-modifiers) <br>
[<span style="color: var(--link)">04 . . Static vs Non-Static</span>](#static-vs-nonstatic) <br>
    <!--&emsp; [<span style="color: var(--link)">01 . . Return Type</span>](#return-types) <br>
    &emsp; [<span style="color: var(--link)">02 . . High and Low</span>](#coding-types-high-and-low) <br>-->
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

In Java, methods contain a lot of information that tell the compiler how to handle that method, who can 'see' that method, and how it can be used. Methods follow this blueprint :

* <span style="color: var(--highlight)">header</span> : where you define how the method will work
* <span style="color: var(--highlight)">body</span> : where you define the actions
* <span style="color: var(--highlight)">return</span> : what the method will give you back (the output)

```java
public class Main {

/*
    access modifier - static/not - return type - name - (input parameter1, input parameter2, ...) {
        actual code
        .
        .
        .
        return paramenter;
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

Variables all have scopes in which you can use them, and after the scope, they are automatically deleted by the program. You, as the programmer, needs to know and define the scope of each variable you use in your program.


```java
public class Main {
    public static void main (String[] args) {
        int num1 = 5; //scope start of num1
        int num2 = 7;

        int num3 = add (num1, num2); //a is now num1, b is now num2, c is now num3
        System.out.println(num3); //will print 14 (5 + 7 + 2)
    } //scope end of : num1, num2, num3

    public static int add (int a, int b) { //scope start of a, b
        int c = 2; //scope start of c
        c += a + b; //+= means c = c + a + b
        return c;
    } //scope end of c
}
```

<br>

### <a id="base-concepts-main"><span style="color: var(--title)">01.01 MAIN</span></a>
________________

<br>

In my previous examples you might have seen this : 

```java
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

When you compile and run the code, a new window will open either in the IDE's built-in terminal, or in your computer's terminal itself. The console will contain the output of the code as a process exit. 

You can print on the console as we have done it with <span style="color: var(--highlight)">System.out.println();</span> (System -> Output -> Print + new line)


</span>
