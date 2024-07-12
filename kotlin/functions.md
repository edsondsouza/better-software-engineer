# Functions

- A function is a block of code which only runs when it is called.
- You can pass data, known as parameters, into a function.
- Functions are used to perform certain actions, and they are also known as methods.

## Predefined Functions
> `println()`

## Create your own functions

```kotlin
fun foo() {
    println("Help, World!")
}    
```

## Call a function
```kotlin
fun main() {
    foo()
}
```

> A function can be called multiple times.

## Function Parameters
```kotlin
fun main() {
    userInfo("Edson", "Dsouza")
    userInfo("Benjamin", "Franklin")
}

fun userInfo(firstName: String, secondName: String) {
    println("The user name is $firstName $secondName")
}
```

## Return Values
```kotlin
fun main() {
    val result = foo(10, 10)
    println(result)
}

fun foo(num1: Int, num2: Int): Int {
    val sum = num1+num2
    return sum
}
```

## Shorter Syntax for Return Values
```kotlin
fun main() {
    val result = foo(10, 20)
    println(result)
}

fun foo(num1: Int, num2: Int): Int  = num1 + num2
```

## Default Argument
In Kotlin, you can provide default values for function parameters. If the caller does not provide a value for a parameter with a default value, the default value will be used.
```kotlin
fun main() {
    val result = userInfo("Welcome")
    println(result)
}

fun userInfo(greeting: String, username: String = "Guest005") {
    println("Hello $username, $greeting to Hotel Plaza")
}
```

## Named Argument
Named arguments allow you to specify which parameter you're assigning a value to, making the code more readable and flexible.
```kotlin
fun main() {
    val result = userInfo(greeting = "Welcome")
    println(result)
}

fun userInfo(username: String = "Benjamin", greeting: String) {
    println("Hello $username, $greeting to Hotel Plaza")
}
```

## Lambda Functions
Lambda expressions in Kotlin are essentially anonymous functions that can be used as values. They are a concise way to represent functions and are particularly useful when you want to pass a small piece of functionality to another function.
```kotlin
// syntax
val lambdaName: (Type1, Type2) -> ReturnType = { param1: Type1, param2: Type2 -> 
    // function body
}
```

### Without Lambda Function
```kotlin
fun main() {
    val result = foo(10, 10)
    println(result)
}

fun foo(firstNumber: Int, secondNumber: Int): Int {
	val sum = firstNumber + secondNumber
    return sum
}
```

### With Lambda Function
```kotlin
fun main() {
	val sum: (Int, Int) -> Int = {
        firstNumber, secondNumber -> 
        firstNumber + secondNumber
        
    } 
    val result = sum(10, 10)
    println(result)
}
```
