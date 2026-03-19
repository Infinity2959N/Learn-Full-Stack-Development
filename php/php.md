# PHP (HyperText Preprocessor)

Widely used open source server code scripting language that is especially suited for web development and can be embedded into HTML..
PHP scripts are executed on the server, and the result is returned to the browser as plain HTML. It is a powerful tool for making dynamic and interactive web pages. PHP is also used for command-line scripting and can be used in standalone graphical applications. It supports a wide range of databases, making it a popular choice for web developers.

## Basic Syntax

```php
<?php
echo "Hello, World!";
$x+$y= $z;
?>
```

File extention: .php

Contains text like HTML, CSS, JavaScript, and PHP code. When a PHP file is accessed through a web server, the server processes the PHP code and generates HTML output that is sent to the client's browser.

In this example, the `<?php` tag indicates the start of a PHP script, and `?>` indicates the end. The `echo` statement is used to output the string "Hello, World!" to the browser.

**Current Version: PHP 8.2 (as of June 2024)**
New Features in PHP 8.2:

- Read only classes: Classes that cannot be extended or instantiated.
- Disjunctive Normal Form Types: Allows for more complex type declarations.
- Deprecation of dynamic properties: Dynamic properties are now deprecated, encouraging developers to declare properties explicitly.
- Performance improvements and bug fixes.

## Key Features of PHP 8.0 and later

**JIT (Just-In-Time) Compilation**: Introduced in PHP 8.0, JIT compilation can improve performance by compiling code at runtime, although its benefits may vary depending on the application.

- Faster execution of code, especially for CPU-intensive tasks.
- Can lead to significant performance improvements in certain scenarios, such as complex algorithms or heavy computations.
- May not provide noticeable benefits for typical web applications, as the performance gain depends on the specific use case and the nature of the code being executed.

**Union Types**: Introduced in PHP 8.0, union types allow a parameter or return type to accept multiple types.

```php
<?php
function processInput(int|string $input) {
    if (is_int($input)) {
        return "You entered an integer: $input";
    } else {
        return "You entered a string: $input";
    }
}
echo processInput(42); // Output: You entered an integer: 42
echo processInput("Hello"); // Output: You entered a string: Hello
?>
```

**Named Arguments**: Introduced in PHP 8.0, named arguments allow you to specify the name of the parameter when calling a function, making it easier to understand and maintain code.

```php<?php
function createUser($name, $age, $email) {
    return "User created: Name: $name, Age: $age, Email: $email";
}
echo createUser(name: "Alice", age: 30, email: "alice@mailprovider.com");
?>
```

**Match Expression**: Introduced in PHP 8.0, the match expression is a more concise and powerful alternative to the switch statement.

```php<?php
$day = "Monday";
$result = match ($day) {
    "Monday" => "Start of the week",
    "Friday" => "End of the week",
    "Saturday", "Sunday" => "Weekend",
    default => "Midweek",
};
echo $result; // Output: Start of the week
?>
```

**Null Safe Operator**: Introduced in PHP 8.0, the null safe operator (`?->`) allows you to access properties or methods of an object without having to check if the object is null.

```php
<?php
$user = null;
echo $user?->name; // Output: null (instead of throwing an error)
?>
```

**Attributes**: Introduced in PHP 8.0, attributes (also known as annotations) allow you to add metadata to classes, methods, properties, and parameters.

```php<?php
#[Attribute]
class ExampleAttribute {
    public function __construct(public string $value) {}
}
#[ExampleAttribute("This is an example")]
class MyClass {
}
?>
```

**Error Handling**: PHP has a robust error handling mechanism that allows developers to manage errors gracefully. You can use `try-catch` blocks to handle exceptions and prevent the application from crashing.

```php
<?php
try {
    $result = 10 / 0; // This will cause a division by zero error
} catch (DivisionByZeroError $e) {
    echo "Error: " . $e->getMessage();
}
?>
```

## New Functions of PHP 8.0 and later

- `str_contains()`: Checks if a string contains a specific substring.
- `str_starts_with()`: Checks if a string starts with a specific substring.
- `str_ends_with()`: Checks if a string ends with a specific substring.
- `get_debug_type()`: Returns the type of a variable for debugging purposes.
- `fdiv()`: Performs floating-point division and handles division by zero gracefully.

## Variables

```php
<?php
$name = "John";
$age = 30;
echo "My name is $name and I am $age years old.";
?>
```

In this example, we declare two variables, `$name` and `$age`, and assign them values. We then use the `echo` statement to output a string that includes the values of these variables.

## Decision Making

Decision making is an important part of programming, allowing the program to execute different actions based on the conditions. In php, decision making helps control the flow of program by executing different blocks of code, depeding on certain conditions or expressions. Php provides several constructs for decision making including if-elseif-else, and switch. These **control structures** can be used to make logical decisions.

## Control Structures

```php
<?php
$number = 10;
if ($number > 0) {
    echo "The number is positive.";
} elseif ($number < 0) {
    echo "The number is negative.";
} else {
    echo "The number is zero.";
}
?>
```

if (check and execute), if-else (`is` and `not is` conditon), if-elseif-else (for multiple conditions), switch-case (better way to write if-elseif-else for multiple decisions for a same variable).
In this example, we use an `if` statement to check if the variable `$number` is greater than, less than, or equal to zero, and output a corresponding message.

## Functions

```php
<?php
function greet($name) {
    return "Hello, $name!";
}
echo greet("Alice");
?>
```

In this example, we define a function called `greet` that takes a parameter `$name` and returns a greeting message. We then call the function with the argument "Alice" and output the result.

## Arrays

```php
<?php
$fruits = ["Apple", "Banana", "Cherry"];
echo $fruits[0]; // Output: Apple
?>
```

In this example, we create an array called `$fruits` that contains three elements. We then access the first element of the array using its index (0) and output it.

In php, there are 3 types of arrays: indexed arrays (numerically indexed), associative arrays (key-value pairs), and multidimensional arrays (arrays containing other arrays).

```php
<?php
// Indexed array
$fruits = ["Apple", "Banana", "Cherry"];
// Associative array
$person = ["name" => "John", "age" => 30, "city" => "New York"];
// Multidimensional array
$matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
?>
```

## File Handling

Often need to open and process a file for different tasks. Php has seceral built in functons for creating, reading, uploading, and editing files.

1. readfile(): Reads file and write it to the buffer
2. fopen(): Open the file
3. fread(): Read something from the file.
4. fgets(): Read a specific string (line).
5. fgetc(): Read a specific character.
6. feofc(): End of the file.
7. fclose(): Colse the file.
8. unlink(): Delete the file.

```php
<?php
echo readfile($filename.extension)
echo unlink($filename)
>
```
