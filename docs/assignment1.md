# Assignment 1

> Unit 1 and 2

## What is HTML

HTML, which stands for HyperText Markup Language, is the standard markup language used to create and structure web pages and web applications. It forms the backbone of the World Wide Web, allowing developers to define the content and layout of documents that are displayed in web browsers.

### Key Concepts

- **Markup Language**: HTML uses tags to annotate text, images, and other content, indicating how they should be displayed or interpreted by browsers.
- **HyperText**: Refers to the ability to link documents together, enabling navigation between pages via hyperlinks.
- **Elements and Tags**: HTML documents are composed of elements, each defined by tags (e.g., `<p>` for paragraphs, `<h1>` for headings). Tags are enclosed in angle brackets and often come in pairs: an opening tag and a closing tag.
- **Structure**: A basic HTML document includes elements like `<html>`, `<head>`, and `<body>`, providing a hierarchical structure.

### History and Evolution

- Developed by Tim Berners-Lee in 1991 as part of the World Wide Web project.
- Maintained by the World Wide Web Consortium (W3C) and WHATWG.
- Latest version is HTML5, introduced in 2014, which added new semantic elements, multimedia support, and APIs for modern web development.

### Purpose and Importance

- **Accessibility**: Semantic HTML improves accessibility for users with disabilities and search engines.
- **Interoperability**: Works across different browsers and devices.
- **Integration**: Often used alongside CSS for styling and JavaScript for interactivity to create dynamic web experiences.

In summary, HTML is essential for building the structure of web content, making it readable and navigable for users worldwide.

## Define all semantic tags of HTML

Semantic HTML tags provide meaning to the content they enclose, improving accessibility and SEO. Here are the main semantic tags in HTML5:

- `<article>`: Represents a self-contained composition in a document, such as a blog post or news article.
- `<aside>`: Represents content that is tangentially related to the content around it, often used for sidebars or pull quotes.
- `<details>`: Creates a disclosure widget where information is visible only when toggled open.
- `<figcaption>`: Provides a caption or legend for a `<figure>` element.
- `<figure>`: Represents self-contained content, like images or diagrams, optionally with a caption.
- `<footer>`: Represents the footer of a document or section, containing author info, copyright, etc.
- `<header>`: Represents introductory content or navigational aids at the top of a page or section.
- `<main>`: Represents the main content of the document, unique and central to the page.
- `<mark>`: Highlights text for reference or notation purposes.
- `<nav>`: Defines a section for navigation links.
- `<section>`: Represents a standalone section of a document with related content.
- `<summary>`: Provides a summary or caption for a `<details>` element.
- `<time>`: Represents a specific period in time, such as dates or times.

## Write a simple code to create hyperlink

Here is a simple HTML code snippet to create a hyperlink:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Hyperlink Example</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>Click the link below to visit OpenAI's website:</p>
    <a href="https://www.openai.com" target="_blank">Visit OpenAI</a>
</body>
</html>
```

## Why we need CSS. Define all types of CSS

CSS, or Cascading Style Sheets, is essential for web development because it allows developers to separate content from design. While HTML provides the structure and content of a webpage, CSS is used to control the visual presentation, including layout, colors, fonts, and overall aesthetics. This separation enhances maintainability, improves load times, and allows for greater flexibility in design.

### Types of CSS

1. **Inline CSS**: Applied directly within an HTML element using the `style` attribute. It affects only that specific element.

   ```html
   <p style="color: blue;">This is an inline styled paragraph.</p>
   ```

2. **Internal CSS**: Defined within a `<style>` tag in the `<head>` section of an HTML document. It applies styles to the entire document.

   ```html
    <head>
         <style>
              p {
                color: green;
              }
         </style>
    </head>
3. **External CSS**: Linked to an external stylesheet using the `<link>` tag.

    ```html
    <head>
         <link rel="stylesheet" type="text/css" href="styles.css">
    </head>
    ```

## What do you understand by JavaScript. What are the differences between function, conditions and loops

JavaScript is a high-level, interpreted programming language that is primarily used for creating interactive and dynamic content on websites. It is one of the core technologies of the World Wide Web, alongside HTML and CSS. JavaScript enables developers to add functionality to web pages, such as responding to user interactions, manipulating the Document Object Model (DOM), handling events, and performing asynchronous operations. Originally developed by Brendan Eich in 1995 for Netscape Navigator, JavaScript has evolved significantly and is now standardized as ECMAScript. It can run on the client-side (in browsers) via engines like V8 in Chrome or SpiderMonkey in Firefox, and on the server-side using environments like Node.js. JavaScript is versatile, supporting object-oriented, functional, and imperative programming paradigms, and it includes features like prototypes, closures, and asynchronous programming with promises and async/await.

### Differences between Functions, Conditions, and Loops

Functions, conditions, and loops are fundamental constructs in JavaScript (and programming in general), each serving distinct purposes in controlling the flow and organization of code. Here's a detailed breakdown of their differences:

#### Functions

- **Purpose**: Functions are reusable blocks of code designed to perform a specific task or set of tasks. They encapsulate logic, promote code reusability, and help in organizing code into modular units.
- **How they work**: A function is defined using the `function` keyword (or arrow functions with `=>`), and it can take parameters (inputs) and return a value (output). Functions are called (invoked) to execute their code.
- **Key Characteristics**:
  - Can be declared, expressed, or arrow functions.
  - Support parameters and return values.
  - Enable code abstraction and separation of concerns.
  - Example:

    ```javascript
    function greet(name) {
        return `Hello, ${name}!`;
    }
    console.log(greet('World')); // Outputs: Hello, World!
    ```

- **Differences from Conditions and Loops**: Unlike conditions and loops, which control the flow of execution based on logic or repetition, functions are about defining and calling blocks of code. They don't inherently decide whether to execute code or repeat it; instead, they group operations that can be invoked as needed.

#### Conditions

- **Purpose**: Conditions (often implemented with `if`, `else if`, `else`, or switch statements) allow the program to make decisions and execute different code paths based on whether certain criteria are met.
- **How they work**: They evaluate a boolean expression (true or false) and execute code blocks accordingly. This enables branching logic in the program.
- **Key Characteristics**:
  - Use comparison operators (e.g., `==`, `===`, `>`, `<`) or logical operators (`&&`, `||`, `!`).
  - Can be nested or chained for complex decision-making.
  - Ternary operator (`condition ? trueValue : falseValue`) is a shorthand for simple conditions.
  - Example:

    ```javascript
    let age = 18;
    if (age >= 18) {
        console.log('You are an adult.');
    } else {
        console.log('You are a minor.');
    }
    ```

- **Differences from Functions and Loops**: Conditions are about decision-making and branching, not about reusing code (like functions) or repeating actions (like loops). They execute code conditionally but do not define reusable blocks or iterate over data.

#### Loops

- **Purpose**: Loops are used to repeat a block of code multiple times, typically until a condition is met or for a specified number of iterations. They are essential for iterating over arrays, processing data, or performing repetitive tasks.
- **How they work**: Loops check a condition and execute the code block repeatedly as long as the condition is true. Common types include `for`, `while`, `do-while`, and `for...of`/`for...in` for arrays and objects.
- **Key Characteristics**:
  - `for` loop: Ideal for known number of iterations, with initialization, condition, and increment.
  - `while` loop: Continues as long as the condition is true.
  - `do-while` loop: Executes at least once before checking the condition.
  - Can include `break` to exit early or `continue` to skip iterations.
  - Example:

    ```javascript
    for (let i = 0; i < 5; i++) {
        console.log(`Iteration ${i}`);
    }
    // Outputs: Iteration 0, Iteration 1, ..., Iteration 4
    ```

- **Differences from Functions and Conditions**: Loops focus on repetition, not on defining reusable code (functions) or making decisions (conditions). They execute code multiple times but don't encapsulate logic for reuse or branch based on evaluations.

In summary, functions organize and reuse code, conditions control execution paths based on logic, and loops handle repetition. Together, they form the backbone of structured programming in JavaScript, allowing for complex, efficient, and maintainable code.
