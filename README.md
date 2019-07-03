# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```
```
var problem = "split this string into words and print them on separate lines"

var wordArray = problem.components(separatedBy:" ")
    for word in wordArray {
        print(word)
    }
```

Example

Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```


## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "
```
```
let testString = "  How   about      thesespaces  ?  "

var condensedString = testString.replacingOccurrences(of: " +", with: " ", options:.regularExpression)

    print(condensedString)
```

## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`
```
let input = "Swift is the best language"
let newWords = input.components(separatedBy: " ")
var output = ""
    for word in newWords.reversed() {
        output += "\(word) "
    }

```
## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`
```
let sampleInput = "danaerys dad cat civic bottle"
let wordArray = sampleInput.components(separatedBy: " ")

var output = 0 //how many palindromes
    for word in wordArray {
        if word == String(word.reversed()) {
            output += 1
            }
        }
    print(output)
```

## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`
```
var studentRecord = "PPALLP"
var numAbscences = 0
var numLateness = 0
var reward = true

for status in studentRecord {
    if status == "A" {
        numAbscences += 1
        }
    if status == "L" {
        numLateness += 1
        }
    if numAbscences > 1 || numLateness > 2 {
        reward = false
        break
        }
    }
if reward == true {
    print("Student eligible for rewards")
    } else {
    print("Student are not eligible for rewards")
}

```
## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`
