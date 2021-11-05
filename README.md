
# <strong> Swift 의 활용

* [기본](#기본)<br>
* [기본 오퍼레이터](#기본-오퍼레이터)
* [데이터 타입](#data-types) 
* [함수](#function)
* [클로저](#closure)
</strong>


### 기본 
---
Swift 문법에서 Contant 형은 `let age: Int = 20` 과 같이 정의를 한다. 변수는 `var number: Int = 30` 과 같이 표현하며, 데이터 타입은 변수 명 뒤에 콜론(:) 과 함께 대문자로 시작하는 데이터 타입을 지정. 
상수 또는 변수를 선언할 때 유형 주석을 제공하여 상수 또는 변수가 저장할 수 있는 값의 종류를 명확히 할 수 있습니다. 상수 또는 변수 이름 뒤에 콜론, 공백, 사용할 유형 이름을 차례로 배치하여 유형 주석을 작성합니다. 타입지정을 하지 않을 경우에는 swift가 알아서 유추하여 지정된다. 

**다양한 변수지정**
```swift 

let age = 55
let names = "Faker"
 
let age: Int = 20       
var number: Int = 30    
var name: String = "Faker"
var names: Array<String> = ["Faker", "ShowMaker", "Bdd"]
var names: [String] = ["Faker", "ShowMaker", "Bdd"]

var char: Character = "A" 

var pi: Double = 3.14159 
var pi: Float = 3.14 
var boolean: Bool = true // -- or false 

// semi-colon is good 
var x = 0.0, y = 0.0 , z = 0.0; 

// 정수 바운드리 
let minValue = UInt8.min 
let maxValue = UInt8.max 

```
|     Type     |     Size     |     Range     |
|--------------|--------------|---------------|
|Int8|8 bit|-128 ~ 127|
|Int16|16 bit|-2^15 ~ 2^15 - 1|
|Int32|32 bit|-2^31 ~ 2^31 - 1|
|Int64|64 bit| -2^63 ~ 2^63 - 1 |
|UInt|플랫폼에 따라 다름| 0 ~ 2^32 or 2^64|


**다양한 주석처리**
```swift
// -- one line comments 
/* 
    multi-line comments 
*/ 

```

**타입별칭 (Type Alias)**
```swift

typealias DataInt = Int32;

let Max = DataInt.max 
let Min = DataInt.min

print(Max); 
print(Min);

```
**튜플(Tuple)**
* 튜플은 여러 값을 단일 복합 값으로 그룹화합니다. 튜플 내의 값은 모든 유형이 될 수 있으며 서로 동일한 유형일 필요는 없습니다. 
```swift
let http404Error = (404, "Not Found")

let (statusCode, statusMessage) = http404Error 
print("The status code is \(statusCode)")
print("The status message is \(statusMessage)")

// 변수를 무시하고 싶다면 
let (statusCode, _) = http404Error 
print("The status code is \(statusCode)")

// or 
print("The status code is \(http404Error.0)")
print("The status message is \(http404Error.1)")

// 튜플이 정의될 때 튜플의 개별 요소 이름을 지정할 수 있습니다. 
let http200Status = (statusCode: 200, description: "OK")
print("The status Code is \(http200status.statusCode)")
print("The status message is \(http200status.description)")

```
**Optional**
* 값이 없을 수있는 상황에서 옵션을 사용합니다. 선택 사항은 두 가지 가능성을 나타냅니다. 값이 있으며 선택 사항을 눌러 해당 값에 액세스 할 수 있거나 값이 전혀 없습니다. 

* 1 
* 2
* 3
### 기본 오퍼레이터

---
