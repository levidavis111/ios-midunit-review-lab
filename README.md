## Mid Unit-1 Review


## Strings

1. **Given a String, return a String with each letter uppercased**

Input: `Hello, there`

Output: `HELLO, THERE`

var myString = "hello, there"

print(myString.uppercased())

2. **Given a String, return a String alternating between uppercase and lowercase letters**

var myString = "hello, there"
var myStringArray = [String]()
var myBlankString = ""

for (i,j) in myString.enumerated() {
//    print(i,j)
if i % 2 == 0 {
j.uppercased()
myBlankString += j.uppercased()
}
else {
myBlankString += String(j)
}
}
print(myBlankString)

Input: `Hello, there`

Output: `HeLlO, tHeRe`


3. **Given a String, return a String with all occurrences of a given letter removed**

Input: `Hello, there`

Output: `Hllo, thr`

var myString = "hello, there"
print(myString.replacingOccurrences(of: "e", with: ""))


## Arrays


1. **Given an array of type [Int], return the largest element**

Input: `[1,5,2,4,1,4]`

Output: `5`


var myArray = [1,5,2,4,1,4,10]

print(myArray.max()!)



2. **Given an array of type [Int], return the smallest element**

Input: `[1,5,2,4,1,4]`

Output: `1`

var myArray = [1,5,2,4,1,4]

print(myArray.min()!)

3. **Given an array of type [Int], return its sum**

Input: `[1,5,2,4,1,4]`

Output: `17`

var myArray = [1,5,2,4,1,4]

print(myArray.reduce(0, +))


4. **Given an array of type [Double], return its average**

Input: `[3,4.5,7.5,2,1]`

Output: `3.6`

var myArray = [3,4.5,7.5,2,1]
var emptyArray: [Double] = []

var reduced = myArray.reduce(0, +)
var average = reduced / Double(myArray.count)
print(average)


5. **Given an array of type [Double] and a Double, return the sum of all numbers in the array greater than a given number**

Input: `[3,4.5,7.5,2,1], 3`

Output: `12`


var arrayOfDoubles = [3,4.5,7.5,2,1]
var oneDouble: Double = 3
var sum: Double = 0

for i in arrayOfDoubles {
if i > oneDouble {
sum += i
}
}
print(sum)


6. **Given an array of type [Double], return the product of all the elements**

Input: `[3,4.5,7.5,2,1]`

Output: `202.5`

var doublesArray = [3,4.5,7.5,2,1]


func arrayProduct(_ a: [Double]) -> Double {
var product: Double = 1

for i in a {
product = product * i
}

return product
}
print(arrayProduct(doublesArray))

7. **Given an array of type [Int], return the second smallest value in the array**

Input: `[3,6,1,9,4,8]`

Output: `3`

var myArray = [3,6,1,9,4,8]

myArray.sorted().dropFirst()
print(myArray[0])


## Optionals

1. **Given an array of type [String?] return an array of [String] removing all nil values**

Input: `[nil, "We", "come", nil, "in", "peace"]`

Output: `["We", "come", "in", "peace"]`

var stringArray = [nil, "We", "come", nil, "in", "peace"]
var emptyArray: [String] = []


for i in stringArray {
if let i = i {
emptyArray.append(i)
}

}
print(emptyArray)

2. **Given an array of type [String?]? return an array of [String] removing all nil values**

Input: `nil`

Output: `[]`

var nilArray: [String?]? = [nil]
var emptyArray: [String] = []

if let nilArray = nilArray {
for i in nilArray {
if let i = i {
emptyArray.append(i)
}
}
}
print(emptyArray)


3. **Given an array of type [Int?] return the sum of all non-nil values.  Use guard statements in your solution.**

Input: `[4, nil, 9, 5, nil]`

Output: `18`

var optionalArray: [Int?] = [4, nil, 9, 5, nil]
var sum = 0
for i in optionalArray {
guard let i = i else {
continue
}
sum += i
}
print(sum)

4. **Given an array of type [Int?]? return the sum of all non-nil values.  Use guard statements in your solution.**

Input: `nil`

Output: `0`

var optionalArray: [Int?] = [nil]
var sum = 0

for i in optionalArray {
guard let i = i else {
continue
}
sum += i
}
print(sum)


5. **Given an array of type [Int?] and an optional Int, return the sum of all values not equal to the given number.  If the given number is nil, return the sum of all non-nil values.**

Input: `[1, 1, nil, 3, 5, nil, 1, nil, 3, 5, nil, 5, nil, 3], 1`

Output: `24`

var myArray: [Int?] = [1, 1, nil, 3, 5, nil, 1, nil, 3, 5, nil, 5, nil, 3]
var optionalInt: Int? = 1
var sum = 0

for i in myArray {
if let i = i {
if let optionalInt = optionalInt {
if i != optionalInt {
sum += i
}
}

}
}
print(sum)


## Dictionaries

Dictionaries
1. **Given an array of type [String], return a copy of the array with all duplicate values removed**

Input: `["apple", "apple", "banana", "banana", "banana", "cake", "cake"]`

Output: `["apple", "banana", "cake"]`

var myArray = ["apple", "apple", "banana", "banana", "banana", "cake", "cake"]
var myDict: [String:Int] = [:]

for (k,v) in myArray.enumerated() {
myDict[v] = k

}
print(myDict.keys)

2. **Given a String, find the most frequently occurring letter**

Input: `Never trust a computer you can't throw out a window ~ Steve Wozniak`

Output: `t`

var myString = "Never trust a computer you can't throw out a window ~ Steve Wozniak"
var myDict: [Character:Int] = [:]
var counter = 0
var emotyString = String()
var myArray = [Character]()

for i in myString {
myArray.append(i)
}
print(myArray)

for i in




Closures

1. **Given an array of type [String], return an array that contains the Strings sorted alphabetically with capital letters first (Swift will do that part automatically)**

var myArray = ["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]
print(myArray.sorted())

Output: `["Never", "a", "a", "can\'t", "computer", "out", "throw", "trust", "window", "you"]`


//2. **Given an array of type [String], return an array that contains the Strings sorted by length**

var myArray = ["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]

print(myArray.sorted(by: {(a,b) -> Bool in
return a.count > b.count
}))
//Output: `["a", "a", "you", "out", "Never", "trust", "can\'t", "throw", "window", "computer"]`

print(myArray.sorted(by: {$0.count < $1.count}))

3. **Given an array of type [String], return an array containing all Strings at least 4 characters long**

var myArray = ["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]
print(myArray.filter({$0.count >= 4}))
Output: `["Never", "trust", "computer", "can\'t", "throw", "window"]`

4. **Given an array of type [String], return a String containing all of the Strings from the array combined and separated by spaces.  Do this first without using the `joined(separator:) method`**

var myArray = ["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]
print(myArray.reduce("", {$0 + " " + $1}))

Output: `Never trust a computer you can't throw out a window`


/ENUMNUMNUMNUM

1. **Given an array of type [Int] and an instance of NumberType (defined below), return an array containing only all the even or odd numbers.**
var myArray = [1,2,3,4,5,6]
enum NumberType {
case even
case odd

func caseEvenOdd(input:[Int]) -> [Int] {
var emptyArray = [Int]()
switch self {
case .even:
emptyArray = myArray.filter({$0 % 2 == 0})
case.odd:
emptyArray = myArray.filter({$0 % 2 != 0})
}
return emptyArray
}

}
var myType = NumberType.even.caseEvenOdd(input: myArray)
print(myType)


2. **Given a String and an instance of StringType (defined below), return the String either lowercased or uppercased**

var myString = "Design is not just what it looks like and feels like. Design is how it works"
enum StringType {
case lowercase
case uppercase

func upperLower(input:String) {
switch self {
case .lowercase:
print(input.lowercased())
case .uppercase:
print(input.uppercased())
}
}
}

var newString = StringType.uppercase
newString.upperLower(input: myString)

3. **Given an array of type [FileStatus] (defined below) and an Int, return an array containing only files that were saved more than that many times**


enum FileStatus: CustomStringConvertible {
case unsaved
case saved(numberOfVersions: Int)
var description: String {
switch self {
case .unsaved: return "Unsaved File"
case let .saved(numberOfVersions): return "File that has been saved \(numberOfVersions) times"
}
}
}

var fileStatus = [FileStatus.saved(numberOfVersions: 5), FileStatus.saved(numberOfVersions: 3), FileStatus.saved(numberOfVersions: 8)]

var file = FileStatus.saved(numberOfVersions: 4)
fileStatus.filter({$0 > file})

