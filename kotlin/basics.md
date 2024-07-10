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
