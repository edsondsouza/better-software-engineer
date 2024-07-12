# Arrays

```kotlin
val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")

println(cars[0]) // access element of an array

cars[0] = "Opel" // change the element of an array

println(cars.size) // length of an array

// check if element exists
if ("Volvo" in cars) {
  println("It exists!")
} else {
  println("It does not exist.")
}

// loop though an arrya
val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
for (car in cars) {
  println(car)
}
```

# For-Loop
Unlike Java and other programming languages, there is no traditional for loop in Kotlin.

In Kotlin, the for loop is used to loop through arrays, ranges, and other things that contains a countable number of values.

You will learn more about ranges in the next chapter - which will create a range of values.

```kotlin
val nums = arrayOf(1, 5, 10, 15, 20)
for (x in nums) {
  println(x)
}
```

# Ranges
With the for loops, you can also create ranges of values with "`..`"

```kotlin
for (chars in 'a'..'x') {
    println(chars)
}
```

```kotlin
for (nums in 5..15) {
    println(nums)
}
```

> The first and last value is included in the range.

# Check if a value exits
```kotlin
val nums = arrayOf(2, 4, 6, 8)
if (2 in nums) {
    println("It exists!")
} else {
    println("It does not exist.")
}
```

# Break or Continue a Range
```kotlin
for (nums in 5..15) {
  if (nums == 10) {
    break
  }
  println(nums)
} 
```

```kotlin
for (nums in 5..15) {
  if (nums == 10) {
    continue
  }
  println(nums)
} 
```
