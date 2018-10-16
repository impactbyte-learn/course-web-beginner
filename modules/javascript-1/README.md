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
3.14
0.1234
5.2e4 //5.2 * 10^4
```

### Boolean

Falsy values, values **interpreted as false**, are

```0
*0
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

### Object

Functions, arrays and what we call objects are object types

```js
{ a: 1, b: 2 } // object
[1,2,3] // array
function a () { /* do something */ } // function
```

## Variables

A variable is a literal assigned to an identifier, so you can reference and use it later in the program.

### Types

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

## Conditionals

Used to executes a statement if a specified condition is truthy. If the condition is falsy, another statement can be executed.

### Types

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

## JavaScript Object

Used to store a collection of data written as **name:value** pairs

## Loop

Used to execute the same block of code a specified number of times or while a specified condition is true

### Types

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
