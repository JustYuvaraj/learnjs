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
  
## `this`**  
`this` is a special keyword that refers to the context in which the current code is being executed. Its value depends on how a function is called.The **`this`** keyword refers to the **object** that is currently calling the function. 

### **1️⃣ In the Global Scope**  
**outside any function**, it refers to the global object:  
- **In browsers →** `window`  
- **In Node.js →** `globalThis`  

```js
console.log(this); // window (in browsers)
```

---

### **2️⃣ Inside an Object Method**  
When a function is inside an object, `this` refers to **that object**.  

```js
const user = {
    name: "Alice",
    greet() {
        console.log(this.name); // "Alice"
    }
};

user.greet(); // 'this' refers to 'user'
```

---

### **3️⃣ Inside a Regular Function**  
- **Without strict mode:** `this` refers to the **global object**.  
- **With strict mode (`"use strict"`)**: `this` is **undefined**.  

```js
function show() {
    console.log(this);
}

show(); // In browsers: window, In strict mode: undefined
```

---

### **4️⃣ In a Constructor Function**  
When using a **constructor function**, `this` refers to the **new object** being created.  

```js
function Person(name) {
    this.name = name;
}

const person1 = new Person("John");
console.log(person1.name); // "John"
```
### `calling function with a specific context:

#### **Syntax of `call`**
```javascript
functionName.call(thisArg, arg1, arg2, ...);
```
- `thisArg` → The value of `this` inside the function.  
- `arg1, arg2, ...` → Arguments passed individually.  

```javascript
function greet(greeting, punctuation) {
    console.log(greeting + ", " + this.name + punctuation);
}

const person = { name: "Alice" };

greet.call(person, "Hello", "!"); // → Pass arguments **individually**.  
```

---

#### **Syntax of `apply`**
```javascript
functionName.apply(thisArg, [arg1, arg2, ...]);
```
- `thisArg` → The value of `this` inside the function.  
- `[arg1, arg2, ...]` → Arguments passed as an array.  

##### **Example:**
```javascript
function greet(greeting, punctuation) {
    console.log(greeting + ", " + this.name + punctuation);
}

const person = { name: "Alice" };

greet.apply(person, ["Hello", "!"]); // Output: Hello, Alice!
```
## Binding

###  `bind()`
The `bind()` method creates a new function with a specific `this` value, without modifying the original function.

### Syntax
```js
function functionName() {
    return this.property;
}
const boundFunction = functionName.bind(object);
```

```js
function getName() {
    return this.name;
}
const newFunction = getName.bind({ name: 'Ted' });
console.log(newFunction()); // Ted
console.log(getName()); // undefined
```

### Binding Cannot Be Overwritten
Once bound, the `this` value remains unchanged:
```js
const newFunction2 = newFunction.bind({ name: 'Walt' });
console.log(newFunction2()); // Ted
```

### Argument Binding
You can also bind arguments:
```js
function greet(greeting) {
    return `${greeting}, ${this.name}`;
}
const sayHello = greet.bind({ name: 'Alice' }, 'Hello');
console.log(sayHello()); // Hello, Alice
```
## Implicit Binding in `this`
The value of `this` depends on **how** a function is called. When calling a function as an **object's property**, `this` refers to that object.
```js
const obj = {
    value: 2,
    getValue: function() {
        return this.value;
    }
};

console.log(obj.getValue()); // 2
```
✅ Here, `this` is implicitly bound to `obj`, so `this.value` is `2`.

## Losing Implicit Binding
If we **store the function reference** separately and call it, `this` is lost:

### Example:
```js
const fn = obj.getValue;
console.log(fn()); // undefined
```
❌ `this` is no longer bound to `obj`. It refers to the **global scope** instead.

### Why?
The function `getValue` is stored in `fn` without its original context, so `this` defaults to the global object (or `undefined` in strict mode).

#### **Call-Site in JavaScript**  

The **call-site** is **where a function is called** in the code, not where it is defined. The value of `this` in a function depends on **how** and **where** the function is called.  

#### **Example 1: Calling a method inside an object**  
```js
const obj = {
    value: 10,
    getValue: function() {
        return this.value;
    }
};

console.log(obj.getValue()); // 10
```
✅ **Call-site**: `obj.getValue()` → `this` refers to `obj`.  

### Assigning a function to a variable**  
```js
const fn = obj.getValue;
console.log(fn()); // undefined
```
❌ **Call-site**: `fn()` → `this` refers to the global object (or `undefined` in strict mode).  

### **Key Rule**  
- The value of `this` depends on **how** a function is called, not where it was defined.


## Unbound Function

In JavaScript, functions inside other functions can lose their context (`this`). This issue is common in **asynchronous programming**, where functions execute later (e.g., network calls, animations, user interactions).

### Issue Example
```js
const YEAR = 1000 * 60 * 60 * 24 * 365;

function addYear() {
    setTimeout(function() {
        this.age++;
    }, YEAR);
}

const person = { name: 'Fred', age: 29 };

addYear.call(person);
```
**Problem:** When `setTimeout` executes, `this` refers to the global context, not `person`.

---

## Fixes for Context Issues
### 1. **Using a Closure**
Store `this` in a variable:
```js
function addYear() {
    const that = this;
    setTimeout(function() {
        that.age++;
    }, YEAR);
}
```
This ensures `that` keeps the original `this` value.

---
### 2. **Using `.bind()`**
Bind `this` to the function:
```js
function addYear() {
    setTimeout(function() {
        this.age++;
    }.bind(this), YEAR);
}
```
`.bind(this)` creates a new function with `this` permanently set.

### 3. **Using Arrow Functions** *(Recommended)*
Arrow functions **inherit `this`** from the surrounding function:
```js
function addYear() {
    setTimeout(() => {
        this.age++;
    }, YEAR);
}
```
# Prototypes in JavaScript

## **Class Concept in Programming**
- **Class:** A template for creating objects (instances).
- **Instance:** An object with its own properties (**state**).
- **Class Functions:** Copied into each new instance.

## **JavaScript and Prototypes**
- JavaScript **does not** have traditional classes.
- Uses **prototypes** instead of copying functionality.
- Objects are **linked** rather than **duplicated**.

## **Key Differences**
| Feature          | Classes             | Prototypes (JavaScript)    |
|------------------|---------------------|-----------------------     |
| Functionality    | Copied to instances | Shared via prototype chain |
| Object Linking   | Independent objects | Objects linked together    |

## **Prototype Mechanism**
- Each object has an internal **prototype link**.
- Forms a **prototype chain** for property/method lookup.
- Searches the chain until found or reaches `null`.
  
## **Prototype Chain**
- Every object in JavaScript has a **prototype**.
- If a property/method is not found in an object, JavaScript looks up the **prototype chain**.
- The chain ends at `Object.prototype`.

### **Example**
```js
function Animal(name) {
    this.name = name;
}
const animal = new Animal("Bud");
```
- `animal` inherits methods from `Object.prototype`.
- These methods are **shared**, not duplicated.

### **Proof of Shared Methods**
```js
const animal1 = new Animal("Bud");
const animal2 = new Animal("Lassie");
console.log(animal1.hasOwnProperty === animal2.hasOwnProperty); // true
```
- `hasOwnProperty` is found in `Object.prototype`, so both instances share it.

## **Constructor Functions & `new`**
- Functions like `Car` can act as constructors.
- `new` creates a new object and binds `this`.
```js
function Car(make, model) {
    this.make = make;
    this.model = model;
}
const car1 = new Car('Toyota', 'Camry');
const car2 = new Car('Honda', 'Civic');
console.log(car1.make); // Toyota
console.log(car2.model); // Civic
```
## ** Prototype and Methods**

## **1️⃣ Understanding Prototypes**
- Prototypes allow objects to inherit methods from a shared prototype object.
- Adding a method to `Shape.prototype` ensures all instances can access it without duplication.

## **2️⃣ Creating the `Shape` Constructor**
```javascript
function Shape(x, y) {
    this.position = { x, y };
}
```
- Initializes an object with `position.x` and `position.y`.

## **3️⃣ Adding Methods to the Prototype**
```javascript
Shape.prototype.move = function(x, y) {
    this.position.x += x;
    this.position.y += y;
};
```
- `move` updates `position` and is shared across all instances.

## **4️⃣ Example Usage**
```javascript
const shape = new Shape(0, 0);
console.log(shape.position); // { x: 0, y: 0 }

shape.move(5, 10);
console.log(shape.position); // { x: 5, y: 10 }
```

## **5️⃣ Prototype Chain Lookup**
- JavaScript first **searches for `move`** on the instance (`shape`).
- If not found, it checks `Shape.prototype`.
- If still not found, it looks at `Object.prototype`.
- Since `move` exists in `Shape.prototype`, it is executed from there.

## **6️⃣ Avoid Arrow Functions for Prototypes**
🚨 **Do NOT use arrow functions for prototype methods:**
```javascript
Shape.prototype.move = (x, y) => {
    this.position.x += x;
    this.position.y += y;
};
```
❌ **Wrong!** Arrow functions do not bind `this` to the instance.
✅ **Use regular functions** to maintain correct `this` binding.

# **`Object.create` in JavaScript**

## **1️⃣ What is `Object.create`?**
- Creates a new object with a specified prototype.
- Links objects via the prototype chain.

## **2️⃣ Example: Linking Objects**
```javascript
const car = { make: 'Toyota', model: 'Camry' };
const camry = Object.create(car);

console.log(camry.make); // Toyota
console.log(camry.model); // Camry
```
✅ `camry` inherits properties from `car`.

## **3️⃣ Prototype Chain Behavior**
```javascript
car.make = "Not Toyota";
console.log(camry.make); // Not Toyota
```
✅ `camry` reflects changes in `car` because it’s linked, not copied.

## **4️⃣ Using `Object.create` for Inheritance**
```javascript
function Shape(x, y) { this.position = { x, y }; }
function Circle(x, y, radius) {
    Shape.call(this, x, y);
    this.radius = radius;
}
Circle.prototype = Object.create(Shape.prototype);
```
✅ `Circle` now inherits from `Shape`.

##  Classes

### What are Classes?
- A structured way to create objects in JavaScript.
- Introduced in ES2015, using prototypes behind the scenes.

### Class Syntax
- Defined using the `class` keyword followed by a name and `{}`.
- Contains methods, including a special `constructor` method.

```javascript
class Hello {
    constructor() {
        console.log('hello!');
    }
}

const h1 = new Hello(); // hello!
const h2 = new Hello(); // hello!
```
- `constructor()` runs once per instance creation.
- `h1` and `h2` are instances of `Hello`.

### Initializing Properties in a Constructor
- The `constructor` initializes properties on an instance using `this`.

```javascript
class Team {
    constructor() {
        this.sport = "soccer";
    } 
}

const t1 = new Team();
console.log(t1.sport); // soccer
```
- `sport` is an instance property initialized to "soccer".

###  Instances
- Instances are objects created from a class.
- They borrow properties and methods from the class template.

### Creating Instances
- Use the `new` keyword to create an instance of a class.

```javascript
class Team {
    constructor(name) {
        this.name = name;
    }
}

const team1 = new Team("Giants");
const team2 = new Team("Jets");
```
- `team1` and `team2` are both instances of `Team`.
- Each instance has its own `name` property.

### How `this` Works in Instances
- The `this` keyword refers to the specific instance being created.
- For `team1`, `this` refers to `team1`, and for `team2`, it refers to `team2`.

```javascript
console.log(team1.name); // "Giants"
console.log(team2.name); // "Jets"
```
- `team1.name` stores "Giants".
- `team2.name` stores "Jets".
  ```
## Class Methods

### What are Methods?
- Functions inside a class that define behavior for instances.

### Defining a Method
```javascript
class Team {
    constructor() {
        this.wins = 0;
        this.losses = 0;
    }
    changeRecord(isWin) {
        isWin ? this.wins++ : this.losses++;
    }
}
```
##  Subclasses

### What are Subclasses?
- Subclasses **inherit** properties and methods from a parent class.
- Use the `extends` keyword to create a subclass.

### Creating a Subclass
```javascript
class Shape {
    constructor() {
        this.position = { x: 0, y: 0 };
    }
}

class Rectangle extends Shape {}
```
- `Rectangle` extends `Shape`, inheriting its properties.
- 
### Accessing Inherited Properties
```javascript
const rect = new Rectangle();
console.log(rect.position.x); // 0
console.log(rect.position.y); // 0
```

## `super` keyword**

### **Extending a Class**
When a subclass extends a parent class, it can use `super` to invoke the parent's constructor.

```javascript
class Shape {
    constructor() {
        this.position = { x: 0, y: 0 };
    }
}

class Rectangle extends Shape {
    constructor() {
        super(); // calls the constructor of Shape. Note super() must be called in a subclass before using this  else ReferenceError.
        this.height = 10; // only After calling `super()`, a subclass can define its own properties.
        this.width = 5;
    }
}
```
- `Rectangle` now inherits `position` from `Shape`.

### **Accessing Properties from Parent Class**
```javascript
const rectangle = new Rectangle();
console.log(rectangle.position.x); // 0
console.log(rectangle.height); // 10
console.log(rectangle.width); // 5
```
## Calling Super Methods

### Parent and Child Class Relationship
- The **parent class** is the class being extended.
- The **child class** is the class extending another class.
- `super` allows the child class to call methods from the parent class.

### Example: Calling a Parent Method
```javascript
class Potion {
    constructor() {
        this.empty = false;
    }
    
    drink() {
        this.empty = true;
    }
}

class NoisyPotion extends Potion {
    drink() {
        super.drink();
        console.log("LOUD NOISES!");
    }
}

const potion = new NoisyPotion();
potion.drink();  //  LOUD NOISES!
```
## Binary

Binary is a **number system** using only **0** and **1** as symbols. It is the foundation of computer systems. Humans commonly use **decimal**, which has **10 symbols (0-9)**.

### Representing Values
- **Decimal (Base 10):** Each digit can be **0-9**.
- **Binary (Base 2):** Each digit can be **0 or 1**.

### Multiple Characters Representation
#### Decimal
- **1 digit:** 10 values (0-9)
- **2 digits:** 100 values (00-99)
- **3 digits:** 1000 values (000-999)
- Formula: **10^n** (where n = number of characters)

#### Binary
- **1 bit:** 2 values (0,1)
- **2 bits:** 4 values (00,01,10,11)
- **3 bits:** 8 values (000-111)
- Formula: **2^n**

### Counting in Binary
Same rules as decimal counting:
- **Decimal:** 0, 1, 2, 3, ..., 8, 9, 10, 11, 12...
- **Binary:** 0, 1, 10, 11, 100, 101, 110, 111, 1000...

Binary is used in computers because **electric signals** are read as **0 (no current) or 1 (current)**.

### Bits, Nibbles, and Bytes
- **Bit:** Single binary digit (0 or 1)
- **Nibble:** 4 bits (e.g., 1011)
- **Byte:** 8 bits (e.g., 10001100)
- **256 values (2^8)** can be represented with **1 byte**.
- Example range: **0-255** or **-128 to 127** (for signed representation).

### Binary Magnitudes
| Decimal   | Binary Equivalent  |
|-----------|-------------------|
| **1,000** (thousand) | **1024** (kilobit/kibibit) |
| **1,000,000** (million) | **1024^2** (megabit/mebibit) |
| **1,000,000,000** (billion) | **1024^3** (gigabit/gibibit) |

#### Bytes
| Decimal (SI) | Binary Equivalent |
|-------------|------------------|
| **1 KB (kilobyte)** = 1000 bytes | **1 KiB (kibibyte)** = 1024 bytes |
| **1 MB (megabyte)** = 1,000,000 bytes | **1 MiB (mebibyte)** = 1,048,576 bytes |
| **1 GB (gigabyte)** = 1,000,000,000 bytes | **1 GiB (gibibyte)** = 1,073,741,824 bytes |

## Hexadecimal

Hexadecimal is commonly used to represent raw data due to its **easy conversion to and from binary**.

### **16 Symbols**
- Hexadecimal uses **16 symbols**: `0-9` and `a-f`.
- The decimal equivalents for `a-f` are **10-15**.
- Hex characters are **case-insensitive** (`A` or `a` can be used interchangeably).

### **0x Prefix**
- Hexadecimal numbers are typically **denoted with the prefix** `0x`.
- Example: `0x4fd979de3edf0f56aa9716b898ec8`.
- The `0x` prefix indicates the **following characters are in hexadecimal**.

## **Converting Hexadecimal to Binary**
- Each **hexadecimal character represents four binary digits** (a **nibble**).

### **Mapping Table**
| HEX | BINARY  |
|-----|--------|
| 0   | 0000   |
| 1   | 0001   |
| 2   | 0010   |
| ... | ...    |
| e   | 1110   |
| f   | 1111   |

#### **Binary to Hexadecimal**
Binary: `11110100110110010111`

Step-by-step grouping into nibbles:
```
1111 0100 1101 1001 0111
F    4    D    9    7
```
Thus, `11110100110110010111` in binary is **`0xF4D97` in hexadecimal**.

#### **Hexadecimal to Binary**
Hexadecimal: `0x1C3AF`

Step-by-step conversion:
```
1    C    3    A    F
0001 1100 0011 1010 1111
```
Thus, `0x1C3AF` is **`00011100001110101111` in binary**.

## Array Sort

### Sorting in JavaScript
JavaScript arrays have a built-in `sort()` method that sorts elements **in place**. It takes an **optional comparison function** to define custom sorting logic.

### Default Sorting Behavior
Without a comparison function, `sort()` converts elements to **strings** and sorts them lexicographically:
```js
const result = [20, 1, 2, 3].sort();
console.log(result); // [1, 2, 20, 3]
```
**Issue:** Since numbers are treated as strings, "20" comes before "3" because "2" is less than "3".

### Custom Sorting with Comparison Function
To correctly sort numbers, pass a comparison function:
```js
[3, 2, 4, 1].sort(function(a, b) {
    return a - b; // Ascending order
});
```
### How the Comparison Function Works
- If **`a - b`** is **negative**, `a` comes **before** `b`.
- If **`a - b`** is **positive**, `b` comes **before** `a`.
- If **`a - b`** is **zero**, order remains unchanged.

### Sorting in Descending Order
```js
[3, 2, 4, 1].sort((a, b) => b - a);
```

### **String Comparison **  

JavaScript provides the **`localeCompare()`** method to compare strings based on **alphabetical order, case sensitivity, and locale settings**.  

---

### **How `localeCompare()` Works**
The method returns:  
✅ `0` → if both strings are equal  
✅ `-1` → if the first string comes **before** the second  
✅ `1` → if the first string comes **after** the second  

```js
console.log('a'.localeCompare('a')); // 0 (both are equal)
console.log('a'.localeCompare('b')); // -1 ('a' comes before 'b')
console.log("apple".localeCompare("abcd")); // 1 ('apple' comes after 'abcd')
```

---

### **Sorting Strings with `localeCompare()`**
Since `localeCompare()` returns numerical values, we can use it for **sorting arrays alphabetically**:

```js
const words = ["banana", "apple", "cherry"];
words.sort((a, b) => a.localeCompare(b));

console.log(words); // ["apple", "banana", "cherry"]
```

---

### **Handling Case Sensitivity & Accents**
By default, `localeCompare()` is **case-sensitive**:

```js
console.log('Z'.localeCompare('a')); // -1 ('Z' comes before 'a')
```

To **ignore case differences**, use `{ sensitivity: 'base' }`:

```js
console.log('Z'.localeCompare('a', undefined, { sensitivity: 'base' })); // 0 (case ignored)
```
## map

The **map** method in JavaScript allows us to apply a function to each element of an array and return a new array with the transformed elements.

### Example:

Let's define a function that adds one to a number:

```js
function addOne(x) {
    return x + 1;
}
```

Applying this function to an array using `map`:

```js
const arr = [3, 4, 5];

const newArr = arr.map(function(x) {
    return x + 1;
});

console.log(newArr); // [4, 5, 6]
```

### Explanation:
- **map** iterates through each element in the array.
- The function inside `map` is applied to each element.
- A new array is returned with the transformed values.

## Mapping a Function

In JavaScript, the `map()` method allows applying a function to each element of an array and returning a new array with the results.

```js
const arr = [3, 4, 5];
const newArr = arr.map(x => x + 1);
console.log(newArr); // [4, 5, 6]
```

### Using Named Functions
Instead of anonymous functions, we can use named functions:

```js
function addOne(x) {
    return x + 1;
}
const result = [1, 2, 3].map(addOne);
console.log(result); // [2, 3, 4]
```

### Using Built-in Functions

```js
const absolutes = [-1, 1, -2, 2].map(Math.abs);
console.log(absolutes); // [1, 1, 2, 2]
```

## Extra Arguments in `map()`
The callback function in `map()` receives **three arguments**:
1. **Element (`el`)** – The current value being processed.
2. **Index (`i`)** – The position of the element in the array.
3. **Array (`arr`)** – The entire array itself.

Example:

```js
[10, 20].map((el, i, arr) => {
    console.log(el, i, arr);
});
```

**Console Output:**
```
10 0 [10, 20]
20 1 [10, 20]
```

## Unexpected Behavior with Extra Arguments
Consider this function:

```js
function sayHello(name, greeting = "Hello") {
    return `${greeting} ${name}!`;
}
```

Using `map()` without an anonymous function:

```js
const result = ['Steve', 'Amanda'].map(sayHello);
console.log(result); // ["0 Steve!", "1 Amanda!"]
`//becoz index is being passed to sayHello as the second argument. to use the default greeting we need to explicitly only send one argument:
sayHello('Steve', 0) → "0 Steve!"
sayHello('Amanda', 1) → "1 Amanda!"
//only pass one argument (name) manually:

const result = ['Steve', 'Amanda'].map(name => sayHello(name));
console.log(result); // ["Hello Steve!", "Hello Amanda!"]
```

### Mapping Over Objects

The `map` method is not limited to arrays of numbers. It also works with objects, allowing you to transform them while keeping the original array unchanged.

#### Example:

```js
const users = [
    { name: 'Corey', loggedIn: true },
    { name: 'Anna', loggedIn: false }
];

const loggedOutUsers = users.map(user => ({
    name: user.name,
    loggedIn: false
}));

console.log(loggedOutUsers);
/*
[
    { name: 'Corey', loggedIn: false },
    { name: 'Anna', loggedIn: false }
]
*/
```
### Array Map Index

When using `map`, the callback function receives the **index** of each element as the second parameter.

#### Example:
```js
[10, 20, 30].map((el, i) => {
    console.log(i);
});
```
### Array Filtering

The `filter` method is used to **select elements** from an array based on a **boolean condition**.

#### Example: Filtering Values
To keep only elements equal to `1`:
```js
const ones = [1, 2, 3, 1, 1].filter(el => el === 1); 
console.log(ones); 
// **checks each element** callback` returns `true` to **keep** an element, `false` to **remove** it.
```
## Filtering Objects

We can filter objects just like we filter numbers, booleans, and strings!

```javascript
const teams = [
    { name: 'Mets', wins: 86 },
    { name: 'Braves', wins: 97 },
    { name: 'Dodgers', wins: 106 }
];
```

If we want to select teams with fewer than 100 wins, we can use `filter`:

```javascript
const lessThan100 = teams.filter(team => team.wins < 100);
```
## Filtering By Index

When supplying a function to `filter`, the first argument is the element, and the second argument is the position of that element (a zero-based index).

### Example:
```javascript
['a', 'b', 'c'].filter(function(el, i) {
    console.log(el, i);
});
```
1. First Iteration: logs `a, 0`
2. Second Iteration: logs `b, 1`
3. Third Iteration: logs `c, 2`

 index starts at `0` and increments by `1` each iteration.

### Practical Example: Keeping Elements at Even Indices
```javascript
const letters = ['a', 'b', 'c', 'd', 'e'];
const evenIndexLetters = letters.filter((el, i) => i % 2 === 0);
console.log(evenIndexLetters); // ['a', 'c', 'e']
```
# Array Reduce

## What is Reduce?
`reduce()` is used to process an array and return a **single value**. It works by accumulating values from the array through an iterative process.

### Example: Sum of Numbers
For `[1,2,4]`, using `reduce()` to sum all elements:

```js
const sum = [1, 2, 4].reduce((acc, curr) => acc + curr);
console.log(sum); // 7
```

### How it Works:
- **First Iteration**:  
  - `acc = 1` (default first value)  
  - `curr = 2`  
  - `acc + curr = 3`  

- **Second Iteration**:  
  - `acc = 3` (previous result)  
  - `curr = 4`  
  - `acc + curr = 7`  

- Final result: **7**

### Default Accumulator
By default, `reduce()` uses the **first element** as the initial accumulator. However, we can **explicitly** provide an initial value:

```js
const sum = [1, 2, 4].reduce((acc, curr) => acc + curr, 0); //  This starts with `acc = 0`, 
```
**Finding the Largest Value with Reduce**

To find the largest value in an array using `reduce`, compare elements and return the greater one.

### Example:
```js
const numbers = [1, 4, 2, 5];
const max = numbers.reduce((a, b) => (a > b ? a : b));
console.log(max); // 5
```
### initial value of the accumulator.
In reduce, the second argument serves as the initial value of the accumulator.
```js
const sum = [-1, -2, -4].reduce(function(acc, curr) {
    return acc + curr;
}, 1);
console.log(sum); // Output: -6
```

### Ternary Operator (`? :`):
- `(a > b ? a : b)` is a shorthand for:
  ```js
  if (a > b) return a; else return b;
  
  ```

### Removing Duplicates with Reduce

We can use `reduce` to remove duplicates from an array in JavaScript.

#### **Code:**
```js
function removeDuplicates(numbers) {
    return numbers.reduce((acc, num) => {
        if (!acc.includes(num)) acc.push(num);
        return acc;
    }, []);
}

console.log(removeDuplicates([2,2,3,5,1,3,4])); // [2,3,5,1,4]
```
## Grouping With Reduce

We can use `reduce` to **group** objects in an array by a specific property.

### **Example Input:**
```js
const foods = [
    { food: 'apple', type: 'fruit' },
    { food: 'orange', type: 'fruit' },
    { food: 'carrot', type: 'vegetable' }
];
```

### **Desired Output:**
```js
{
    fruit: ['apple', 'orange'],
    vegetable: ['carrot']
}
```

### **Implementation:**
```js
function group(foods) {
    return foods.reduce((accumulator, currentValue) => {
        accumulator[currentValue.type] = accumulator[currentValue.type] || [];
        accumulator[currentValue.type].push(currentValue.food);
        return accumulator;
    }, {});
}
```
## Recursion
  recursion is when a function calls itself.
 "if a function calls itself, when does it stop?".

```js
function go() {
    go();
}
```
This function `go` is recursive, but it doesn't know when to stop! It will keep running until we run out of memory or the JavaScript engine ends it.

 **function's arguments change over time until they reach a certain point** `**base case**`.  determines  to exit the recursion. 
```js
function go(n) {
    if(n === 0) {
        // base case, exit recursion
        return; // terminates the current call and all previous calls in the recursion stack
    }
    // change our argument
    go(n - 1);
}

// call the function
go(5);
```
## Call Stack

### What is a Call Stack?
The **call stack** is a data structure in JavaScript that keeps track of function calls.that keeps track of where the program has been so it knows where to return to! It follows the **Last In, First Out (LIFO)** principle, meaning the last function added is the first one removed. 

### How It Works
1. When a function is **called**, it is added to the **top** of the stack.
2. If that function calls another function, the new function is **pushed** onto the stack.
3. When a function **completes**, it is **removed (popped)** from the stack, and execution resumes from where it left off.
4. This process continues until the stack is empty.

### Recursion and the Call Stack
```js
function countdown(n) {
    if (n === 0) return;
    countdown(n - 1);
}
```
Calling `countdown(5)` adds multiple function calls to the stack:
```
countdown(5);
    countdown(4);
        countdown(3);
            countdown(2);
                countdown(1); // Functions finish in reverse order
```
Without a base case, recursion keeps running and causes a **stack overflow**:

**Error:** `Maximum call stack size exceeded!`

### Factorial Function and Call Stack Breakdown
```js
function factorial(n) {
    if (n == 1)
        return 1;
    return n * factorial(n - 1);    
}
```
#### Calling `factorial(5)`
1. `factorial(5)` is added to the stack.
2. `factorial(4)` is called inside `factorial(5)`, so it is pushed onto the stack.
3. `factorial(3)`, `factorial(2)`, and `factorial(1)` follow in the same manner.
4. When `factorial(1)` is reached, it **returns 1** and starts popping functions from the stack.
5. `factorial(2)` computes `2 * 1 = 2` and is removed.
6. `factorial(3)` computes `3 * 2 = 6` and is removed.
7. `factorial(4)` computes `4 * 6 = 24` and is removed.
8. `factorial(5)` computes `5 * 24 = 120` and is removed.
9. Stack is now empty!

#### Call Stack Flow for `factorial(5)`
```
factorial(5)
    factorial(4)
        factorial(3)
            factorial(2)
                factorial(1) // Returns 1
```
Functions return and are popped in reverse order:
```
                factorial(1) returns 1
            factorial(2) returns 2 * 1 = 2
        factorial(3) returns 3 * 2 = 6
    factorial(4) returns 4 * 6 = 24
factorial(5) returns 5 * 24 = 120
```
✅ **Stack is now empty!**

### Stack?
A **stack** is a **LIFO (Last-In-First-Out)** data structure, meaning the most recently added element is removed first.

### **LIFO in Detail**
- **Push** → Adds an element to the **top** of the stack.
- **Pop** → Removes the **top** element from the stack.

---

### **Implementing Push & Pop**
A simple **Stack** class:

```js
class Stack {
    constructor() {
        this.items = []; // Array to store stack elements
    }
    
    push(item) {
        this.items.push(item); // Add item to the top
    }
    
    pop() {
        return this.items.pop(); // Remove and return the top item
    }
}

const stack = new Stack();
stack.push(1);
stack.push(2);
stack.push(3);
stack.push(4);

console.log(stack.pop()); // 4
console.log(stack.pop()); // 3
```
- Elements **pop in reverse order** (Last-In-First-Out).

---

### **Using JavaScript Array Methods**
JavaScript provides **push()** and **pop()** methods that work similarly:

```js
const arr = [1, 2, 3];
arr.push(4);
console.log(arr); // [1,2,3,4]

const top = arr.pop();
console.log(top); // 4
console.log(arr); // [1,2,3]
```
```
const { MAX_STACK_SIZE } = require('./config');

class Stack {
    constructor() {
        this.items = [];
    }
    push(item) {
        if (this.items.length >= MAX_STACK_SIZE )
            throw new Error("stack overflow")
        this.items.push(item)
…    
        return this.items[this.items.length - 1]
    }
}

module.exports = Stack;
```

```
const Stack = require('./Stack');

class OperationManager {
    constructor() {
        this.operations = new Stack()
        this.undos  = new Stack()

    }

    addOperation(operation) {
        this.operations.push(operation)
    }

    undo() {
        this.undos.push(this.operations.pop())
    }

    redo() {
        this.operations.push(this.undos.pop())
    }

    redoAll() {
        if(this.undos.isEmpty() == false){
             this.redo()
             return this.redoAll()   
        } 

    }
}

module.exports = OperationManager;
```
## Linked Lists

### What is a Linked List?
A **linked list** is a data structure where each element (**node**) is connected to the next one through a reference (or pointer). It consists of:
- **Data** (stores value)
- **Next** (reference to the next node)

### How It Works
1. **Starting from the head**, follow the `next` pointer to traverse the list.
2. **Insertion**: Add a new node by updating the `next` reference.
3. **Deletion**: Remove a node by changing the `next` pointer of the previous node.

### Example of Removing a Node
Before deletion:
```
Node1 -> Node2 -> Node3
```
Removing `Node2`:
```
Node1 -> Node3  (Node2 is skipped)
```

### Understanding the Head Node
- The **head** is the first node in the linked list.
- Each node contains a reference to the next node.
- The last node's `next` reference is `null`, marking the end of the list.

### Linked List Constructor
Create a constructor function for `LinkedList`.
- It should initialize a `head` property set to `null` by default.

### Example
```js
const linkedList = new LinkedList();
console.log(linkedList.head); // null
```
## Add First to Linked List

### Problem Statement
We need to implement a method **addFirst** in a **LinkedList** class. This method should add a new node to the **front** of the linked list, making it the new **head**.

### Implementation Breakdown
#### **Case 1: No Existing Head Node**
If the linked list is empty (**head is null**), the new node simply becomes the **head**.

#### **Case 2: Existing Head Node**
If there is already a head node:
1. Set the **next** of the new node to the current **head**.
2. Update the **head** of the linked list to the new node.

### Solution Code
```js
class Node {
    constructor(data) {
        this.data = data;
        this.next = null;
    }
}

class LinkedList {
    constructor() {
        this.head = null;
    }

    addFirst(node) {
        if (this.head === null) {
            // No existing head node, set the new node as the head
            this.head = node;
        } else {
            // Set the new node's next to current head
            node.next = this.head;
            // Update the head to the new node
            this.head = node;
        }
    }
}
```
#  Node.js
Node.js is a JavaScript runtime environment.
It allows you to run JavaScript programs outside of a web browser.
It provides the necessary tools and libraries to execute JavaScript on your local machine.
Node.js uses the V8 JavaScript engine developed by Google.
## Install Node.js
1. Visit [nodejs.org](https://nodejs.org/).
2. Download and run the installer for your OS.
3. Verify installation by running the following in the terminal:
   ```sh
   node -v
   ```

## Run JavaScript with Node.js REPL
- Open a terminal and type:
  ```sh
  node
  ```
- Run JavaScript commands.
- Exit with:
  ```sh
  .exit
  ```

## Install a Text Editor
- Recommended editors:
  - [VS Code](https://code.visualstudio.com/)
  - [Sublime Text](https://www.sublimetext.com/)

## Run a JavaScript Script
1. Create a file `index.js` in your editor.
2. Add the following code:
   ```js
   const myName = "Dan";
   const message = `Hello, ${myName}!`;
   console.log(message);
   ```
3. Save the file and navigate to its location in the terminal.
4. Run the script:
   ```sh
   node index.js
   ```

## Command Line Arguments
1. Modify `index.js` to accept arguments:
   ```js
   const message = `Hello, ${process.argv[2]}!`;
   console.log(message);
   ```
2. Run the script with an argument:
   ```sh
   node index.js Dan
   ```
# Node Package Manager (NPM)

## Overview
NPM (Node Package Manager) helps developers **manage and share packages** easily. It provides:
- A **registry** of ready-to-use packages.
- A **command-line tool** to install and manage dependencies.
- **Versioning** to prevent breaking changes.

## Getting Started
### **Initialize a New Project**
1. Create a new project folder.
2. Run:
   ```sh
   npm init -y
   ```
   This creates a `package.json` file.

## Installing Packages
To install **faker-js**, run:
```sh
npm i @faker-js/faker
```
This adds a `dependencies` section in `package.json`:
```json
{
  "dependencies": {
    "@faker-js/faker": "^8.3.1"
  }
}
```

## Using a Package
Create `index.js` and add:
```js
const { faker } = require("@faker-js/faker");
console.log(`Hello, ${faker.person.fullName()}!`);
```
Run the script:
```sh
node index.js
```

## Understanding Versioning (SemVer)
NPM follows **Semantic Versioning (SemVer)**:
```
MAJOR.MINOR.PATCH (e.g., 2.3.5)
```
- **MAJOR (2.x.x)** → Breaking changes.
- **MINOR (x.3.x)** → New features, backward-compatible.
- **PATCH (x.x.5)** → Bug fixes, backward-compatible.

### **Versioning Rules in package.json**
| Syntax      | Allows Updates For |
|------------|-------------------|
| `*` or `x` | Any version (not recommended). |
| `^1.0.0`   | Minor & patch updates (`1.1.0`, `1.2.5`). |
| `~1.0.0`   | Patch updates only (`1.0.1`, `1.0.9`). |





