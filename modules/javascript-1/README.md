# JavaScript 1

# JavaScript

JavaScript is a popular programming language that usually used to build web application rapidly.

## Rules
- **Semicolos**, aren’t mandatory, and JavaScript does not have any problem in code that does not use them.
- JavaScript is **case sensitive**. A variable named `something` is different from `Something`.
- **Comments**
  ```js
  /*
    this comment is for multiple line
    1
    2
    3
  */

  // this comment is for single line
  ```

## Where do I Write JS?
### In HTML
```html
<!DOCTYPE html>
<html>
<head>
  <title>Document</title>
</head>
<body>
  <script>
    alert('Hi')
  </script>
</body>
</html>
```

### In a Seperate File
`index.html`:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Document</title>
</head>
<body>
  <script src="index.js"></script>
</body>
</html>
```

`index.js`:
```js
alert('Hi')
```

## JavaScript Data Types

- [String](#string)
- [Number](#number)
- [Boolean](#boolean)
- [Undefined](#undefined)
- [Null](#null)
- [Object](#object)

### String

```js
"Impact Byte"
'blablabla'

'Hello, ' + 'World' // 'Hello, World'
```

#### Template String

template strings are string literals that allow a more powerful way to define strings. You can perform string **substitution** and you can have **multiline** string easily.

```js
const text = 'world'
`Hello, ${text}`

// result = Hello, world
```

### Number

```js
10
5354576767321
0xCC // hex
-3.14
0.1234
5.2e4 //5.2 * 10^4
```

### Boolean

Falsy values, values **interpreted as false**, are

```js
0
NaN
undefined
null
'' // empty string
```

All the rest is considered a **truthy value**.

### Undefined

`undefined` indicates that a variable has not been initialized and the value is absent.

### Null

`null` is a special value that indicates the absence of a value.

## JavaScript Object

Used to store a collection of data written as **name:value** pairs

```js
{
  string: 'Hi',
  boolean: true,
  number: 123
}
```

## Variables

A variable is a literal assigned to an identifier, so you can reference and use it later in the program.

#### `var`

```js
var a // undefined value
var b = 1
var c, d = 2 // bad practice

a = 0
```

#### `let` (ES6)

let is a new feature introduced in ES2015 and it’s essentially a block scoped version of var.

```js
let number = 0
```

#### `const` (ES6)

Variables declared with `const` is initialized, its value can never be changed again, and it can’t be reassigned to a different value.

```js
const PI = 3.14
const circleArea = PI * 14^2
```

## Functions

- A `function` is a block of code, self contained, that can be defined once and run any times you want.
- A `function` can optionally accept parameters, and returns one value.

### Types

#### Regular Function

```js
function dosomething() {
  // do something
}
```

#### Arrow Function

An arrow function has a shorter syntax than [function](#regular-function) and does not have its own `this`

```js
const dosomething = () => {
  // do something
}
```

#### Immediately Invocated Function Expressions (IIFE)

An IIFE is a function that’s immediately executed right after its declaration:

```js
(function dosomething() {
  // do something
})()
```

### Parameters

- A function can have one or more parameters
  ```js
  function dosomething(foo, bar) {
    // do something
  }
  ```
- Starting with ES6/ES2015, functions can have default values for the parameters
  ```js
  function dosomething(foo = 123) {
    console.log(foo)
  }

  dosomething() // 123
  dosomething(456) // 456
  ```

### `return`
The `return` statement stops the execution of a `function` and returns a value from that `function`.

```js
function calculateSquareArea(s) {
  let area = s * s

  return area
}
```

## Conditionals

Used to executes a statement if a specified condition is truthy. If the condition is falsy, another statement can be executed.

#### `if`

```js
if (true) {
  // do something
}

if (true) // do something
```

#### `if...else`

```js
if (true) {
  // do something
} else {
  // do something else
}
```

#### `else if`

```js
if (123) {
  // do something
} else if (456) {
  // do something else if
} else {
  // do something else
}
```

#### Ternary Operator (Shorthand)

A shortcut for the `if` statement that takes three operands.

```js
true ? /* do something */ : /* do something else */
```

#### `switch`
```js
var color = "green";

switch(color) {
  case "yellow":
    alert("yellow color");
    break;
  case "red":
    alert("red color");
    break;
  default:
    alert("no known color specified");
    break;
}
```

## Array

An array is used to store a collection of data.

### Initialize Array

```js
const a = []
const a = [1, 2, 3]
const a = Array.of(1, 2, 3) // [1, 2, 3]
const a = Array.from('foo') // ['f', 'o', 'o']
const a = Array(6).fill(1) // init an array of 6 items of value 1
```

#### Bad Practice

```js
const a = new Array(1, 2, 3)
```

### Manipulating Arrays

#### Adding

```js
let a = []

console.log(a) // []

a[0] = 'abc'

console.log(a) // ['abc']
```

## Loop

Used to execute the same block of code a specified number of times or while a specified condition is true

#### `for`

```js
const list = ['a', 'b', 'c']

for (let i = 0; i < list.length; i++) {
  console.log(list[i])
}
```

#### `do...while`

```js
const list = ['a', 'b', 'c']
let i = 0

do {
  console.log(list[i])

  i = i + 1
} while (i < list.length)
```

#### `while`

```js
const list = ['a', 'b', 'c']
let i = 0

while (i < list.length) {
  console.log(list[i])

  i = i + 1
}
```

#### `for..in` (JavaScript Object only)

Iterates all the enumerable properties of an object, giving the property names.

```js
for (let property in object) {
  console.log(property) // key
  console.log(object[property]) // value
}
```

#### `for...of`

```js
const list = ['a', 'b', 'c']

for (const value of list) {
  console.log(value)
}
```

## Built-in Functions
### `String`
```js
let string = "Impact Byte"

string[2] // p
string.charAt(2) // p
string.length // 11
```

#### `String.toUpperCase()`
```js
string.toUpperCase() // IMPACT BYTE
```

#### `String.toLowerCase()`
```js
string.toLowerCase() // impact byte
```

#### `String.split(separator[, limit])`
```js
string.split(" ") // ["Impact", "Byte"]
string.split(" ", 1) // ["Impact"]
```

#### `String.replace(regexp|string, newString)`
```js
string.replace("Byte", "Hub") // Impact Hub
```

#### `String.slice(begin[, end])`
```js
string.slice(2, 4) // pa
string.slice(11) // t Byte
```

#### `String.substring(from[, to])`
```js
string.substring(0, 5) // Impac
string.substring(11) // t Byte
```

#### `String.substr(start[, length])`
```js
string.substr(0, 5) // Impac
string.substr(5) // t Byte

```

### `Math`
#### `Math.min(value1, value2, ...n)`
```js
Math.min(1, 3, 0.5, 10) // 0.5
```

#### `Math.max(value1, value2, ...n)`
```js
Math.max(1, 3, 0.5, 10) // 10
```

#### `Math.ceil(value)`
```js
Math.ceil(5.95) // 6
Math.ceil(5.25) // 6
```

#### `Math.floor(value)`
```js
Math.floor(5.95) // 5
Math.floor(5.25) // 5
```

#### `Math.random(value)`
Generate random number between 0 and 1.
```js
Math.random() // 0.28442271261566443
```

### `Array`
```js
let array = [1, 2, 3]

array[1] // 2
array.length // 3
```

#### `Array.push(element1, element2, elementN)`
```js
array.push(3) // [1, 2, 3, 3]
```

#### `Array.unshift(element1, element2, elementN)`
```js
array.unshift(-1, 0) // [-1, 0, 1, 2, 3]
```

#### `Array.pop()`
```js
array.pop() // 3
```

#### `Array.shift()`
```js
array.shift() // 1
```

#### `Array.indexOf(element)`
```js
array.indexOf(3) // 2
array.indexOf(4) // -1
```

#### `Array.concat(element)`
```js
array.concat([4, 5, 6]) // [1, 2, 3, 4, 5, 6]
```

### `Object`
#### `Object.keys(obj)`
```js
Object.keys({ firstName: 'John', lastName: 'Doe' }) // ['firstName', 'lastName']
```

#### `Object.values(obj)`
```js
Object.values({ firstName: 'John', lastName: 'Doe' }) // ['John', 'Doe']
```

#### `Object.assign(target, ...sources)`
```js
Object.assign({ firstName: 'John', lastName: 'Doe' }, { age: 40 }) // { firstName: 'John', lastName: 'Doe', age: 40 }
```
