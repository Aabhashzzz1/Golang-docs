# GoLang

> Go language is a programming language initially developed at Google in the year 2007 by Robert Griesemer, Rob Pike, and Ken Thompson. It is a statically-typed language having syntax similar to that of C. It provides garbage collection, type safety, dynamic-typing capability, many advanced built-in types such as variable length arrays and key-value maps. It also provides a rich standard library. The Go programming language was launched in November 2009 and is used in some of the Google's production systems.

## Features

```go
The most important features of Go programming are listed below-
1. Support for environment adoption patterns similar to dynamic languages. For example, type inference (x:=0 is valid declaration of a variable x of type int)
2. Compilation time is fast.
3. In-built concurrency support:- lightweight processes (via go routines), channels select statement.
4. Go programs are simple, concise and safe.
5. Support for interfaces and Type embedding.
6. Production of statically linked native binaries without external dependencies.

Other features-
1. Support for type inheritance.
2. Support for method or operator overloading.
3. Support for circular dependencies among packages.
4. Support for pointer arithmetic.
5. Support for assertions.
6. Support for generic programming.
```

## Go program extension

> It should be written into one or more test files with the extension **`.go`**
>
> For example- `hello.go`

## Program Structure

> A go program basically consits of the following parts-
>> * Package declaration
>> * Import packages
>> * Functions
>> * Variables
>> * Statements and Expressions
>> * Comments


> Let us look simple code that would print the words "Hello World"-
```go
package main

import "fmt"
func main() {
    /* This is a sample program */
    fmt.Println("Hello, World!")
}
```

> Let us take at the various parts of the above program-
>> * The line of the program package main defines the packages name in which this program should lie. It is a mandatory statement, as Go programs run in packages. The main package is the starting point to run the program. Each package has a path and name associated with it
>> * The next line import "fmt" is a proprocessor command which tells the Go compiler to include the files lying in the package fmt.
>> * The next line func main() is the main function where the program execution begins.
>> * The next line /*...*/ is ignored by the compiler and it is there to add comments in the program. Comments are also represented using // similar to Java, Javascript or C++ comments
>> * The next line fmt.Println(...) is another function available in Go which causes the message "Hello, World!" to be displayed on the screen. Here fmt package has exported Println mathod which is used to display the message on the screen
>> * Notice: The capital P of Println method. In Go language, a name is exported if it starts with capital letter. Exported means the function or variable/constant is accessible to the importer of the respective package.

## Executing a program
> `Let us discuss how to save the source code in a file, compile it and finally execute the program. Please follow the steps given below-`
>> * `Open a text editor and add the above-mentioned code.`
>> * `Save the file as hello.go`
>> * `Open the command prompt.`
>> * `Go to the directory where you saved the file.`
>> * `Type go run hello.go and press enter to run your code.`
>> * `If there are no errors in your code, then you will see "Hello, World!" printed on the screen.`

```go
$ go run hello.go
Hello, World!
```

## Basic Syntax
> `We discussed the basic syntax of a Go program. Now it will be easy to understand the other basic building blocks of the Go programming language`
>> ### Tokens
>>> `A Go program consists of various tokens. A token is either a keyword, an identifier, a constant, a string literal, or a symbol. For example, the following Go statement consits of six tokens-`
```go
fmt.Println("Hello, World!")
```
>>> `The individual tokens are-`
```go
fmt

Println
(
    "Hello, World!"
)
```
>
>> ### Line Separator
>>> `In a Go program, the line separator key is a statement terminator. That is, individual statement don't need a special seprator like ";" in C. The Go compiler internally places ";" as the statment terminator to indicates the end of the one logical entity`
>>>
>>> `For example, take a look at the following statements-`
```go
fmt.Println("Hello, world!")
fmt.Println("I am in Go Programming World!")
```
>
>> ### Comments
>>> `Comments are like helping texts in your Go program and they are ignored by the compiler. They start with /* as shown below-`
```go
/* my first program in Go */
```
>
>> ### Identifiers
>>> `A Go identifier is a name used to identify a variable, function, or any other user-defined item. An identifier starts with a letter A to Z or a to z or an underscore (_) followed by zero or more letters, underscores, and digits (0-9)`
> 
> **`identifier = letter { letter | unicode_digit }`**
>>> `Go does not allow punctuation characters such as @, $, and % within identifiers. Go is a case-sentitive programming language. Thus, Manpower and manpower are two different identifers in Go. Here are some examples of acceptance identifiers-`
>>>> * `aabhash`
>>>> * `malviya`
>>>> * `abc`
>>>> * `move_name`
>>>> * `a_123`
>>>> * `myname15`
>>>> * `_temp`
>>>> * `a`
>>>> * `a10S`
>
>> ### Keywords
>>> `The following list shows the reserved words in Go. These reserved words may not be used as constant or variable or any other identifier names`
```go
break       default         func        interface       select
case        defer           go          map             struct
chan        else            goto        package         switch
const       fallthrough     if          range           type
continue    for             import      return          var
```
>
>> ### Whitespace
>>> `Whitespace is the term used in Go to describe blanks, tabs, newline characters and comments. A line containing only whitespace, possibly with a comment, is known as a blank line and a Go compiler totally ignore it.`
>>> 
>>> `Whitespaces separate one part of a statement from another and enables ths compiler to identify where one element on a statment, such as int, end, and the next element begins. Therefore, in the following statement-`
```go
var age int;
```
>>> `There must be at least one whitespace character (ususally a space) between int and age for the compiler to be able to distinguish them. On the other hand, in the following statement-`
```go
fruit = apples + oranges;       // get the total fruit
```
>>> `No whitespace character are necessary between fruit and = or between = and apples, althrough you are free to include some if you wish for readability purpose`

## Data Types
> `In Go Programming language, data types refer to an extensive system used for declaring variables or functions of different types. The type of a variable determines how much space it occupies in storage and how the bit pattern stored is interpreted`
>
> `The types in Go can be classified as follows-`
> 
| Sr. No. | Types and Description |
| :-----: | :---- |
|   1   | **Boolean types** - They are boolean types and consists of the two predefined constansts: (a) **_true_** (b) **_false_**    |
|   2   | **Numeric types** - They are again arithmetic type and they represents (a) **_integer types_** (b) **_floating point value_** through program   |
|   3   | **String types** - A string type represent the set of string values. Its value is a sequence of bytes. Strings are immutable types that is once created, it is not possible to change the contents of a string. The predeclared string type is string   |
|   4   | **Derived types** - They include (a) **_pointer types_** (b) **_array types_** (c) **_structure types_** (d) **_union types_** (e) **_function types_** (f) **_slice types_** (g) **_interface types_** (h) **_map types_** (i) **_channel types_**
> `Array types and structure types are collectively refers to as` **aggregate types.** `The type of a function specifies the set of all function with the same perameter and result types. We will discuss the basic type in the following section`
> 
>> ### Integer types
>>> `The predefined architecture-independent interger types are-`
>>>
| Sr. No. | Types and Description |
| :-----: | :---- |
| 1 | **uint8** - `Unsigned 8-bit integers (0 to 255)` |
| 2 | **uint16** - `Unsigned 16-bit integers (0 to 65535)` |
| 3 | **uint32** - `Unsigned 32-bit integers (0 to 4294967295)` |
| 4 | **uint64** - `Unsigned 64-bit integers (0 to 18446744073709551615)` |
| 5 | **int8** - `Singed 8-bit integers (-128 to 127)` |
| 6 | **int16** - `Signed 16-bit integers (-32768 to 32767` |
| 7 | **int32** - `Signed 32-bit integers (-2147483648 to 2147483647)` |
| 8 | **int64** - `Signed 64-bit integers (-9223372036854775808 to 9223372036854775807)` |
>
>> ### Floating types
>>> `The predefined architecture-independent float types are-`
>>>
| Sr. No. | Types and Description |
| :-----: | :---- |
| 1 | **float32** - `IEEE-754 32-bit flating-point number` |
| 2 | **float64** - `IEEE-754 64-bit flating-point number` |
| 3 | **complex64** - `Complex numbers with float32 real and imaginary parts` |
| 4 | **complex128** - `Complex numbers with float64 real and imaginary parts` |
> `The value of an n-bit integer is n bits and is represented using two's complement arithmetic operations`
>

>> ### Other Numberic types
>>> `There is also a set of numberic types with implementation-specific sizes-`
>>>
| Sr. No. | Types and Description |
| :-----: | :---- |
| 1 | **byte** - `same as uint8` |
| 2 | **rune** - `same as int32` |
| 3 | **uint** - `32 or 64 bits` |
| 4 | **int** - `same size as uint` |
| 5 | **uintpr** - `an unsigned integer to store the uninterpreted bits of a pointer value` |

## Variables
> `A variable is nothing but a name given to a storage area that the programs can manipulate. Each variable in Go has specific type, which determines the size and layout of the variable's memory, the range of valus that can be stored within that memory, and the set of operations that can be applied to the variable.`
>
> `The name of a variable can be composed of letters, digits and the undescore character. It must begin with either a letter or an underscore, Upper and lowercase letters are distinct because Go is case-sensitive.`
>
| Sr. No. | Types and Description |
| :-----: | :---- |
| 1 | **byte** - `Typically a single octet (one byte). The is an byte type.` |
| 2 | **int** - `The most natural size of integer for the machine.` |
| 3 | **float32** - `A single-precision floating point value` |
> `Go programming language also allows to define various other types of variables such as Enumeration, Pointers, Array, Structure, and Union`
>
>> ### Variable defination
>>> `A variable defination tells the compiler where and how much storage to create for the variable. A variable defiantion specifies a data type and contains a list of one or more variable of that type as follows-`
>>>
```go
var variable_list optional_data_type;
```
>>> `Here,` **optional_data_type** `is a valid Go data type including byte, int, float32, complex64, boolean or any user-defined object etc. and ` **variable_list** `may consist of one or more identifier names  separated by commas. Some valid declarations are shown here-`
>>>
```go
var x, y, z int;
var c, ch byte;
var f, salary flat32;
d = 15
```
>>> `The statement` "**var x, y, z int;**" `declares and defines the variable x, y and z; which instructs the compiler to create variables named x, y, and z of type int.`
>>>
>>> `Variables can be initialized (assigned an initial value) in their declaration. The type of variable is automatically judged by the compiler based on the value passed to it. The initializer consists of an equal sign followed by a constant expression as follows-`
>
```go
variable_name = value;
```
>> ### Static type declaration
>>> `A static type variable declaration provides assurance to the compiler that there is one variable available with the given type and name so that the compiler can proceed for further compilation without requiring the complete detail of the variable. A varialbe declaration has its meaning at the time of compilation only, the compiler needs the actual variable declaration at the time of linking of the program.`
>>>
>>> `Example-`
>>>
```go
package main

import "fmt"

func main() {
    var x float64
    x = 20.0
    fmt.Println(x)
    fmt.Printf("x is of type %T\n", x)
}
```
>>> `When the above code is compiled and executed, it produces the following result-`
```
20
x is of type float64
```
>
>> ### Dynamic type declaration (type interfence)
>>> `A dynamic type variable declaration requires the compiler to interprete the type of the variable based on the value passed to it. The compiler does not reqiure a variable to have type statically as a necessary requirement.`
>>>
>>> `Example-`
>>>
>>> `Try the following example, where the variables have been declared without any type. Notice, in case of type interence, we initialized the variable` **y** `with` **:=** `operator, whereas` **x** `is initialized using` **=** `operator.`
```go
package main

import "fmt"

func main() {
    var x float64 = 20.0
    y := 15
    fmt.Println(x)
    fmt.Println(y)
    fmt.Printf("x is of type %T\n", x)
    fmt.Printf("y is of type %T\n", y)
}
```
>>> `When the above code is compiled and executed, it produces the following result-`
```
20
15
x is of type float64
y is of type int
```
>
>> ### Mixed variable declaration
>>> `Variables of different types can be declared in one go using type inference`
>>>
>>> `Example-`
>>>
```go
package main

import "fmt"

func main() {
    var a, b, c = 3, 4 ,"foo"

    fmt.Println(a)
    fmt.Println(b)
    fmt.Println(c)
    fmt.Printf("a is of type %T\n", a)
    fmt.Printf("b is of type %T\n", b)
    fmt.Printf("c is of type %T\n", c)
}
```
>>> `When the above code is compiled and executed, it produces the following result-`
>>>
```
3
4
foo
a is of type int
b is of type int
c is of type string
```
>>
>> ### The lvalues and the rvalues
>>> `There are two kind of expression in Go-`
>>>
| Sr. No. | Expression |
| :----:  | :----   |
| 1 | **lvalue** - `Expressions that refer to a memory location is called` "lvalue" `expression. An lvalue may appear as either the left-hand or right-hand side of an assignment.` |
| 2 | **rvalue** - `The term rvalue refers to a data value that is stored at some address in memory. An rvalue is an expression that cannot have a value assigned to it which means an rvalue may appear on the right, but not left-hand side of an assignment` |
>>> `The following statement is valid-`
```
x = 20.0
```
>>> `The following statement is not valid. It would generate compile-time error-`
```
10 = 20
```

## Constants
> `Constants refer to fixed values that the program may not alter during its execution. These fixed values are also called` **literals.**
>
> `Constants can be of any of the basic data types like an` _integer constant_ `, a` _character constant_ `, or a` _string literal_ `. There are also enumeration constants as well.`
>
> `Constants are treated just like regular variables except that their values cannot be modified after their defination.`
>
> ### Integer literals
>> `An integer literals can be a decimal, octal, or hexadecimal constant. A prefix specifies the base or radix: 0x or 0X for hexadecimal, 0 for octal and nothing for decimal.`
>>
>> `An integer literal can also have a suffix that is a combination of U and L, for undigned and long, respectively. The suffix can be uppercase or lowercase and can be in any order.`
>>
>> `Here are some example of integer literals-`
```go
212     /* Legal */
215u    /* Legal */
0xFeeL  /* Legal */
078     /* Illegal: 8 is not an octal digit */
032UU   /* Illegal: cannot repeat a suffix */
```
>>
>> `Following are other example of various type of Integer literals-`
```go
85      /* decimal */
0213    /* octal   */
0x4b    /* hexadecimal */
30      /* int  */
30u     /* unsigned int */
30l     /* long */
30ul    /* unsigned long */
```
>
> ### Floating-point literals
>> `A floating point literals has an integer part, a decimal point, a fractional part, and an exponent part. You can represent floating point literal either in decimal form or exponential form.`
>>
>> `While representing using decimal form, you must include the decimal point, the exponent, or both and while representing using exponential form, you must include the integer part, the fractional part, or both. The signed exponent is introduced by e or E`
>>
>> `Here are some examples of floating-point literals-`
```go
3.14159     /* Legal */
314159E-5L  /* Legal */
510E        /* Illegal: incomplete exponeny */
210f        /* Illegal: no decimal or exponent */
.e55        /* Illegal: missing integer or fraction */
```
>
> ### Escape Sequence
>> `When certain characters are preceded by a backslash, they will jave a special meaning in Go. These are known as Escape Sequence codes which are used to represent newline (`**\n**`), tab (`**\t**`), backspace, etc. Here you have a list of some of such escape sequence codes-`
>>
| Escape Sequence | Meaning |
| :-------------: | :-----: |
| \\ | \character |
| \' | 'character |
| \" | "character |
| \? | ?character |
| \a | Alert or bell |
| \b | Backspace |
| \f | Form feed |
| \n | Newline |
| \r | Carriage return |
| \t | Horizontal tab |
| \v | Vertical tab |
| \000 | Octal number of one to three digits |
| \xhh... | Hexadecimal number of one or more digits |
>>
>> `The following example show how to use` **\t** `in a program-`
>>
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```
>> `When the above code is compiled and executed, it produces the following result-`
>>
```
Hello, World!
```
>
> ### String literals
>> `String literals or constants are enclosed in double quotes` **""** `. A string contains characters that are similar to character literals: plain characters, escape sequences, and universal characters.`
>>
>> `You can break a long time into multiple lines using string literal and seprating them using whitespaces.`
>>
>> `Here are some examples of string literals. All the three forms are identical springs.`
>>
```
"hello, world"

"hello, \

world"

"hello, "   "w" "orld"
```
>
> ### The _**const**_ keyword
>> `You can use` **const** `prefix to declare constants with a specific type as follows-`
>>
```
const variable type = value
```
>> `The following example shows how to use the` **const** `keyword-`
>>
```go
package main

import "fmt"

func main() {
    const LENGTH int = 10
    const WIDTH int = 5
    var area int

    area = LENGTH * WIDTH
    fmt.Println("value of area : %d", area)
}
```
>> `When the above code is compiled and executed, it produces the following result-`
```
value of area : 50
```
>> `Note: It is a good programming practice to define constants in CAPITALS.`

## Operators
> `An operator is a symbol that tells the compiler to perform specific mathematical or logical manipulations. Go language is rich in built-in operators and provides the following types of operators-`
>> * `Arithmetic Operators`
>> * `Relational Operators`
>> * `Logical Operators`
>> * `Bitwise Operators`
>> * `Assignment Operators`
>> * `Miscellaneous Operators`
>>
>> ### Arithmetic Operator
>> `Following table shows all the arithmetic operators supported by Go language.`
>>
| Operator | Decription |
| :------: | :--- |
| + | Adds two operands |
| - | Substracts second operands from the first |
| * | Multiplies both operands |
| / | Divides the numberator by the denominator |
| % | Modules operator, gives the remainder after an integer division. |
| ++ | Increment operator. It increase the integer value by one. |
| -- | Decrement operator. It decrease the integer value by one. |
>>
>> ### Relational Operators
>> `The following table shows all the relational operators support by Go language.`
>>
| Operator | Description |
| :------: | :---- |
| == | It checks if the values of the operands are equal or not; if yes, the condition becomes true. |
| != | It checks if the values of two operands are equal or not; if the values are not equal, then the condition becomes true. |
| > | It checks if the value of left operands is greater than the value of right operand; if yes, the condition becomes true. |
| < | It checks if the value of left operand is less than the value of the right operand; if yes, the condition becomes true. |
| >= | It checks if the value of the left operand is greater than or equal to the value of the right operand; if yes, the condition becomes true |
| <= | It checks if the value of the left operand is less than or equal to the value of the right operand; if yes, the conditon becomes true. |
>>
>> ### Logical Operators
>> `The following table list all the logical operators supported by Go language.`
>>
| Operator | Description | 
| :------: | :---- |
| && | Called Logical AND operator. If both the operands are non-zero, then condition beacuse true. |
| // | Called Logical OR operator. If any of the two operands is non-zero, then condition becomes true. |
| ! | Called Logical NOT operator. Use to reverses the logical state of its operand. If a condition is true then Logical NOT operator will make false. |
>>
>> ### Bitwise Operators
>> `Bitwise operators work on bits and perform bit-by-bit operation. The truth tables for &, | and ^ are as follows-`
>>
|  p  |  q  | p & q | p / q | p ^ q |
| :-: | :-: | :---: | :---: | :---: |
|  0  |  0  |   0   |   0   |   0   |
|  0  |  1  |   0   |   1   |   1   |
|  1  |  1  |   1   |   1   |   0   |
|  1  |  0  |   0   |   1   |   1   |
>>
>> ### Assignment Operators
>> `The following table lists all the assignment operators supported by Go language-`
>>
| Operator | Description |
| :------: | :----       |
| = | Simple assignment operator. Assigns values from right side operands to left side operand |
| += | Add AND assignment operator, it adds right operand to the left operand and assign the result to left operand |
| -= | Substract AND assignment operator, it substracts right operand from the left operand and assign the result to left operand |
| *= | Multiply AND assignment operator, it multiples right operand with the left operand and assign the result to the left operand | 
| /= | Divide AND assignment operator, it divides left operand with the right operand and assign the result to the left operand |
| %= | Modulus AND assignment operator, it takes modulus using two operands and assign the result to left operand |
| <<= | Left-shift AND assignment operator |
| >>= | Right-shift AND assignment operator |
| &= | Bitwise AND assignment operator | 
| ^= | Bitwise exclusive OR and assignment operator |
| /= | Bitwise inclusive OR and assignment operator |
>>
>> ### Miscellaneous Operators
>> `There are a few other important operators supported by Go language including` **sizeof** `and ?:.`
>>
| Operator | Description |
| :------: | :---- |
| & | Returns the address of a varible. |
| * | Pointer to a variable. |
>>
>> ### Operators Precedence
>> `Operator precedence determines the grouping of terms in an expression. This affects how an expression is evaluated. Certain operators have higher precedence than others; for example, the multiplication operator has higher precedence than the addition operator.`
>>
>> `For example: x = 7 + 3 * 2; here, x is assigned 13, not 20 because operator * has higher precedence than +, so it first gets multiplied with 3 * 2 and then adds into 7.`
>>
>> `Here, operators with the highest precedence appear at the top of the table, those with the lowest appear at the bottom. Within an expression, higher precedence operatorss will be evaluated first.`
>>
| Category | Operator | Associativity |
| :------: | :------: | :----: |
| Postfix | () [] -> . ++ -- | Left to right |
| Unary | + - ! ~ ++ -- (type)* & sizeof | Right to left |
| Multiplicative | * / % | Left to right |
| Additive | + - | Left to right |
| Shift | << >> | Left to right |
| Relation | < <= > >= | Left to right |
| Equality | == != | Left to right |
| Bitwise AND | & | Left to right |
| Bitwise XOR | ^ | Left to right |
| Bitwise OR | / | Left to right |
| Logical AND | && | Left to right |
| Logical OR | // | Left to right |
| Assignment | = += -= *= /= %= >>= <<== &= ^= /= | Right to left |
| Comma | , | Left to right |

## Decision Making
> `Decision Making structures require that the programmer specify one or more condition to be evaluated or tested by the program, along with a statement or statements to be executed if the condition is determined to be false.`
>
> `Go programming language provides the following types of descision making statements.`
>
| Sr. No. | Statement & Description |
| :-----: | :----- |
| 1 | if statement - An **if statement** consists of a boolean expression followed by one or more statement |
| 2 | if...else statement - An **if statement** can be followed by an optional **else statement**, which executes when the boolean expression is false. |
| 3 | nested if statement - You can use one **if** or **else if** statement inside another **if** or **else if** statement(s).
| 4 | switch statement - A **switch** statement allows a variable to be tested for equality against a list of values. |
| 5 | select statement - A **select** statement is similar to **switch** statement with difference that case statement refers to channel communications. |

## Loops
> `Programming language provides various control structure that allow for more complicated execution paths`
> 
> `A loop statement allows us to execute a statement or group of statements multiple times.`
>
> `Go programming language privides the following types of loop to handle looping requirements.`
>
| Sr. No. | Loop Type & Description |
| :-----: | :----- |
| 1 | for loop - It executes a squence of statment multiple times and abbreviates the code that manages the loop varable. |
| 2 | nested loop - These are one or multiple loops inside any of loop. |
>
>> ### Loop Control Statements
>> `Loop control statements change an execution from its normal sequence. When an execution leaves its scope, all automatic objects that were created in that scope are destroyed.`
>> 
>> `Go supports the following control statements-`
>>
| Sr. No. | Control Statement & Description |
| :-----: | :---- |
| 1 | break statement - It terminates a **for loop** or **switch** statement and transfers execution to the statement immediately following this for loop or switch. |
| 2 | continue statement - It causes the loop to skip the remainder of its body and immediately retest its condition prior to reiterating. |
| 3 | goto statement - It transfers control to the labeled statement. |
>
>> ### The Infinite Loop
>> `A loop becomes an infinite loop if its condition never becomes false. The for loop is traditionally used for this purpose. Since none of the three expressions that form the for loop are required, you can make an endless loop by leaving the conditional expression empty or by passing true to it.`
>>
```go
package main

import "fmt"

func main() {
    for true {
        fmt.Printf("This loop will run forever. \n")
    }
}
```
> **Note** `- You can terminate an infinite loop by pressing` **Ctrl + C** `keys.`

## Functions
> `A function is a group of statement that together perform a task. Every Go program has at least one function, which is` **main()** `. You can divide your code into separate functions. How you divide your code into separate functions. How you divide your code among different functions is up to you, but logically, the division should be such that each function performs a specific task.`
>
> `A function` **declaration** `tells the compiler about a function name, return type, and parameters. A function` **defination** `provides the actual body of the function.`
>
> `Functions are also known as` **method, sub-routine** `or` **procedure.**
>
> ## Defining
>> `The general form of a function defination in Go programming language is as follows-`
>>
```go
func function_name( [parameter list] ) [return_types]
{
    //body of the function
}
```
>>





