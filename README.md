# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {

}
```

```
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(cost: Double) -> Double {
let tax = ceil(nyTax) - nyTax
let price = itemCost * tax
return price
}
totalWithTax(cost: itemCost)
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"
```
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(cost: Double) -> String {
let tax = ceil(nyTax) - nyTax
let price = itemCost * tax
let readable = "This is your total: $\(Int((ceil(price)))) tax included "
return readable
}
print(totalWithTax(cost: itemCost))
```
## Question 2

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```
```
let todaysTemperature = 72

func howIsItOutside(temp: Int) -> Int {
if temp <= 40 {
print("It's cold out.")
} else if temp >= 85 {
print("It's really warm.")
} else {
print("Weather is moderate.")
}
return temp
}
howIsItOutside(temp: todaysTemperature)
```


## Question 3

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`
```
var num1 = 20
var num2 = 5

func min2(a: Int, b: Int) -> Int{
if a < b{
return a
}
else{
return b
}
}
print(min2(a: num1, b: num2))
```


## Question 4

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`
```
var input = 12345
func lastDigit(_ number: Int) -> Int{
let digit = number % 10

return digit
}
lastDigit(12345)
```


## Question 5

Write a function that takes in any two positive integers and return the sum.
```
func Digit(x: UInt, y: UInt) -> Int{
let sum = x + y

return Int(sum)
}
print(Digit(x: 123,y: 45))

```

## Question 6

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |

```
func classGrade(grade: Int) -> String{
switch grade{
case 100:
print("A+")
break
case 90...99:
print("A")
break
case 80...89:
print("B")
break
case 70...70:
print("C")
break
case 65...69:
print("D")
break
default:
print("F")
}

return ""
}
print("Your grade for this class: \(classGrade(grade: 60))")

```


## Question 7

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)

```
func calculator(num1: Int, num2: Int, mathOperator: String  ) -> Int{
var answer = 0
switch mathOperator {
case "+":
answer = num1 + num2
break
case "-":
answer = num1 - num2
break
case "*":
answer = num2 * num1
break
case "/":
answer = num1 / num2
break
default:
print("Not a math operator")
}

return answer
}

print("The answer is: \(calculator(num1: 2, num2: 2, mathOperator: "/"))")
```


## Question 8

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

let myFinalCost = totalWithTip() //Fill in the arguments
```
```
let mealCost = 45
let tipPercentage = 0.15

//Write your code below
func totalWithTip(cost: Int) -> Double{
let tip = 1 + tipPercentage
let total = Double(cost) * tip

return total
}
let myFinalCost = totalWithTip(cost: mealCost)
print("your total comes to $\(myFinalCost)")
```

Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

//Write your code below

let myFinalCostWithTipAndTax = totalWithTipAndTax() //Fill in the arguments in function
```
```
let mealCost = 45
let tipPercentage = 0.15
let taxPercentage = 0.09

func totalWithTipAndTax(cost: Int) -> Double{
let tip = 1  + tipPercentage
let tax = 1 + taxPercentage
let total = Double(cost) * tip * tax

return total
}
let myFinalCostWithTipAndTax = totalWithTipAndTax(cost: mealCost)
print("your total comes to $\(ceil(myFinalCostWithTipAndTax))")
```

## Question 9

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`
```
func repeatPrint(message: String, count:Int) -> String{
for _ in 0...count{
print(message, terminator: "")
}

return ""
}
repeatPrint(message: "+", count: 10)
```

## Question 10

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`
```
func first(_ n: Int) -> [Int]{
var anArray = [Int]()
for i in 0...n{
anArray.append(i)
}

return anArray
}
print(first(3))
```


## Question 11

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)
```
func copy(_ num: Int) -> String{
if num % 5 == 0 && num % 3 == 0 {
print("FizzBuzz")
}
else if num % 5 == 0{
print("Buzz")
}
else if  num % 3 == 0{
print("Fizz")
}
else{
for i in 1...num{
print(i)
}
}
return ""
}
print(copy(196))
```

## Question 12

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`
```
func reverse(numbers: [Int]) -> [Int]{
var list = [Int]()
for i in numbers{
list.append(i)
}
list.reverse()

return list
}
print(reverse(numbers: [1,2,3,4]))
```


## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.


## Question 14

Write a function that sums all the even indices of an array of Ints.
```
var nums = [1,2,3,4,5,6,7,8,9]
func even(_ numbers: [Int]) -> Int{
var sum = 0
for i in numbers{
if i % 2 == 0 {
sum = sum + i
}
}

return sum
}
print(even(nums))
```


## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`


## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

## Question 17

Write a function that determines if a value is inside of array.


## Question 18

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`


## Question 19

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.


## Question 20

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`


## Question 21

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```

Sample output: `3`


## Question 22

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]
```

Output: `13`


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.


## Question 24

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

## Question 25

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`


## Question 26

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`


## Question 27

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`


## Question 28

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`


## Question 29

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`


## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`


## Question 31

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`


## Question 32

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)


## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)


## Question 34

Write your own `min()` and `max()` functions for an Array of Ints


## Question 35

Given two arrays of Ints, write a function that tells you all the values they have in common.


## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.


## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`
