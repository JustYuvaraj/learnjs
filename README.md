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
# Automatic Semicolon Insertion
JavaScript statements should end with `;`.

# Booleans

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

- **String Interpolation with Backticks**: You can also use **backticks** to define strings, which allows string interpolation. This is useful for inserting variables inside the string.
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



