# GoLang

> `Go language is a programming language initially developed at Google in the year 2007 by Robert Griesemer, Rob Pike, and Ken Thompson. It is a statically-typed language having syntax similar to that of C. It provides garbage collection, type safety, dynamic-typing capability, many advanced built-in types such as variable length arrays and key-value maps. It also provides a rich standard library. The Go programming language was launched in November 2009 and is used in some of the Google's production systems.`

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

> `It should be written into one or more test files with the extension` **.go**
>
> `For example-` __hello.go__

## Program Structure

> `A go program basically consits of the following parts-`
>> * `Package declaration`
>> * `Import packages`
>> * `Functions`
>> * `Variables`
>> * `Statements and Expressions`
>> * `Comments`


> `Let us look simple code that would print the words "Hello World"-`
```go
package main

import "fmt"
func main() {
    /* This is a sample program */
    fmt.Println("Hello, World!")
}
```

> `Let us take at the various parts of the above program-`
>> * `The line of the program package main defines the packages name in which this program should lie. It is a mandatory statement, as Go programs run in packages. The main package is the starting point to run the program. Each package has a path and name associated with it`
>> * `The next line import "fmt" is a proprocessor command which tells the Go compiler to include the files lying in the package fmt.`
>> * `The next line func main() is the main function where the program execution begins.` 
>> * `The next line /*...*/ is ignored by the compiler and it is there to add comments in the program. Comments are also represented using // similar to Java, Javascript or C++ comments`
>> * `The next line fmt.Println(...) is another function available in Go which causes the message "Hello, World!" to be displayed on the screen. Here fmt package has exported Println mathod which is used to display the message on the screen` 
>> * `Notice: The capital P of Println method. In Go language, a name is exported if it starts with capital letter. Exported means the function or variable/constant is accessible to the importer of the respective package.`

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
