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
