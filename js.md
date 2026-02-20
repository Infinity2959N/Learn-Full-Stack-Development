# JavaScript

JavaScript is a versatile programming language primarily used for web development to create interactive and dynamic web pages. It can be executed on the client side (in the browser) as well as on the server side (using environments like Node.js).

## Data Types

JavaScript supports several data types, including:

- **Number**: Represents both integer and floating-point numbers. Example: `42`, `3.14`
- **String**: Represents a sequence of characters. Example: `"Hello, World!"`
- **Boolean**: Represents logical values `true` or `false`.
- **Object**: Represents complex data structures. Example: `{ name: "Alice", age: 30 }`
- **Array**: Represents a list of values. Example: `[1, 2, 3, 4, 5]`
- **Undefined**: Represents a variable that has been declared but not assigned a value.
- **Null**: Represents the intentional absence of any object value.

## Syntax crash course (Drawing parallel to python)

- **Variables**: Declared using `var`, `let`, or `const`. Example:
  
  ```javascript
  let age = 25;
  const name = "John";
  ```
  
  - Difference in declaration keywords:
    - `var`: Function-scoped or globally-scoped, can be re-declared and updated.
    - `let`: Block-scoped, can be updated but not re-declared within the same scope.
    - `const`: Block-scoped, cannot be updated or re-declared; must be initialized at declaration.
- **Functions**: Defined using the `function` keyword or arrow function syntax. Example:
  
  ```javascript
    function greet() {
        console.log("Hello!");  // console.log is used to print output to the console
    }
    const greet = () => {
        console.log("Hello!");
    }
    ```

- **Control Structures**: Includes `if`, `else`, `for`, `while`, and `switch`. Example:

    ```javascript
    if (age > 18) {
        console.log("Adult");
    } else {
        console.log("Minor");
    }

    for (let i = 0; i < 5; i++) {
        console.log(i);
    }
    ```

- **Comments**: Single-line comments use `//`, and multi-line comments use `/* ... */`. Example:

    ```javascript
    // This is a single-line comment
    
    /*
        This is a multi-line comment
    */
    ```

## Conditions

JavaScript conditional statements are used to make decisions in a program based on given conditions. They control the flow of execution by running different code blocks depending whether a condition is true or false.

1. **if statement:** if statement checks the condition written inside the parentheses. If the condition evaluates to true, the code block inside the curly braces is executed.

    ```javascript
    if (condition) {
        // code to be executed if condition is true
    }
    ```

2. **if...else statement**:

    ```javascript
    if (condition) {
        // code to be executed if condition is true
    } else {
        // code to be executed if condition is false
    }
    ```

3. **else if statement**: You can use multiple else if statements to check for multiple conditions.

    ```javascript
    if (condition1) {
        // code to be executed if condition1 is true
    } else if (condition2) {
        // code to be executed if condition2 is true
    } else {
        // code to be executed if both conditions are false
    }
    ```

4. **switch statement**: The switch statement is used to perform different actions based on different conditions. It is often used as an alternative to multiple if...else if statements.

    ```javascript
    switch (expression) {
        case value1:
            // code to be executed if expression === value1
            break;
        case value2:
            // code to be executed if expression === value2
            break;
        // you can have any number of case statements
        default:
            // code to be executed if expression doesn't match any case
    }
    ```

    Example:

    ```javascript
    let day = 3;
    let dayName;
    switch (day) {
        case 1:
            dayName = "Monday";
            break;
        case 2:
            dayName = "Tuesday";
            break;
        case 3:
            dayName = "Wednesday";
            break;
        case 4:
            dayName = "Thursday";
            break;
        case 5:
            dayName = "Friday";
            break;
        case 6:
            dayName = "Saturday";
            break;
        case 7:
            dayName = "Sunday";
            break;
        default:
            dayName = "Invalid day";
    }
    console.log(dayName); // Output: Wednesday
    ```

- Reasons to use conditions:
  - To execute different code blocks based on varying conditions.
  - To control the flow of the program and make decisions.
  - To handle different scenarios and inputs effectively.
  - To improve code readability and maintainability by clearly defining decision-making logic.

## Loops

JavaScript provides several types of loops to execute a block of code multiple times.

1. **for loop**: The for loop is used to run a block of code a specific number of times. (Number of iterations is known in advance). Includes initialization, condition and increment/decrement in syntax.

    ```javascript
    for (initialization; condition; increment/decrement) {
        // code to be executed
    }
    ```

    Example:

    ```javascript
    for (let i = 0; i < 5; i++) {
        console.log(i); // Output: 0, 1, 2, 3, 4
    }
    ```

2. **while loop**: The while loop continues to execute a block of code as long as the specified condition is true.

    ```javascript
    while (condition) {
        // code to be executed
    }
    ```

    Example:

    ```javascript
    let i = 0;
    while (i < 5) {
        console.log(i); // Output: 0, 1, 2, 3, 4
        i++;
    }
    ```

3. **do...while loop**: The do...while loop is similar to the while loop, but it guarantees that the code block will be executed at least once before checking the condition.

    ```javascript
    do {
        // code to be executed
    } while (condition);
    ```

    Example:

    ```javascript
    let i = 0;
    do {
        console.log(i); // Output: 0, 1, 2, 3, 4
        i++;
    } while (i < 5);
    ```

4. **for...in loop**: The for...in loop is used to iterate over the properties of an object.

    ```javascript
    for (key in object) {
        // code to be executed
    }
    ```

    Example:

    ```javascript
    const person = { name: "Alice", age: 30, city: "New York" };
    for (let key in person) {
        console.log(key + ": " + person[key]);
    }
    // Output:
    // name: Alice
    // age: 30
    // city: New York
    ```

5. **for...of loop**: The for...of loop is used to iterate over iterable objects like arrays, strings, maps, and sets.

    ```javascript
    for (element of iterable) {
        // code to be executed
    }
    ```

    Example:

    ```javascript
    const numbers = [10, 20, 30, 40, 50];
    for (let num of numbers) {
        console.log(num); // Output: 10, 20, 30, 40, 50
    }
    ```

## Functions

Functions in JavaScript are reusable blocks of code designed to perform a specific task. They can be defined using the `function` keyword or as arrow functions. Functions can take parameters and return values. Help organize code and reduce redundancy.

1. **Function Declaration**:

    ```javascript
    function functionName(parameters) {
        // code to be executed
        return value; // optional
    }
    ```

    Example:

    ```javascript
    function add(a, b) {
        return a + b;
    }
    console.log(add(5, 3)); // Output: 8
    ```

2. **Function Expression**:

    ```javascript
    const functionName = function(parameters) {
        // code to be executed
        return value; // optional
    };
    ```

    Example:

    ```javascript
    const multiply = function(a, b) {
        return a * b;
    };
    console.log(multiply(4, 6)); // Output: 24
    ```

3. **Arrow Function**:

    ```javascript
    const functionName = (parameters) => {
        // code to be executed
        return value; // optional
    };
    ```

    Example:

    ```javascript
    const subtract = (a, b) => {
        return a - b;
    };
    console.log(subtract(10, 4)); // Output: 6
    ```

4. **Anonymous Function**: A function without a name, often used as an argument to other functions.

    ```javascript
    setTimeout(function() {
        console.log("This message is displayed after 2 seconds");
    }, 2000);
    ```

5. **Immediately Invoked Function Expression (IIFE)**: A function that is executed immediately after it is defined.

    ```javascript
    (function() {
        console.log("This function runs immediately!");
    })();
    ```

## Pop-up boxes

JavaScript provides three types of pop-up boxes to interact with users: `alert`, `confirm`, and `prompt`.

1. **Alert Box**: Displays a message to the user with an OK button.

    ```javascript
    alert("This is an alert box!");
    ```

2. **Confirm Box**: Asks the user to confirm an action with OK and Cancel buttons. It returns `true` if OK is clicked and `false` if Cancel is clicked.

    ```javascript
    const userConfirmed = confirm("Do you want to proceed?");
    if (userConfirmed) {
        console.log("User chose to proceed.");
    } else {
        console.log("User canceled the action.");
    }
    ```

3. **Prompt Box**: Asks the user to input a value. It returns the input value if OK is clicked and `null` if Cancel is clicked.

    ```javascript
    const userInput = prompt("Please enter your name:");
    if (userInput !== null) {
        console.log("Hello, " + userInput + "!");
    } else {
        console.log("User canceled the prompt.");
    }
    ```

## Events

JavaScript events are actions or occurrences that happen in the system you are programming, which the system tells you about so your code can respond to them. Common events include user interactions like clicks, mouse movements, key presses, and form submissions.

1. **Event Listeners**: You can attach event listeners to HTML elements to respond to specific events.

    ```javascript
    element.addEventListener(event, function, useCapture);
    ```

    Example:

    ```javascript
    const button = document.getElementById("myButton");
    button.addEventListener("click", function() {
        alert("Button was clicked!");
    });
    ```

2. **Common Events**:
    - `click`: Triggered when an element is clicked.
    - `mouseover`: Triggered when the mouse pointer is moved over an element.
    - `mouseout`: Triggered when the mouse pointer is moved out of an element.
    - `keydown`: Triggered when a key is pressed down.
    - `keyup`: Triggered when a key is released.
    - `submit`: Triggered when a form is submitted.
    - `load`: Triggered when the whole page has loaded.
    Example:

    ```javascript
    window.addEventListener("load", function() {
        console.log("Page has fully loaded");
    });
    ```

3. **Event Object**: When an event occurs, an event object is created that contains information about the event, such as the target element, type of event, and more.
    Example:

    ```javascript
    document.addEventListener("click", function(event) {
        console.log("Clicked element:", event.target);
    });
    ```

4. **Removing Event Listeners**: You can remove an event listener using the `removeEventListener` method.

    ```javascript
    element.removeEventListener(event, function, useCapture);
    ```

    Example:

    ```javascript
    const button = document.getElementById("myButton");
    function handleClick() {
        alert("Button was clicked!");
    }
    button.addEventListener("click", handleClick);
    // To remove the event listener
    button.removeEventListener("click", handleClick);
    ```

## Advantages of JavaScript

- Enhances user experience with interactivity.
- Client-side execution reduces server load.
- Versatile: can be used for both front-end and back-end development.
- Large ecosystem with numerous libraries and frameworks.
- Easy to learn and widely supported across browsers.

## Disadvantages of JavaScript

- Browser compatibility issues.
- Security vulnerabilities if not properly managed.
- Can lead to performance issues if not optimized.
- Client-side code can be disabled by users.

## Basic Syntax

```javascript
// This is a single-line comment
/*
    This is a multi-line comment
*/
let variableName = value; // Variable declaration
function functionName(parameters) {
    // Function definition
    return value; // Optional return statement
}
if (condition) {
    // Conditional statement
} else {
    // Alternative block
}
for (let i = 0; i < 5; i++) {
    // Looping structure
}
while (condition) {
    // While loop
}
```

- **Variable Declaration**: `let`, `const`, `var`
- **Function Definition**: `function functionName(parameters) { ... }`
- **Conditional Statements**: `if`, `else`, `switch`
- **Loops**: `for`, `while`, `do...while`, `for...in`, `for...of`
- **Comments**: `//` for single-line, `/* ... */` for multi-line
Example:

```javascript
let message = "Hello, World!";
function greet(name) {
    return message + " My name is " + name + ".";
}
console.log(greet("Alice")); // Output: Hello, World! My name is Alice.
```

Common Methods:

- `console.log()`: Outputs messages to the web console.
- `alert()`: Displays an alert dialog with a message.
- `document.getElementById()`: Selects an HTML element by its ID.
- `addEventListener()`: Attaches an event handler to an element.
Example:

```javascript
console.log("Welcome to JavaScript!");
alert("This is an alert message.");
const element = document.getElementById("myElement");
element.addEventListener("click", function() {
    console.log("Element clicked!");
});
```

Common Libraries/Frameworks:

- **jQuery**: Simplifies HTML DOM manipulation, event handling, and AJAX interactions.
- **React**: A JavaScript library for building user interfaces, particularly single-page applications.
- **Angular**: A TypeScript-based open-source web application framework led by the Angular Team
- **Vue.js**: A progressive framework for building user interfaces, focusing on the view layer.
- **Node.js**: A runtime environment that allows executing JavaScript on the server side.
- **Express.js**: A minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.
- **Lodash**: A utility library that provides functions for common programming tasks using a functional programming paradigm.
Example:

```javascript
// Using jQuery to hide an element on button click
$(document).ready(function() {
    $("#myButton").click(function() {
        $("#myElement").hide();
    });
});
```

```javascript
// Using React to create a simple component
import React from 'react';
function HelloWorld() {
    return <h1>Hello, World!</h1>;
}
export default HelloWorld;
```

```javascript
// Using Express.js to create a simple server
const express = require('express');
const app = express();
app.get('/', (req, res) => {
    res.send('Hello, World!');
});
app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000');
});
```
