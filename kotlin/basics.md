# Where Kotlin Is Used
Kotlin is a modern, trending programming language that was released in 2016 by JetBrains.

It has become very popular since it is compatible with Java (one of the most popular programming languages out there), which means that Java code (and libraries) can be used in Kotlin programs.

Kotlin is used for:
- Mobile applications (specially Android apps)
- Web development
- Server side applications
- Data science
- And much, much more!

# Comments
- Single-line comment: //
- Multi-line comment: /* */

# Package
It is a way to organize and group related code
```kotlin
package com.learnxinyminutes.kotlin
```

# The Entry Point
The entry point of any Kotlin program is the function named main. The function main is passed an array containing any command line arguments. Since Kotlin 1.3 the "main" function can also be defined with any parameters.
```kotlin
fun main(args: Array<String>){
    // code goes here
}
```

# Variables
There are mainly two ways in which the variables can be declared in Kotlin
```kotlin
var x = 9
val y = 10
```
The main difference between the `var` and `val` is that once the variable is declared using `val`, the variable cannot be reassigned again.

```kotlin
// variable example
var fooVariable = 9
fooVariable = 10 // this is allowed

val barVariable = 9
barVariable = 10 // this is not allowed
```

// In most of the cases, Kotlin can determine what the type of a variable is, so we don't have to explicitly specify it every time.
```kotlin
val fooVariable: Int = 9 // explicitly defining the type of variable

// println() is to print the value, readln() is to get the input from the user
```

# Datatypes
Numbers, Boolean, Characters, Strings, Arrays, Any, Nothing, Unit

## Numbers
- Byte => 8 bits
- Short => 16 bits
- Int => 32 bits
- Long => 64 bits

When you initialize a variable with no explicit type specification, the compiler automatically infers the type with the smallest range enough to represent the value starting from Int. If it is not exceeding the range of Int, the type is Int. If it exceeds, the type is Long. To specify the Long value explicitly, append the suffix L to the value. Explicit type specification triggers the compiler to check the value not to exceed the range of the specified type.

## Floating-point types
- Float => 32 bits
- Double => 64 bits

```kotlin
/* You can initialize Double and Float variables with numbers having a fractional part. 
It's separated from the integer part by a period (.) 
For variables initialized with fractional numbers, the compiler infers the Double type: */

val pi = 3.14 // Double
// val one: Double = 1 // Error: type mismatch
val oneDouble = 1.0 // Double

val e = 2.7182818284 // Double
val eFloat = 2.7182818284f // Float, actual value is 2.7182817
```

## Literal constants for numbers﻿
There are the following kinds of literal constants for integral values:

- Decimals: 123
- Longs are tagged by a capital L: 123L
- Hexadecimals: 0x0F
- Binaries: 0b00001011

> Octal literals are not supported in Kotlin.

Kotlin also supports a conventional notation for floating-point numbers:

- Doubles by default: 123.5, 123.5e10
- Floats are tagged by f or F: 123.5f

You can use underscores to make number constants more readable:

```kotlin
val oneMillion = 1_000_000
val creditCardNumber = 1234_5678_9012_3456L
val socialSecurityNumber = 999_99_9999L
val hexBytes = 0xFF_EC_DE_5E
val bytes = 0b11010010_01101001_10010100_10010010
```

## Use Float or Double?

The precision of a floating point value indicates how many digits the value can have after the decimal point. The precision of Float is only six or seven decimal digits, while Double variables have a precision of about 15 digits. Therefore it is safer to use Double for most calculations.

Also note that you should end the value of a Float type with an "F".

## Type Conversion
Type conversion is when you convert the value of one data type to another type.

`toByte()`, `toShort()`, `toInt()`, `toLong()`, `toFloat()`, `toDouble()` or `toChar()`

# Operators
Operators are used to perform operations on variables and values.

The value is called an operand, while the operation (to be performed between the two operands) is defined by an operator.

Kotlin divides the operators into the following groups:

- Arithmetic operators (Add, Sub, Mul, Div, Mod, Incre, Decre)
- Assignment operators (=, +=, -=, *=, /=, %=)
- Comparison operators (==, !=, >, <. >=, <=)
- Logical operators (&&, ||, !)

## Bitwise operations﻿
Kotlin provides a set of bitwise operations on integer numbers. They operate on the binary level directly with bits of the numbers' representation. Bitwise operations are represented by functions that can be called in infix form. They can be applied only to Int and Long:

```kotlin
val x = (1 shl 2) and 0x000FF000
Here is the complete list of bitwise operations:
```

- `shl(bits)` – signed shift left

- `shr(bits)` – signed shift right

- `ushr(bits)` – unsigned shift right

- `and(bits)` – bitwise AND

- `or(bits)` – bitwise OR

- `xor(bits)` – bitwise XOR

- `inv()` – bitwise inversion

# Strings
String are used for storing text. A string contains a collection of characters surrounded by double quotes.

```kotlin
val greeting = "Hello"
val greeting: String = "Hello"
```

> If you want to create a `String` without assigning the value (and assign the value later), you must specify the type while declaring the variable

```kotlin
// example 1 => This works fine

var name: String
name = "John"
println(name)

// example 2 => This will generate an error
var name
name = "John"
println(name)
```

## Access a String
```kotlin
var txt = "Hello World"
println(txt[0]) // first element (H)
println(txt[2]) // third element (l)
```

## String length
```kotlin
var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
println("The length of the txt string is: " + txt.length) // 26
```

## String Functions
```kotlin
var txt = "Hello World"
println(txt.toUpperCase())   // Outputs "HELLO WORLD"
println(txt.toLowerCase())   // Outputs "hello world"
```

## Comparing Strings
The `compareTo(string)` function compares two strings and returns 0 if both are equal:

```kotlin
var txt1 = "Hello World"
var txt2 = "Hello World"
println(txt1.compareTo(txt2))  // Outputs 0 (they are equal)
```

## Finding a String in a String
The `indexOf()` function returns the index (the position) of the first occurrence of a specified text in a string (including whitespace):

```kotlin
var txt = "Please locate where 'locate' occurs!"
println(txt.indexOf("locate"))  // Outputs 7
```

## Quotes inside a String
```kotlin
var txt1 = "It's alright"
var txt2 = "That's great"
```

## String concatenation
```kotlin
var firstName = "John"
var lastName = "Doe"
println(firstName + " " + lastName)
```

> or

```kotlin
var firstName = "John "
var lastName = "Doe"
println(firstName.plus(lastName))
```

## String Templates/Interpolation
```kotlin
var firstName = "John"
var lastName = "Doe"
println("My name is $firstName $lastName")
```

# Boolean
Either `true` or `false`

# if...else

```kotlin
if (condition) {
    // block of code
} else if (condition) {
    // block of code
} else {
    // block of code
}
```

## if...else expressions
```kotlin
val time = 20
val greeting = if (time < 18) {
  "Good day."
} else {
  "Good evening."
}
println(greeting)
```

> When using if as an expression, you must also include else (required).

> Note: You can ommit the curly braces `{}` when `if` has only one statement:
```kotlin
fun main() {
  val time = 20
  val greeting = if (time < 18) "Good day." else "Good evening."
  println(greeting)
}
// This example is similar to the "ternary operator" (short hand if...else) in Java.
```

# When
> The when expression is similar to the switch statement in Java.
```kotlin
val day = 4

val result = when (day) {
  1 -> "Monday"
  2 -> "Tuesday"
  3 -> "Wednesday"
  4 -> "Thursday"
  5 -> "Friday"
  6 -> "Saturday"
  7 -> "Sunday"
  else -> "Invalid day."
}
println(result)

// Outputs "Thursday" (day 4)
```

# While
The `while` loop loops through a block of code as long as a specified condition is `true`:
```kotlin
// while
while (condition) {
  // code block to be executed
}

// do..while
do {
  // code block to be executed
}
while (condition);
```

# Break/Continue
- The `break` statement is used to jump out of the loop
- The `continue` statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration.
