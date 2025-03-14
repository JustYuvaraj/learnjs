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



