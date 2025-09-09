# JavaScript ES6 Questions & Answers

This document contains important JavaScript ES6 questions and their explanations.

---

## 1️⃣ What is the difference between `var`, `let`, and `const`?

*Answer:*  
- **`var`**
  - Function-scoped or globally scoped.
  - Can be redeclared and updated.
  - Hoisted (initialized as `undefined` before declaration).

- **`let`**
  - Block-scoped.
  - Can be updated but **cannot be redeclared** in the same scope.
  - Not hoisted like `var`.

- **`const`**
  - Block-scoped.
  - Cannot be updated or redeclared.
  - Must be initialized at the time of declaration.
  - Ideal for values that should not change (constants).

**Example:**

var x = 10;
x = 20; // okay
var x = 30; // okay

let y = 10;
y = 20; // okay
// let y = 30; // ❌ Error

const z = 10;
// z = 20; // ❌ Error

---

## 2️⃣ What is the difference between `map()`, `forEach()`, and `filter()`?

*Answer:*  
map()

Creates a new array with the result of calling a function on each element.

Returns the same number of elements as the original array.

forEach()

Iterates over each element.

Does not return anything (undefined).

Used for side effects like logging or updating variables.

filter()

Creates a new array containing elements that satisfy a condition (returns true).

Can return fewer elements than the original array.

---

## 3️⃣ What are arrow functions in ES6?

*Answer:*  
Arrow functions provide a shorter syntax for writing functions.

They do not have their own this, so they inherit this from the surrounding scope.

Useful for concise callbacks.

// Regular function
function sum(a, b) {
  return a + b;
}

// Arrow function
const sumArrow = (a, b) => a + b;

console.log(sumArrow(2, 3)); // 5

---

## 4️⃣ How does destructuring assignment work in ES6?

*Answer:*  
Allows extracting values from arrays or objects into variables.

Makes code cleaner and reduces repetitive access.

Example:

// Array destructuring
const numbers = [1, 2, 3];
const [a, b] = numbers;
console.log(a, b); // 1 2

// Object destructuring
const person = {name: 'Alice', age: 25};
const {name, age} = person;
console.log(name, age); // Alice 25

---

## 5️⃣ Explain template literals in ES6. How are they different from string concatenation?

*Answer:*  
Template literals use backticks (`) instead of quotes.

Allow interpolation (embedding variables) using ${}.

Support multi-line strings without \n.

Difference from string concatenation:

Concatenation uses + and can be messy.

Template literals are cleaner and readable.

Example:

const name = 'Alice';
const age = 25;

// String concatenation
console.log('Name: ' + name + ', Age: ' + age);

// Template literal
console.log(`Name: ${name}, Age: ${age}`);
