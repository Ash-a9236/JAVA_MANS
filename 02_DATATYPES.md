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

# <span style="color: var(--title)">CODING IN JAVA 02
## <span style="color: var(--title)">DATATYPES

<br>
TABLE OF CONTENTS <br> <br>

[<span style="color: var(--link)">01 . . Base Concepts</span>](#base-concepts) <br>
[<span style="color: var(--link)">02 . . Primary Datatypes</span>](#primary-datatypes) <br>
[<span style="color: var(--link)">03 . . String</span>](#strings) <br>
[<span style="color: var(--link)">04 . . Arrays</span>](#arrays) <br>
    <!--&emsp; [<span style="color: var(--link)">01 . . Return Type</span>](#return-types) <br>
    &emsp; [<span style="color: var(--link)">02 . . High and Low</span>](#coding-types-high-and-low) <br>-->
[<span style="color: var(--link)">05 . . ArrayList</span>](#arraylist) <br> 
[<span style="color: var(--link)">06 . . In memory</span>](#in-memory) <br> 

<br>

________
### <a name="base-concepts"><span style="color: var(--title)">01.00 BASE CONCEPTS</span></a>
________________

<br>

As I mentionned before, JVM (Java Virtual Machine) and compiler are not interpreter. Basically, <span style="color: var(--highlight)">they cannot assume the data type of a variable as would an interpreter</span>. This means that you, the programmer, needs to <span style="color: var(--highlight)">define everything</span> for the compiler.

Identifying a data type is your way of saying to your compiler 'this is this, and you can do action 1, action 2, and action 3 with it'.

Data types come into 2 types (technically 3, but we will see the generics later): primary and non-primary data types. Primary data types are what we call 'directly referenced in memory' and are data types to which you can perform basic opetations to. At the opposite, non-primary, or 'reference data types' are classes, so actual objects that need built-in methods (methods that are predefined within Java, but still methods) to perfom the same actions as the primary data types, and more. 

The way to differencitate the primary from the reference data types is : 

| PRIMARY      | REFERENCE     |
|--------------|---------------|
| declaration in all lowercase (i.e. int, double) | declaration with the first letter capitalized (i.e. String) |
| cannot call built-in methods (i.e. int.toUpperCase() is invalid) | has build-in methods (i.e. randomString.toUpperCase()) |
| prints the value automatically | need to call the toString() method to print, if not, will print the memory address |


You need to note that each primary data type has its own 'wrapper class', which basically mean, its own non-primary data type equivalent. They are here to perform operations when the primary data type fails, in a few edge cases. 

| PRIMARY  | WRAPPER     |
|----------|-------------|
| int      | Integer()   |
| double   | Double()    |
| float    | Float()     |
| char     | Character() |



<br>

________
### <a name="primary-datatypes"><span style="color: var(--title)">02.00 PRIMARY DATATYPES</span></a>
________________

<br>

As mentionned in the introduction, primary datatypes are directly referenced, which basically means they are directly translated to binary in your computer. In the INTRODUCTION.md sheet, you might remeber the table I gave you : 

| NAME | SYMBOL | WRAPPER CLASS | SIZE | MIN VALUE | MAX VALUE | 
|------|--------|---------------|------|-----------|-----------|
| integer | <span style="color: var(--highlight)">int</span> | Integer | 4 bytes | -2 147 483 648 | 2 147 483 647 |
| double | <span style="color: var(--highlight)">double</span> | Double | 8 bytes | -1.79769313486232 e 308 | 1.79769313486232 e 308 |
| float | <span style="color: var(--highlight)">float</span> | Float | 4 bytes | -3.402823 e 38 | 3.402823 e 38 |
| boolean | <span style="color: var(--highlight)">bool</span> | Boolean |1 byte | false | true |
| character | <span style="color: var(--highlight)">char</span> | Character | 2 bytes | \u0000 (or 0) | \uffff (or 65 535) |

Those are the basic primary data types which you will mostly use in your code.

Apart from the boolean, all of the otehr data types are numbers. Even char, it just references the unicode sheet as I mentionned before, but at the end of the day, it is a number which your computer simply translates from a letter (you can even declare you char as numbers, which your computer will translate, like so : char a = 92;).
The only difference between all of those binary declarations are 
1. if there is a floating point (yes to all, except for integer, boolean, char)
2. what is the low and high bound

knowing point #1 is the most important, point #2 is mostly for memory optimization, which you do not particularly need to think about at the moment since java automatically allocates (gives memory to data) and deprecates (marks the memory as 'free to use' when you are finished with it) memory.


<br>

#### <a id="console-print"><span style="color: var(--title)">02.01 OPERATIONS AND FLOATING POINTS</span></a>
________________

<br>






</span>
