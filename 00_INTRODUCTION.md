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

# <span style="color: var(--title)">CODING IN JAVA 00
## <span style="color: var(--title)">INTRODUCTION TO PROGRAMMING

<br>
TABLE OF CONTENTS <br> <br>

[<span style="color: var(--link)">01 . . Base Concepts</span>](#base-concepts) <br>
[<span style="color: var(--link)">02 . . Some Standards</span>](#some-standards) <br>
[<span style="color: var(--link)">03 . . IDEs</span>](#ides) <br>
[<span style="color: var(--link)">04 . . Types of coding and quirks</span>](#coding-types) <br>
    &emsp; [<span style="color: var(--link)">01 . . Types of coding</span>](#coding-types-types) <br>
    &emsp; [<span style="color: var(--link)">02 . . High and Low</span>](#coding-types-high-and-low) <br>
    &emsp; [<span style="color: var(--link)">03 . . Quirks</span>](#coding-types-quirks) <br>
[<span style="color: var(--link)">05 . . Number Systems</span>](#number-systems) <br> 
    &emsp; [<span style="color: var(--link)">01 . . Computer Memory</span>](#number-systems-computer-memory) <br>
    &emsp; [<span style="color: var(--link)">02 . . Binary</span>](#number-systems-binary) <br>
    &emsp; [<span style="color: var(--link)">03 . . Other Systems</span>](#number-systems-other-systems) <br>
[<span style="color: var(--link)">06 . . Us</span>](#us) <br> 
[<span style="color: var(--link)">07 . . Data Types & NULL</span>](#data-types) <br>
  &emsp; [<span style="color: var(--link)">01 . . Primitive</span>](#data-types-primitive) <br>
  &emsp; [<span style="color: var(--link)">02 . . Non-Primitive</span>](#data-types-non-primitive) <br>
  &emsp; [<span style="color: var(--link)">03 . . Null</span>](#data-types-null) <br>
  <!--
<br> &emsp; 01.01 . . [<span style="color:#B9C3D6">Some Standards](#someStandards)
<br> &emsp; 01.02 . . [<span style="color:#B9C3D6">IDEs](#ides)
<br> &emsp; 01.03 . . [<span style="color:#B9C3D6">Types of coding and quirks](#codingTypes)
<br> &emsp; 01.04 . . [<span style="color:#B9C3D6"> Number Systems](#methods) -->

<br>

________
### <a name="base-concepts"><span style="color: var(--title)">01.00 BASE CONCEPTS</span></a>
________________

<br>
Coding is simply <span style="color: var(--highlight)">translating</span> what you want to say in human-english to a computer-understandable language. It is putting abstact concepts like cats and bananas and making your computer make them do 'stuff', which is basically whatever you want. 
<br><br>
Learning how to code is mostly learning concepts through a language that then further translate to pretty much every programming language.
Of course, there are different types of programmings, but at the core, an int in Java will have the same definition in C++.
<br><br>
Those coding sheets will be using and teaching <span style="color: var(--highlight)">Java</span>, an <span style="color: var(--highlight)">Object Oriented Programming language</span>.



<br> <br>

________
### <a id="some-standards"><span style="color: var(--title)">02.00 SOME STANDARDS</a>
________________

<br>
In programming, each language has its set of standards, especially for naming. <br> 
In Java (and most other OOP languages) the standards are : <br> <br>

* <span style="color: var(--highlight)">Variables are in camel case</span> : the first word is never capitalized, all words are together, and every first letter of every word is capitalized (i.e. camelCase, num3, tryNum, fName, thisIsASentenceInCamelCase, etc.) <br> <br>
*  <span style="color: var(--highlight)">Non-primary data types and classes start with a capital letter</span> (i.e. Cat, Array, String, Banana, etc.) <br> <br>
* <span style="color: var(--highlight)">Constants and Enums are always named in all caps</span> : TRYCOUNT, PI, NUMBER, E, etc. <br> <br>
* <span style="color: var(--highlight)">Method naming should be simple</span> and straight to the point : nameFormatting instead of willFormatAStringToCapitalizeTheFirstLetterOfEveryWord <br> <br>
* <span style="color: var(--highlight)">Methods and classes should always think of the 'blackbox'</span> : hide code from each other <br> <br>
* <span style="color: var(--highlight)">Methods should never be more than 50 lines of code</span> <br><br>
* When a piece of code is reused more than 3 times throughout your code, create a method and call it. <span style="color: var(--highlight)">Avoid redundant code at all cost</span> <br> <br>
* <span style="color: var(--highlight)">Avoid unecessary spaces in the code</span> (i.e. extra lines) <br> <br>
* <span style="color: var(--highlight)">Classes should always be organized</span> : data fields, constructors, helper methods, equals and hashcode, getters and setters <br> <br>
* <span style="color: var(--highlight)">Every method should have its documentation</span>

<br>

________
### <a id="ides"><span style="color: var(--title)">03.00 INTEGRATED DEVELOPMENT ENVIRONMENT</a>
________________

<br>

to code we need something called a <span style="color: var(--highlight)">coding environment</span>, or <span style="color: var(--highlight)">IDE</span> (Integrated Development Environment)

They are apps which contain everything you need to be able to code and then compile said code

They usually contain :
<br> &emsp; - Editor
<br> &emsp; - Compiler
<br> &emsp; - Debugger
<br> &emsp; - Terminal
<br> &emsp; - Version Control
<br> &emsp; - Code snippets & navigation
<br> &emsp; - Extensions and Plugins

> For more information see <a href="https://www.geeksforgeeks.org/what-is-ide/"><span style="color: var(--link)">**WHAT IS AN IDE?**</a></span>

IDE are usually paying, but they also usually have a <span style="color: var(--highlight)">Communitiy Edition</span> which is free

Some popular IDEs include :
<br> &emsp; - Visual Studio Code
<br> &emsp; - Visual Studio 22
<br> &emsp; - IntelliJ IDEA
<br> &emsp; - PyCharm
<br> &emsp; - Eclipse


When you compile and run the code, a new window will open either in the IDE's built-in terminal, or in your computer's terminal itself
it will contain the output of the code

If the code contains an error, the terminal will also display the error type and where it is, for easier debugging


<br>

```java
public class Main {
    public static void main (String[] args) {
        System.out.println("Hello World !");
    }
}
```

Console :
```
Hello World !

Process finished with exit code 0
```

<br>

<br>

________
### <a id="coding-types"><span style="color: var(--title)">04.00 TYPES OF CODING & QUIRKS</a>
________________

<br>
In this manual, we will go through programming with Java but, as you might have guessed, there are many many more programming languages and types of programming.
<br><br>

>*note that I will simplify and only present two styles in this manual*

<br>

________
### <a id="coding-types-types"><span style="color: var(--title)">04.01 TYPES</span></a>
________________

<br>

As mentionned, Java is an <span style="color: var(--highlight)">OOP</span> or <span style="color: var(--highlight)">Object Oriented</span>. This is one of the most used type of programming right now! For example, the Windows OS (operating system) is programmed in OOP languages (C++, C) (You can access its object through the hive, AKA Regedit).
<br> In OOP, the compiler will be able to 'jump' from action to actions or file to file through 'method calls'. This allows us to write and organize code more efficiently.

<br>


```java
public class Main {
    public static void main (String[] args) {
        System.out.println("Hello World !");
        methodC(); //'calling' the method 'methodC'
        methodA();
        methodB();
    }

    public static void methodA () {
        System.out.println("methodA"); //prints methodA on the console
    }

       public static void methodB () {
        System.out.println("methodB");
    }

       public static void methodC () {
        System.out.println("methodC");
    }
}
```

Console :
```console
methodC
methodA
methodB

Process finished with exit code 0
```

<br><br>
Another style is called <span style="color: var(--highlight)">scripting</span>. At the opposite of OOP, the compiler cannot 'jump' between objects, files, and actions, but rather goes and executes everything line by line.

<br>
For example, HTML and CSS (for webpages) are scripting languages. Bash (in your terminal) and git are both scripting languages as well.

<br>

Bash scripting (you can copy-paste it line by line in your terminal as well!): 

```console
echo hello
echo 'this is line 1'
echo 'I cannot go back to line 1'
```

Console :
```console
hello
this is line 1
I cannot go back to line 1

Process finished with exit code 0
```

<br> <br>

________
### <a id="coding-types-high-and-low"><span style="color: var(--title)">04.02 HIGH & LOW</span></a>
________________

<br>

You can also differenciate programming languages with how close they are to english vs how close they are to machine language.
The <span style="color: var(--highlight)">closer to the machine the lower their level of abstraction is</span>. Basically, the lower they are, the more you need to understand how the machine works, and the more you will need to declare everything for your computer. 
The lowest programming language (apart from binary) is called Assembly. It was the first programming language and is one-to-one with binary, hence why it is so low.

When we are talking about high level programming languages, we mean languages that are almost like written english. They might seem more intuitive but be mindful that they hide *a lot*, which we call 'abstraction'.

The furtest you go from the hardware, the more abstraction you add to your program. You will see that concepts from the first few ideas we will go through are very close to what the machine does and how it handles basic computation. As we go, we will remove ourselves gradually from me & the machine, and the questions of 'how will the computer understand this?' and slowly go to more abstract concepts.


|            | HIGH | LOW  |
|------------|------|------|
| **Fridenly to** | Programmer | Machine|
| **Understandable** | Easy | Not really |
| **Readability** | Easy | Complex |
| **Debugging** | Easy | Complex |
| **Maintenance** | Easy | Complex |
| **Portable** | Yes | No |
| **Runs on** | Anything | Machine-dependent |
| **Translation to binary with** | Compiler / Interpreter | Assembler |
| **Used** | Widely | Not common |
| **Execution speed** | Slow | Fast |


A few languages by levels, lowest to highest :

Machine language > Assembly > C > C++ > Rust > Go > Java > JavaScript > Ruby > Python

* <span style="color: var(--highlight)">Machine Code and Assembly</span> are still the lowest in terms of how close they are to the hardware. <br>
* <span style="color: var(--highlight)">C and C++</span> are very close to hardware as well, with C++ adding more abstraction features like OOP. <br>
* <span style="color: var(--highlight)">Rust</span> is a modern systems language that provides memory safety with low-level control. <br>
* <span style="color: var(--highlight)">Go</span> is designed for simplicity and performance, with some higher-level abstractions. <br>
* <span style="color: var(--highlight)">Java</span> runs on the JVM, offering portability and automatic memory management. <br>
* <span style="color: var(--highlight)">JavaScript</span> is a higher-level scripting language primarily used for web development. <br>
* <span style="color: var(--highlight)">Ruby</span> is even higher-level, known for its elegant syntax and simplicity. <br>
* <span style="color: var(--highlight)">Python</span> is very high-level and emphasizes ease of use, often abstracting away many details of memory and processing. <br>

*All from ChatGPT summary*

<br>

________
### <a id="coding-types-quirks"><span style="color: var(--title)">04.03 QUIRKS</span></a>
________________

<br>

All programming languages have 'quirks' that you need to be aware of. In Java, you must note (principally) that 

* It is <span style="color: var(--highlight)">case sensitive</span> : hello and HELLO are not the same, int a = 2; and int A  = 2; are not the same
* You need to <span style="color: var(--highlight)">define the type of variable</span> : Java does not have an interpreter, therefore it cannot 'guess' or 'assume' the type of a variable
* You need to <span style="color: var(--highlight)">define the access modifiers</span> for the methods : public, private, protected, default
* <span style="color: var(--highlight)">Automatic garbage collection</span> : you do not need to worry about the discarded objects and variables
* <span style="color: var(--highlight)">NullPointerException</span> : is an exception that you will see a lot and will have to debug a lot. Java is not able to handle null pointers and therefore exits if the null is not manually handled
* <span style="color: var(--highlight)">Wrapper Classes</span> are different from their primitive data types. This leads to type conversion errors when you upcast or downcast.
* <span style="color: var(--highlight)">No multiple inheritance</span> : a child can only have one parent (which we can override by implementing multiple interfaces)
* <span style="color: var(--highlight)">No multiple return values</span> : each method can only return one type of value and one value only (we can override this by returning an object or an array)


Other programming languages have their own quirks, like SQL that is case insensitive and differs between DBMS (Database Management System), or python that needs to have specific indentation. Once you learn them programming in that language becomes relatively easy, especially if you know the base concepts.



<br> <br>

________
### <a id="number-systems"><span style="color: var(--title)">05.00 NUMBER SYSTEMS</a></span>
________________

<br>

In programming (and other computer-related fields), you will come accross different <span style="color: var(--highlight)">number systems</span>. While they are confusing at first, they do have a purpose : make it easier to read, write, and undestand binary code. 
They are basically shortcuts to make binary calculation, which makes it easier for a human to translate a random number, value, or even idea into something the computer can understand.

<br>

________
### <a id="number-systems-computer-memory"><span style="color: var(--title)">05.01 COMPUTER MEMORY</span></a>
________________

<br>

Your computer has two memories : the <span style="color: var(--highlight)">RAM</span> (Rapid / Random Access Memory) and the <span style="color: var(--highlight)">SSD</span> (Solid State Drive). The SSD is like a giant library that contains everything from your operating system (OS like Windows, Mac, Linux, Adroid, ect.) to your word documents or even this file. 
<br> The RAM is like a cart beside the librarian's desk where all the books you are using at the moments are stored. The RAM makes it easier and faster to access them.
<br> When you are programming, you are only using the RAM. All the variables, objects and the program itself will run on the RAM.

For obvious reasons, your computer cannot speak 'human'. Since the beginning of computing, we tried to make a numbering system that could work and that lead to the fewest possible errors. After quite a bit of searching, we settled down on a 2-digit system which we called 'binary'. Your computer can therefore only understand two states : there is electricity (on) and there is no electricity (off), which we directly translate to 0s and 1s called <span style="color: var(--highlight)">bits</span>

<br>

#### <a id="number-systems-binary"><span style="color: var(--title)">05.02 BINARY</span></a>
---------------------
<br>

the <span style="color: var(--highlight)">binary system</span> counts in powers of <span style="color: var(--highlight)">2</span> instead of our regular number system (decimal) which counts in powers of 10

binary numbers can only count in 0s and 1s therefore :

0000 = 0 (all set to 0)
<br>1000 = 1 (first position $2^0$ is set to 1 => $2^0$ * 1 = 1)
<br>0100 = 2 (position 1 ($2^0$) = 0 + position 2 ($2^1$) = 2 => 0 + 2 = 2)
<br>1100 = 3 (position 1 ($2^0$) = 1 + position 2 ($2^1$) = 2 => 1 + 2 = 3)
<br>0010 = 4 (position 1 ($2^0$) = 0 + position 2 ($2^1$) = 0 + position 3 ($2^2$) = 4 => 0 + 0 + 4 = 4)

etc.

<br>

a <span style="color: var(--highlight)">byte</span> is composed of <span style="color: var(--highlight)">8 bits</span>, therefore, <span style="color: var(--highlight)">0000 0000</span>


| NAME | SYMBOL | SIZE (b) | SIZE (B) | SIZE (KB) | SIZE (MB) | SIZE (GB) |
|------|--------|----------|----------|-----------|-----------|-----------|
| BIT  |    b   |     1    |     -    |     -     |     -     |     -     |
| BYTE |    B   |     8    |     1    |     -     |     -     |     -     |
| KILOBYTE | KB |   8192   |    1024  |     1     |     -     |     -     |
| MEGABYTE | MB |  8 388 608 | 1 048 576 |  1024  |     1     |     -     |
| GIGABYTE | GB |     -    |1 073 741 824| 1 048 576 | 1024   |      1    |
| TERABYTE | TB |     -    |     -    |1 073 741 824 | 1048576 |   1024   |



<br>

#### <a id="number-systems-characters-and-ascii"><span style="color: var(--title)">05.03 CHARACTERS & ASCII</span></a>
---------------------
<br>

> For the ASCII reference sheet see <a href="https://www.ascii-code.com/"><span style="color: var(--link)">**ASCII**</a></span> <br>For the Unicode reference chart see <a href="https://www.unicode.org/charts/"><span style="color: var(--link)">**UNICODE**</a></span>


All characters such as letters and symbols are also represented in binary for computers like numbers. It is an international standard for computer science and all informatics related stuff. The ASCII table is the english subset of the unicode table, wich encodes every symbol and letter from all the world's languages. Unicode also references emojis and their behaviours (hence why a smily face on apple is also a smily face on android). <br>

To reference them, we use a reference sheet called the <span style="color: var(--highlight)">ASCII code</span>, which uses 8 bit for every character, where each letter has a reference number which *all programming languages understand* and can lead to programming errors when defining and setting data types and variables in Java.

(ex. char letter = 'a'; => char + 1; will return 'b' BUT int number = a; will return 96 since the ASCII for lower case a is 96)


<br>

#### <a id="number-systems-other-systems"><span style="color: var(--title)">05.04 OTHER SYSTEMS</a></span>
---------------------
<br>

through programming we use different numbering system to be able to communicate more effectively with a computer (after all, computers think in binary, not in decimals)

The one that is the most used in other field is the HEXADECIMAL system, for mostly colours. 


| NAME | BASE | REFERENCE | DIGITS | EXAMPLE |
|------|------|-----------|--------|---------|
| DECIMAL | 10 | 0 - 9    | 0 - 9  | 54 |
| BINARY  | 2  | 0, 1     | 0 - 1  | 0010 1101 |
| OCTAL   | 8  | BINARY   | 0 - 7  | 7 (111 in binary) |
| HEXADECIMAL | 16 | BINARY | 1 - 9 + A - F | 01FA29 (is also used as colour code)|


for reference, <span style="color: var(--highlight)">1 byte</span> is <span style="color: var(--highlight)">0000</span> and will range from <span style="color: var(--highlight)">0</span> to <span style="color: var(--highlight)">255</span> (256 total values - the 0 value)



<br>

________
### <a id="us"><span style="color: var(--title)">06.00 US</a></span>
________________

<br>

After all of this information, we should start coding a bit! 
<br> First and foremost you will need to <a href="https://www.oracle.com/java/technologies/downloads/#jdk24-windows"><span style="color: var(--link)">install Java on your computer</a></span>. 

> please NEVER EVER EVER install anything if its not from an official source (the actual developpers) and without verifying the installation through the provided key. All installation instructions are in the documentation provided by the developper. FOLLOW THEM. <br> If you run into a problem, if your computer crashes, if you are unsure of the source, etc., trying to undo those installations is long and hard and sometimes near impossible without having to wipe the entirety of your computer. <br> Make sure you know what you are doing before doing. (trust me on this one. Trust the fact that you should trust no one except those who are legally bounded to give you this trust).

<br> Throughout this manual, I will use <a href="https://www.jetbrains.com/idea/download/?source=post_page---------------------------&section=windows"><span style="color: var(--link)">**IntelliJ IDEA Community Edition**</a> IDE but feel free to use which ever you prefer. The shortcuts might not be the same but the idea will always be the same.

For the syntax and everything as the code, we will have those general rules (you can update them in the settings of your IDE) :
* All curly brackets will be on the same line <br>
* We will use the camel case naming system (thisIsAVariable) <br>
* <a href="https://www.jetbrains.com/idea/download/?source=post_page---------------------------&section=windows"><span style="color: var(--link)">IntelliJ IDEA</a></span> (to download) <br>
* <a href="https://maven.apache.org/what-is-maven.html"><span style="color: var(--link)">Maven</a></span> will be our build (to select on every new project) <br>
* <a href="https://mvnrepository.com/artifact/junit/junit"><span style="color: var(--link)">JUnit</a></span> for testing (to add to any new project later) <br>
* JavaFX for any UI <br>
* SDK and JDK 21 or higher (to download through IntelliJ) <br>
* <a href="https://desktop.github.com/download/"><span style="color: var(--link)">GitHub</a></span> & <a href="https://git-scm.com/downloads"><span style="color: var(--link)">Git</a></span> for version control (for now I advise you to only download GitHub desktop) <br>

As a reference, you should always have those settings :

![image info](/Images/00_INTRODUCTION_00_createAProjectSettings.png)

<!-- 
IF THE FIRST IMAGE DOESNT LOAD : UNCOMMENT THIS
<img src="/Images/00_INTRODUCTION_00_createAProjectSettings.png" alt="creating a new project settings"/>
-->

The only thing you need to change is the GroupId : change it to your GitHub handle or any marking that will act as your copyright. It will appear on any piece of code that you will write and therefore mark it as yours.

<br>

________
### <a id="data-types"><span style="color: var(--title)">07.00 DATATYPES & NULL</a></span>
________________

<br>

variables can be different <span style="color: var(--highlight)">data types</span>, which we define, to tell the computer what 'stuff' something is. Some languages (like JavaScript, Python, Ruby, ect.) do not necessitate explicit data type definition. They are called <span style="color: var(--highlight)">dynamically typed</span> (or untyped) languages. Java is **not** one of those languages. You will need to specify everything from start to finish. For example, if we want to define a simple integer (number), like 4, the compilier doesn't know what '4' is, therefore, we add <span style="color: var(--highlight)">int</span> in front of it, thus defining 4 for the computer

Java, like every programming language can do automatic conversions, which is when you force (cast) a type uppon a variable of another type. Conversions towards higher values can work while conversions towards lower values are not recommended since information will be lost or the system will crash. For example, you can convert an integer (4) to a double (4.0) without a problem. The compiler will simply add the decimal point. But, converting the double (4.5) to the integer (4), Java will not do a rounding. It will simply remove the decimal point. 

> For the type casting reference in Java see  <a href="https://storage.googleapis.com/www.examclouds.com/primitives/widening-conversions.png"><span style="color: var(--link)">**AUTOMATIC CONVERSION IN JAVA**</a></span>


<br>

#### <a id="data-types-primitive"><span style="color: var(--title)">07.01 PRIMITIVE</a></span>
---------------------
<br>

primitive data types are data that is <span style="color: var(--highlight)">directly referenced</span> in the memory of the computer as a series of bytes (0 and 1) they can hold a maximum value defined by the number of bytes they are defined to occupy in the computer memory

It is important to know the basic minimum and maximum value for your datatypes for specific cases. For example, doing a calculator with only ints will make you run into problems if you try to input numbers that will add to one higher than the maximum value. Another example would be trying to store phone numbers in ints (which will definitly not work : trust me we all tried).

| NAME | SYMBOL | WRAPPER CLASS | SIZE | MIN VALUE | MAX VALUE | 
|------|--------|---------------|------|-----------|-----------|
| integer | <span style="color: var(--highlight)">int</span> | Integer | 4 bytes | -2 147 483 648 | 2 147 483 647 |
| double | <span style="color: var(--highlight)">double</span> | Double | 8 bytes | -1.79769313486232 e 308 | 1.79769313486232 e 308 |
| float | <span style="color: var(--highlight)">float</span> | Float | 4 bytes | -3.402823 e 38 | 3.402823 e 38 |
| boolean | <span style="color: var(--highlight)">bool</span> | Boolean |1 byte | false | true |
| character | <span style="color: var(--highlight)">char</span> | Character | 2 bytes | \u0000 (or 0) | \uffff (or 65 535) |

<br>

In your ide, it will look like this :

```java
public class Main {
    public static void main (String[] args) {
        int num1 = 3;
        double num2 = 5.5;
        float num3 = 5.6;
        boolean isTrue = true;
        char char1 = 'a';

        double addition = num1 + num2; //8.5
        addition = addition + num3; //14.1
    }
}
```

<br>

#### <a id="data-types-non-primitive"><span style="color: var(--title)">07.02 NON-PRIMITIVE</a></span>
---------------------
<br>

In programming languages, non-primitive data types are data types which are actually <span style="color: var(--highlight)">classes</span>. Non-primitive data types are <span style="color: var(--highlight)">not directly referenced</span> in the memory, but the computer rather holds the <span style="color: var(--highlight)">memory address</span> of the class. 
In Java the only non-primitive data type (for now) is the <span style="color: var(--highlight)">String</span>. It is easier to see it in java as it is written with a capitalized s (String), therefore defining it as a class

-> the string is a sequence of characters

non-primitive data types also contain methods which can be used to modify them (for example : <span style="color: var(--highlight)">.toUpperCase()</span> which capitalizes every letter of a given string)

<br>

```java
public class Main {
    public static void main (String[] args) {
        String name = "John Doe";
        printName(name); //calling the method
    }

    //method
    public void printName (String name) { 
        System.out.println(name); //will print the memory address, not the value

        name.toString(); //will print the value of the string : John Doe
    }  
}
```

<br>

#### <a id="data-types-null"><span style="color: var(--title)">05.03 NULL</a></span>
---------------------
<br>

In programming, you will see a lot of 'NULL' and NULL handling. 
The null is a pointer in the memory which is the holder value for 'nothing'. It does not hold a value and rather carries the pointer towards a specific memory address which the compiler knows as null.
Be careful : 
<br> &emsp; - NULL can only be assigned to reference-type data types, or non-primitive data types
<br> &emsp; - NULL doesn't mean 'empty' or 'zero' (String = null; is not equal to String = "";)
<br> &emsp; - Checking for null is always recommended to avoid the null pointer exceptions



</span>

