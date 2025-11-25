<!--@ash-a9236 2025 : please see license for -->

<!--VARIABLES-->

<style>

  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Fira+Code&display=swap');

  :root {
    --text: #F7E0CD;
    --title: #708C69;
    --highlight: #D69992;
    --link: #B15A43;
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
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
[<span style="color: var(--link)">08 . . Documentation</span>](#documentation) <br>

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
	    System.out.println(addNums(5, 7)); //calling the method again but printing the result this time

        String name = "hello";
	    System.out.println(name);
        name.toUpperCase(); //calling the toUpperCase method
        //name = "HELLO" now
	    System.out.println(name);
    }

    public static void makeSound () {
        System.out.println("Bing!");
    }

    public int addNums (int a, int b) {
        return a + b;
    }

}
```

Output

```console
Bing!
12
hello
HELLO

Process finished with exit code 0
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
|  \\\  | inserting a backslash |
|      |            |
| %b   | Boolean |
| %d   | int placeholder |
| %s   | String |
| %c   | char |
| %f   | double or float |

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



<br> <br>

________
### <a name="return-types"><span style="color: var(--title)">05.00 RETURN TYPES</span></a>
________________

<br>

All methods need to have what we call a <span style="color: var(--highlight)">return parameter</span>, which is basically the <span style="color: var(--highlight)">output</span> of the method. To decide which return type you want, you can ask yourself 'what do I want from this method?'.

Returns of methods can be of any data types, wether it's a primary, non-primary, or even generic data types, the only rule is that it has to match between the header and the return statement.
All return types need to have the keyword <span style="color: var(--highlight)">return</span> + the value at the end or a breaking point of a method, except for the <span style="color: var(--highlight)">void</span> return type (you do not explecitly need to declare it but you can just write 'return;' without any value attached to it). Void means that the method will essentitally return nothing, which we usually use to print information on the screen.

The return keyword signifies the exit of the method to the compiler.


```java
package asha9236.example;

public class Main {
	public static void main (String[] args) {
	//main method
	}

	public static void makeSound () {
		System.out.println("Bing!");
		return; //not necessary but can be used for clarity
	}

	public int addNums (int a, int b) { //return type : int
		int c = a + b;
		return c; //matches return data type (int)
		//we could also simplify the method by simply writing 'return a + b;' because it still returns an int
	}

	public static String printName (String firstName, String lastName) { //return type : String
		String fullName = firstName.substring(0, 1).toUpperCase() + firstName.substring(1).toLowerCase(); //capitalize the first letter and then lowercase the rest of the name
		fullName += " " + lastName.substring(0, 1).toUpperCase() + lastName.substring(1).toLowerCase(); //adding the last name with the first letter capitalized
		return fullName;

		/* ANOTHER WAY TO WRITE THIS METHOD
		firstName += firstName.substring(0, 1).toUpperCase() + firstName.substring(1).toLowerCase();
		fullName += lastName.substring(0, 1).toUpperCase() + lastName.substring(1).toLowerCase();
		return firstName + " " + lastName;
		*/
	}
}
```


<br> <br>

________
### <a name="naming"><span style="color: var(--title)">06.00 NAMING</span></a>
________________

<br>

As you might have noticed, in programming we love to have very direct and no-brainers names for everything. This goes for every programming language, concept or even when you, the programmer, name your methods or variables.

In java, all the naming is done in <span style="color: var(--highlight)">camel case</span>, which means that :
* the first word is all in lower case
* all the following words have their first letter capitalized
* no space between the words

basicallyThisIsASentenceInCamelCase
camelCase
printName
showMeYourCat
sendMeAPictureOfYourPetForExtraBrowniePoints

You must note that all the final / unchaning variables (all the constants), they are all capitalized to indicate their final state (if the name contains multiple words, you can use snake case to make is clearer)

MAX_COUNT
PI
MIN
MAX_ATTEMPS
E

Furthermore, when you name a method or a variable, it should be as straight to the point as you can.

| GOOD                              | BAD                               |
|-----------------------------------|-----------------------------------|
| printName                         | willPrintTheFullNameOfTheUser     |
| sum                               | addsTwoIntegersTogether           |
| checkISBN                         | checksIfTheISBNIsConform          |
| firstName                         | theFirstNameOfMainUser            |


Bonus :

There are other naming conventions such as :
* <span style="color: var(--highlight)">pascal</span> case, which is basically camel case but the first word is also capitalized (ThisIsPascalCase, thisIsCamelCase)
* <span style="color: var(--highlight)">kebab</span> case, where you use a hyphen to separate the words (this-is-kebab-case)
* <span style="color: var(--highlight)">snake</span> case, where you use an underscore instead of a hyphen (this_is_snake_case, this_is_not_kebab_case)





<br> <br>

________
### <a name="inputs"><span style="color: var(--title)">07.00 INPUTS</span></a>
________________

<br>

In essence, methods are like the functions you might have seen in basic algebra. You 'input x' and get y as an output of the function. For us, the ys are the returns, and the xs are the method inputs.

The input of your method are located in the parenthesis section of the header. They need to be formatted this way :
* input type (int, double, String, int[], etc.)
* input name (fName, age, tryCount, etc.)

The inputs you put in your methods header will always be required to be filled when you call that method. For example, if you ask for num1, num2 and num3 in your base method definition, everytime you call the method, you will need to 'pass on' 3 numbers.

```java
package asha9236.example;

public class Main {
	public static void main (String[] args) {
	    addNums(2, 3, 4); //9

        int num = 4;
        int secondNum = 7;

        addNums(num, secondNum, num);
	}

	public static int addNums (int num1, int num2, int num3) {
		return num1 + num2 + num3; //15
	}

}
```

<br> <br>

________
### <a name="documentation"><span style="color: var(--title)">08.00 DOCUMENTATION</span></a>
________________

<br>

Through the code examples, you might have seen what we call 'comments' that I added to clarify what each line / action was doing. With methods, we usually do the same to explain the entire method through what we call 'documentation'.

To add documentation you can simply write '/**' and the IDE should complete the rest for you. The IDE will add the necessary information for you to fill :
* a small sentence that describes the method
* each input parameter and what they do
* what the method returns

for example (from one of my early projects, do not worry about figuring out what everything means or how they connect exactly + I would advise you to copy-paste it in a java file so you can see exactly how it shows)

```java
package asha9236.example;

public class Main {
	public static void main (String[] args) {}

    /**
     * checks if an ISBN is in a valid format
     * @param inputISBN the input isbn
     * @return the isbn if it is valid
     * @throws InvalidISBNException the exception thrown when the ISBN is not valid
     */
    protected String ISBNChecker(String inputISBN) throws InvalidISBNException {
        inputISBN = inputISBN.replace("-", "");
        if (inputISBN.length() != 13 && inputISBN.length() != 10) {
            throw new InvalidISBNException("ISBN must be exactly 10 or 13 characters long without dashes.");
        }
        for (char c : inputISBN.toCharArray()) {
            if (Character.isLetter(c)) {
                throw new InvalidISBNException("ISBN should not contain letters.");
            }
        }
        return inputISBN;
    }

    /**
     * displays the same type of error messages throughout the whole system
     * @param message the input message to be displayed
     */
    public void setErrorMessage (String message) {
        System.out.println("[ERROR : " + message + "]");
    }

    /**
     * changes the name of the logged-in user
     * @param console the sytsem console
     */
    public void settingsChangeName (Console console) {
        clearScreenSequence(console);
        appHeader();
        System.out.println(messages.getString("prompt.newName"));
        String newName = console.readLine();
        System.out.println(newName + "  " + messages.getString("prompt.choice") + "?");
        String ans = console.readLine().toUpperCase().charAt(0) + "";

        if (ans.equals("Y")) {
            model.changeName(newName);
        } else {
            view.setErrorMessage(messages.getString("error.message.operationAborted"));
            currentState = MenuState.SETTINGS;
        }
        currentState = MenuState.SETTINGS;
    }


    /**
     * Check if the student already borrowed the book by its ID
     * @param borrowedBooks the borrowed books list of the student
     * @param isbn the isbn of the book to be borrowed
     * @return true if the book is already borrowed, false if not
     */
    private boolean isAlreadyBorrowed (ArrayList<Book> borrowedBooks, String isbn) {
        for (Book borrowedBook : borrowedBooks) {
            if (borrowedBook.getISBN().equals(isbn)) {
                System.out.println(LocalizationManager.getMessage("book.owned"));
                return true;
            }
        }
        return false;
    }
}
```

Remember that while your code might make sense to you, at the moment you write it, it often doesn't automatically make sense to anyone else or even future you. Documentation and comments are here to help clarify your code to any other programmer or onlooker.


</span>
