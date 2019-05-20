# Kotlin Tutorials
* Kotlin is a ```JVM``` Language it needs JVM to execute its bytecode.
* It supports to avoid ```NullPointerExceptions```
* Supports Immutability
* Kotlin is an Object Oriented language
* It is used for Functional Pprogramming Language
* Functional
    * You can pass a function as parameter to another function.
    * Or a Function can return another function
* Less Ceremony
    * No more boilerplates
    * Less code, more results
    * Code less clean

## Evolution of Kotlin
* ```July, 2011``` Kotlin unvelied by Jetbrains
* ```February, 2012``` Kotlin was open sourced under Apache 2 license
* ```February 2016``` Kotlin 1.0 released.
* ```May 2017``` Google I/O Kotlin was adopted for Android officially.

## Types of apps that can be built using Kotlin
* Server-side Apps
* Android Development
* Web Development Kotlin.JS
* Destop Applicaions JavaFX, TornadoFX
* Native Development Kotlin/Native Library

## Why Kotlin?
* It is because it is consise, kotlin code is leasser then java code
* It is safe from null pointer exceptions
* It is interoperable with JAVA
* It is also tool friendly

## Functions in Kotlin
Function in kotlin are defined by ```fun```
```kotlin
fun main(args:Array<String>){
    println("Hi I am Akshay")
    print("Hi Hello World")
}
```
Java Code demands class files Kotlin needs JVM in return similar to JAVA<br>

**Does Kotlin creates a class internally**<br>
Yes -> The kotlin compliler internally creates a class file which is loaded into memory for execution in runtime.<br>
Kotlin Code **->** Class File **->** JVM
* In kotlin there is no static function / usage the main function is itself declared static.
* We dont create class in kotlin because internally kotlin creates a class.

### Print function
In Kotlin there are two different print functions ```print()``` and ```println()```
both are for single line and next line respectively. You can also perform operaions in print functions.
```kotlin
println("Akshay Bengani")
println(10/9) // 1
println(10.0/9) // 1.1111111111112
println(true) // true
```
### Comments in Kotlin
Similar to JAVA Kotlin also have single line comments and multi line comments ```//``` Single line, ```/* */``` Multi line comments.<br>
```kotlin
// Hey I am a single line comment
println("Multiline comments")
/*
line0
I am a multiple line comment
line2
*/
```
## Variables in Kotlin
In Kotlin we use ```var``` keyword to declare a variable
```kotlin
var a = 10
a =  15
println(a)
// 15
```
### Explicitly define datatype of a variable
In Kotlin we can also define specific datatype to the variable by using ```:``` with Datatype
```kotlin
var name : String = "Akshay bengani"
var age : Int
println(name)
```
### Concatination in Kotlin
In Kotlin there are several ways to concatinate text/string with variables and other values.
```kotlin
var name = "Akshay Bengani"
println("My name is " + name)
println("My name is ${name}")
```
### Constants in Kotlin
To define a constant in Kotlin we use the keyword ```val``` for constants
```kotlin
val age : Int = 25
age = age + 5 // This will give an error
println(age)
```
## Conditional Statements in Kotlin
In Kotlin we dont have Ternary operators ```?:``` for if else here ```if else``` are statements.<br>

**Without block single line statement**
```kotlin
var a = 20
var b = 30
var large = if(a>b) a else b
println("Largest is ${large}") // Largest is 30
```
**With Block single line statement**
```kotlin
var a = 20
var b = 30
var large if(a>b){
    println("A is Largest")
    a
} else {
    println("B is Largest")
    b
}
println("Largest is ${large}) // Largest is 30
```
### Switch in Kotlin named as when
* In kotlin we dont have the keyword ```switch``` like other languages we have another keyword called ```when``` for the replacement.  <br>
* There is another indicator or assignment operator in Kotlin ```->``` This is used similar like the assignment operator ```=``` in kotlin.
* We dont need to use ```{}``` if it is a singe line statement.
* Similar to Python we also have ```in``` operator in Kotlin to check that the value is in between or in the collection or group.<br>

**When with ```{}```** 
```kotlin
var a = "Red"
when(a)
{
    "Red" -> {
        println("Value is Red")
    }
    "Green" -> {
        println("Value is Green")
    }
    else -> {
        println("Value is neither Red or Green")
    }
}
```
**When without ```{}```**
```kotlin
var a = "Red"
when(a){
    "Red" -> println("Value is Red")
    "Green" -> println("Value is Green")
    else -> println("Value is nither Red or green")
}
```
**When with ```in``` operator**<br>
In Kotlin we can give numeric ranges using ```..``` operator between two numbers. Both the values are inclusive in the series.
```kotlin
var x = 10
when(x){
    in 1..10 -> println("X is between 1 to 10")
    in 20..30 -> println("X is between 20 to 30")
    else -> println("X not comes in between 1 to 30")
}
```
## Loops in Kotlin
In kotlin we have all the 3 loops ```while```, ```do while``` and  ```for```.<br>

### ```for``` loop in Kotlin
Similar to python we use ```in``` operator in ```for``` loop.

**```for``` loop using ```in```**
```kotlin 
for(i in 1..10){
    println(i)   // 1 2 3 4 5 6 7 8 9 10
}
```
### ```While``` loop in Kotlin
```kotlin
var x = 1
while(x<=10){
    println(x)
    x++
}
```
### ```do while``` loop in Kotlin
```kotlin
var x = 1
do{
    println(x)
    x++
}while(x<=10)
```
## Arrays in Kotlin
In kotlin we have keywords to create arrays similar like PHP or Python they have a special function called ```array()``` to declare an array. <br>
In Kotlin there is a function called ```arrayOf()``` which will be used to create array's in Kotlin.
```Kotlin
var a = arrayOf(1,2,3,4)
println(a)      // [Ljava.lang.Integer;@2c7b84de
println(a[0])   // 1
```
**Traverse elements of array in loop**
```kotlin
var a = arrayOf(1,2,3,4)
for(i in a){
    println(i)
}
```
**Array with different datatype**
```kotlin
var a = arrayOf(1,2,3.5,59.5,"Akshay",84,true)
for(i in a){
    println(i)
}
```
**Restrict array to store single datatype entries only**
```kotlin
var a = arrayOf<Int>(1,2,3,4,5,"Akshay",6) // This will give error here
for(i in a){
    println(i)
}
```
**2D Matrix using multidimensional array**
```kotlin
var arr = arrayOf(
    arrayOf(1,2,3),
    arrayOf(4,5,6),
    arrayOf(7,8,9)
)
for(i in arr){
    for(j in i){
        print("${j} ")
    }
    println("")
}
/*
    1 2 3
    4 5 6
    7 8 9
*/
```
## Classes in Kotlin
Classes are similar like JAVA we use the same syntax to create a new class. Create a new file same as the new class name  
```kotlin
class Hero{
    var name : String = ""
}
```
**To create object of a class simple use**
```kotlin
var ironman = Hero()
ironman.name = "Tony Stark"
println("The name of ironman is ${ironman.name}")
```
We can also write multiple classes in a single file same as the below example
**Lets write another example**
```kotlin
// File name is Main.kt
fun main(args : Array<String>){

    var samsung = Brand()
    samsung.phone = "Samsung Galaxy S10"
    var MI = Brand()
    MI.phone = "Readme Note 4"

    println("My samsung phone name is ${samsung.phone} \nMy MI phone name is ${MI.phone}")
}
class Brand{
    var phone : String = ""
}
```
### Parameterized Functions with Return Type
In Kotlin we have to specify the return type after the function parameter brackets. The datatype before curli braces is the return type datatype
```kotlin
fun findSquare(a : Int) : Int {
    return a * a
}
fun sum(a : Int, b : Int) : Int {
    return a + b
}
```
**Class containing function and function calling with return type**
```kotlin
// File name Main.kt
fun main(args : Array<String>){
    var a : Int = 20
    var b : Int = 40
    var myMath = MyMath()
    var c : Int = myMath.sum(a,b)
    var d : Int = myMath.mul(a,b)
    var e : Float = 403.43
    var f : Float = 33.2
    var g : Float = myMath.div(e,f)
    var h : String = myMath.vote(23)
    println("Sum of two numbers ${a} and ${b} is ${c}")
    println("Product of two numbers ${a} and ${b} is ${d}")
    println("Division of two numbers ${e} and ${f} is ${g}")
    println("Can I vote ${h}")
}
class MyMath{
    fun sum(a : Int,b : Int) : Int{
        return a + b
    }
    fun mul(a : Int,b : Int) : Int{
        return a * b
    }
    fun div(a : Float,b : Float) : Float{
        return a / b
    }
    fun vote(a : Int) : String{
        return if(a>=18) "Yes you can vote" else "No You cannot vote"
    }
}
```
<object data="https://kotlinlang.org/docs/kotlin-docs.pdf" type="application/pdf" width="700px" height="700px">    
</object>









