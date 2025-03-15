### What are Programs?

- **Programs**: Text files written by humans to instruct computers.
- **Code**: The text written in a program, often referred to as "code."
- **Programmers/Coders**: People who write programs.
- **Programming Language**: A human-readable language used to write programs (e.g., Python, Java).
- **Compiler/Interpreter**: Tools that translate code into machine instructions for execution.
- **Execution**: The process of running the program line-by-line after translation.

### Parsing

- **Parsing**: The process of breaking up each line of a program to determine its meaning for the machine.
- **Tokens**: A program statement is broken into tokens, e.g., `const a = 4` → `const`, `a`, `=`, `4`.
- **Syntax**: Defines the meaning of tokens in a language. Example in **JavaScript**:
  - `const` → Declares a variable.
  - `a` → Variable name.
  - `=` → Assignment operator.
  - `4` → Value assigned to `a`.
- **Compiler’s Role**:
  1. Parses statements.
  2. Forms a tree-like structure.
  3. Generates machine instructions from the structure.
- **Compilation and Execution**:
  - Some languages compile machine code for execution on servers.
  - **JavaScript** uses **Just-in-Time (JIT) Compilation**, where code is compiled just before execution for faster performance.
 
### Variables in JavaScript

- **Variable**: A way to store a value for later use in a program.
- 
  ```javascript
  const a = 3;
  
### Multiple Variables in JavaScript

- **Statement**: Each line of code in JavaScript is called a statement. For example:
  ```javascript
  const a = 4;
  const b = a;
  ```
JavaScript statements should end with `;`.

### Booleans

Variables can store booleans: `true` or `false`.

Example:

```javascript
const loggedIn = false; // User is not logged in.
const purchasedItem = true; // User purchased the item.
Valid variable characters: a-z, A-Z, $, _, 0-9 (cannot start with a digit).
UPPER_SNAKE_CASE is used for environment variables or pre-execution values.
```
### Strings in JavaScript

- **What is a String?**: A string is a sequence of characters (letters, numbers, symbols) put together to form a message.

- **Defining Strings**: In JavaScript, you can define a string in three ways:
  1. **Double quotes**:
     ```javascript
     const myName = "Dan";
     Escaping Double Quotes Inside Double Quotes use  backslash (\) \"
     ```
  2. **Single quotes**:
     ```javascript
     const anotherName = 'Cody';
     
     ```
  - Both double quotes (`"`) and single quotes (`'`) can be used interchangeably for defining strings.

  3. **String Interpolation with Backticks**: You can also use **backticks** to define strings, which allows string interpolation. This is useful for inserting variables inside the string.
  ```javascript
  const helloMessage = `Hello ${anotherName}, my name is ${myName}!`;
  
### Changing a Variable in JavaScript

- **Constants with `const`**: When you declare a variable with `const`, its value cannot be changed after initialization. If you attempt to modify it, JavaScript will throw an error.

  ```javascript
  const a = 3;
  a = 5;  // This will throw an error: TypeError: Assignment to constant variable.
  // Use let for Mutable Variables
  let a = 3;
  a = 5;  // This is allowed, and a now equals 5.
  ```
  
### Comments in JavaScript


**Single-line Comment**: Uses `//` to add comments that are ignored by the JavaScript engine:
  ```javascript
  // This is a comment
  multi-line Comment*
  /* The price of all of our items
   Denominated in U.S. Dollars */
```
### JavaScript Functions & Operators

- **What is a Function?**: A function is a reusable block of code that takes inputs, performs some operations, and returns an output based on those inputs.

  - **Example**: Imagine a function that adds 1 to any number you give it:
    - **Input** → **Function** → **Output**
    - Input: `1` → Output: `2`
    - Input: `4` → Output: `5`
### JavaScript Function Syntax

- **Calling a Function**: To call (or invoke) a function means to execute it. Often, you pass specific input values when calling a function.

  - **Example**: Calling the `addOne` function with an input of `2`:
    ```javascript
    const output = addOne(2);
    ```
    - Here, `addOne` is the function, and the value `2` is passed as the input.

  - **No Input Function**: Some functions don't need input values:
    ```javascript
    const message = getMessage();
    ```
    - This calls the `getMessage` function without any inputs.

- **Function Declaration**: To call a function, you first need to declare (define) it.

  - **Example 1**: A function that adds `1` to the input value:
    ```javascript
    function addOne(input) {
        return input + 1;
    }
    ```

  - **Example 2**: A function that returns a string without any inputs:
    ```javascript
    function getMessage() {
        return "Hello World!";
    }
    ```

- **Return Statement**: The `return` keyword specifies what value a function will output when called. The function will return this value to where it was called.

  - **Example**: If you call `addOne(1)`:
    ```javascript
    const a = addOne(1);
    ```
    - The variable `a` will be assigned the return value of `addOne(1)`, which is `2`.

- **Declaring a Function**: "Declaring a function" is another way of saying "defining a function." Once a function is declared, you can call it from other parts of your program.

### Parameters and Arguments in JavaScript

- **Parameters**: Variables defined in the function declaration to accept inputs.
- **Function with Input**: To create a function that accepts an input, define the parameter in the parentheses.

  ```javascript
  function addNumbers(a, b) {
      return a + b;
  }
  ```
  **Arguments**: The actual values passed to the function when called.
  Calling the Function: When calling a function, pass the argument inside the parentheses.
```javascript
addNumbers(1, 2);
```
### Multiplying Numbers & Passing Multiple Function Inputs

- **Multiplication Operator (`*`)**: To multiply numbers, use the `*` operator.

  ```javascript
  const a = 2;
  const b = a * 3; // b will be 6
  ```
### Division Operator (`/`)

- The **division operator** `/` divides the left-side value by the right-side value.

  ```javascript
  const result = 8 / 4; // result will be 2

- ### Multiple Inputs in Functions

- You can define a function that accepts multiple inputs, separated by commas.

  ```javascript
  function sum(a, b, c) {
      return a + b + c;
  }
  ```
  ### Operator Precedence in JavaScript

- **Multiplication vs. Addition**: 
  - The multiplication operator (`*`) takes precedence over the addition operator (`+`).
  
  ```javascript
  5 + 1 * 2 // Evaluates to 7
  4 / 4 * 2
  (5 + 1) * 2
  ```
  - Left-to-Right Evaluation with Same Precedence:
  - same precedence, like division (/) and multiplication (*),
  - The parenthesis will always be evaluated first before any other part of the expression

### **Generating Random Numbers in JavaScript**

- JavaScript provides the `Math.random()` function to generate a **random decimal number** between `0` and `1` (but **never exactly `1`**).

  ```javascript
  const myRandomNumber = Math.random();
  // 0.238476238476
  //0.874562938562
  //0.998472938472
  //multiply the result of Math.random() to scale the random number to a specific range.
  function getRandomIntInRange(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
  }
  //Math.floor() function will round a number down to the nearest integer. eg : 2.999 ==> round this input down to 2
  ```
  # 🔹 Console Log in JavaScript

## **What is `console.log`?**
`console.log` prints values to the **console** during program execution.  
 console is a built-in JavaScript object that provides methods to display messages in the developer console of a web browser/ Node.js
 The developer console is a browser tool that enables viewing logs, debugging programs, and executing JavaScript commands directly.
```javascript
console.log("Hello, world!");
```
### 🔹 Conditionals in JavaScript

### **What Are Conditionals?**
Conditionals allow a program to execute different code based on whether a condition is **true** or **false**.

---

### **🔹 The `if-else` Statement**
Used to execute a block of code **only if a condition is met**.

```javascript
if (loggedIn) {
    goToDashboard(); // Runs if loggedIn is true
} 
else {
    goToLogin(); // Runs if loggedIn is false
}
```
### 🔹 If Statement in JavaScript

### **What is an `if` Statement?**
The `if` statement allows a program to execute code **only if a condition is true**.

```javascript
if (1 === 1) {
    console.log("Yup, that's true!");
}
```
### **`!==`**
The **strict inequality operator (`!==`)** checks if two values are **not equal**.  
It returns **`true`** if the values are different, otherwise **`false`**.

```javascript
console.log(1 !== 2); // true
console.log(2 !== 2); // false
```
### Truthy & Falsy Values in If Conditions  

In JavaScript, any value can be classified as either truthy or falsy:  

### ✅ Truthy Values (Evaluate to true)  
- `true`  
- Any non-zero number (e.g., `42`, `-1`)  
- Any non-empty string (e.g., `"hello"`)  
- Any object (e.g., `{}`) or array (e.g., `[]`)  
- `Infinity`  

### ❌ Falsy Values (Evaluate to false)  
- `false`  
- `0`  
- `""` (empty string)  
- `null`  
- `undefined`  
- `NaN`
### Booleans as Conditions  

Consider the following code:  

```javascript  
const a = true;  

if (a === true) {  
    console.log('hi!'); // hi!  
}
// instead
if(a) {
    console.log('hi!'); // hi!
}
```

### **1️⃣ Function Without a `return` Statement**
In JavaScript, if a function does **not** explicitly return a value, it **automatically returns `undefined`**.

```javascript
function add(a, b) {
    // No return statement
}

const value = add(2, 3); 
console.log(value); // undefined
```
### 🔹 Greater Than & Less Than Operators in JavaScript
to compare **different values** using:
- **Greater than (`>`)** -  checks if the left value is greater than the right.
- **Less than (`<`)** - checks if the left value is smaller than the right

```javascript
console.log(1 > 4); // false
console.log(4 > 1); // true

console.log(4 < 1); // false
console.log(1 < 4); // true
```
### 🔹 Returning Early in JavaScript

###  **Use `return`?**
- Using `return` **exits** the function **immediately**.
- No code after `return` will be executed.
- Using `return` in `if-else`**
Both of the following functions accomplish the **same task**:

### ✅ **Using `if-else`**
```javascript
function isEqual(a, b) {
    if (a === b) {
        return true; // Exits the function immediately
    }
    return false; // Only runs if a !== b , note no else statement is used
}
// Removing the else  would not work! 
function isEqual(a,b) {
    if(a === b) {
        console.log('They are equal!');
    }
    // this line will always be reached
    console.log('They are not equal!');
}
```
**`>=` (Greater Than or Equal)**
**`<=` (Less Than or Equal)**
These operators also check for **equality** along with comparison.
```javascript
console.log(1 >= 2); // false
console.log(1 >= 1); // true
```
### **`else if`?**
to check **multiple conditions** and perform different actions based on which condition is met.
```javascript
if (firstCondition) {
    // Executes if firstCondition is true
} else if (secondCondition) {
    // Executes if firstCondition is false AND secondCondition is true
} else {
    // Executes if neither condition is true
}
```
### Loops

Computers are super efficient at running a large number of simple tasks! As programmers, we take advantage of this speed by writing programs that repeatedly perform a task until a certain condition is met.
For example, to read books:
1. Read each book until none are left.
2. Read each page until none are left.
3. Read each word until none are left.

### Pseudocode Example
```plaintext
while books left
    read book
    while pages left
        read page
        while words left
            read word
```
### For Loop Breakdown

A `for` loop consists of four parts: **Initialization, Condition, Update, and Statement**.

```javascript
for ([initialization]; [condition]; [update]) {
    statement;
}
```
### **Initialization**
`let i = 1;`  
- Runs once at the beginning of the loop.  
- Creates a variable and initializes its starting value.  

### **Condition**
`i <= 4;`  
- Checked before each iteration.  
- If `true`, the statement runs; if `false`, the loop stops.  

### **Update**
`i++;`  
- Runs at the end of each iteration.  
- Updates a variable for the next execution.  
- The `++` operator (increment operator) adds `1` to `i`, equivalent to `i = i + 1`.  

### **Statement**
`{ sum = sum + i; }`  
- Executes as long as the condition is `true`.  
- Performs the main operation of the loop.  
- Example: Adding `i` to the total sum in each iteration.  
- `sum += i;` : Shortcut for `sum = sum + i`.  
- Adds the right-hand side value to the left-hand side variable.
- Use the + operator to add two or more strings together!

### Modulus Operator

The `%` (modulus) operator returns the **remainder** of a division.

For example, `8 % 3` gives `2` because `8` divided by `3` leaves a remainder of `2`.

## Examples:

```javascript
console.log(1 % 2); // 1
console.log(7 % 4); // 3
let count = 0;
for(let i = 1; i <= 11; i++) {
    const remainder = i % 2;
    const isEven = remainder === 0;
    if(isEven) {
        count++;
    }
}
console.log(count); // 5
```
# While Loop

A `while` loop runs as long as its condition remains `true`:

```javascript
while (b > 5) {
    // do something
}
//break statement exits the loop even if the condition is still true:
while (true) {
    if (b > 2) {
        // exit the loop
        break;
    }
}
```
## String Manipulation

Messages are stored in **strings**, and sometimes we need to manipulate them.
### Looking up Characters
- To access characters in a **string** using:

1. The `.charAt()` method.
2. Square brackets (`[]`).

### Examples:

```javascript
console.log("Hello".charAt(1)); // e
console.log("Hello"[1]);        // e
```
### Comparing Strings

In JavaScript, strings can be compared using:

1. **Strict equality (`===`)** – Checks for exact match, including case and whitespace.
2. **Comparison operators (`<`, `>`)** – Determines lexicographical order.

### Equality Comparison:

```javascript
console.log('a' === 'a');  // true
console.log('a' === 'A');  // false (case-sensitive)
console.log('a' === 'a '); // false (extra space)
```
### Character Casing

To **ignore character casing** in strings, JavaScript provides two methods:

- **`toLowerCase()`** – Converts all characters to lowercase.
- **`toUpperCase()`** – Converts all characters to uppercase.

```javascript
console.log("Hello".toLowerCase()); // "hello"
console.log("Hello".toUpperCase()); // "HELLO"
```
### String Length

The **`length`** property allows us to determine the number of characters in a string.

### Examples:

```javascript
console.log("a".length); // 1
console.log("Hello".length); // 5
```
### IndexOf

The **`indexOf`** method finds the first occurrence of a character or substring in a string.

### Examples:

```javascript
console.log("Hello".indexOf("e")); // 1
console.log("abca".indexOf("a")); // 0
console.log("abc".indexOf("q")); // -1
console.log("happy dog bark".indexOf("dog")); // 6
```
### Slicing Strings

The **`slice`** method extracts a portion of a string and returns it as a new string.

### Syntax:
```javascript
string.slice(startIndex, endIndex);
console.log("The 40 Thieves".slice(4, 8)); // "40 T"
//endIndex (optional): The position where slicing stops (not included in the result).
```
### Negative Arguments in `slice`

We can use **negative values** in the `slice` method to extract characters starting **from the end** of the string.

### Syntax:
```javascript
string.slice(-startIndex, -endIndex);
console.log("the apple".slice(-5, -2)); // "app"
//startIndex: Starts slicing from the end of the string.
//endIndex (optional): Stops slicing from the end (not included in the result).
```
## Arrays in JavaScript

Arrays are used to store **multiple elements** in a single variable. Instead of storing individual values separately, arrays allow efficient storage and manipulation of multiple items.

## Declaring an Array
An array is created using square brackets `[]` and values are separated by commas.
- Easily store many elements.
- Allow element retrieval using an index. arr[0]
- Quickly provide the total length of the element arr.length
- Just like strings, **arrays use zero-based indexing**. This means:
- The **first element** is at **index `0`**.
- The **second element** is at **index `1`** ..
```javascript
const scores = [70, 80, 65, 100, 90, 95];
let total = 0; 
for(let i = 0; i < array.length; i++) {
    total += array[i];
}
```
### Contains Element

To check if an element exists in an array, use `indexOf`:

```javascript
const element = 3;
const array = [1, 2, 3];
const isContained = array.indexOf(element) >= 0;  //If indexOf returns -1, the element is not in the array.
console.log(isContained); // true
 // push method adds elements to the new array
```
### Returning a New Array

To filter an array, create a new array and push elements that satisfy a condition:

```javascript
function greaterThanFive(array) {
    const newArray = [];
    for (let i = 0; i < array.length; i++) {
        if (array[i] > 5) {
            newArray.push(array[i]);
        }
    }
    return newArray;
}
```
### Reference in JavaScript

### Primitive Values (Stored by Value)
When storing a **primitive value** (like numbers, strings, or booleans), assigning it to another variable **copies the value**.

### Example:
```javascript
let a = 3;
let b = a;

a = 10;

console.log(a); // 10
console.log(b); // 3
```
### Objects and Arrays (Stored by Reference)

When storing an **object or array**, assigning it to another variable **copies the reference, not the value**.

## Example:
```javascript
let a = [1,2,3];
let b = a;

a[0] = 5;

console.log(a); // [5,2,3]
console.log(b); // [5,2,3]

const arr = [1, 2, 3];
arr[0] = 10;  // ✅ Allowed

arr = [4, 5, 6]; // ❌ Error: Assignment to constant variable no new reference
```
### Modifying Array Values

- to **read** array values use square brackets such as `array[0]`.
- to **write new values** to those positions using the **assignment operator `=`**.

## Example:
```javascript
const array = [1,2,3];
array[0] = 5;
console.log(array); // [5,2,3]
```
### 🔹 `splice` Method:
- Allows us to **remove** elements from an array **in place**.
- Takes **two arguments**:
  1. **Starting index** (where removal begins).
  2. **Number of elements** to remove.
```javascript
// Remove Elements Greater Than 5
function greaterThanFive(array) {
    for (let i = array.length - 1; i >= 0; i--) {
        if (array[i] > 5) {
            array.splice(i, 1);
        }
    }
}
```
## Objects in JavaScript

Objects are a **fundamental data structure** in JavaScript, allowing us to **store key-value pairs**.

## 🔹 Object Syntax:
An object is defined using **curly braces `{}`** and contains **key-value pairs**.

### Example: Creating an Object
```javascript
const person = {
    hairColor: 'brown',
    toes: 10,
    grumpy: true
};
//Retrieve Values
console.log( person.toes ); // 10
console.log( person['toes'] ); // 10
// use the . property accessor operator or  use brackets [] just like with arrays!
```
### Enumerated Type?
An enumerated type (or enum) is a way to give meaningful names to numbers.
Instead of using raw numbers, we use descriptive labels.

```javascript
const card = {
    suit: 1, //  we store a card's suit as a number, it is hard to understand:
    value: 5
};

const CARD_SUITS = {
    DIAMONDS: 0,
    HEARTS: 1,
    SPADES: 2,
    CLUBS: 3
};

const card = {
    suit: CARD_SUITS.HEARTS,
    value: 5
};
//✔️ CARD_SUITS.HEARTS is still 1, but now it's understandable.
```
###  Array of Objects in JavaScript
We can store **objects inside arrays** to manage structured data efficiently.

```javascript
//expo.js
const team1 = {
    name: "Mets",
    wins: 86,
    inPlayoffs: false,
};
const teams = [team1, team2, team3];
for(let i = 0; i < teams.length; i++) {
    console.log(teams[i].name); 
}
module.exports = team1; // Exporting team1
// impo.js
const team1 = require('./expo'); // Importing team1

//object without a name property, this will log undefined.
```
### Find the Number of Keys
 1. Using `in` Operator - use the `in` operator to iterate over all properties:
```javascript
const object = { a: 1, b: 2, c: 3 };

for (let key in object) {
    console.log(key);
}
```
 2. Using Object.keys() -Returns an array of keys. and Object.values() -  Returns an array of values.
```javascript
const obj = { a: 1, b: 2, c: 3 };
console.log(Object.keys(obj));   // ['a', 'b', 'c']
console.log(Object.values(obj)); // [1, 2, 3]
```
### Editing  Object Properties

```javascript
const person = {
    name: "James",
    age: 22
};

person.name = "Sally";
person["age"] = 30;
```
### Deleting  Object Properties
```javascript
delete person.name;
console.log(person.name); // undefined
```
### Logical Operators
 help us concisely express complex conditions.
OR - || Logical OR  evaluate to true if either (or both) of the inputs are true.
AND - && operator for requiring both conditions to be true.
NOT - ! operator for negating a condition.
### **JavaScript Default Operator (`||`)**

The **Logical OR (`||`)** operator is often called the **default operator** because it allows setting default values when a variable is **falsy**.
```javascript
console.log("" || "Something Else"); 
// Output: "Something Else"
const message = WELCOME_MESSAGE || "Hello there!";
```
### `&&` (Logical AND) Operator
Returns the first falsy value it finds.
If all values are truthy, it returns the last truthy value
The `&&` operator, also known as the **Logical AND operator** or the **guard operator**, is used to **return the first falsy value** or the **last truthy value**.

- If **both operands are truthy**, it **returns the second operand**.
- If **the first operand is falsy**, it **returns the first operand** without evaluating the second one.

```javascript
console.log(true && "Hello");   // "Hello" (both are truthy, returns second operand)
console.log([] && "Array");     // "Array"

console.log(false && "Hello");  // false (first operand is falsy, returns it)
console.log(undefined && "Object"); // undefined
```
### Logical OR (`||`) Operator
Returns the first truthy value it finds.
If all values are falsy, it returns the last falsy value.
- If the **first operand is truthy**, it **returns the first operand** and does **not** evaluate the second one (**short-circuiting**).
- If the **first operand is falsy**, it evaluates the second operand and **returns it**.
- 
```javascript
console.log(true || "Hello");   // true  (first operand is truthy)
console.log({} || "Object");    // {}    (truthy, returns first operand)

console.log(false || "Hello");  // "Hello" (false is falsy, returns second)
console.log(undefined || "Object"); // "Object" (undefined is falsy, returns second)
```
###  Logical NOT (`!`) Operator

The `!` (Logical NOT) operator is used to **negate** a boolean value, flipping `true` to `false` and vice versa.
- `!true` → `false`
- `!false` → `true`
- **Truthy values** become `false`, and **falsy values** become `true`.
- 
```javascript
console.log(!true);  // false
console.log(!undefined); // true
console.log(!null);      // true
console.log(!NaN);       // true
```
## 🚀 Exceptions in Programming  

### Exceptions
An **exception** is an unexpected error in a function. If not handled, it is **thrown**, stopping execution and passing control back to the caller.
The caller can **catch** it or let it **bubble up** the call stack. If uncaught, the program **crashes**.  

### Handling Exceptions  
Consider sending emails to users:  

- `emailUsers` calls `sendEmail` for each user.  
- If `sendEmail` fails, it **throws an error**.  
- `emailUsers` **catches** and logs the error, continuing with other users.  
Catching exceptions ensures the program **keeps running** despite errors.
 
### Fatal Exceptions  
Fatal errors are critical issues in a program that cannot be fixed during runtime, resulting in the program needing to stop. 
- Fatal errors indicate a **critical failure**.  
- Exceptions thrown from **lower functions** can be **handled at higher levels**.  
- If uncaught, the program **terminates**.  
# 🚀 Throwing Errors in JavaScript  

###  Run-Time Error
A **run-time error** occurs when JavaScript itself throws an error, stopping execution due to an unexpected issue.  

### 🔹 Creating an Error  
Errors in JavaScript can be created using the **`Error`** object:  
```javascript
- `const error1 = new Error("Something bad happened!");`  //Errors are usually created with **`new`** since it generates a **new instance** of the `Error` object
- `const error2 = Error("Something bad happened!");`
```

### 🔹 Throwing an Error  
Throwing an error **immediately stops execution** at that point.  
We should **throw errors** in places where execution must stop due to an issue. Execution will **resume** only if the error is **caught** elsewhere.  
```javascript
const a = 3;

if (a === 3) {
    throw new Error("We don't want a to be 3");
}
```
###  Catching Errors 

### 🔹 What is Catching an Error?  
Catching an error means **handling an exception** so that the program does not crash unexpectedly.  
When an error is thrown, we can **catch it** and decide how to respond—either logging it, fixing it, or notifying the user.  

### How to Catch Errors?  
We use a `try...catch` block to handle errors **gracefully**.  

### Syntax:  

```js
try {
    readFile("book"); 
}
catch(ex) {
    console.log(ex); // EISDIR: illegal operation , will only execute if an error (ex) is thrown by readFile.
}
```
### 🔄 Catch & Return in JavaScript  

### 🔹 What Happens When an Error is Thrown?  
When an error is thrown:  
1️⃣ Execution **stops immediately**.  
2️⃣ The program **jumps** to the nearest `catch` block.  
3️⃣ If not caught, the program **crashes**.  

###🔹 Handling Errors with Return Values  

Instead of letting errors crash the program, we can **catch them and return a value** to indicate success or failure.  

```js
function writeLogFile(id, contents) {
    try {
        writeFile(`logs/${id}`, contents); // Attempt to write a file
    } 
    catch (ex) {
        return false; // Return false if an error occurs
    }
    return true; // Return true if successful
}
```
## Error Types

Let's explore several different types of JavaScript run-time errors.

### **Type Error**
Occurs when a variable is not the expected type for an operation.

```js
const x = 3;
x(); // Throws TypeError: x is not a function.

let b;
b.prop; // Throws TypeError: Cannot read property 'prop' of undefined
```

---

### **Reference Error**
Occurs when trying to access an undefined variable.

```js
z(); // Throws ReferenceError: z is not defined.
```

---

### **Syntax Error**
Occurs when the code has invalid JavaScript syntax.

```js
const a = 3;
a.72; // Throws SyntaxError: Unexpected number.
```
If using a transpiler like Babel, this may fail at the compilation step.

---

### **Range Error**
Occurs when a value is outside the allowed range.

```js
new Array(Infinity); // Throws RangeError: Invalid array length.
```

---

## Type Conversion

Type conversion changes a value’s type, either explicitly or implicitly.

### **Explicit Conversion**
Done intentionally using methods like `.toString()` or `Number()`.

```js
const a = (1).toString();
console.log(a); // "1"
console.log(typeof a); // string
```

### **Implicit Conversion**
Happens automatically due to JavaScript's loose typing.

```js
const b = "3" + "4";
console.log(b); // "34"
console.log(typeof b); // string
```
JavaScript converts numbers to strings when using the `+` operator with strings.

## **Strings to Numbers**

### **Explicit Conversion**
Using the `Number()` function:

```js
const string = "2";
console.log(Number(string)); // 2

const invalidString = "hello";
console.log(Number(invalidString)); // NaN
```

### **Using parseInt and parseFloat**
These methods convert numbers from strings but remove trailing non-numeric characters.

```js
console.log(parseInt("12px")); // 12
console.log(parseFloat("12.34px")); // 12.34
```

### **Implicit Conversion**
Using the `+` operator:

```js
const string = "2";
console.log(+string); // 2

const invalidString = "hello";
console.log(+invalidString); // NaN  stands for "Not A Number", typeof NaN will evaluate to "number"
```
The `+` operator implicitly converts a string to a number, returning `NaN` if conversion fails.


## **typeof Operator**
The `typeof` operator checks a value’s type.

```js
console.log(typeof 1); // "number"
console.log(typeof "1"); // "string"
console.log(typeof {}); // "object"
```
## **To String Conversion**

### **Explicit Conversion**
Using `.toString()` or `String()`:

```js
const a = 123;
console.log(a.toString()); // "123"
console.log(String(a)); // "123"

console.log(false.toString()); // "false"
```

### **Implicit Conversion**
Using `+ ""`:

```js
console.log(123 + ""); // "123"
console.log(true + ""); // "true"
```
 auto converts values to strings when concatenating with an empty string.

### **String Concatenation with Numbers**
When a number is combined with a string, both are converted to strings:

```js
console.log(2 + "2"); // "22"
```
## **Logical NOT (`!`) & Double NOT (`!!`)**

### **Single NOT (`!`)**
Flips a boolean value:
```js
console.log(!3); // false
console.log(!""); // true
```

### **Double NOT (`!!`) for Boolean Conversion**
Converts any value to a boolean:
```js
console.log(!!3); // true
console.log(!!""); // false
```

## **Boolean Conversion**

### **Explicit Conversion**
Using `Boolean()`:
```js
console.log(Boolean(2)); // true
console.log(Boolean("")); // false
```

### **Truthy & Falsy Values**
- **Falsy**: `false`, `0`, `""`, `null`, `undefined`, `NaN`
- **Truthy**: Everything else

### **Implicit Boolean Conversion**
Used in conditionals:
```js
if (3) console.log('3 is truthy!');
```
## **Loose Equals (`==`) vs. Strict Equals (`===`)**

### **Strict Equals (`===`)**
Compares values **without** type conversion:
```js
console.log(3 === 3); // true
console.log("apple" === "orange"); // false
console.log("2" === 2); // false
```

### **Loose Equals (`==`)**
Attempts **type conversion** before comparison:
```js
console.log("2" == 2); // true
```
## **JSON (JavaScript Object Notation)**

### **1. What is JSON?**
JSON is a **lightweight data format** used to store and exchange data between systems. It is based on **JavaScript object syntax** but exists as a **string**.

### **2. JSON Syntax**
- Data is stored as **key-value pairs**.
- Keys must be **strings** and enclosed in **double quotes**.
- Values can be **strings, numbers, objects, arrays, booleans, or null**.

#### **Example JSON Data:**
```json
{
  "name": "Jim",
  "age": 25,
  "isStudent": false
}
```

### **3. Why Use JSON?**
✅ **Standard Format** – Used universally for data exchange.
✅ **Lightweight** – Minimal syntax for easy parsing.
✅ **Readable** – Simple structure makes it human-readable.
✅ **Compatible** – Works across different programming languages.

### **4. Converting Data to JSON**
To convert a JavaScript object to JSON format, use `JSON.stringify()`:
```js
const person = { name: "Jim", age: 25 };
const jsonString = JSON.stringify(person);
console.log(jsonString); // '{"name":"Jim","age":25}'
```

### **5. Converting JSON to JavaScript Object**
To parse a JSON string back into a JavaScript object, use `JSON.parse()`:
```js
const jsonData = '{"name":"Jim","age":25}';
const obj = JSON.parse(jsonData);
console.log(obj.name); // Jim
```
ECMAScript is the specification that JavaScript follows.
Recent editions add new features, like in ES2015 (e.g., arrow functions, classes).
Older browsers may not support these features, so transpilers like Babel help convert the code to be compatible.
### **Destructuring, Rest, and Spread in JavaScript**  

#### **1. Destructuring**  
Destructuring allows **unpacking** values from objects or arrays into variables.  

#### 🔹 **Object Destructuring**  
```js
const obj = { a: 2, b: 3 };
const { a, b } = obj;
console.log(a); // 2
console.log(b); // 3
```
- Values are assigned to variables with the **same property names**.  

#### 🔹 **Array Destructuring**  
```js
const arr = ["hello", "world"];
const [a, b] = arr;
console.log(a); // "hello"
console.log(b); // "world"
```
- Values are assigned based on their **position** in the array.  

#### 🔹 **Destructuring in Function Arguments**  
```js
function addThree([a, b, c]) {
    return a + b + c;
}
console.log(addThree([1, 2, 3])); // 6
```
- Function parameters can be **destructured directly**.  

---

### **2. Rest Parameters**  
Rest parameters collect remaining **function arguments** into an array.  

#### 🔹 **Basic Usage**  
```js
function log(...args) {
    console.log(args);
}
log(1, 2, 3, 4, 5); // [1, 2, 3, 4, 5]
```
- `...args` gathers **all arguments** into an array.  

#### 🔹 **Partial Rest Parameters**  
```js
function log(a, b, ...others) {
    console.log(others);
}
log(1, 2, 3, 4, 5); // [3, 4, 5]
```
- First two arguments are assigned, **rest go into an array**.  

#### 🔹 **Rest in Destructuring**  
```js
const [a, b, ...others] = [1, 2, 3, 4, 5];
console.log(others); // [3, 4, 5]
```
- Useful for **extracting remaining elements**.  

---

### **3. Spread Operator**  
Spread expands **arrays or objects** into individual elements.  

#### 🔹 **Using Spread in Functions**  
```js
const numbers = [1, 2, 3];
function add(a, b, c) {
  return a + b + c;
}
console.log(add(...numbers)); // 6
```
- Spreads the array into **separate arguments**.  

