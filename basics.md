#### comment

    // let's learn swift

#### variable

    var str : String = "hello"

#### constant

    let birdsong : Bool = true

#### : ?

    : <= is defining explicitly the type, otherwise it is inferred.

#### print

    print("hello")
    print(variable)

sends this to the console output

    println("prints to a new line")

use variables inside strings (like rails)

    println("build \(str)")
    var message = "\(str) John"

    let language = "Swift"
    println("Learning \(language)")

* mutable string = variable
* imutable string = constant
* concatenation = "aa" + "bb"  

    println("Bread\nMilk\nHoney")

* \n
* \t
* "\u{1F496}" <= unicode, emoji heart

#### numbers

    var version = 1.0 ...double
    let year = 2015 ...int
    var version : Float = 1.0 ...now we've explicitly set it to float, will always assume double

    let title = "A Dance with Dragons"
    let price = 9.99
    let yearPublished = 2011

#### binary

    let height = 12
    let width = 10
    let area = height * width
    let areaInMeters = Double(area) / 10.764

#### operator precedence

    var x = 100 + 100 - 5 * 2 / 3 % 7
    = 197
    precedence 150
    1. multiplication
    2. division
    3. remainder
    precedence 140
    4. addition
    5. subtraction
    << left to right >>


    let y = 25 - 5 * 2
    = 15 (25 - 10)

    let a = (2 + 2) * 2 + 2
    = 10

    let remainder = 7 % 7
    = 0

    let z = 100 / 2 + 5
    = 55

#### unary operators

    var score = 5
    score++
    ++score

    let on = true
    let off = !on
    => false

    var levelScore = 100
    var totalScore = -levelScore
    = -100
    var levelScore = 100
    var totalScore = --levelScore
    = 99
    var totalScores = 10 - 20
    ++totalScores
    = -9

#### arrays

    var todo = ["aa", "bb", "cc"]
    todo += ["dd"]
    => ["aa", "bb", "cc", "dd"]
    todo[0]
    => "aa"
    todo.count
    => 4

    var todo = ["Learn Swift", "Build App", "Deploy App"]
    println(todo.count)
    => 3

#### collections

    todo.append("ee")
    => ["aa", "bb", "cc", "dd", "ee"]
    todo[2] = "22"
    => 22
    todo
    => ["aa", "bb", "22", "dd", "ee"]
    let item = todo.removeLast()
    item
    => "ee"
    let other = todo.removeAtIndex(2)
    other
    => "22"
    todo
    => ["aa", "bb", "dd"]
    todo.insert(item, atIndex: 0)
    => ["ee", "aa", "bb", "dd"]


    var todo = ["Learn Swift", "Build App", "Deploy App"]
    todo += ["Debug App", "Fix Bugs"]
    let item = todo.removeAtIndex(2)
    todo.insert("Learn iOS", atIndex: 1)

#### dictionaries

* key / value
* similar to JSON

    var countries = [ "CA": "Canada", "BE": "Belgium"]
    => ["BE": "Belgium", "CA": "Canada"]
    countries["CA"]
    => {Some "Canada"}
    countries["US"]
    => nil
    countries["US"] = "United States"
    countries
    => ["BE": "Belgium", "US": "United States", "CA": "Canada"]
    let ca = countries.removeValueForKey("CA")

    let currencies = ["US": "Dollar", "UK":"Pound", "JP": "Yen"]
    let ukCurrency = currencies["UK"]

#### Loops

    for item in todo {
      println(item)
    }
    =>
    ee
    aa
    bb
    dd

* view / show assistant editor to show the actual values

    for number in 1...10 {
      println("\(number) times 2 is \(number*2)")
    }
    =>
    1 times 2 is 2
    2 times 2 is 4
    3 times 2 is 6
    4 times 2 is 8
    5 times 2 is 10
    6 times 2 is 12
    7 times 2 is 14
    8 times 2 is 16
    9 times 2 is 18
    10 times 2 is 20

* 1...10 is a range from 1 to 10, closed range, inclusive
* 1..<10 is a range from 1 to 9, half closed range, upper limit is non-inclusive

    for number in 1...10 {
      println("\(number) * 7 = \(number*7)")
    }

#### control flow

    var index = 0
    let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    while index < numbers.count {
        println(numbers[index])
        index++
    }


    var index = 0
    while index < todo.count {
    println(todo[index])
        index++
    }


    index = 0
    do {
      println(todo[index])
      index++
    } while index < todo.count


    let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    var index = 0
    while index < numbers.count {
      println(numbers[index])
      index++
    }

#### for condition increments

    for var i = 0; i < todo.count; i++ {
      println(todo[i])
    }
    =>
    index, condition, increment

* < less than
* <= less than or equal to
* > greater than
* >= greater than or equal to
* == equal to
* != not equal to
* === identical
* !== not identical

#### if statement

    let cards = 1...13
    for card in cards {
      if card == 11 {
        println("Jack")
      } else {
        println(card)
      }
    }


    let months = [1, 2, 3]
    for month in months {
        if month == 1 {
            println("January")
        } else if month == 2 {
            println("February")
        } else if month == 3 {
            println("March")
        }
    }

#### switch

    for month in months {
        switch month {
        case 1:
            println("January")
        case 2...3:
            println("Others")
        default:
            println(month)
        }
    }

#### comparision and logical operators

* && is the AND operator
* || is the OR operator
* ! is the NOT operator
