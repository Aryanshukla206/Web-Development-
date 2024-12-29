# 🌟 Master JavaScript Notes 🌟

## 🛠️ Variables

### 🏷️ `var`

- Used to declare 📦.
- Function-scoped, not block-scoped.
- Can be redeclared and updated.

```javascript
var x = 10;
x = 20; // ✅ Allowed
var x = 30; // ✅ Allowed
console.log(x); // 30
```

### 🔒 `let`

- Block-scoped.
- Cannot be redeclared in the same 🏠 but can be updated.

```javascript
let y = 10;
y = 20; // ✅ Allowed
let y = 30; // ❌ Error
console.log(y);
```

### 🔐 `const`

- Block-scoped.
- Must be initialized at the time of declaration and cannot be updated or redeclared.

```javascript
const z = 10;
z = 20; // ❌ Error
console.log(z); // 10
```

## 🗂️ Data Types

### ✏️ `String`

- Text values enclosed in single, double, or backticks.

```javascript
let str = "Hello, World!";
console.log(str.length); // 13
```

### 🔢 `Number`

- Represents integers and floating-point numbers.

```javascript
let num = 42;
console.log(num + 10); // 52
```

### ✅ `Boolean`

- Represents true or false.

```javascript
let isJavaScriptFun = true;
console.log(isJavaScriptFun); // true
```

### 🗝️ `Object`

- Key-value pairs.

```javascript
let obj = { name: "Aryan", age: 25 };
console.log(obj.name); // "Aryan"
```

### 📚 `Array`

- Ordered list of 📦.

```javascript
let arr = [1, 2, 3];
console.log(arr[0]); // 1
```

### 🚫 `Null`

- Represents an intentional absence of value.

```javascript
let value = null;
console.log(value); // null
```

### 🤷 `Undefined`

- 📦 declared but not assigned.

```javascript
let unassigned;
console.log(unassigned); // undefined
```

## ➕ Operators

### ➗ Arithmetic

- `+`, `-`, `*`, `/`, `%`

```javascript
console.log(10 + 5); // 15
```

### 📋 Assignment

- `=`, `+=`, `-=`, etc.

```javascript
let x = 5;
x += 10;
console.log(x); // 15
```

### ⚖️ Comparison

- `==`, `===`, `!=`, `!==`, `<`, `>`

```javascript
console.log(10 === "10"); // false
```

### 🔗 Logical

- `&&`, `||`, `!`

```javascript
console.log(true && false); // false
```

### ☝️ Unary

- `typeof`, `+`, `-`, `!`

```javascript
console.log(typeof 123); // "number"
```

### ❓ Ternary (Conditional)

- `condition ? expr1 : expr2`

```javascript
let age = 18;
let type = age >= 18 ? "Adult" : "Minor";
console.log(type); // "Adult"
```

## 🔄 Control Flow

### ❓ `if`

```javascript
if (x > 10) {
  console.log("x is greater than 10");
}
```

### ❗ `else`

```javascript
if (x > 10) {
  console.log("x is greater");
} else {
  console.log("x is not greater");
}
```

### 🤔 `else if`

```javascript
if (x > 10) {
  console.log("Greater");
} else if (x === 10) {
  console.log("Equal");
} else {
  console.log("Smaller");
}
```

### 🔄 `switch`

```javascript
switch (day) {
  case 1:
    console.log("Monday");
    break;
  default:
    console.log("Unknown");
}
```

### 🌀 `for`

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### 🔁 `while`

```javascript
while (x > 0) {
  console.log(x--);
}
```

### 🔂 `do-while`

```javascript
do {
  console.log(x);
} while (x-- > 0);
```

## 🛠️ Functions

### 📝 Declaration

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

### 💭 Expression

```javascript
const greet = function(name) {
  return `Hello, ${name}!`;
};
```

### 🚀 Arrow Function

```javascript
const greet = (name) => `Hello, ${name}!`;
```

### ⏩ IIFE

```javascript
(function() {
  console.log("Immediately Invoked!");
})();
```

## 🌍 Scope

### 🌐 Global

- Available everywhere.

### 🔒 Local

- Declared inside functions.

### 🛑 Block

- Declared using `let` or `const` inside blocks.

### 🔄 Lexical

- Inner functions have access to outer 📦.

```javascript
function outer() {
  let x = 10;
  function inner() {
    console.log(x);
  }
  inner();
}
```

## 🗂️ Arrays

### 🛠️ Array Methods

- `push()`, `pop()`, `shift()`, `unshift()`, `splice()`, `slice()`, `concat()`

```javascript
let arr = [1, 2, 3];
arr.push(4); // [1, 2, 3, 4]
arr.pop(); // [1, 2, 3]
arr.shift(); // [2, 3]
arr.unshift(0); // [0, 2, 3]
```

### 🔄 Iteration

#### forEach()

```javascript
arr.forEach((num) => console.log(num));
```

#### map()

```javascript
let squared = arr.map((num) => num ** 2);
console.log(squared); // [1, 4, 9]
```

#### filter()

```javascript
let evens = arr.filter((num) => num % 2 === 0);
console.log(evens); // [2]
```

#### reduce()

```javascript
let sum = arr.reduce((acc, num) => acc + num, 0);
console.log(sum); // 6
```

...

