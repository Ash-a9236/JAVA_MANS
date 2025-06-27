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

<br>

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

<br>

________
### <a id="base-concepts-main"><span style="color: var(--title)">01.01 MAIN</span></a>
________________

<br>

The <span style="color: var(--highlight)">main</span> method is your program's entry point





</span>
