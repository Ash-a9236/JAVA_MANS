<!--VARIABLES-->

[#8C8C07]:text
[#C9A176]:highlight
[#2C6485]:notes

<span style="color:#8C8CF7">

# <span style="color:#C9A176">CODING IN JAVA 00
## <span style="color:#C9A176">INTRODUCTION TO PROGRAMMING

<br>
TABLE OF CONTENTS <br>
<br> 01 . . [<span style="color:#8C8CF7">Base Concepts](#baseConcepts)
<br> 02 . . [<span style="color:#B9C3D6">Some Standards](#someStandards)
<br> 03 . . [<span style="color:#B9C3D6">IDEs](#ides)
<br> 04 . . [<span style="color:#B9C3D6">Types of coding and quirks](#codingTypes)
<br> 05 . . [<span style="color:#B9C3D6"> Number Systems](#numSystems)
<br> 06 . . [<span style="color:#B9C3D6">Us](#us)
<br> 07 . . [<span style="color:#B9C3D6">Data Types & NULL](#dataTypes)
<br> 08 . . [<span style="color:#B9C3D6">Im stuck!](#stuck)
  <!--
<br> &emsp; 01.01 . . [<span style="color:#B9C3D6">Some Standards](#someStandards)
<br> &emsp; 01.02 . . [<span style="color:#B9C3D6">IDEs](#ides)
<br> &emsp; 01.03 . . [<span style="color:#B9C3D6">Types of coding and quirks](#codingTypes)
<br> &emsp; 01.04 . . [<span style="color:#B9C3D6"> Number Systems](#methods) -->

<br>

________
### <a id="baseConcepts"><span style="color:#C9A176">01.00 BASE CONCEPTS</a>
________________

<br>
Coding is simply translating what you want to say in human-english to a computer-understandable language. It is putting abstact concepts like cats and bananas and making your computer make them do 'stuff', which is basically whatever you want. 
Learning how to code is mostly learning concepts through a language that then further translate to pretty much every programming language.
Of course, there are different types of programmings, but at the core, an int in Java will have the same definition in C++.

Those coding sheets will be using and teaching Java, an Object Oriented Programming language.

<br>

________
### <a id="someStandards"><span style="color:#C9A176">02.00 SOME STANDARDS</a>
________________

<br>
In programming, each language has its set of standards, especially for naming. 

In Java (and most other OOP languages) the standards are : 
<br> &emsp; - Variables are in camel case, therefore : the first word is never capitalized, all words are together, and every first letter of every word is capitalized (i.e. camelCase, num3, tryNum, fName, thisIsASentenceInCamelCase, etc.)
<br> &emsp; - Non-primary data types and classes start with a capital letter (i.e. Cat, Array, String, Banana, etc.)
<br> &emsp; - Constants and Enums are always named in all caps (i.e. TRYCOUNT, PI, NUMBER, E, etc.)
<br> &emsp; - Method naming should be simple and straight to the point (i.e. nameFormatting instead of willFormatAStringToCapitalizeTheFirstLetterOfEveryWord)
<br> &emsp; - Methods and classes should always think of the 'blackbox', AKA hide code from each other
<br> &emsp; - Methods should never be more than 50 lines of code
<br> &emsp; - When a piece of code is reused more than 3 times throughout your code, create a method and call it. **Avoid redundant code at all cost**
<br> &emsp; - Avoid unecessary spaces in the code (i.e. extra lines)
<br> &emsp; - Classes should always be organized (data fields, constructors, helper methods, equals and hashcode, getters and setters)

<br>

________
### <a id="ides"><span style="color:#C9A176">03.00 INTEGRATED DEVELOPMENT ENVIRONMENT</a>
________________

<br>

to code we need something called a <span style="color:C9A176">coding environment</span>, or <span style="color:C9A176">IDE</span> (Integrated Development Environment)

They are apps which contain everything you need to be able to code and then compile said code

They usually contain :
<br> &emsp; - Editor
<br> &emsp; - Compiler
<br> &emsp; - Debugger
<br> &emsp; - Terminal
<br> &emsp; - Version Control
<br> &emsp; - Code snippets & navigation
<br> &emsp; - Extensions and Plugins

> <span style="color:#2C6485"> For more information see  <a href="https://www.geeksforgeeks.org/what-is-ide/"><span style="color:#2C6485">**WHAT IS AN IDE?**</a>

IDE are usually paying, but they also usually have a <span style="color:C9A176">Communitiy Edition</span> which is free

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
```

<br>

<br>

________
### <a id="codingTypes"><span style="color:#C9A176">04.00 TYPES OF CODING & QUIRKS</a>
________________

<br>


<br>

________
### <a id="numSystems"><span style="color:#C9A176">04.00 NUMBER SYSTEMS</a>
________________

<br>

In programming (and other computer-related fields), you will come accross different number systems. While they are confusing at first, they do have a purpose : make it easier to read, write, and undestand binary code. 
They are basically shortcuts to make binary calculation, which makes it easier for a human to translate a random number, value, or even idea into something the computer can understand.

________
### <span style="color:#C9A176">04.01 COMPUTER MEMORY
________________

<br>

For obvious reasons, your computer cannot speak 'human'. Since the beginning of computing, we tried to make a numbering system that could work and that lead to the fewest possible errors. After quite a bit of searching, we settled down on a 2-digit system which we called 'binary'. Your computer can therefore only understand two states : there is electricity (on) and there is no electricity (off), which we directly translate to 0s and 1s called <span style="color:C9A176">bits</span>

<br>

#### <span style="color:#C9A176">04.02 BINARY
---------------------
<br>

the <span style="color:C9A176">binary system</span> counts in powers of <span style="color:C9A176">2</span> instead of our regular number system (decimal) which counts in powers of 10

binary numbers can only count in 0s and 1s therefore :

0000 = 0 (all set to 0)
<br>1000 = 1 (first position $2^0$ is set to 1 => $2^0$ * 1 = 1)
<br>0100 = 2 (position 1 ($2^0$) = 0 + position 2 ($2^1$) = 2 => 0 + 2 = 2)
<br>1100 = 3 (position 1 ($2^0$) = 1 + position 2 ($2^1$) = 2 => 1 + 2 = 3)
<br>0010 = 4 (position 1 ($2^0$) = 0 + position 2 ($2^1$) = 0 + position 3 ($2^2$) = 4 => 0 + 0 + 4 = 5)

etc.

<br>

a <span style="color:C9A176">byte</span> is composed of <span style="color:C9A176">8 bits</span>, therefore, <span style="color:C9A176">0000 0000</span>


| NAME | SYMBOL | SIZE (b) | SIZE (B) | SIZE (KB) | SIZE (MB) | SIZE (GB) |
|------|--------|----------|----------|-----------|-----------|-----------|
| BIT  |    b   |     1    |     -    |     -     |     -     |     -     |
| BYTE |    B   |     8    |     1    |     -     |     -     |     -     |
| KILOBYTE | KB |   8192   |    1024  |     1     |     -     |     -     |
| MEGABYTE | MB |  8 388 608 | 1 048 576 |  1024  |     1     |     -     |
| GIGABYTE | GB |     -    |1 073 741 824| 1 048 576 | 1024   |      1    |
| TERABYTE | TB |     -    |     -    |1 073 741 824 | 1048576 |   1024   |



<br>

#### <span style="color:#C9A176">04.03 CHARACTERS & ASCII
---------------------
<br>

> <span style="color:#2C6485"> For the ASCII reference sheet see  <a href="https://www.ascii-code.com/"><span style="color:#2C6485">**ASCII TABLE**</a>


characters such as letters and symbols are also represented in binary for computers.

to reference them, we use a reference sheet called the <span style="color:C9A176">ASCII code</span>, which uses 8 bit for every character

each letter has a reference number which *all programming languages understand* and can lead to programming errors when defining and setting data types and variables

(ex. char letter = 'a'; => char + 1; will return 'b' BUT int number = a; will return 96 since the ASCII for lower case a is 96)


<br>

#### <span style="color:#C9A176">04.04 OTHER SYSTEMS
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


for reference, <span style="color:C9A176">1 byte</span> is <span style="color:C9A176">0000</span> and will range from <span style="color:C9A176">0</span> to <span style="color:C9A176">255</span> (256 total values - the 0 value)



<br>

________
### <a id="us"><span style="color:#C9A176">05.00 US</a>
________________

<br>

After all of this information, we should start coding a bit! 
Throughout this manual, I will use IntelliJ IDEA Community Edition IDE but feel free to use which ever you prefer. The shortcuts might not be the same but the idea will always be the same.

For the syntax and everything as the code, we will have those general rules :
<br> * All curly brackets will be on the same line
<br> * We will use the camel case naming system (thisIsAVariable)
<br> * IntelliJ IDEA
<br> * Maven will be our build
<br> * JUnit for testing
<br> * JavaFX for any UI
<br> * SDK 21
<br> * GitHub & Git for version control

<br>

________
### <a id="dataTypes"><span style="color:#C9A176">06.00 DATATYPES & NULL</a>
________________

<br>

variables can be different <span style="color:C9A176">data types</span>, which we define, to tell the computer what 'stuff' something is. Some languages (like JavaScript, Python, Ruby, ect.) do not necessitate explicit data type definition. They are called <span style="color:C9A176">dynamically typed</span> (or untyped) languages. Java is **not** one of those languages. You will need to specify everything from start to finish. For example, if we want to define a simple integer (number), like 4, the compilier doesn't know what '4' is, therefore, we add <span style="color:C9A176">int</span> in front of it, thus defining 4 for the computer

Java, like every programming language can do automatic conversions, which is when you force (cast) a type uppon a variable of another type. Conversions towards higher values can work while conversions towards lower values are not recommended since information will be lost or the system will crash. For example, you can convert an integer (4) to a double (4.0) without a problem. The compiler will simply add the decimal point. But, converting the double (4.5) to the integer (4), Java will not do a rounding. It will simply remove the decimal point. 

> <span style="color:#2C6485"> For the type casting reference in Java see  <a href="https://storage.googleapis.com/www.examclouds.com/primitives/widening-conversions.png"><span style="color:#2C6485">**AUTOMATIC CONVERSION IN JAVA**</a>


<br>

#### <a id="primitive"><span style="color:#C9A176">02.01 PRIMITIVE</a>
---------------------
<br>

primitive data types are data that is <span style="color:C9A176">directly referenced</span> in the memory of the computer as a series of bytes (0 and 1) they can hold a maximum value defined by the number of bytes they are defined to occupy in the computer memory

| NAME | SYMBOL | SIZE | MIN VALUE | MAX VALUE | 
|------|--------|------|-----------|-----------|
| integer | <span style="color:C9A176">int</span> | 4 bytes | -2 147 483 648 | 2 147 483 647 |
| double | <span style="color:C9A176">double</span> | 8 bytes | -1.79769313486232 e 308 | 1.79769313486232 e 308 |
| float | <span style="color:C9A176">float</span> | 4 bytes | -3.402823 e 38 | 3.402823 e 38 |
| boolean | <span style="color:C9A176">bool</span> | 1 byte | false | true |
| character | <span style="color:C9A176">char</span> | 2 bytes |  | |

<br>

#### <a id="nonPrimitive"><span style="color:#C9A176">02.02 NON-PRIMITIVE</a>
---------------------
<br>

In programming languages, non-primitive data types are data types which are actually <span style="color:C9A176">classes</span>. Non-primitive data types are <span style="color:C9A176">not directly referenced</span> in the memory, but the computer rather holds the <span style="color:C9A176">memory address</span> of the class. 
In Java the only non-primitive data type (for now) is the <span style="color:C9A176">String</span>. It is easier to see it in java as it is written with a capitalized s (String), therefore defining it as a class

-> the string is a sequence of characters

non-primitive data types also contain methods which can be used to modify them (for example : <span style="color:C9A176">.toUpperCase()</span> which capitalizes every letter of a given string)

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

#### <a id="nullDataType"><span style="color:#C9A176">02.02 NULL</a>
---------------------
<br>

In programming, you will see a lot of 'NULL' and NULL handling. 
The null is a pointer in the memory which is the holder value for 'nothing'. It does not hold a value and rather carries the pointer towards a specific memory address which the compiler knows as null.
Be careful : 
<br> &emsp; - NULL can only be assigned to reference-type data types, or non-primitive data types
<br> &emsp; - NULL doesn't mean 'empty' or 'zero' (String = null; is not equal to String = "";)
<br> &emsp; - Checking for null is always recommended to avoid the null pointer exceptions


________
### <a id="stuck"><span style="color:#C9A176">09.00 IM STUCK!</a>
________________

<br>


