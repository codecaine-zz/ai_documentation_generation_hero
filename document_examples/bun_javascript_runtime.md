Control Structures
As of my last update, Bun does not specifically have "edit statements" as part of its API or feature set. Instead, Bun is a modern JavaScript runtime like Node.js, but aims for improved performance and developer experience. You might be referring to techniques or tools in the Bun ecosystem or generic coding practices such as working with the REPL or hot reloading.

Here's how you might typically work with Bun:

1. **Installation**: Start by installing Bun. If you haven't installed it yet, run:
   ```bash
   curl -fsSL https://bun.sh/install | bash
   ```

2. **Basic Usage**: To run a script with Bun, use:
   ```bash
   bun run script.js
   ```

3. **Bun REPL**: Bun provides a Read-Eval-Print Loop (REPL) for interactive
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [1. Basic `for` Loop](#1-basic-for-loop)
- [2. Iterating Over an Array](#2-iterating-over-an-array)
- [3. `for...of` Loop](#3-forof-loop)
- [4. `for...in` Loop](#4-forin-loop)
- [5. Nested `for` Loop](#5-nested-for-loop)
- [6. Using `break` and `continue`](#6-using-break-and-continue)
- [Example 1: Basic While Loop](#example-1-basic-while-loop)
- [Example 2: Using `while` Loop for Array Traversal](#example-2-using-while-loop-for-array-traversal)
- [Example 3: Using `while` Loop to Wait for a Condition](#example-3-using-while-loop-to-wait-for-a-condition)
- [Example 4: Using `do...while` Loop](#example-4-using-dowhile-loop)
- [Note](#note)
- [Example 1: Basic Counter](#example-1-basic-counter)
- [Example 2: User Input Validation](#example-2-user-input-validation)
- [Example 3: Array Iteration](#example-3-array-iteration)
- [Example 4: Sum until Max Value](#example-4-sum-until-max-value)
- [Example 5: Generating Random Numbers](#example-5-generating-random-numbers)
- [`break` Statement](#break-statement)
- [`continue` Statement](#continue-statement)
- [Usage in Other Loops](#usage-in-other-loops)
- [Summary](#summary)
- [Declaring Variables](#declaring-variables)
- [Using Variables](#using-variables)
- [Points to Note](#points-to-note)
- [Integers](#integers)
- [Floats](#floats)
- [Strings](#strings)
- [Conversions](#conversions)
- [Important Notes](#important-notes)
- [Example 1: Basic Enum-like Structure](#example-1-basic-enum-like-structure)
- [Example 2: Enum with Numeric Values](#example-2-enum-with-numeric-values)
- [Example 3: Enum with Symbol Values for Enhanced Safety](#example-3-enum-with-symbol-values-for-enhanced-safety)
- [Explanation](#explanation)
- [Defining Arrays](#defining-arrays)
- [Accessing Array Elements](#accessing-array-elements)
- [Modifying Arrays](#modifying-arrays)
- [Iterating Over Arrays](#iterating-over-arrays)
- [Advanced Array Methods](#advanced-array-methods)
- [Creating and Manipulating Lists](#creating-and-manipulating-lists)
- [Iterating Over Lists](#iterating-over-lists)
- [List Transformations and Queries](#list-transformations-and-queries)
- [Using Objects](#using-objects)
  - [Creating an Object](#creating-an-object)
  - [Accessing Values](#accessing-values)
  - [Adding or Updating Entries](#adding-or-updating-entries)
  - [Deleting Entries](#deleting-entries)
  - [Iterating Over an Object](#iterating-over-an-object)
- [Using the Map Class](#using-the-map-class)
  - [Creating a Map](#creating-a-map)
  - [Adding Entries](#adding-entries)
  - [Accessing Values](#accessing-values-1)
  - [Updating Entries](#updating-entries)
  - [Deleting Entries](#deleting-entries-1)
  - [Checking for a Key](#checking-for-a-key)
  - [Iterating Over a Map](#iterating-over-a-map)
  - [Getting the Size of a Map](#getting-the-size-of-a-map)
- [Choosing Between Objects and Maps](#choosing-between-objects-and-maps)
- [Example 1: Creating and Using a Set](#example-1-creating-and-using-a-set)
- [Example 2: Iterating Over a Set](#example-2-iterating-over-a-set)
- [Example 3: Converting Between Sets and Arrays](#example-3-converting-between-sets-and-arrays)
- [Example 4: Performing Set Operations](#example-4-performing-set-operations)
- [Example 5: Removing Elements and Clearing a Set](#example-5-removing-elements-and-clearing-a-set)
- [Example 1: Defining a Tuple as a Fixed-Size Array](#example-1-defining-a-tuple-as-a-fixed-size-array)
- [Example 2: Using TypeScript for Tuple Annotations](#example-2-using-typescript-for-tuple-annotations)
- [Example 3: Using Tuples for Function Return Values](#example-3-using-tuples-for-function-return-values)
- [Example 4: Immutable Tuples with Object.freeze](#example-4-immutable-tuples-with-objectfreeze)
- [1. Choose a Database Library](#1-choose-a-database-library)
- [2. Install the Database Library](#2-install-the-database-library)
- [3. Write the Connection Code](#3-write-the-connection-code)
  - [Example: Connecting to PostgreSQL with `pg`](#example-connecting-to-postgresql-with-pg)
  - [Example: Connecting to MySQL with `mysql2`](#example-connecting-to-mysql-with-mysql2)
  - [Example: Connecting to MongoDB](#example-connecting-to-mongodb)
- [4. Handle Disconnects and Errors](#4-handle-disconnects-and-errors)
- [5. Closing the Connection](#5-closing-the-connection)
- [Setting Up](#setting-up)
- [Creating and Querying Tables](#creating-and-querying-tables)
- [Explanation](#explanation-1)
- [Next Steps](#next-steps)
- [Example: Using JOINs](#example-using-joins)
- [Example: Using Subqueries](#example-using-subqueries)
- [Notes](#notes)
- [Explanation:](#explanation-2)
- [Example Code](#example-code)
- [Key Steps](#key-steps)
- [Notes](#notes-1)
- [Example 1: Basic Error Handling](#example-1-basic-error-handling)
- [Example 2: Handling Specific Error Types](#example-2-handling-specific-error-types)
- [Example 3: Promises with Try-Catch](#example-3-promises-with-try-catch)
- [Example 4: Nested Try-Catch Blocks](#example-4-nested-try-catch-blocks)
- [Try-Catch-Finally](#try-catch-finally)
- [Throwing Exceptions](#throwing-exceptions)
- [Custom Error Types](#custom-error-types)
- [Asynchronous Error Handling](#asynchronous-error-handling)
  - [Promises](#promises)
  - [Async/Await](#asyncawait)
- [Bun-Specific Details](#bun-specific-details)
- [Example 1: Basic Usage of finally](#example-1-basic-usage-of-finally)
- [Example 2: Resource Management](#example-2-resource-management)
- [Example 3: Completing Async Operations](#example-3-completing-async-operations)
- [Example 4: Using with Promise chain](#example-4-using-with-promise-chain)
- [Using Logs](#using-logs)
  - [Example: Simple Logging](#example-simple-logging)
- [Using Error Messages](#using-error-messages)
  - [Example: Using try-catch for Error Handling](#example-using-try-catch-for-error-handling)
  - [Example: Custom Error Classes](#example-custom-error-classes)
- [Using BUN.run() to Manage Logs in Bun](#using-bunrun-to-manage-logs-in-bun)
  - [Example: Running a Script with Bun](#example-running-a-script-with-bun)
- [Reading Text Files](#reading-text-files)
  - [Asynchronously](#asynchronously)
  - [Synchronously](#synchronously)
- [Writing Text Files](#writing-text-files)
  - [Asynchronously](#asynchronously-1)
  - [Synchronously](#synchronously-1)
- [Important Notes](#important-notes-1)
- [Reading a Binary File](#reading-a-binary-file)
- [Writing to a Binary File](#writing-to-a-binary-file)
- [Converting Text to Binary and Writing to a File](#converting-text-to-binary-and-writing-to-a-file)
- [Working with a JSON File](#working-with-a-json-file)
- [Working with a CSV File](#working-with-a-csv-file)
- [Summary](#summary-1)
- [Reading from a File Stream](#reading-from-a-file-stream)
- [Writing to a File Stream](#writing-to-a-file-stream)
- [Piping Streams](#piping-streams)
- [Reading a File](#reading-a-file)
- [Writing to a File](#writing-to-a-file)
- [Using Asynchronous Methods](#using-asynchronous-methods)
  - [Reading a File Asynchronously](#reading-a-file-asynchronously)
  - [Writing to a File Asynchronously](#writing-to-a-file-asynchronously)
- [Key Points](#key-points)
- [Example 1: Function Declaration](#example-1-function-declaration)
- [Example 2: Function Expression](#example-2-function-expression)
- [Example 3: Arrow Function](#example-3-arrow-function)
- [Example 4: Immediately Invoked Function Expression (IIFE)](#example-4-immediately-invoked-function-expression-iife)
- [Example 5: Functions with Default Parameters](#example-5-functions-with-default-parameters)
- [Example 6: Asynchronous Function with Async/Await](#example-6-asynchronous-function-with-asyncawait)
- [Default Arguments](#default-arguments)
- [Optional Arguments](#optional-arguments)
- [Combining Default and Optional Arguments](#combining-default-and-optional-arguments)
- [Basic Function Return](#basic-function-return)
- [Using Arrow Functions](#using-arrow-functions)
- [Return in Asynchronous Functions](#return-in-asynchronous-functions)
- [Return in Generators](#return-in-generators)
- [Returning Objects](#returning-objects)
- [Using Return Values in Array Methods](#using-return-values-in-array-methods)
- [Basic GET Request](#basic-get-request)
- [POST Request with JSON Body](#post-request-with-json-body)
- [Handling Different Response Types](#handling-different-response-types)
- [Using Query Parameters](#using-query-parameters)
- [Setting Up a WebSocket Server](#setting-up-a-websocket-server)
- [Setting Up a WebSocket Client](#setting-up-a-websocket-client)
- [Key Points to Remember](#key-points-to-remember)
- [FTP using `basic-ftp`](#ftp-using-basic-ftp)
- [SFTP using `ssh2-sftp-client`](#sftp-using-ssh2-sftp-client)
- [SSH using `node-ssh`](#ssh-using-node-ssh)
- [JSON Example](#json-example)
- [XML Example](#xml-example)
- [Additional Considerations](#additional-considerations)
- [Using Express.js with Bun](#using-expressjs-with-bun)
- [Using Fastify with Bun](#using-fastify-with-bun)
- [Using Koa.js with Bun](#using-koajs-with-bun)
- [Defining a Class](#defining-a-class)
- [Using a Class](#using-a-class)
- [Inheritance](#inheritance)
- [Static Methods and Properties](#static-methods-and-properties)
- [Private Fields and Methods](#private-fields-and-methods)
- [Creating Objects](#creating-objects)
  - [Using Object Literals](#using-object-literals)
  - [Using a Constructor Function](#using-a-constructor-function)
- [Instancing Classes](#instancing-classes)
  - [Defining and Instancing a Class](#defining-and-instancing-a-class)
  - [Inheritance with Classes](#inheritance-with-classes)
- [Example 1: Class-Based Inheritance](#example-1-class-based-inheritance)
- [Example 2: Prototype-Based Inheritance](#example-2-prototype-based-inheritance)
- [Example 3: Extending Built-in Classes](#example-3-extending-built-in-classes)
- [Example 4: Using Inheritance with the `extends` and `super` Keywords](#example-4-using-inheritance-with-the-extends-and-super-keywords)
- [Implementing with Bun](#implementing-with-bun)
- [Explanation:](#explanation-3)
- [Example 1: Basic Pattern Matching](#example-1-basic-pattern-matching)
- [Example 2: Case Insensitive Matching](#example-2-case-insensitive-matching)
- [Example 3: Global Search with `match`](#example-3-global-search-with-match)
- [Example 4: Replace Substring](#example-4-replace-substring)
- [Example 5: Capturing Groups](#example-5-capturing-groups)
- [Example 6: Split Using Regex](#example-6-split-using-regex)
- [Example 7: Positive Lookahead](#example-7-positive-lookahead)
- [Example 8: Negative Lookbehind](#example-8-negative-lookbehind)
- [Using Capturing Groups](#using-capturing-groups)
- [Conclusion](#conclusion)
- [Example 1: Simple Substitution](#example-1-simple-substitution)
- [Example 2: Case-Insensitive Substitution](#example-2-case-insensitive-substitution)
- [Example 3: Using Capture Groups](#example-3-using-capture-groups)
- [Example 4: Using a Replacement Function](#example-4-using-a-replacement-function)
- [Example 5: Complex Pattern Replacement](#example-5-complex-pattern-replacement)
- [1. Email Validation](#1-email-validation)
- [2. URL Validation](#2-url-validation)
- [3. IPv4 Address Validation](#3-ipv4-address-validation)
- [4. Phone Number Validation (US)](#4-phone-number-validation-us)
- [5. Password Complexity Validation](#5-password-complexity-validation)
- [6. Hexadecimal Color Code Validation](#6-hexadecimal-color-code-validation)
- [Example 1: Simple Regex Replacement with a Callback](#example-1-simple-regex-replacement-with-a-callback)
- [Example 2: Conditional Replacement](#example-2-conditional-replacement)
- [Example 3: Using Regex for Transformation](#example-3-using-regex-for-transformation)
- [Example: Symmetric Encryption and Decryption](#example-symmetric-encryption-and-decryption)
- [Explanation:](#explanation-4)
- [Important Notes:](#important-notes-2)
- [Digital Signatures](#digital-signatures)
- [Digital Certificates](#digital-certificates)
- [Example: HTTPS Server Using Bun's Native `https` Module](#example-https-server-using-buns-native-https-module)
- [Example: HTTPS Client Request Using Bun's Native `https` Module](#example-https-client-request-using-buns-native-https-module)
- [Using Third-Party Libraries for Enhanced Functionality](#using-third-party-libraries-for-enhanced-functionality)
- [Example: Simple ACL for an API](#example-simple-acl-for-an-api)
  - [Step 1: Define Users and Roles](#step-1-define-users-and-roles)
  - [Step 2: Middleware to Check ACL](#step-2-middleware-to-check-acl)
  - [Step 3: Define Routes with ACL](#step-3-define-routes-with-acl)
- [Run the Example with Bun](#run-the-example-with-bun)
- [Example 1: Basic Test](#example-1-basic-test)
- [Example 2: Testing Asynchronous Code](#example-2-testing-asynchronous-code)
- [Example 3: Grouping Tests with Describe](#example-3-grouping-tests-with-describe)
- [Example 4: Running Tests with Setup and Teardown](#example-4-running-tests-with-setup-and-teardown)
- [Running the Tests](#running-the-tests)
- [Writing Tests](#writing-tests)
- [Running Tests](#running-tests)
- [Tips for Effective Testing](#tips-for-effective-testing)
- [Example 1: Using Bun's built-in Debugger](#example-1-using-buns-built-in-debugger)
- [Example 2: Breakpoints in the Code](#example-2-breakpoints-in-the-code)
- [Example 3: Logging and Conditional Breakpoints](#example-3-logging-and-conditional-breakpoints)
- [Example 4: Viewing Call Stack and Scopes](#example-4-viewing-call-stack-and-scopes)
- [Example 1: Using `bunyan`](#example-1-using-bunyan)
- [Example 2: Using `winston`](#example-2-using-winston)
- [Example 3: Using `pino`](#example-3-using-pino)
- [Notes:](#notes-2)

<!-- /code_chunk_output -->

 JavaScript execution. You can start it by simply typing:
   ```bash
   bun
   ```
   In the REPL, you can type JavaScript commands and immediately see the results, which is useful for quick edits and testing.

4. **File Watching and Hot Reloading**: If you are looking for "edit statement" like features for real-time code updates, consider using Bun with automatic file watching for server scripts. While Bun might not support this directly out-of-the-box in the same way some other tools do, you can typically accomplish hot reloading using some development configurations or tools.

5. **Developing and Testing**: Bun includes its own package manager, test runner, and bundler. To edit and test your code:
   - Organize your code in a project directory.
   - Use Bun's toolchain to install dependencies, run tests, and bundle your code.

Ensure to keep up with the [official Bun documentation](https://bun.sh/docs) for the most recent updates and explore any new features or plugins that might enhance your workflow, including hot module replacement (HMR) solutions if that's what you're seeking.

Certainly! Below are some examples of using `for` loops in Bun, the JavaScript runtime:

### 1. Basic `for` Loop
This loop will iterate from 0 to 4 and print each number.

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### 2. Iterating Over an Array
This loop will iterate over the elements of an array and print each one.

```javascript
const fruits = ['apple', 'banana', 'cherry'];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```

### 3. `for...of` Loop
The `for...of` loop is used to iterate over iterable objects like arrays.

```javascript
const colors = ['red', 'green', 'blue'];

for (const color of colors) {
  console.log(color);
}
```

### 4. `for...in` Loop
The `for...in` loop is used to iterate over the properties of an object.

```javascript
const car = { make: 'Toyota', model: 'Corolla', year: 2020 };

for (const key in car) {
  console.log(`${key}: ${car[key]}`);
}
```

### 5. Nested `for` Loop
A `for` loop can be nested inside another `for` loop to handle multi-dimensional data structures like matrices (2D arrays).

```javascript
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

for (let i = 0; i < matrix.length; i++) {
  for (let j = 0; j < matrix[i].length; j++) {
    console.log(matrix[i][j]);
  }
}
```

### 6. Using `break` and `continue`
`break` exits the loop, and `continue` skips the current iteration.

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break; // Exit the loop when i is 5
  }
  if (i % 2 === 0) {
    continue; // Skip even numbers
  }
  console.log(i); // Only prints odd numbers: 1, 3
}
```

These examples demonstrate a variety of ways to use `for` loops in JavaScript and should work without any changes in the Bun runtime, as it supports standard JavaScript syntax.

Here are some examples of using `while` loops in the Bun JavaScript runtime:

### Example 1: Basic While Loop

```javascript
let count = 0;

while (count < 5) {
  console.log(`Count is: ${count}`);
  count++;
}
```

In this example, the `while` loop continues to execute as long as the condition `count < 5` is true. It increments the `count` variable by 1 in each iteration and logs the current count to the console.

### Example 2: Using `while` Loop for Array Traversal

```javascript
const fruits = ['apple', 'banana', 'cherry'];
let index = 0;

while (index < fruits.length) {
  console.log(`Fruit: ${fruits[index]}`);
  index++;
}
```

This example uses a `while` loop to iterate through the elements of an array. The loop condition checks if the current `index` is less than the length of the `fruits` array.

### Example 3: Using `while` Loop to Wait for a Condition

```javascript
let ready = false;

// Simulate an asynchronous operation using setTimeout
setTimeout(() => {
  ready = true;
}, 3000);

console.log("Waiting for ready...");

while (!ready) {
  // Busy-wait (not recommended for real-world use)
}

console.log("Ready!");
```

This example demonstrates a busy-wait loop, which continues to loop until the `ready` variable is set to true. Note that busy-waiting like this is generally not recommended for real-world applications due to its inefficient use of CPU resources.

### Example 4: Using `do...while` Loop

```javascript
let number;
do {
  number = Math.floor(Math.random() * 10);
  console.log(`Generated number: ${number}`);
} while (number !== 5);

console.log("Exited loop since we found 5!");
```

In this example, a `do...while` loop is used to generate random numbers between 0 and 9 until the number 5 is generated. The loop guarantees at least one execution before the condition is checked.

### Note

When running these examples in Bun, use the Bun command line to execute the JavaScript files, just like you would with Node.js:
```bash
bun run <filename>.js
```

These examples assume you are familiar with JavaScript syntax and fundamental programming concepts. If you're using Bun, you should also ensure that you are using it in an environment compatible with the latest JavaScript syntax and APIs.

In JavaScript, the `do-while` loop is used to execute a block of code at least once and then repeat the execution as long as a specified condition is true. Below are some examples demonstrating how to use `do-while` loops in the Bun JavaScript runtime.

### Example 1: Basic Counter
This example illustrates a simple use of a `do-while` loop to print numbers from 1 to 5.

```javascript
let counter = 1;

do {
  console.log('Counter:', counter);
  counter++;
} while (counter <= 5);
```

### Example 2: User Input Validation
Here’s a hypothetical example assuming an environment where prompt-like functions are available, illustrating data validation for user input.

```javascript
let number;

do {
  number = parseInt(prompt("Enter a number greater than 10: "), 10);
} while (isNaN(number) || number <= 10);

console.log("You entered:", number);
```

### Example 3: Array Iteration
This example demonstrates iterating over an array using a `do-while` loop.

```javascript
const fruits = ['apple', 'banana', 'cherry'];
let index = 0;

do {
  console.log(fruits[index]);
  index++;
} while (index < fruits.length);
```

### Example 4: Sum until Max Value
This example calculates the sum of numbers until the sum reaches a maximum value.

```javascript
let sum = 0;
let i = 1;
const max = 20;

do {
  sum += i;
  i++;
} while (sum + i <= max);

console.log('Sum:', sum);
```

### Example 5: Generating Random Numbers
Generate random numbers until a number greater than 0.8 is generated.

```javascript
let randomNumber;

do {
  randomNumber = Math.random();
  console.log('Generated:', randomNumber);
} while (randomNumber <= 0.8);
```

These examples cover various use cases of the `do-while` loop, demonstrating its ability to ensure a block of code runs at least once and continues based on a condition.

In JavaScript, both `break` and `continue` statements are used to control the flow of loops, and this behavior is consistent across different JavaScript runtimes, including Bun. Here's how you can use them:

### `break` Statement

The `break` statement is used to terminate the current loop or switch statement prematurely. When a `break` statement is encountered, the control flow exits the loop immediately and continues with the statement following the loop.

**Example: Using `break` in a loop:**

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break; // Exit the loop when i is 5
  }
  console.log(i); // Outputs 0, 1, 2, 3, 4
}
```

In this example, the loop will print numbers from 0 to 4. When `i` becomes 5, the `break` statement is executed, terminating the loop.

### `continue` Statement

The `continue` statement is used to skip the current iteration of the loop and move to the next iteration. When a `continue` statement is encountered, the remaining code inside the loop for the current iteration is skipped, and the loop proceeds to the next iteration.

**Example: Using `continue` in a loop:**

```javascript
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    continue; // Skip even numbers
  }
  console.log(i); // Outputs 1, 3, 5, 7, 9
}
```

In this example, the loop will skip printing even numbers by using the `continue` statement, thus only printing the odd numbers.

### Usage in Other Loops

The `break` and `continue` statements can be used in other types of loops as well (like `while` and `do...while` loops). Here’s a quick example using a `while` loop:

```javascript
let i = 0;
while (i < 10) {
  i++;
  if (i === 3) {
    continue; // Skip when i is 3
  }
  if (i === 8) {
    break; // Stop the loop when i is 8
  }
  console.log(i); // Outputs 1, 2, 4, 5, 6, 7
}
```

### Summary

- **`break`**: Exits the loop early.
- **`continue`**: Skips the current iteration and continues with the next iteration of the loop.

These constructs let you have more fine-grained control over your loops, making your code cleaner and more efficient in scenarios where certain conditions require skipping or prematurely exiting iterations.

In JavaScript, including the Bun runtime, the use of `goto` is not supported because JavaScript doesn't have a `goto` statement like some other languages (e.g., C or BASIC). However, JavaScript does support labeled statements, which can be used with loops to break out or continue to a specific loop.

Here's a simple example using labels with loops:

```javascript
outerLoop: for (let i = 0; i < 3; i++) {
  console.log(`Outer loop iteration: ${i}`);
  innerLoop: for (let j = 0; j < 3; j++) {
    console.log(`  Inner loop iteration: ${j}`);
    if (j === 1) {
      console.log('  Breaking out of both loops');
      break outerLoop; // This will break out of the outer loop
    }
  }
}

console.log('Done');
```

In this example, the label `outerLoop` is used with the `break` statement to exit the outer loop when a specific condition is met in the inner loop.

Another example with `continue`:

```javascript
outerLoop: for (let i = 0; i < 3; i++) {
  console.log(`Outer loop iteration: ${i}`);
  for (let j = 0; j < 3; j++) {
    if (j === 1) {
      console.log('  Skipping the rest of the inner loop...');
      continue outerLoop; // This skips the current iteration of the outer loop
    }
    console.log(`  Inner loop iteration: ${j}`);
  }
}

console.log('Done');
```

Here, the label `outerLoop` is used with the `continue` statement, which skips the current iteration of the outer loop when a certain condition is met in the inner loop.

While labels can be useful in specific scenarios, it's generally recommended to use them sparingly, as overusing labels can make code harder to read and follow.

Data Types and Variables
In Bun, which is a modern JavaScript runtime similar to Node.js or Deno, you can declare and use variables using standard JavaScript syntax. Here are some examples:

### Declaring Variables

1. **Using `let`**:
   Allows you to declare a block-scoped, mutable variable.

   ```javascript
   let name = "Alice";
   console.log(name); // Outputs: Alice
   ```

2. **Using `const`**:
   Allows you to declare a block-scoped, read-only constant. Once assigned, the value of a `const` variable cannot be changed.

   ```javascript
   const age = 30;
   console.log(age); // Outputs: 30

   // The following line would throw an error because `age` is a constant
   // age = 31;
   ```

3. **Using `var`**:
   Declares a function-scoped or globally-scoped variable that can be re-assigned.

   ```javascript
   var city = "New York";
   console.log(city); // Outputs: New York
   ```

### Using Variables

Once declared, you can use these variables in expressions, function calls, or anywhere else in your Bun application where variables are needed.

```javascript
// Example using `let`
let greeting = "Hello";
let person = "Bob";
console.log(greeting + ", " + person + "!"); // Outputs: Hello, Bob!

// Example using `const`
const pi = 3.14159;
function calculateCircumference(diameter) {
  return pi * diameter;
}

console.log(calculateCircumference(10)); // Outputs: 31.4159

// Example using `var`
var isAvailable = true;
if (isAvailable) {
  console.log("The item is in stock."); // Outputs: The item is in stock.
} else {
  console.log("The item is out of stock.");
}
```

### Points to Note

- Prefer `let` and `const` over `var` for block scoping and to avoid hoisting-related issues.
- Use `const` when you don't intend to reassign a variable after it is initialized.
- Variables declared with `let` and `const` are not attached to the global `window` or `global` object in Bun, aligning with ES6 specs.

In Bun, as with any JavaScript runtime, you can work with integers, floats, and strings using standard JavaScript syntax and methods. Here's a brief guide on how to handle these data types:

### Integers

Integers in JavaScript are part of the `Number` type. You can perform various arithmetic operations with them.

```javascript
let a = 5;
let b = 10;

// Addition
let sum = a + b; // 15

// Subtraction
let difference = b - a; // 5

// Multiplication
let product = a * b; // 50

// Division
let quotient = b / a; // 2

// Remainder
let remainder = b % a; // 0
```

### Floats

Floats are simply numbers with decimals in JavaScript. Like integers, they are part of the `Number` type and can be manipulated using arithmetic operations.

```javascript
let c = 5.7;
let d = 3.3;

// Addition
let sumFloat = c + d; // 9.0

// Subtraction
let differenceFloat = c - d; // 2.4

// Multiplication
let productFloat = c * d; // 18.81

// Division
let quotientFloat = c / d; // 1.7272727272727273
```

### Strings

Strings are used to represent textual data. You can use various methods to manipulate strings in JavaScript:

```javascript
let hello = "Hello";
let world = "World";

// Concatenation
let greeting = hello + " " + world + "!"; // "Hello World!"

// Length
let length = greeting.length; // 12

// Accessing characters
let firstCharacter = hello[0]; // "H"

// Substrings
let subString = hello.substring(0, 3); // "Hel"

// Upper and lower case
let upper = hello.toUpperCase(); // "HELLO"
let lower = world.toLowerCase(); // "world"
```

### Conversions

Converting between these types is often necessary:

- **From String to Integer/Float**:
  - Use `parseInt()` for integers.
  - Use `parseFloat()` for floats.

```javascript
let numString = "42";
let integer = parseInt(numString); // 42

let floatString = "42.58";
let floatNum = parseFloat(floatString); // 42.58
```

- **From Number to String**:
  - Use the `toString()` method on numbers.

```javascript
let num = 123;
let numStr = num.toString(); // "123"
```

### Important Notes

- All numbers in JavaScript are double-precision floating-point (64-bit) as per the IEEE 754 standard. This means precise integer representation is possible up to `Number.MAX_SAFE_INTEGER`, which is `2^53 - 1`.
- For very large integers, consider using the `BigInt` type, although it’s more than just simple conversion.

With these basics, you can work effectively with integers, floats, and strings in Bun’s JavaScript runtime. Remember that Bun aims to provide a robust JavaScript environment, thus standard JavaScript practices apply seamlessly.

Enumerated types, or enums, are not natively supported in JavaScript as they are in languages like TypeScript or Java. However, we can implement similar behavior in JavaScript using objects. Below are examples of how you can create and use enums in the Bun JavaScript runtime.

### Example 1: Basic Enum-like Structure

```javascript
const Color = Object.freeze({
    RED: 'red',
    GREEN: 'green',
    BLUE: 'blue',
});

// Usage
function getColorName(color) {
    switch (color) {
        case Color.RED:
            return 'Red';
        case Color.GREEN:
            return 'Green';
        case Color.BLUE:
            return 'Blue';
        default:
            return 'Unknown color';
    }
}

console.log(getColorName(Color.RED));   // Output: Red
console.log(getColorName('yellow'));    // Output: Unknown color
```

### Example 2: Enum with Numeric Values

```javascript
const Direction = Object.freeze({
    UP: 1,
    DOWN: 2,
    LEFT: 3,
    RIGHT: 4,
});

// Usage
function moveDirection(direction) {
    switch (direction) {
        case Direction.UP:
            console.log('Moving up');
            break;
        case Direction.DOWN:
            console.log('Moving down');
            break;
        case Direction.LEFT:
            console.log('Moving left');
            break;
        case Direction.RIGHT:
            console.log('Moving right');
            break;
        default:
            console.log('Invalid direction');
    }
}

moveDirection(Direction.UP);   // Output: Moving up
moveDirection(5);              // Output: Invalid direction
```

### Example 3: Enum with Symbol Values for Enhanced Safety

```javascript
const Animal = Object.freeze({
    DOG: Symbol('dog'),
    CAT: Symbol('cat'),
    BIRD: Symbol('bird'),
});

// Usage
function describeAnimal(animal) {
    switch (animal) {
        case Animal.DOG:
            return 'This is a dog.';
        case Animal.CAT:
            return 'This is a cat.';
        case Animal.BIRD:
            return 'This is a bird.';
        default:
            return 'Unknown animal.';
    }
}

console.log(describeAnimal(Animal.DOG));        // Output: This is a dog.
console.log(describeAnimal(Symbol('rabbit')));  // Output: Unknown animal.
```

### Explanation

- **Object.freeze()**: Used to make the `Color`, `Direction`, and `Animal` objects immutable, preventing any changes after their declaration.
- **Symbol**: Provides a unique value which can help prevent accidental overlap with other values (e.g., using strings) which makes enums more robust.
- **Switch Statements**: Commonly used to handle different enum values.

These examples demonstrate a common pattern used in JavaScript to emulate enumerated types. This pattern is fully compatible with the Bun runtime as it builds on standard JavaScript constructs.

In Bun, which is a fast JavaScript runtime like Node.js or Deno, you can define and use arrays in the same way you would in standard JavaScript. Here are some examples:

### Defining Arrays

1. **Literal Notation**

```javascript
const fruits = ['apple', 'banana', 'cherry'];
console.log(fruits); // Output: ['apple', 'banana', 'cherry']
```

2. **Using the Array Constructor**

```javascript
const numbers = new Array(1, 2, 3, 4, 5);
console.log(numbers); // Output: [1, 2, 3, 4, 5]
```

### Accessing Array Elements

```javascript
const colors = ['red', 'green', 'blue'];
console.log(colors[0]); // Output: 'red'
console.log(colors[2]); // Output: 'blue'
```

### Modifying Arrays

1. **Adding Elements**

```javascript
const animals = ['dog', 'cat'];
animals.push('rabbit');
console.log(animals); // Output: ['dog', 'cat', 'rabbit']
```

2. **Removing Elements**

```javascript
const cars = ['Toyota', 'Ford', 'BMW'];
cars.pop();
console.log(cars); // Output: ['Toyota', 'Ford']
```

### Iterating Over Arrays

1. **Using `for` Loop**

```javascript
const numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}
// Output: 1 2 3 4 5
```

2. **Using `forEach` Method**

```javascript
const letters = ['a', 'b', 'c'];
letters.forEach(letter => {
  console.log(letter);
});
// Output: 'a' 'b' 'c'
```

3. **Using `for...of` Loop**

```javascript
const items = ['pen', 'notebook', 'eraser'];
for (const item of items) {
  console.log(item);
}
// Output: 'pen' 'notebook' 'eraser'
```

### Advanced Array Methods

1. **Mapping**

```javascript
const numbers = [1, 2, 3, 4, 5];
const squared = numbers.map(num => num * num);
console.log(squared); // Output: [1, 4, 9, 16, 25]
```

2. **Filtering**

```javascript
const ages = [18, 21, 16, 30];
const adults = ages.filter(age => age >= 18);
console.log(adults); // Output: [18, 21, 30]
```

3. **Reducing**

```javascript
const values = [10, 20, 30];
const sum = values.reduce((total, value) => total + value, 0);
console.log(sum); // Output: 60
```

These examples demonstrate fundamental operations on arrays in JavaScript using Bun. The behavior is consistent with standard ECMAScript implementations, so you can apply the same array methods and manipulation techniques in Bun as you would in other JavaScript environments.

The Bun JavaScript runtime supports working with lists, which in JavaScript are typically managed using arrays. Below are some examples of how you can use lists in Bun:

### Creating and Manipulating Lists

```javascript
// Creating a list
let fruits = ['apple', 'banana', 'cherry'];

// Accessing elements
console.log(fruits[0]); // Outputs: 'apple'
console.log(fruits[1]); // Outputs: 'banana'

// Adding elements to a list
fruits.push('date');
console.log(fruits); // Outputs: ['apple', 'banana', 'cherry', 'date']

// Removing the last element
fruits.pop();
console.log(fruits); // Outputs: ['apple', 'banana', 'cherry']

// Adding an element to the beginning
fruits.unshift('kiwi');
console.log(fruits); // Outputs: ['kiwi', 'apple', 'banana', 'cherry']

// Removing the first element
fruits.shift();
console.log(fruits); // Outputs: ['apple', 'banana', 'cherry']

// Removing elements by index
fruits.splice(1, 1); // Removes 'banana'
console.log(fruits); // Outputs: ['apple', 'cherry']

// Replacing elements
fruits[1] = 'blueberry';
console.log(fruits); // Outputs: ['apple', 'blueberry']
```

### Iterating Over Lists

```javascript
// Using for loop
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

// Using for...of loop
for (let fruit of fruits) {
  console.log(fruit);
}

// Using forEach method
fruits.forEach(fruit => {
  console.log(fruit);
});
```

### List Transformations and Queries

```javascript
// Mapping list to a new list
let uppercasedFruits = fruits.map(fruit => fruit.toUpperCase());
console.log(uppercasedFruits); // Outputs: ['APPLE', 'BLUEBERRY']

// Filtering list
let longNamedFruits = fruits.filter(fruit => fruit.length > 5);
console.log(longNamedFruits); // Outputs: ['blueberry']

// Checking if some elements satisfy a condition
let hasApple = fruits.some(fruit => fruit === 'apple');
console.log(hasApple); // Outputs: true

// Checking if all elements satisfy a condition
let allFruitsStartWithB = fruits.every(fruit => fruit[0] === 'b');
console.log(allFruitsStartWithB); // Outputs: false

// Reducing list to a single value
let concatenatedFruits = fruits.reduce((accumulator, current) => accumulator + current, '');
console.log(concatenatedFruits); // Outputs: 'appleblueberry'
```

These examples demonstrate how to create and manipulate lists (arrays) in the Bun JavaScript runtime. You can perform various operations like adding, removing, iterating, and transforming elements efficiently with JavaScript's powerful array methods.

In JavaScript, dictionaries are typically implemented using objects or the `Map` class. Since Bun is a modern JavaScript runtime, it supports all standard JavaScript features, including objects and the `Map` class. Below are examples of how you can work with dictionaries using these two approaches.

### Using Objects

Objects in JavaScript are collections of key-value pairs. They are the most straightforward way to create a dictionary-like structure.

#### Creating an Object

```javascript
const dictionary = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};
```

#### Accessing Values

```javascript
console.log(dictionary.key1); // Output: 'value1'

// You can also use bracket notation
console.log(dictionary['key2']); // Output: 'value2'
```

#### Adding or Updating Entries

```javascript
dictionary.key4 = 'value4'; // Adding a new key-value pair
dictionary.key1 = 'newValue1'; // Updating the value of an existing key
```

#### Deleting Entries

```javascript
delete dictionary.key2;
```

#### Iterating Over an Object

You can use `for...in` to loop over the keys of an object.

```javascript
for (let key in dictionary) {
  if (dictionary.hasOwnProperty(key)) {
    console.log(key, dictionary[key]);
  }
}
```

### Using the Map Class

The `Map` class provides a more sophisticated way to handle key-value pairs, particularly when working with keys that are not strings.

#### Creating a Map

```javascript
const map = new Map();
```

#### Adding Entries

```javascript
map.set('key1', 'value1');
map.set('key2', 'value2');
map.set('key3', 'value3');
```

#### Accessing Values

```javascript
console.log(map.get('key1')); // Output: 'value1'
```

#### Updating Entries

```javascript
map.set('key1', 'newValue1');
```

#### Deleting Entries

```javascript
map.delete('key2');
```

#### Checking for a Key

```javascript
console.log(map.has('key3')); // Output: true
console.log(map.has('key2')); // Output: false
```

#### Iterating Over a Map

You can use `for...of` to loop over entries in a `Map`.

```javascript
for (let [key, value] of map) {
  console.log(key, value);
}
```

#### Getting the Size of a Map

```javascript
console.log(map.size); // Output: the number of key-value pairs in the map
```

### Choosing Between Objects and Maps

- Use **objects** for simple key-value storage where keys are known and are strings.
- Use **Map** for more complex scenarios, especially when keys can be of any type or when key insertion order matters.

Both objects and maps are fully supported in Bun, and you can use them as you would in any modern JavaScript environment.

In Bun, you can use JavaScript's built-in `Set` object, which is part of the ECMAScript standard and works seamlessly in any environment that supports modern JavaScript, including the Bun runtime. Here are some examples of using sets in Bun:

### Example 1: Creating and Using a Set

```javascript
// Create a new Set
const mySet = new Set();

// Add values to the Set
mySet.add(1);
mySet.add(2);
mySet.add(3);
mySet.add(2); // Duplicate values are ignored

console.log(mySet); // Output: Set(3) { 1, 2, 3 }

// Check if the Set contains a value
console.log(mySet.has(2)); // Output: true
console.log(mySet.has(4)); // Output: false

// Get the size of the Set
console.log(mySet.size); // Output: 3
```

### Example 2: Iterating Over a Set

```javascript
const mySet = new Set([1, 2, 3, 4, 5]);

// Use forEach to iterate over Set elements
mySet.forEach(value => {
  console.log(value);
});

// Use for...of loop to iterate over Set elements
for (const value of mySet) {
  console.log(value);
}
```

### Example 3: Converting Between Sets and Arrays

```javascript
// Convert an Array to a Set
const array = [1, 2, 3, 4, 5, 5, 6];
const mySet = new Set(array);

console.log(mySet); // Output: Set(6) { 1, 2, 3, 4, 5, 6 }

// Convert a Set to an Array
const newArray = Array.from(mySet);

console.log(newArray); // Output: [1, 2, 3, 4, 5, 6]
```

### Example 4: Performing Set Operations

```javascript
const setA = new Set([1, 2, 3, 4]);
const setB = new Set([3, 4, 5, 6]);

// Union of two Sets
const union = new Set([...setA, ...setB]);
console.log(union); // Output: Set(6) { 1, 2, 3, 4, 5, 6 }

// Intersection of two Sets
const intersection = new Set([...setA].filter(x => setB.has(x)));
console.log(intersection); // Output: Set(2) { 3, 4 }

// Difference of two Sets
const difference = new Set([...setA].filter(x => !setB.has(x)));
console.log(difference); // Output: Set(2) { 1, 2 }
```

### Example 5: Removing Elements and Clearing a Set

```javascript
const mySet = new Set([1, 2, 3, 4, 5]);

// Remove an element from the Set
mySet.delete(3);
console.log(mySet); // Output: Set(4) { 1, 2, 4, 5 }

// Clear the entire Set
mySet.clear();
console.log(mySet); // Output: Set(0) {}
```

These examples demonstrate how to create and manipulate sets in JavaScript using the Bun runtime or any other modern JavaScript environment.

In JavaScript, there isn't a built-in tuple data structure like there is in languages such as Python or TypeScript. However, you can treat arrays as tuples by using specific conventions or patterns, especially when using a runtime like Bun. Here's how you can work with tuple-like structures in JavaScript:

### Example 1: Defining a Tuple as a Fixed-Size Array

```javascript
// Define a tuple as a fixed-size array
const point = [10, 20]; // A tuple representing a point (x, y)

// Accessing tuple elements
const x = point[0]; // 10
const y = point[1]; // 20

// Output the values
console.log('x:', x); // x: 10
console.log('y:', y); // y: 20
```

### Example 2: Using TypeScript for Tuple Annotations

If you're using TypeScript with Bun, you can define tuples with more clarity:

```typescript
// Define a tuple with TypeScript
type Point = [number, number];
const point: Point = [10, 20];

// Destructuring a tuple
const [x, y] = point;

// Output the values
console.log('x:', x); // x: 10
console.log('y:', y); // y: 20
```

### Example 3: Using Tuples for Function Return Values

Tuples can be used to return multiple values from a function:

```javascript
// Function returning a tuple
function getCoordinates() {
  return [10, 20]; // A tuple representing a point (x, y)
}

const [x, y] = getCoordinates();

// Output the values
console.log('x:', x); // x: 10
console.log('y:', y); // y: 20
```

### Example 4: Immutable Tuples with Object.freeze

Although JavaScript arrays are mutable, you can freeze an array to make it immutable, similar to a tuple:

```javascript
// Creating an immutable tuple
const point = Object.freeze([10, 20]);

// Trying to modify the tuple (this will fail)
point[0] = 30; // This won't change the value as the array is frozen

console.log(point); // [10, 20]
```

Working with tuples in Bun doesn't differ significantly from using standard JavaScript practices, as Bun is designed to be highly compatible with Node.js and typical JavaScript runtime environments.

Databases
To connect to a database in the Bun JavaScript runtime, you'll typically use a Node.js-compatible database library. Bun aims to maintain compatibility with Node.js APIs, which allows you to use many of the existing libraries. Here's a step-by-step guide for connecting to a database using Bun:

### 1. Choose a Database Library
Depending on the type of database you are using (e.g., PostgreSQL, MySQL, MongoDB), you'll want to pick an appropriate library. Some popular choices include:
- PostgreSQL: `pg` or `@databases/pg`
- MySQL: `mysql2`
- MongoDB: `mongodb`

### 2. Install the Database Library
Before connecting to the database, you need to install the database client library. If you are using Bun, you typically use Bun's package manager:

```bash
bun add pg       # For PostgreSQL
bun add mysql2   # For MySQL
bun add mongodb  # For MongoDB
```

### 3. Write the Connection Code

#### Example: Connecting to PostgreSQL with `pg`
```javascript
import { Client } from 'pg';

const client = new Client({
  user: 'your-username',
  host: 'localhost',
  database: 'your-database',
  password: 'your-password',
  port: 5432,  // default PostgreSQL port
});

async function connectToDatabase() {
  try {
    await client.connect();
    console.log('Connected to the database successfully!');
    
    // You can now execute queries on the client
    // const res = await client.query('SELECT NOW()');
    // console.log(res.rows[0]);
  } catch (error) {
    console.error('Failed to connect to the database', error);
  }
}

connectToDatabase();
```

#### Example: Connecting to MySQL with `mysql2`
```javascript
import mysql from 'mysql2/promise';

async function connectToDatabase() {
  const connection = await mysql.createConnection({
    host: 'localhost',
    user: 'your-username',
    database: 'your-database',
    password: 'your-password'
  });

  console.log('Connected to the database successfully!');
  
  // You can now execute queries on the connection
  // const [rows, fields] = await connection.execute('SELECT * FROM your_table');
  // console.log(rows);
}

connectToDatabase().catch(error => console.error('Failed to connect to the database', error));
```

#### Example: Connecting to MongoDB
```javascript
import { MongoClient } from 'mongodb';

const url = 'mongodb://localhost:27017';
const client = new MongoClient(url);

async function connectToDatabase() {
  try {
    await client.connect();
    console.log('Connected to MongoDB successfully!');
    
    // Specify the database name
    const db = client.db('your-database');

    // You can now perform operations on the database
    // const collection = db.collection('your-collection');
    // const docs = await collection.find({}).toArray();
    // console.log(docs);
  } catch (error) {
    console.error('Failed to connect to MongoDB', error);
  }
}

connectToDatabase();
```

### 4. Handle Disconnects and Errors
It is important to handle database connection errors and any potential disconnects gracefully. Each database library provides ways to handle such cases through events or retry mechanisms.

### 5. Closing the Connection
Make sure to properly close the connection when your application is shutting down or when the connection is no longer needed.

```javascript
await client.end();  // For `pg`
await connection.end();  // For `mysql2`
await client.close();  // For `mongodb`
```

This is a basic guideline, and depending on your application's architecture, you might need to manage connections differently (like using connection pooling). Always refer to the library's documentation for best practices and advanced features.

Certainly! Here's a basic example of how you can create and query tables using Bun's JavaScript runtime with SQLite. Bun provides a built-in SQLite interface that you can use directly.

### Setting Up

First, ensure you have Bun installed. You can download it from the [official Bun website](https://bun.sh/).

### Creating and Querying Tables

Here is a simple example that demonstrates creating a SQLite database, a table, inserting data into it, and then querying the data.

```javascript
// Import SQLite module from Bun
const { Database } = require('bun:sqlite');

// Create a new database. This will create an in-memory database.
const db = new Database(':memory:');

// Create a table called 'users'
db.run(`
  CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    email TEXT UNIQUE NOT NULL
  )
`);

// Insert a couple of users
db.run('INSERT INTO users (name, email) VALUES (?, ?)', ['Alice', 'alice@example.com']);
db.run('INSERT INTO users (name, email) VALUES (?, ?)', ['Bob', 'bob@example.com']);

// Query all users from the table
const users = db.query('SELECT * FROM users').all();
console.log('All Users:', users);

// Query a specific user by email
const alice = db.query('SELECT * FROM users WHERE email = ?').get('alice@example.com');
console.log('User Alice:', alice);
```

### Explanation

1. **Database Connection**: We create a new SQLite database. Using `':memory:'` makes it an in-memory database for testing purposes. For persistent storage, replace it with a file path like `'./mydb.sqlite'`.

2. **Table Creation**: We define a table `users` with three columns: `id`, `name`, and `email`.

3. **Data Insertion**: We insert some sample data into the `users` table. The `?` placeholders in the SQL statements are used to bind parameters, promoting security against SQL injection.

4. **Querying Data**: We retrieve all users with `.all()` and a specific user using `.get()` by binding the email parameter.

### Next Steps

- **Error Handling**: Implement error handling in production code. You can use try-catch blocks to handle any potential database errors.

- **Transactions**: If you're making multiple changes and want them to succeed or fail as a group, consider using transactions.

- **Persistence**: Use a file path in `new Database()` instead of `':memory:'` for data persistence across sessions.

This code demonstrates using Bun's capabilities to interact with SQLite databases for basic operations. You can expand upon this to suit your application's needs.

To interact with SQL databases using the Bun JavaScript runtime, you would typically use a database driver or library that supports your specific database (e.g., MySQL, PostgreSQL, SQLite). Bun provides native support for SQLite, but for other databases, you might use their respective npm packages. Below are examples of using SQL queries with JOINs and subqueries in a JavaScript environment running with Bun, using SQLite as the database:

### Example: Using JOINs

Assume you have two tables, `users` and `orders`, where `users` has the columns `id`, `name`, and `email`, and `orders` has the columns `id`, `user_id`, and `amount`.

```javascript
// Import Bun's SQLite API
import { Database } from 'bun:sqlite';

// Open a connection to a SQLite database
const db = new Database('mydatabase.sqlite');

// Example using a JOIN to get user names with their corresponding order amounts
const rows = db.query(`
  SELECT users.name, orders.amount
  FROM users
  INNER JOIN orders ON users.id = orders.user_id
`).all();

console.log(rows);
```

### Example: Using Subqueries

Assume you have a table `products` with the columns `id`, `name`, and `price`, and you want to find the most expensive product for each category in another table `categories` with columns `id`, `name`, and `product_id`.

```javascript
// Import Bun's SQLite API
import { Database } from 'bun:sqlite';

// Open a connection to a SQLite database
const db = new Database('mydatabase.sqlite');

// Example using a subquery to find the most expensive product in each category
const rows = db.query(`
  SELECT categories.name AS category_name, products.name AS product_name, products.price
  FROM categories
  JOIN products ON categories.product_id = products.id
  WHERE products.price = (
    SELECT MAX(price)
    FROM products p
    WHERE p.id = categories.product_id
  )
`).all();

console.log(rows);
```

### Notes

- Bun's SQLite API makes it easy to execute SQL commands directly. `all()` method is used to fetch all results from the executed query.
- Proper error handling should be added in production code to handle exceptions that may occur during database operations.
- For databases other than SQLite, consider using appropriate drivers or libraries. For example, `pg` for PostgreSQL, `mysql2` for MySQL, etc.
- Always ensure that SQL queries are safe from injection attacks by using parameterized queries or query builders when handling user input.

These examples illustrate basic JOIN and subquery usage in SQL within a Bun JavaScript environment, specifically targeting a SQLite database.

To use prepared statements in Bun, you typically interact with a database library that supports Bun's runtime environment. Here's a general example of using prepared statements with a SQLite database using `better-sqlite3` which is compatible with Bun.

First, make sure you have the necessary package installed:

```bash
bun add better-sqlite3
```

Now, here's an example of how you can use prepared statements with `better-sqlite3`:

```javascript
import Database from 'better-sqlite3';

// Create or open a database
const db = new Database('example.db', { verbose: console.log });

// Create a table if it doesn't exist
db.exec(`
  CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    age INTEGER
  )
`);

// Insert a new user using a prepared statement
const insertUser = db.prepare('INSERT INTO users (name, age) VALUES (?, ?)');
insertUser.run('Alice', 25);
insertUser.run('Bob', 30);

// Select users using a prepared statement
const selectUsers = db.prepare('SELECT * FROM users WHERE age > ?');
const users = selectUsers.all(20); // Parameter value is 20

console.log(users); // Output results

// Close the database connection when done
db.close();
```

### Explanation:
- **Database Initialization**: We create or open a SQLite database using `better-sqlite3`.
- **Table Creation**: We execute a SQL statement to ensure the `users` table exists.
- **Insert Statement**: A prepared statement is created with placeholders (`?`) for parameters. We then use `.run()` to execute this statement with specific values.
- **Select Statement**: Similarly, a prepared statement is used to select users based on a condition, and we use `.all()` to execute it and fetch the results.
- **Closing the Database**: After operations, we close the connection to the database using `db.close()`.

This example demonstrates basic usage of prepared statements to insert and select data safely and efficiently in a type-safe, parameterized manner, which helps prevent SQL injection attacks. The same approach can be adapted for other database libraries compatible with Bun, such as those for Postgres or MySQL.

Using transactions in a database ensures that a series of operations are completed successfully before making any permanent changes to the database. If one of the operations fails, the entire transaction can be rolled back to maintain data integrity. Below is an example of how you might manage transactions using a database like SQLite in the Bun JavaScript runtime.

Bun has support for SQLite out of the box. You can manage transactions by using the SQLite bindings provided by Bun. Here's an example of how you can perform transactions:

### Example Code

```javascript
// Import Bun's built-in SQLite API
const db = Bun.sqlite.open('my-database.sqlite');

// Begin a transaction
try {
    db.run('BEGIN TRANSACTION');

    // Execute several operations
    db.run('INSERT INTO users (name, email) VALUES (?, ?)', 'Alice', 'alice@example.com');
    db.run('UPDATE accounts SET balance = balance - 100 WHERE user_id = ?', 1);
    db.run('UPDATE accounts SET balance = balance + 100 WHERE user_id = ?', 2);
    
    // Commit the transaction if all operations succeed
    db.run('COMMIT');
} catch (error) {
    // Rollback the transaction if any operation fails
    db.run('ROLLBACK');
    console.error('Transaction failed:', error);
}

// Close the database connection
db.close();
```

### Key Steps

1. **Open a Database Connection**: Use `Bun.sqlite.open()` to connect to your SQLite database.

2. **Begin Transaction**: Use `db.run('BEGIN TRANSACTION')` to start a new transaction.

3. **Execute Database Operations**: Perform your series of database operations, such as inserts, updates, or deletes.

4. **Commit Transaction**: If all operations succeed, finalize the transaction with `db.run('COMMIT')`.

5. **Rollback on Error**: If any operation fails, handle exceptions using a `try-catch` block, and rollback the transaction with `db.run('ROLLBACK')`.

6. **Close the Database**: Use `db.close()` to properly close the database connection when you're done.

### Notes

- Ensure that the database operations you're performing support transactions. Most modern databases including SQLite do.
- Transactions are powerful for maintaining data consistency, especially when dealing with multiple related operations that must all succeed or fail together.
- Always handle exceptions and ensure that resources are cleaned up properly, such as closing the database connection.

Error Handling
In Bun, as in other JavaScript runtimes, `try-catch` blocks are used to handle exceptions that might occur during the execution of code. Here are a few examples illustrating how to use `try-catch` blocks in Bun:

### Example 1: Basic Error Handling

```javascript
try {
  // Intentionally throwing an error
  throw new Error("Something went wrong!");
} catch (error) {
  console.error("Caught an error:", error.message);
} finally {
  console.log("Finally block executed.");
}
```

**Output:**
```
Caught an error: Something went wrong!
Finally block executed.
```

### Example 2: Handling Specific Error Types

```javascript
function parseJSON(jsonString) {
  try {
    const parsedData = JSON.parse(jsonString);
    console.log("Parsed data:", parsedData);
  } catch (error) {
    if (error instanceof SyntaxError) {
      console.error("JSON Syntax Error:", error.message);
    } else {
      console.error("Unexpected Error:", error);
    }
  }
}

parseJSON('{"valid": "json"}');  // Valid JSON
parseJSON("{invalid: json}");    // Invalid JSON
```

**Output:**
```
Parsed data: { valid: 'json' }
JSON Syntax Error: Unexpected token i in JSON at position 1
```

### Example 3: Promises with Try-Catch

When using asynchronous code and promises, `try-catch` alone won't handle errors unless you use `async/await`.

```javascript
async function fetchData(url) {
  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data = await response.json();
    console.log("Fetched data:", data);
  } catch (error) {
    console.error("Failed to fetch data:", error.message);
  }
}

fetchData('https://jsonplaceholder.typicode.com/posts/1');
```

### Example 4: Nested Try-Catch Blocks

```javascript
try {
  console.log("Outer try block");

  try {
    console.log("Inner try block");
    throw new Error("Error in inner block");
  } catch (innerError) {
    console.error("Caught an error in inner catch:", innerError.message);
  }

  throw new Error("Error in outer block");
} catch (outerError) {
  console.error("Caught an error in outer catch:", outerError.message);
} finally {
  console.log("Executed final cleanup.");
}
```

**Output:**
```
Outer try block
Inner try block
Caught an error in inner catch: Error in inner block
Caught an error in outer catch: Error in outer block
Executed final cleanup.
```

These examples demonstrate how to use `try-catch` for error handling in various scenarios, such as simple errors, handling specific error types, working with asynchronous calls using `async/await`, and structured error handling with nested `try-catch` blocks.

In Bun JavaScript runtime, handling exceptions is similar to other JavaScript environments, but there are some specifics and optimizations offered by Bun. Below is a comprehensive guide on how to work with exception handling in Bun:

### Try-Catch-Finally

The standard way to handle exceptions in JavaScript is through the use of `try`, `catch`, and `finally` blocks. Bun supports these constructs as well:

```javascript
try {
  // Code that may throw an error
  riskyOperation();
} catch (error) {
  // Code to handle the error
  console.error("An error occurred:", error);
} finally {
  // Code that runs regardless of whether an error occurred or not
  cleanup();
}
```

### Throwing Exceptions

You can throw exceptions using the `throw` statement. This is identical to other JavaScript environments:

```javascript
function riskyOperation() {
  if (somethingWentWrong) {
    throw new Error("Something went wrong!");
  }
}

try {
  riskyOperation();
} catch (error) {
  console.error("Caught an error:", error);
}
```

### Custom Error Types

Creating custom error types can help you handle specific error scenarios more gracefully. Here’s how you can define and use a custom error type:

```javascript
class MyCustomError extends Error {
  constructor(message) {
    super(message);
    this.name = "MyCustomError";
  }
}

function anotherRiskyOperation() {
  if (anotherProblem) {
    throw new MyCustomError("A custom error occurred!");
  }
}

try {
  anotherRiskyOperation();
} catch (error) {
  if (error instanceof MyCustomError) {
    console.error("Caught a custom error:", error);
  } else {
    console.error("Caught a general error:", error);
  }
}
```

### Asynchronous Error Handling

For asynchronous operations, you can handle errors using `.catch()` for promises or `try...catch` within `async/await` constructs:

#### Promises

```javascript
doSomethingAsync()
  .then(result => {
    // Handle successful result
  })
  .catch(error => {
    // Handle error
    console.error("Promise error:", error);
  });
```

#### Async/Await

```javascript
async function performAsyncTask() {
  try {
    const result = await doSomethingAsync();
    // Use the result
  } catch (error) {
    console.error("Async error:", error);
  }
}

performAsyncTask();
```

### Bun-Specific Details

Bun is designed to be fast and efficient, offering improved performance for common operations, including exception handling. However, the general approach to working with exceptions remains similar to standard JavaScript practices. Bun aims to optimize these operations under the hood, ensuring that exception handling doesn't become a bottleneck.

By following these standard practices for exception handling, you can effectively manage errors in your Bun applications while benefiting from Bun's performance enhancements.

Creating and using custom error classes in Bun's JavaScript runtime follows the same principles as in any JavaScript environment. Here's how you can define and work with custom error classes:

```javascript
// Define a custom error class by extending the built-in Error class
class CustomError extends Error {
  constructor(message) {
    // Pass the message to the parent Error class
    super(message);

    // Set the name property to help with identification
    this.name = this.constructor.name;

    // Maintain correct stack trace for where the error was thrown (only works in V8 runtime)
    if (typeof Error.captureStackTrace === 'function') {
      Error.captureStackTrace(this, this.constructor);
    }
  }
}

// Define another custom error class for demonstration
class NotFoundError extends CustomError {
  constructor(resource) {
    // Construct a suitable error message
    const message = `${resource} was not found.`;
    // Call the parent constructor with the message
    super(message);

    // You can add additional properties if needed
    this.resource = resource;
  }
}

// Example function that might throw a CustomError
function fetchData(key) {
  if (key === 'invalid') {
    throw new CustomError('Invalid key provided');
  } else if (key === 'missingResource') {
    throw new NotFoundError('Resource');
  }

  return { data: 'some data' }; // Simulated data retrieval
}

// Using the custom error classes
try {
  // Attempt to fetch data with an invalid key
  const data = fetchData('invalid');
  console.log(data);
} catch (error) {
  if (error instanceof NotFoundError) {
    console.error('Handling NotFoundError:', error.message);
  } else if (error instanceof CustomError) {
    console.error('Handling CustomError:', error.message);
  } else {
    console.error('An unexpected error occurred:', error.message);
  }
}

try {
  // Attempt to fetch data with a missing resource
  const data = fetchData('missingResource');
  console.log(data);
} catch (error) {
  if (error instanceof NotFoundError) {
    console.error('Handling NotFoundError:', error.message);
  } else if (error instanceof CustomError) {
    console.error('Handling CustomError:', error.message);
  } else {
    console.error('An unexpected error occurred:', error.message);
  }
}
```

In this example:

1. **CustomError**: A basic custom error class that extends the built-in `Error` class. It sets the name of the error to the class name for easier identification.

2. **NotFoundError**: Extends `CustomError` to represent a more specific error type. It includes an additional `resource` property to indicate which resource was not found.

3. **Error Handling**: The `try-catch` blocks show how you can catch and handle these specific error types, providing more detailed error handling logic depending on the error class.

This approach allows for clearer, more maintainable code, especially when dealing with complex applications that require detailed error management. Use custom errors to encapsulate specific error scenarios, providing clearer debugging information and better handling at runtime.

Here's how you can use `finally` blocks in the Bun JavaScript runtime. A `finally` block is often used to execute code after a `try` block, regardless of whether an exception was thrown or not. This can be useful for cleaning up resources or ensuring certain code runs.

Here are some examples:

### Example 1: Basic Usage of finally
```javascript
try {
  console.log("Try block: executing some code");
  // Simulating an error
  if (Math.random() > 0.5) {
    throw new Error("An error occurred.");
  }
  console.log("Try block: completed without error");
} catch (err) {
  console.error("Catch block: caught an error", err);
} finally {
  console.log("Finally block: This runs regardless of try/catch outcome");
}
```

### Example 2: Resource Management
```javascript
function manageResource() {
  let resource = null;
  try {
    console.log("Allocating resource");
    resource = {name: "Resource"}; // Simulating resource allocation

    // Perform operations with the resource
    console.log("Using resource");

    if (Math.random() < 0.5) {
      throw new Error("Error while using the resource");
    }

    console.log("Resource used successfully");
  } catch (err) {
    console.error("Error occurred during resource management:", err);
  } finally {
    // Clean up the resource
    if (resource) {
      console.log("Cleaning up the resource");
      resource = null; // Simulating resource deallocation
    }
    console.log("Finally block executed");
  }
}

manageResource();
```

### Example 3: Completing Async Operations
Although `finally` doesn't wait for any pending async operations within its block, it's often used with promises to perform cleanup:
```javascript
async function fetchData() {
  try {
    console.log("Fetching data...");
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log("Data fetched:", data);
  } catch (err) {
    console.error("Failed to fetch data:", err);
  } finally {
    console.log("Finished attempting to fetch data");
  }
}

fetchData();
```

### Example 4: Using with Promise chain
```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log("Data received:", data);
  })
  .catch(error => {
    console.error("Error fetching data:", error);
  })
  .finally(() => {
    console.log("Finally block: This runs after the Promise chain, regardless of outcome");
  });
```

In these examples, the `finally` block is used to output messages indicating that it is executed, or to perform some cleanup tasks, regardless of the success or failure of the preceding code. This demonstrates its utility in ensuring certain parts of your code are run, such as releasing resources or logging completion, no matter what happens in the `try` or `catch`.

Using error messages and logs effectively is crucial for understanding and debugging your applications during development and in production. Here’s how you can use them in the Bun JavaScript runtime:

### Using Logs

Bun has some built-in utilities for logging. Use `console.log()`, `console.info()`, `console.warn()`, and `console.error()` to log messages at various levels.

#### Example: Simple Logging

```javascript
// Basic usage of console logging
console.log("This is a log message");
console.info("This is an info message");
console.warn("This is a warning message");
console.error("This is an error message");
```

Logs can help you trace the flow of execution and understand what's happening in your code.

### Using Error Messages

Handling errors gracefully and providing informative error messages can help diagnose issues quickly. You can create custom errors or use built-in ones.

#### Example: Using try-catch for Error Handling

```javascript
function divide(a, b) {
  if (b === 0) {
    throw new Error("Division by zero is not allowed");
  }
  return a / b;
}

try {
  const result = divide(10, 0);
  console.log("Result:", result);
} catch (error) {
  console.error("Error occurred:", error.message);
}
```

In this example, we throw an error when an illegal operation is attempted and catch it to log an appropriate message.

#### Example: Custom Error Classes

Creating custom error classes can help encapsulate error-specific information and make error handling more robust.

```javascript
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}

function validateInput(input) {
  if (!input) {
    throw new ValidationError("Input cannot be empty");
  }
}

try {
  validateInput("");
} catch (error) {
  if (error instanceof ValidationError) {
    console.error("Validation Error:", error.message);
  } else {
    console.error("Unexpected Error:", error);
  }
}
```

Custom error classes like `ValidationError` provide a clean way to handle different types of errors selectively.

### Using BUN.run() to Manage Logs in Bun

Bun provides `bun run` for running scripts, which can help manage logs more effectively.

#### Example: Running a Script with Bun

Create a script file named `example.js` with log statements and error handling:

```javascript
// example.js

console.log("Script started");

try {
  // Some code that might throw
  throw new Error("This is a test error");
} catch (error) {
  console.error("Caught an error:", error.message);
}

console.log("Script ended");
```

Run the script using Bun:

```sh
bun run example.js
```

Executing the script with Bun will display the logs and errors in the console, helping you trace the execution flow and understand any issues that arise.

By effectively using logs and error messages, you can enhance your ability to debug and monitor applications running with Bun.

File Input/Output
In the Bun JavaScript runtime, you can easily read and write text files using the built-in `fs` module. Here's a quick guide on how to do both:

### Reading Text Files

To read a text file, you can use the `fs.readFile` or `fs.readFileSync` method, depending on whether you prefer asynchronous or synchronous operation.

#### Asynchronously

```javascript
import { promises as fs } from 'bun:fs';

async function readTextFile(filePath) {
  try {
    const data = await fs.readFile(filePath, 'utf-8');
    console.log(data);
  } catch (error) {
    console.error('Error reading file:', error);
  }
}

readTextFile('./example.txt');
```

#### Synchronously

```javascript
import { readFileSync } from 'bun:fs';

function readTextFileSync(filePath) {
  try {
    const data = readFileSync(filePath, 'utf-8');
    console.log(data);
  } catch (error) {
    console.error('Error reading file:', error);
  }
}

readTextFileSync('./example.txt');
```

### Writing Text Files

To write to a text file, you can use `fs.writeFile` or `fs.writeFileSync`:

#### Asynchronously

```javascript
import { promises as fs } from 'bun:fs';

async function writeTextFile(filePath, content) {
  try {
    await fs.writeFile(filePath, content, 'utf-8');
    console.log('File written successfully');
  } catch (error) {
    console.error('Error writing file:', error);
  }
}

writeTextFile('./example.txt', 'Hello, Bun!');
```

#### Synchronously

```javascript
import { writeFileSync } from 'bun:fs';

function writeTextFileSync(filePath, content) {
  try {
    writeFileSync(filePath, content, 'utf-8');
    console.log('File written successfully');
  } catch (error) {
    console.error('Error writing file:', error);
  }
}

writeTextFileSync('./example.txt', 'Hello, Bun!');
```

### Important Notes

- Always handle potential errors using try-catch blocks, especially with synchronous operations to prevent your application from crashing.
- The file encoding 'utf-8' is specified to ensure the text is handled correctly for reading and writing.
- Asynchronous operations are generally preferred for I/O operations to avoid blocking the event loop, which is critical in a scalable application. However, synchronous operations can be useful for simple scripts or situations where you need to maintain a specific order of execution.

That's it! You can use these methods to manage text files in the Bun JavaScript runtime.

Working with binary files in the Bun JavaScript runtime involves reading and writing binary data using built-in APIs. Here are a few examples to demonstrate how you can handle binary files in Bun:

### Reading a Binary File

To read a binary file, you can use the `Bun.file()` method along with `arrayBuffer()`. Here's an example:

```javascript
async function readBinaryFile(filePath) {
  try {
    // Open the binary file
    const file = Bun.file(filePath);

    // Read the file as an ArrayBuffer
    const arrayBuffer = await file.arrayBuffer();

    // Create a Uint8Array to work with the binary data
    const data = new Uint8Array(arrayBuffer);

    // Process the binary data
    console.log("Binary data:", data);
  } catch (error) {
    console.error("Error reading binary file:", error);
  }
}

readBinaryFile("./path/to/your/binaryfile.bin");
```

### Writing to a Binary File

To write binary data to a file, you can create a `Uint8Array` and use `Bun.write()`. Here's an example:

```javascript
async function writeBinaryFile(filePath, data) {
  try {
    // Write the binary data to the file
    await Bun.write(filePath, new Uint8Array(data));

    console.log("Binary file written successfully!");
  } catch (error) {
    console.error("Error writing binary file:", error);
  }
}

// Example binary data
const binaryData = [0x00, 0xFF, 0xAA, 0xBB, 0xCC];

writeBinaryFile("./path/to/your/outputfile.bin", binaryData);
```

### Converting Text to Binary and Writing to a File

If you need to convert text to binary data before writing it, you can use `TextEncoder`. Here’s an example:

```javascript
async function writeTextAsBinary(filePath, text) {
  try {
    // Encode the text as binary data
    const encoder = new TextEncoder();
    const binaryData = encoder.encode(text);

    // Write the binary data to the file
    await Bun.write(filePath, binaryData);

    console.log("Text written as binary successfully!");
  } catch (error) {
    console.error("Error writing text as binary:", error);
  }
}

writeTextAsBinary("./path/to/your/textbinaryfile.bin", "Hello, Bun!");
```

These examples demonstrate basic binary file operations in Bun, covering reading, writing, and encoding text to binary. Adjust the file paths as needed for your environment.

Certainly! Let me show you examples that demonstrate how to work with CSV and JSON file formats using the Bun JavaScript runtime.

### Working with a JSON File
**Reading and Writing JSON files**

```javascript
import { readFileSync, writeFileSync } from 'fs';

// Reading JSON file
const jsonData = readFileSync('data.json', 'utf8');
const jsonObj = JSON.parse(jsonData);

console.log('Read JSON:', jsonObj);

// Modifying the JSON data
jsonObj.newKey = 'newValue';

// Writing to JSON file
writeFileSync('data.json', JSON.stringify(jsonObj, null, 2));
console.log('Updated JSON written to file');
```

### Working with a CSV File
To handle CSV files, you will often require a library to parse and stringify data, as the CSV format is not natively supported in Bun. One popular library for this purpose is `papaparse`.

**Reading and Writing CSV files**

Firstly, install `papaparse`:

```bash
bun add papaparse
```

```javascript
import Papa from 'papaparse';
import { readFileSync, writeFileSync } from 'fs';

// Reading CSV file
const csvData = readFileSync('data.csv', 'utf8');
const parsedData = Papa.parse(csvData, { header: true });

console.log('Parsed CSV Data:', parsedData.data);

// Modifying the CSV data
const modifiedData = parsedData.data.map(row => {
  return { ...row, newColumn: 'newValue' };
});

// Converting JSON data back to CSV
const csvString = Papa.unparse(modifiedData);

// Writing to CSV file
writeFileSync('data.csv', csvString);
console.log('Updated CSV written to file');
```

### Summary
- For JSON files, you can easily use the `fs` module to read and write JSON data with `JSON.parse()` and `JSON.stringify()`.
- For CSV files, using a library like `papaparse` can simplify the process of parsing and stringifying CSV data.

These examples assume you have respective `data.json` and `data.csv` files available in the same directory as your script. Make sure to adjust file paths as necessary for your specific use case.

In Bun, handling file streams is quite similar to Node.js, but there are some differences in the API and behavior. Bun aims to provide better performance and DX (developer experience). Here's how you can work with file streams using Bun:

### Reading from a File Stream

To read from a file stream in Bun, you can use the built-in `fs` module and methods like `createReadStream`.

```javascript
import { createReadStream } from 'fs';

// Create a read stream for a file
const readStream = createReadStream('./example.txt', { encoding: 'utf-8' });

// Listen for 'data' events to read in chunks
readStream.on('data', (chunk) => {
  console.log('Received chunk: ', chunk);
});

// Listen for the 'end' event to know when the file is fully read
readStream.on('end', () => {
  console.log('Finished reading file.');
});

// Handle errors
readStream.on('error', (err) => {
  console.error('Error reading file:', err);
});
```

### Writing to a File Stream

To write to a file stream, you can use the `createWriteStream` method.

```javascript
import { createWriteStream } from 'fs';

// Create a write stream to a file
const writeStream = createWriteStream('./output.txt', { encoding: 'utf-8' });

// Write some data to the file
writeStream.write('Hello, world!\n', 'utf-8');

// You can write more data or pipe from another stream
writeStream.write('Appending more text...\n', 'utf-8');

// Close the stream when done
writeStream.end(() => {
  console.log('Finished writing to file.');
});

// Handle errors
writeStream.on('error', (err) => {
  console.error('Error writing to file:', err);
});
```

### Piping Streams

You can also pipe streams, which is a common use case for transforming data as it moves from one stream to another, such as reading from a file and writing to another.

```javascript
import { createReadStream, createWriteStream } from 'fs';

// Create a read stream and a write stream
const sourceStream = createReadStream('./example.txt');
const destinationStream = createWriteStream('./output.txt');

// Pipe the read stream into the write stream
sourceStream.pipe(destinationStream);

// Listen for 'finish' event on the write stream
destinationStream.on('finish', () => {
  console.log('Successfully copied file contents.');
});

// Handle errors on both streams
sourceStream.on('error', (err) => {
  console.error('Error reading source file:', err);
});
destinationStream.on('error', (err) => {
  console.error('Error writing to destination file:', err);
});
```

These examples demonstrate basic file stream operations in Bun, including reading from and writing to files, handling errors, and stream piping. Bun builds on Node.js concepts but is designed for performance, so its behavior is optimized for real-world performance scenarios.

In Bun, you can use the `fs` module for file I/O operations, similar to Node.js. When performing file I/O operations, it's important to handle exceptions to ensure your application can manage errors gracefully. Here's how you can perform file I/O with exception handling in Bun:

### Reading a File

To read a file while handling exceptions, you can use the `fs.readFileSync` method wrapped in a `try-catch` block:

```javascript
import * as fs from 'bun:fs';

try {
  const data = fs.readFileSync('example.txt', 'utf8');
  console.log(data);
} catch (error) {
  console.error('Error reading the file:', error.message);
}
```

### Writing to a File

To write to a file and handle potential errors, use the `fs.writeFileSync` method:

```javascript
import * as fs from 'bun:fs';

try {
  fs.writeFileSync('example.txt', 'Hello, Bun!', 'utf8');
  console.log('File written successfully');
} catch (error) {
  console.error('Error writing to the file:', error.message);
}
```

### Using Asynchronous Methods

If you prefer asynchronous operations, you can use the `fs.promises` API along with `async/await` for cleaner error handling:

#### Reading a File Asynchronously

```javascript
import * as fs from 'bun:fs/promises';

async function readFile() {
  try {
    const data = await fs.readFile('example.txt', 'utf8');
    console.log(data);
  } catch (error) {
    console.error('Error reading the file:', error.message);
  }
}

readFile();
```

#### Writing to a File Asynchronously

```javascript
import * as fs from 'bun:fs/promises';

async function writeFile() {
  try {
    await fs.writeFile('example.txt', 'Hello, Bun!', 'utf8');
    console.log('File written successfully');
  } catch (error) {
    console.error('Error writing to the file:', error.message);
  }
}

writeFile();
```

### Key Points

1. **Synchronous vs Asynchronous**: Use the synchronous methods (`readFileSync`, `writeFileSync`) when dealing with smaller files or when the simplicity of synchronous code benefits your application. For non-blocking operations, prefer asynchronous methods with `fs.promises`.

2. **Error Handling**: Always wrap file I/O operations in `try-catch` blocks to handle errors such as file not found, permission issues, or invalid path.

3. **Encoding**: Specify the encoding (e.g., `'utf8'`) when dealing with text files to ensure proper encoding and decoding of file contents.

By handling exceptions properly, you enhance the robustness and reliability of your application when performing file I/O operations.

Functions and Methods
In Bun JavaScript runtime, you can define and call functions similarly to how you do in Node.js or browser-based JavaScript. Below are some examples demonstrating different ways to define and call functions in Bun.

### Example 1: Function Declaration

```javascript
// Function Declaration
function greet(name) {
    return `Hello, ${name}!`;
}

// Calling the function
const greeting = greet('Alice');
console.log(greeting); // Output: Hello, Alice!
```

### Example 2: Function Expression

```javascript
// Function Expression
const add = function(x, y) {
    return x + y;
};

// Calling the function
const sum = add(5, 7);
console.log(sum); // Output: 12
```

### Example 3: Arrow Function

```javascript
// Arrow Function
const multiply = (a, b) => a * b;

// Calling the function
const product = multiply(4, 6);
console.log(product); // Output: 24
```

### Example 4: Immediately Invoked Function Expression (IIFE)

```javascript
// IIFE
(function() {
    console.log('This function runs immediately!');
})();

// Output: This function runs immediately!
```

### Example 5: Functions with Default Parameters

```javascript
// Function with Default Parameter
function logMessage(message, prefix = 'Info:') {
    console.log(`${prefix} ${message}`);
}

// Calling the function with and without the default parameter
logMessage('Server started'); // Output: Info: Server started
logMessage('User logged in', 'Alert:'); // Output: Alert: User logged in
```

### Example 6: Asynchronous Function with Async/Await

```javascript
// Asynchronous Function
async function fetchData(url) {
    try {
        const response = await fetch(url);
        const data = await response.json();
        return data;
    } catch (error) {
        console.error('Error fetching data:', error);
    }
}

// Calling the asynchronous function
fetchData('https://api.example.com/data')
    .then(data => {
        console.log(data);
    });
```

These examples showcase basic usage of functions in Bun, which aligns with standard JavaScript practices. Bun, being a modern JavaScript runtime, supports all these function types, making it easy for you to write modular and reusable code.

In Bun's JavaScript runtime, working with function arguments is similar to how you would handle them in any JavaScript environment, given that Bun is designed to be compatible with modern JavaScript standards. Below are some key aspects of working with function arguments in Bun:

1. **Default Parameters:**
   JavaScript allows you to set default values for function parameters, which will be used if no argument is provided or if `undefined` is explicitly passed.

   ```javascript
   function greet(name = 'World') {
     console.log(`Hello, ${name}!`);
   }

   greet(); // Hello, World!
   greet('Bun'); // Hello, Bun!
   ```

2. **Rest Parameters:**
   You can gather all remaining arguments into an array using the rest parameter syntax. This is useful for functions that accept a variable number of arguments.

   ```javascript
   function sum(...numbers) {
     return numbers.reduce((total, num) => total + num, 0);
   }

   console.log(sum(1, 2, 3, 4)); // 10
   ```

3. **The `arguments` Object:**
   For traditional function syntax, you can access the `arguments` object within a function. It is array-like but not a real array, holding all the arguments passed to the function.

   ```javascript
   function showArguments() {
     console.log(arguments);
   }

   showArguments('a', 'b', 'c'); // [Arguments] { '0': 'a', '1': 'b', '2': 'c' }
   ```

   Note that the `arguments` object is not available in arrow functions.

4. **Object Destructuring:**
   You can use destructuring to extract properties from objects passed as arguments directly.

   ```javascript
   function createUser({ name, age }) {
     console.log(`Name: ${name}, Age: ${age}`);
   }

   createUser({ name: 'Alice', age: 25 }); // Name: Alice, Age: 25
   ```

5. **Array Destructuring:**
   Similarly, array destructuring can be used for extracting values from arrays.

   ```javascript
   function swap([first, second]) {
     return [second, first];
   }

   console.log(swap([1, 2])); // [2, 1]
   ```

6. **Arrow Functions and Parameters:**
   Arrow functions provide a concise syntax for defining functions and can work with arguments similarly, though they do not have the `arguments` object.

   ```javascript
   const add = (a, b) => a + b;

   console.log(add(5, 3)); // 8
   ```

These features make working with function arguments in Bun's JavaScript runtime flexible and powerful, enabling developers to write readable and maintainable code.

In Bun's JavaScript runtime, just like in standard JavaScript, you can use default and optional function arguments. Here's how you can utilize them:

### Default Arguments

Default arguments are used to specify a default value for a parameter if no argument is provided when the function is called.

```javascript
function greet(name = "World") {
  console.log(`Hello, ${name}!`);
}

// Using the default value
greet(); // Output: Hello, World!

// Overriding the default value
greet("Alice"); // Output: Hello, Alice!
```

### Optional Arguments

JavaScript functions inherently support optional arguments, as any missing arguments will be `undefined`. You can design your function to handle these optional arguments:

```javascript
function introduce(firstName, lastName) {
  if (lastName === undefined) {
    console.log(`Hi, I'm ${firstName}.`);
  } else {
    console.log(`Hi, I'm ${firstName} ${lastName}.`);
  }
}

// Providing both arguments
introduce("John", "Doe"); // Output: Hi, I'm John Doe.

// Leaving the lastName argument optional
introduce("Jane"); // Output: Hi, I'm Jane.
```

### Combining Default and Optional Arguments

You can combine both concepts, using default values for some arguments while allowing others to remain optional:

```javascript
function configureSettings(width = 800, height = 600, color) {
  if (color === undefined) {
    console.log(`Settings: ${width}x${height}, default color`);
  } else {
    console.log(`Settings: ${width}x${height}, color: ${color}`);
  }
}

// Using default width and height, with optional color
configureSettings(); // Output: Settings: 800x600, default color

// Overriding defaults and providing color
configureSettings(1024, 768, "blue"); // Output: Settings: 1024x768, color: blue

// Overriding defaults without color
configureSettings(1024, 768); // Output: Settings: 1024x768, default color
```

These examples show how you can define functions with default and optional parameters in Bun's JavaScript runtime, making your functions more flexible and easier to use.

In the Bun JavaScript runtime, you can leverage return values similar to how you would in other modern JavaScript environments. Below are some examples demonstrating how return values can be utilized:

### Basic Function Return
```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

const message = greet("Alice");
console.log(message); // Output: Hello, Alice!
```

### Using Arrow Functions
```javascript
const square = (x) => x * x;

console.log(square(5)); // Output: 25
```

### Return in Asynchronous Functions
```javascript
async function fetchData(url) {
  const response = await fetch(url);
  return response.json();
}

fetchData('https://api.example.com/data')
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error('Error:', error);
  });
```

### Return in Generators
```javascript
function* numberGenerator() {
  yield 1;
  yield 2;
  return 3;
}

const generator = numberGenerator();

console.log(generator.next()); // Output: { value: 1, done: false }
console.log(generator.next()); // Output: { value: 2, done: false }
console.log(generator.next()); // Output: { value: 3, done: true }
```

### Returning Objects
```javascript
function createUser(name, age) {
  return {
    name: name,
    age: age,
    isActive: true
  };
}

const user = createUser("John", 25);
console.log(user); // Output: { name: 'John', age: 25, isActive: true }
```

### Using Return Values in Array Methods
```javascript
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map(num => num * 2);

console.log(doubled); // Output: [2, 4, 6, 8, 10]
```

These examples demonstrate how return values can be applied in various scenarios in Bun's JavaScript runtime. You can return primitives, objects, execute async operations, use generators, and manipulate arrays.

Bun, like Node.js, runs JavaScript on the server and supports the use of lambda functions (or arrow functions) in various scenarios. Arrow functions in JavaScript are a compact way to write anonymous functions. Here are some examples of using arrow functions in Bun JavaScript runtime:

1. **Basic Arrow Function**

```javascript
const greet = (name) => `Hello, ${name}!`;

console.log(greet("Bun")); // Output: Hello, Bun!
```

2. **Arrow Function with Multiple Parameters**

```javascript
const add = (a, b) => a + b;

console.log(add(5, 3)); // Output: 8
```

3. **Arrow Function with No Parameters**

```javascript
const sayHello = () => console.log("Hello, World!");

sayHello(); // Output: Hello, World!
```

4. **Arrow Function in Array Methods**

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map(num => num * 2);

console.log(doubled); // Output: [2, 4, 6, 8, 10]
```

5. **Arrow Function as an Event Handler**

```javascript
const button = document.createElement('button');
button.innerText = 'Click me';
document.body.appendChild(button);

button.addEventListener('click', (event) => {
    console.log('Button clicked!', event);
});
```

6. **Arrow Function Returning an Object Literal**

```javascript
const createPerson = (name, age) => ({ name, age });

const person = createPerson("Alice", 30);
console.log(person); // Output: { name: 'Alice', age: 30 }
```

7. **Using Arrow Functions for Promises**

```javascript
const fetchData = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => resolve("Data fetched"), 1000);
    });
};

fetchData().then(data => console.log(data)); // Output after 1 second: Data fetched
```

These examples should work seamlessly in the Bun runtime for JavaScript, as they are standard JavaScript features. Remember that Bun aims to be compatible with most existing JavaScript code, especially code that runs on Node.js.

Networking and Web Development
Certainly! Bun is a fast JavaScript runtime like Node.js and Deno but comes with some built-in utilities and APIs. As of the latest versions, you can use the standard Fetch API to make HTTP requests in Bun because it provides a built-in version of the Fetch API, which is similar to the one found in browsers. Here are some examples of how to use HTTP requests in Bun using `fetch`:

### Basic GET Request

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}

fetchData();
```

### POST Request with JSON Body

```javascript
async function postData() {
  const dataToSend = { name: 'John Doe', age: 25 };

  try {
    const response = await fetch('https://api.example.com/users', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify(dataToSend),
    });

    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    
    const responseData = await response.json();
    console.log('Response:', responseData);
  } catch (error) {
    console.error('Error posting data:', error);
  }
}

postData();
```

### Handling Different Response Types

```javascript
async function fetchDataTypes() {
  try {
    const response = await fetch('https://api.example.com/data');
    
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }

    // Example handling JSON response
    const jsonData = await response.json();
    console.log('JSON Data:', jsonData);

    // Example handling text response
    const textData = await response.text();
    console.log('Text Data:', textData);

    // Example handling Blob data (binary data)
    const blobData = await response.blob();
    console.log('Blob Data:', blobData);

  } catch (error) {
    console.error('Error fetching data:', error);
  }
}

fetchDataTypes();
```

### Using Query Parameters

```javascript
async function fetchWithQuery() {
  const params = new URLSearchParams({
    search: 'JavaScript',
    limit: 10,
  });

  try {
    const response = await fetch(`https://api.example.com/search?${params}`);
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data = await response.json();
    console.log('Search Results:', data);
  } catch (error) {
    console.error('Error fetching search results:', error);
  }
}

fetchWithQuery();
```

These examples demonstrate how to use the Fetch API in the Bun JavaScript runtime to perform different types of HTTP operations. The syntax and usage are very similar to how you'd use `fetch` in a browser environment.

To work with WebSockets in the Bun JavaScript runtime, you can use Bun's built-in WebSocket support similar to how you'd work with WebSockets in a standard browser or server environment like Node.js. Here's a basic guide on how to set up a WebSocket server and client using Bun:

### Setting Up a WebSocket Server

1. **Create a WebSocket Server:**

   First, you need to create a WebSocket server using Bun's API. This involves setting up a server that listens for incoming WebSocket connections and handles messages.

   ```javascript
   const { listen } = require('bun');

   const server = listen({
     port: 8080,  // Port number where the server will listen
     fetch(req) {
       const upgradeHeader = req.headers.get('Upgrade');

       if (upgradeHeader !== 'websocket') {
         return new Response('Upgrade Required', { status: 426 });
       }

       // Accept the WebSocket connection
       const { socket, response } = Deno.upgradeWebSocket(req);

       // Set up event handlers for the WebSocket
       socket.onopen = () => {
         console.log('WebSocket connection opened.');
       };

       socket.onmessage = (event) => {
         console.log('Received message:', event.data);
         socket.send(`Echo: ${event.data}`);
       };

       socket.onclose = () => {
         console.log('WebSocket connection closed.');
       };

       socket.onerror = (error) => {
         console.error('WebSocket error:', error);
       };

       return response;
     }
   });

   console.log('WebSocket server running on ws://localhost:8080');
   ```

2. **Run the Server:**

   Save the server code to a file, say `server.js`, and run it using Bun with the command:

   ```sh
   bun server.js
   ```

### Setting Up a WebSocket Client

1. **Create a WebSocket Client:**

   You can create a WebSocket client that connects to the server you set up, sends messages, and handles incoming messages.

   ```javascript
   const ws = new WebSocket('ws://localhost:8080');

   ws.onopen = () => {
     console.log('Connected to the WebSocket server');
     ws.send('Hello, Server!');
   };

   ws.onmessage = (event) => {
     console.log('Received from server:', event.data);
   };

   ws.onclose = () => {
     console.log('Disconnected from the WebSocket server');
   };

   ws.onerror = (error) => {
     console.error('WebSocket error:', error);
   };
   ```

2. **Run the Client:**

   Save the client code to a file, say `client.js`, and run it using Bun with the command:

   ```sh
   bun client.js
   ```

### Key Points to Remember

- **WebSocket Server:** You need to handle the upgrade request, establish the WebSocket connection, and manage incoming and outgoing WebSocket events such as `onopen`, `onmessage`, `onclose`, and `onerror`.
- **WebSocket Client:** Similar to the server, set up event handlers to manage connection states and message exchanges.
- **Port Number:** Ensure the port number used by the WebSocket server matches the one the client is connecting to.

By following these steps, you can effectively set up and manage WebSocket connections in the Bun JavaScript runtime, allowing real-time communication between clients and server.

As of my last update in October 2023, Bun is a modern JavaScript runtime that supports many Node.js APIs, enabling it to use existing Node.js modules. When it comes to protocols like FTP, SFTP, and SSH, there are well-established Node.js libraries that can be used with Bun.

Here's how you can handle each protocol:

### FTP using `basic-ftp`

To use FTP in Bun, you can utilize the `basic-ftp` library, a straightforward and promise-based library for FTP connections.

First, ensure you have `basic-ftp` installed:
```bash
bun add basic-ftp
```

Then, use it in your Bun runtime code:
```javascript
import ftp from 'basic-ftp';

async function ftpExample() {
    const client = new ftp.Client();
    try {
        await client.access({
            host: 'your-ftp-host',
            user: 'your-username',
            password: 'your-password',
            secure: true // set to false if not using FTPS
        });

        console.log(await client.list());

        // Example of downloading a file
        await client.downloadTo("local-file.txt", "remote-file.txt");
    } catch (err) {
        console.error(err);
    } finally {
        client.close();
    }
}

ftpExample();
```

### SFTP using `ssh2-sftp-client`

To handle SFTP, you can use the `ssh2-sftp-client` library, which wraps around `ssh2` to provide a simple promise-based interface for SFTP operations.

First, install the package:
```bash
bun add ssh2-sftp-client
```

Then, utilize it in your Bun code:
```javascript
import SftpClient from 'ssh2-sftp-client';

async function sftpExample() {
    const sftp = new SftpClient();

    try {
        await sftp.connect({
            host: 'your-sftp-host',
            username: 'your-username',
            password: 'your-password'
            // You can also use a private key:
            // privateKey: require('fs').readFileSync('/path/to/private/key')
        });

        console.log(await sftp.list('/remote-directory'));

        // Example of downloading a file
        await sftp.get('/remote-file.txt', 'local-file.txt');
    } catch (err) {
        console.error(err);
    } finally {
        await sftp.end();
    }
}

sftpExample();
```

### SSH using `node-ssh`

For SSH operations, you can use the `node-ssh` library to execute commands on remote servers through SSH.

First, install the `node-ssh` package:
```bash
bun add node-ssh
```

Then, execute SSH commands using the following code:
```javascript
import { NodeSSH } from 'node-ssh';

async function sshExample() {
    const ssh = new NodeSSH();

    try {
        await ssh.connect({
            host: 'your-ssh-host',
            username: 'your-username',
            password: 'your-password'
            // You can also use a private key:
            // privateKey: '/path/to/private/key'
        });

        const result = await ssh.execCommand('ls -l', { cwd: '/remote-directory' });
        console.log('STDOUT: ' + result.stdout);
        console.log('STDERR: ' + result.stderr);
    } catch (err) {
        console.error(err);
    } finally {
        ssh.dispose();
    }
}

sshExample();
```

These examples illustrate how to use each protocol within the Bun JavaScript runtime by leveraging existing Node.js libraries that provide FTP/SFTP/SSH functionalities. Make sure to adapt the examples with your actual host, username, password, and file paths.

Certainly! Below are examples of how you can handle XML and JSON data with web services using the Bun JavaScript runtime. These examples demonstrate how to perform HTTP requests to a web service and process the responses.

### JSON Example

Let's assume you are working with a web service that returns JSON data. Here's how you could fetch and process it using Bun's `fetch` API:

```javascript
// JSON Example: Fetch data from a web service and process it

async function fetchJsonData() {
  const response = await fetch('https://api.example.com/data.json');

  if (!response.ok) {
    throw new Error('Network response was not ok');
  }

  const jsonData = await response.json();
  
  console.log('JSON Data:', jsonData);
  // Process the JSON data as needed
}

fetchJsonData().catch(console.error);
```

### XML Example

Now, let's consider an example of interacting with a web service that returns XML data. You'll need to parse the XML into a usable format, which can be done using DOMParser.

```javascript
// XML Example: Fetch data from a web service and process it

async function fetchXmlData() {
  const response = await fetch('https://api.example.com/data.xml');

  if (!response.ok) {
    throw new Error('Network response was not ok');
  }

  const xmlText = await response.text();
  
  // Parse the XML using DOMParser
  const parser = new DOMParser();
  const xmlDoc = parser.parseFromString(xmlText, 'application/xml');
  
  console.log('XML Data:', xmlDoc);

  // Example: Extract data from the XML
  // Assuming XML structure like <response><item>...</item></response>
  const items = xmlDoc.querySelectorAll('item');
  items.forEach(item => {
    console.log('Item:', item.textContent);
  });
}

fetchXmlData().catch(console.error);
```

### Additional Considerations

- **Error Handling**: Always ensure you have proper error handling around your network calls to gracefully manage issues like network failures or API errors.
  
- **CORS**: If you are making requests to a service that is hosted on a different domain, ensure that CORS (Cross-Origin Resource Sharing) is properly configured on the server to allow your domain to fetch the resources.

- **Security**: When dealing with XML, be cautious of vulnerabilities such as XML External Entity (XXE) attacks. Always validate and sanitize any data that is processed.

These examples demonstrate fetching and processing JSON and XML data using Bun's `fetch` API. Modify the examples as needed based on the specific structure of the data you're working with and the APIs you're interacting with.

As of my knowledge cutoff in October 2023, Bun is a JavaScript runtime that doesn't natively support Python web frameworks like Flask or Django since these frameworks are specifically designed for the Python language. However, I can guide you on how to implement similar web server functionality using JavaScript frameworks or libraries that are compatible with Bun's JavaScript environment.

Below are examples of how to create web servers similar to what you might build with Flask or Django, using Node.js libraries that Bun can work with:

### Using Express.js with Bun

Express.js is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications, similar to Flask for Python. Here's how you can use it with Bun:

```javascript
import express from "express";

const app = express();
const PORT = 3000;

// Define a simple route
app.get("/", (req, res) => {
  res.send("Hello, World!");
});

// More complex route with parameters
app.get("/users/:userId", (req, res) => {
  const userId = req.params.userId;
  res.send(`User ID is: ${userId}`);
});

// Start the server
app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
```

### Using Fastify with Bun

Fastify is another web framework for Node.js that aims to be extremely fast and highly performant, more akin to Django in features but still designed to be lightweight.

```javascript
import Fastify from "fastify";

const fastify = Fastify({ logger: true });

// Simple route
fastify.get("/", async (request, reply) => {
  return { hello: "world" };
});

// More complex route with schema validation
fastify.get("/items/:id", async (request, reply) => {
  const { id } = request.params;
  return { itemId: id };
});

// Start the server
fastify.listen({ port: 3000 }, (err, address) => {
  if (err) {
    fastify.log.error(err);
    process.exit(1);
  }
  fastify.log.info(`Server listening at ${address}`);
});
```

### Using Koa.js with Bun

Koa.js is a web framework designed by the same team behind Express.js, intended to offer a smaller, more expressive, and more robust foundation for web applications and APIs.

```javascript
import Koa from "koa";

const app = new Koa();

// Logger middleware
app.use(async (ctx, next) => {
  await next();
  const rt = ctx.response.get("X-Response-Time");
  console.log(`${ctx.method} ${ctx.url} - ${rt}`);
});

// X-Response-Time middleware
app.use(async (ctx, next) => {
  const start = Date.now();
  await next();
  const ms = Date.now() - start;
  ctx.set("X-Response-Time", `${ms}ms`);
});

// Response middleware
app.use(ctx => {
  ctx.body = "Hello, World!";
});

// Start the server
app.listen(3000);

console.log("Server running on http://localhost:3000");
```

Each of these examples demonstrates how Bun can integrate with popular Node.js frameworks to create web servers with similar capabilities to those that Python's Flask or Django would provide.

Object-Oriented Programming (OOP)
In Bun JavaScript runtime, classes are defined and used similarly to how you would in any modern JavaScript environment, as Bun supports the ECMAScript standard.

Here's a step-by-step guide on how to define and use classes in Bun:

### Defining a Class

1. **Create a Class Declaration:**

   Use the `class` keyword to declare a class. Define its constructor and any methods or properties it should have.

   ```javascript
   class Animal {
     constructor(name, age) {
       this.name = name;
       this.age = age;
     }

     speak() {
       console.log(`${this.name} makes a noise.`);
     }
   }
   ```

   In this example, `Animal` is a class with a constructor that accepts `name` and `age`. It also has a method called `speak`.

2. **Class Expressions:**

   Classes can also be defined using class expressions. This is useful for defining classes dynamically or when you don't need a class name.

   ```javascript
   const Dog = class {
     constructor(breed) {
       this.breed = breed;
     }

     bark() {
       console.log('Woof!');
     }
   };
   ```

### Using a Class

1. **Creating Instances:**

   Use the `new` keyword to create an instance of a class.

   ```javascript
   const myDog = new Animal('Buddy', 3);
   const myPet = new Dog('Labrador');
   ```

2. **Accessing Methods and Properties:**

   You can access properties and methods on the class instance using dot notation.

   ```javascript
   console.log(myDog.name); // Outputs: Buddy
   myDog.speak(); // Outputs: Buddy makes a noise.

   console.log(myPet.breed); // Outputs: Labrador
   myPet.bark(); // Outputs: Woof!
   ```

### Inheritance

Classes in JavaScript can extend other classes using the `extends` keyword. This helps you create a class hierarchy.

```javascript
class Cat extends Animal {
  constructor(name, age, color) {
    super(name, age);
    this.color = color;
  }

  speak() {
    console.log(`${this.name} meows.`);
  }
}

const myCat = new Cat('Whiskers', 2, 'grey');
myCat.speak(); // Outputs: Whiskers meows.
```

In this example, `Cat` extends `Animal`, inheriting its properties and methods but overriding the `speak` method.

### Static Methods and Properties

You can define static methods and properties that belong to the class, not instances of the class.

```javascript
class Calculator {
  static add(a, b) {
    return a + b;
  }
}

console.log(Calculator.add(5, 3)); // Outputs: 8
```

### Private Fields and Methods

For encapsulation, JavaScript supports private fields and methods using the `#` prefix.

```javascript
class Counter {
  #count = 0;

  increment() {
    this.#count++;
  }

  getCount() {
    return this.#count;
  }
}

const counter = new Counter();
counter.increment();
console.log(counter.getCount()); // Outputs: 1
```

Private fields and methods can only be accessed within the class they are defined.

With these tools, you can effectively define and utilize classes in Bun JavaScript runtime, leveraging modern ECMAScript features.

In Bun, as with other JavaScript runtimes, you can create objects and instantiate classes using standard JavaScript syntax. Below are examples demonstrating how to do this:

### Creating Objects

You can create objects in JavaScript using either object literals or constructor functions.

#### Using Object Literals

```javascript
const person = {
  name: "John Doe",
  age: 30,
  greet: function() {
    console.log(`Hello, my name is ${this.name}`);
  }
};

person.greet(); // Output: Hello, my name is John Doe
```

#### Using a Constructor Function

```javascript
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
  this.getDetails = function() {
    return `${this.year} ${this.make} ${this.model}`;
  };
}

const car = new Car("Toyota", "Corolla", 2021);
console.log(car.getDetails()); // Output: 2021 Toyota Corolla
```

### Instancing Classes

JavaScript ES6 introduced classes, which provide a more familiar syntax for creating constructor functions and handling inheritance.

#### Defining and Instancing a Class

```javascript
class Animal {
  constructor(name, species) {
    this.name = name;
    this.species = species;
  }

  makeSound(sound) {
    console.log(`${this.name} the ${this.species} says: ${sound}`);
  }
}

const dog = new Animal("Rex", "dog");
dog.makeSound("Woof!"); // Output: Rex the dog says: Woof!
```

#### Inheritance with Classes

```javascript
class Vehicle {
  constructor(make, model) {
    this.make = make;
    this.model = model;
  }

  displayInfo() {
    console.log(`Vehicle: ${this.make} ${this.model}`);
  }
}

class Car extends Vehicle {
  constructor(make, model, doors) {
    super(make, model); // Call the parent class constructor
    this.doors = doors;
  }

  displayCarInfo() {
    console.log(`Car: ${this.make} ${this.model} with ${this.doors} doors`);
  }
}

const myCar = new Car("Ford", "Mustang", 2);
myCar.displayInfo(); // Output: Vehicle: Ford Mustang
myCar.displayCarInfo(); // Output: Car: Ford Mustang with 2 doors
```

These examples show how you can create and instantiate objects and classes in the Bun runtime, using syntax that is fully compatible with modern JavaScript.

In Bun JavaScript runtime, you can use traditional JavaScript inheritance through classes and prototypes just like in any JavaScript environment. Here are some examples illustrating inheritance:

### Example 1: Class-Based Inheritance

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name);
    this.breed = breed;
  }

  speak() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog('Rex', 'German Shepherd');
dog.speak();  // Rex barks.
```

### Example 2: Prototype-Based Inheritance

```javascript
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function () {
  console.log(this.name + ' makes a noise.');
};

function Dog(name, breed) {
  Animal.call(this, name);
  this.breed = breed;
}

Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;

Dog.prototype.speak = function() {
  console.log(this.name + ' barks.');
};

const dog = new Dog('Max', 'Bulldog');
dog.speak();  // Max barks.
```

### Example 3: Extending Built-in Classes

You can also extend built-in classes, such as `Array`, `Error`, etc.

```javascript
class CustomArray extends Array {
  last() {
    return this[this.length - 1];
  }
}

const arr = new CustomArray(1, 2, 3);
console.log(arr.last());  // 3
```

### Example 4: Using Inheritance with the `extends` and `super` Keywords

You can demonstrate how `super` can be used to invoke the parent class's methods.

```javascript
class Shape {
  constructor(color) {
    this.color = color;
  }

  draw() {
    console.log(`Drawing a shape in ${this.color} color.`);
  }
}

class Circle extends Shape {
  constructor(color, radius) {
    super(color);
    this.radius = radius;
  }

  draw() {
    super.draw();  // Call parent class's method
    console.log(`Drawing a circle with radius ${this.radius}.`);
  }
}

const circle = new Circle('red', 10);
circle.draw();
// Output:
// Drawing a shape in red color.
// Drawing a circle with radius 10.
```

These examples demonstrate how you can use inheritance in Bun's JavaScript runtime, taking advantage of JavaScript's `class` syntax or prototype-based approach for creating hierarchical relationships between objects.

Polymorphism is a core concept in object-oriented programming that allows objects to be treated as instances of their parent class rather than their actual class. This is particularly useful in JavaScript, including when using the Bun JavaScript runtime, as it provides flexibility and scalability in code design.

Here's a simple example of how you can implement polymorphism in Bun's JavaScript environment:

1. **Class Definition and Inheritance**: First, define a base class and subclasses that inherit from it.

```javascript
class Animal {
  speak() {
    console.log("The animal makes a sound");
  }
}

class Dog extends Animal {
  speak() {
    console.log("The dog barks");
  }
}

class Cat extends Animal {
  speak() {
    console.log("The cat meows");
  }
}
```

2. **Using Polymorphism**: You can create instances of these classes and call the `speak` method polymorphically.

```javascript
const animals = [new Animal(), new Dog(), new Cat()];

animals.forEach(animal => animal.speak());
```

In this example, even though the `animals` array contains objects of different types, you can iterate over them and call `speak()` on each. The correct method for each object type is called due to polymorphism.

### Implementing with Bun

While Bun itself focuses on being a fast JavaScript runtime and doesn't require any specific modification when dealing with basic JavaScript features like polymorphism, it's worth ensuring compatibility and performance when deploying such code.

1. **Ensure Bun is Installed**: Use Bun's environment by ensuring it is installed and running your JavaScript.

2. **Running Your Script with Bun**: Save your polymorphism example script to a file, say `polymorphismExample.js`, and run it with Bun:

```bash
bun run polymorphismExample.js
```

This command will execute your JavaScript code using the Bun runtime, effectively demonstrating polymorphism through class inheritance and method overriding.

As Bun aims for efficiency, if your code involves file operations, HTTP servers, or databases, leveraging Bun's APIs for those parts can further enhance performance. Nonetheless, standard polymorphic behaviors, as described here, work seamlessly within Bun just as they do in other JavaScript runtimes.

In JavaScript, interfaces are not a built-in feature like they are in languages such as TypeScript or Java. However, you can simulate interfaces conceptually by using object structures, classes, and ensuring certain methods or properties are present.

Below is an example of how you might implement a similar concept using JavaScript in the Bun runtime environment, including some runtime checks:

```javascript
// Define a "Shape" interface concept
function ShapeInterface(instance) {
  if (typeof instance.getArea !== "function") {
    throw new Error("Class implementing Shape must have a getArea() method");
  }
  if (typeof instance.getPerimeter !== "function") {
    throw new Error("Class implementing Shape must have a getPerimeter() method");
  }
}

// Rectangle class implementing the "Shape" interface
class Rectangle {
  constructor(width, height) {
    this.width = width;
    this.height = height;

    // Check if this class adheres to the ShapeInterface
    ShapeInterface(this);
  }

  getArea() {
    return this.width * this.height;
  }

  getPerimeter() {
    return 2 * (this.width + this.height);
  }
}

// Circle class implementing the "Shape" interface
class Circle {
  constructor(radius) {
    this.radius = radius;

    // Check if this class adheres to the ShapeInterface
    ShapeInterface(this);
  }

  getArea() {
    return Math.PI * this.radius * this.radius;
  }

  getPerimeter() {
    return 2 * Math.PI * this.radius;
  }
}

// Instantiate objects and demonstrate their usage
try {
  const myRectangle = new Rectangle(10, 20);
  console.log("Rectangle Area:", myRectangle.getArea());
  console.log("Rectangle Perimeter:", myRectangle.getPerimeter());

  const myCircle = new Circle(15);
  console.log("Circle Area:", myCircle.getArea());
  console.log("Circle Perimeter:", myCircle.getPerimeter());
} catch (error) {
  console.error(error.message);
}
```

### Explanation:
- **ShapeInterface Function**: This function checks if the passed instance has the required methods (`getArea` and `getPerimeter`). You can extend this with more properties or methods as needed.
- **Rectangle and Circle Classes**: These classes implement the conceptual "Shape" interface by providing the necessary methods.
- In this setup, when you instantiate `Rectangle` or `Circle`, the interface check is performed by calling `ShapeInterface(this)`. If the instance does not implement all required methods, it throws an error.
- **Usage**: You can work with `Rectangle` and `Circle` objects and call their respective methods. If a class does not fulfill the interface contract, errors will be raised when you try to instantiate it.

This is how you can simulate interfaces in JavaScript using Bun, keeping in mind that true interfaces are more about compile-time checks, typically outside the scope of JavaScript's runtime.

Regular Expressions (Regex)
Certainly! Regular expressions (regex) are a powerful tool for pattern matching and text manipulation. Below are some examples of how you can use regex patterns in the Bun JavaScript runtime.

### Example 1: Basic Pattern Matching

```javascript
const regex = /hello/;
const text = "hello world!";
console.log(regex.test(text)); // Output: true
```

### Example 2: Case Insensitive Matching

```javascript
const regex = /hello/i; // 'i' flag for case-insensitive matching
const text = "Hello World!";
console.log(regex.test(text)); // Output: true
```

### Example 3: Global Search with `match`

```javascript
const regex = /world/g;
const text = "world hello world!";
const matches = text.match(regex);
console.log(matches); // Output: ['world', 'world']
```

### Example 4: Replace Substring

```javascript
const regex = /world/;
const text = "hello world!";
const replacedText = text.replace(regex, "Universe");
console.log(replacedText); // Output: "hello Universe!"
```

### Example 5: Capturing Groups

```javascript
const regex = /(\d{3})-(\d{2})-(\d{4})/;
const text = "123-45-6789";
const result = regex.exec(text);
console.log(result);
// Output: ['123-45-6789', '123', '45', '6789']
```

### Example 6: Split Using Regex

```javascript
const regex = /,|;|\s/; // Split on commas, semicolons, or spaces
const text = "apple,banana; orange grape";
const fruits = text.split(regex);
console.log(fruits); // Output: ["apple", "banana", "orange", "grape"]
```

### Example 7: Positive Lookahead

```javascript
const regex = /\d+(?= dollars)/;
const text = "The price is 100 dollars";
const match = text.match(regex);
console.log(match[0]); // Output: "100"
```

### Example 8: Negative Lookbehind

```javascript
const regex = /(?<!\$)\d+/;
const text = "100 dollars";
const match = text.match(regex);
console.log(match[0]); // Output: "100"
```

These examples demonstrate how you can leverage regular expressions in the Bun JavaScript runtime to perform a variety of text processing tasks. Note that all these features assume you are running your JavaScript code in an environment that supports the regular expression features, which Bun does, as it is compatible with modern JavaScript syntax and features.

In Bun's JavaScript runtime, capturing groups can be used as part of regular expressions to extract specific parts of a string. Capturing groups are denoted by parentheses `( ... )` in a regular expression pattern. Here's how you can work with capturing groups in Bun:

### Using Capturing Groups

1. **Basic Example:**
   To capture specific parts of a string, you can use parentheses in your regular expression. For example, to capture a year and a month from a date string:

   ```javascript
   const regex = /(\d{4})-(\d{2})-(\d{2})/;
   const dateStr = "2023-10-15";
   const match = regex.exec(dateStr);

   if (match) {
     console.log(`Year: ${match[1]}, Month: ${match[2]}, Day: ${match[3]}`);
   }
   ```

   Here, `match[1]`, `match[2]`, and `match[3]` are capturing groups for the year, month, and day, respectively.

2. **Named Capturing Groups:**
   Bun supports named capturing groups, which can make your code more readable. Named capturing groups are defined using `(?<name> ... )`. Here's an example:

   ```javascript
   const regex = /(?<year>\d{4})-(?<month>\d{2})-(?<day>\d{2})/;
   const dateStr = "2023-10-15";
   const match = regex.exec(dateStr);

   if (match) {
     console.log(`Year: ${match.groups.year}, Month: ${match.groups.month}, Day: ${match.groups.day}`);
   }
   ```

   `match.groups` will hold the named groups as properties, allowing access via descriptive names instead of numeric indices.

3. **Working with `String.prototype.match`:**
   You can use `String.prototype.match` with capturing groups, which will provide a similar result. However, remember that `match` works differently with the 'g' flag:

   ```javascript
   const regex = /(\d{4})-(\d{2})-(\d{2})/;
   const dateStr = "2023-10-15";
   const match = dateStr.match(regex);

   if (match) {
     console.log(`Year: ${match[1]}, Month: ${match[2]}, Day: ${match[3]}`);
   }
   ```

   Note: Without the global flag, `match` returns additional information about the capturing groups just like `exec`.

4. **Substitution with Capturing Groups:**
   You can use captured groups in `String.prototype.replace` to substitute certain parts of the string:

   ```javascript
   const regex = /(\d{4})-(\d{2})-(\d{2})/;
   const dateStr = "2023-10-15";

   const formattedDateStr = dateStr.replace(regex, '$3/$2/$1');
   console.log(formattedDateStr); // Outputs: "15/10/2023"
   ```

   This uses `$1`, `$2`, and `$3` to refer to the captured groups in the replacement string.

### Conclusion

Working with capturing groups in Bun's JavaScript runtime is similar to working with them in other JavaScript environments. The syntax for creating regular expressions and capturing groups follows ECMAScript standards, making it straightforward to use capturing groups for extracting and manipulating string data effectively.

In Bun.js, which like other JavaScript runtimes, you can use regex substitutions by utilizing the `String.prototype.replace()` method. This method can take a regular expression as its first argument and a replacement string or function as its second argument. Below are some examples demonstrating regex substitutions:

### Example 1: Simple Substitution
Replace all instances of "apple" with "orange".

```javascript
let text = "I have an apple. I like to eat apple pie.";
let result = text.replace(/apple/g, "orange");
console.log(result); // Output: "I have an orange. I like to eat orange pie."
```

### Example 2: Case-Insensitive Substitution
Replace "cat" with "dog", ignoring case sensitivity.

```javascript
let text = "The Cat chased the cat.";
let result = text.replace(/cat/gi, "dog");
console.log(result); // Output: "The dog chased the dog."
```

### Example 3: Using Capture Groups
Swap the order of first name and last name.

```javascript
let name = "Doe, John";
let result = name.replace(/(\w+), (\w+)/, "$2 $1");
console.log(result); // Output: "John Doe"
```

### Example 4: Using a Replacement Function
Capitalize the first letter of each word in a sentence.

```javascript
let text = "hello world";
let result = text.replace(/\b\w/g, (match) => match.toUpperCase());
console.log(result); // Output: "Hello World"
```

### Example 5: Complex Pattern Replacement
Remove all HTML tags from a string.

```javascript
let html = "<div>Hello <strong>World</strong></div>";
let result = html.replace(/<[^>]*>/g, "");
console.log(result); // Output: "Hello World"
```

These examples should work in Bun as long as you're using standard JavaScript string manipulation methods that Bun supports.

In Bun.js, you can utilize regular expressions (RegEx) for validation purposes, just like in traditional JavaScript environments. Below are some examples demonstrating how to use RegEx for various types of validation:

### 1. Email Validation
```javascript
function validateEmail(email) {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

console.log(validateEmail("example@domain.com")); // true
console.log(validateEmail("invalid-email")); // false
```

### 2. URL Validation
```javascript
function validateURL(url) {
  const regex = /^(https?:\/\/)?([\w\d-]+\.){1,2}[a-z]{2,63}(\/[\w\d-]*)*\/?$/i;
  return regex.test(url);
}

console.log(validateURL("https://www.example.com")); // true
console.log(validateURL("ftp://example.com")); // false
```

### 3. IPv4 Address Validation
```javascript
function validateIPv4(ip) {
  const regex = /^(25[0-5]|2[0-4]\d|1\d{2}|\d{1,2})(\.(25[0-5]|2[0-4]\d|1\d{2}|\d{1,2})){3}$/;
  return regex.test(ip);
}

console.log(validateIPv4("192.168.1.1")); // true
console.log(validateIPv4("999.999.999.999")); // false
```

### 4. Phone Number Validation (US)
```javascript
function validatePhoneNumber(phone) {
  const regex = /^\(?([0-9]{3})\)?[-.●]?([0-9]{3})[-.●]?([0-9]{4})$/;
  return regex.test(phone);
}

console.log(validatePhoneNumber("123-456-7890")); // true
console.log(validatePhoneNumber("12345678")); // false
```

### 5. Password Complexity Validation
A password that requires at least one uppercase letter, one lowercase letter, one number, and one special character.
```javascript
function validatePassword(password) {
  const regex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&#])[A-Za-z\d@$!%*?&#]{8,}$/;
  return regex.test(password);
}

console.log(validatePassword("Aa1!aaaa")); // true
console.log(validatePassword("password")); // false
```

### 6. Hexadecimal Color Code Validation
```javascript
function validateHexColor(color) {
  const regex = /^#?([a-f0-9]{6}|[a-f0-9]{3})$/i;
  return regex.test(color);
}

console.log(validateHexColor("#fff")); // true
console.log(validateHexColor("1234567")); // false
```

These examples demonstrate how to use regular expressions within the Bun.js environment to validate various common data formats. You can test and run these examples directly using Bun's JavaScript runtime by placing them in a `.js` file and executing it with the `bun <file>.js` command.

In the Bun JavaScript runtime, regex callbacks work similarly to how they do in Node.js and the browser. Here's how you can use them with the `String.prototype.replace()` method, which is one of the most common use cases for regex callbacks.

### Example 1: Simple Regex Replacement with a Callback

Suppose you want to convert markdown-style links in a string to HTML `<a>` tags:

```javascript
const bunCode = "[Bun](https://bun.sh) is fast and modern!";

const result = bunCode.replace(/\[([^\]]+)\]\(([^)]+)\)/g, (match, text, url) => {
  return `<a href="${url}">${text}</a>`;
});

console.log(result);
// Output: <a href="https://bun.sh">Bun</a> is fast and modern!
```

In this example, the callback function is called for each match. The match, along with any captured groups (in this case, `text` and `url`), are passed as arguments, allowing you to build a replacement string dynamically.

### Example 2: Conditional Replacement

You can also use a callback to perform conditional logic based on the matched content:

```javascript
const text = "101 Development, 202 Security, 303 Testing";

const result = text.replace(/(\d{3}) (\w+)/g, (match, code, department) => {
  if (code === "202") {
    return `${code} [REDACTED]`;
  }
  return match;
});

console.log(result);
// Output: 101 Development, 202 [REDACTED], 303 Testing
```

Here, if a specific department code is matched, the output is modified accordingly.

### Example 3: Using Regex for Transformation

Let's say you want to swap the order of first and last names in a string:

```javascript
const names = "Doe, John; Smith, Jane; Black, Neil";

const swappedNames = names.replace(/(\w+), (\w+)/g, (match, lastName, firstName) => {
  return `${firstName} ${lastName}`;
});

console.log(swappedNames);
// Output: John Doe; Jane Smith; Neil Black
```

This uses a regex callback to capture the last and first names, then returns them swapped.

These examples demonstrate the flexibility of using regex callbacks to dynamically generate replacement strings based on the content of a match.

Security
Using the Bun JavaScript runtime, you can perform encryption and decryption using the Web Crypto API, which is available globally. Here's an example of how you might implement basic encryption and decryption operations:

### Example: Symmetric Encryption and Decryption

We'll use the AES-GCM algorithm for symmetric encryption and decryption.

```javascript
async function generateKey() {
  return await crypto.subtle.generateKey(
    {
      name: "AES-GCM",
      length: 256,
    },
    true, // extractable
    ["encrypt", "decrypt"]
  );
}

async function encryptMessage(key, message) {
  const encoder = new TextEncoder();
  const data = encoder.encode(message);

  const iv = crypto.getRandomValues(new Uint8Array(12)); // Generate a random Initialization Vector

  const encrypted = await crypto.subtle.encrypt(
    {
      name: "AES-GCM",
      iv: iv,
    },
    key,
    data
  );

  return { encryptedData: new Uint8Array(encrypted), iv };
}

async function decryptMessage(key, encryptedData, iv) {
  const decrypted = await crypto.subtle.decrypt(
    {
      name: "AES-GCM",
      iv: iv,
    },
    key,
    encryptedData
  );

  const decoder = new TextDecoder();
  return decoder.decode(decrypted);
}

async function runEncryptionDemo() {
  const key = await generateKey();
  const message = "Hello, Bun!";
  
  console.log("Original Message:", message);

  const { encryptedData, iv } = await encryptMessage(key, message);
  console.log("Encrypted Data:", encryptedData);

  const decryptedMessage = await decryptMessage(key, encryptedData, iv);
  console.log("Decrypted Message:", decryptedMessage);
}

runEncryptionDemo();
```

### Explanation:
- **Key Generation**: We generate a symmetric key using the AES-GCM algorithm.
- **Encryption**: The message is converted to a Uint8Array and encrypted using the key with a randomly generated Initialization Vector (IV). The IV is crucial for decrypting the message.
- **Decryption**: Using the same key and IV, we decrypt the encrypted data back to its original form.

### Important Notes:
- **IV**: Always use a unique IV for each encryption operation. The same IV should never be reused with the same key.
- **Export/Import Keys**: If you need to store and retrieve keys, you can use the `crypto.subtle.exportKey` and `crypto.subtle.importKey` methods.
- **Error Handling**: In a production environment, wrap cryptographic operations with try-catch blocks to manage potential errors gracefully.

This example demonstrates simple symmetric encryption. For more complex scenarios, such as asymmetric encryption, key management, and using other algorithms, the Web Crypto API provides various methods and options to explore.

As of my last update, Bun is a fast JavaScript runtime that has been designed to run applications with a focus on web-compatible API support similar to Node.js and Deno. While Bun is still developing, many core functionalities related to cryptography might not be directly available or might require using external libraries or native Node.js APIs that are also supported in Bun.

To work with digital signatures and certificates in JavaScript within Bun, you can typically rely on the `crypto` module, which is standard in Node.js environments and should be supported in Bun. Here is a general guide on how to handle digital signatures and certificates:

### Digital Signatures

Digital signatures in JavaScript can be handled using the `crypto` module's signing and verifying capabilities. Here's how you can create and verify a digital signature:

1. **Generate a Key Pair**

   To create a digital signature, you'll first need a pair of keys (a private key for signing and a public key for verifying).

   ```javascript
   const crypto = require('crypto');

   const { publicKey, privateKey } = crypto.generateKeyPairSync('rsa', {
     modulusLength: 2048,
   });
   ```

2. **Sign Data**

   Use the private key to sign some data.

   ```javascript
   const sign = crypto.createSign('SHA256');
   sign.update('some data to sign');
   sign.end();

   const signature = sign.sign(privateKey, 'hex');
   console.log(`Signature: ${signature}`);
   ```

3. **Verify Signature**

   Use the public key to verify that the signature is valid for the data.

   ```javascript
   const verify = crypto.createVerify('SHA256');
   verify.update('some data to sign');
   verify.end();

   const isVerified = verify.verify(publicKey, signature, 'hex');
   console.log(`Signature verified: ${isVerified}`);
   ```

### Digital Certificates

Working with digital certificates generally involves reading and parsing the certificate, which is commonly done using external libraries like `forge` or using Node.js APIs that handle X.509 certificates. Bun's compatibility with Node.js APIs should allow you to use similar packages or methods.

1. **Read Certificate**

   Reading a certificate is typically done via file reading APIs:

   ```javascript
   const fs = require('fs');
   const certificate = fs.readFileSync('cert.pem').toString();
   ```

2. **Parse and Verify Certificate**

   You may use a library like `node-forge` to parse and verify certificates, if such a package is available and functional within the Bun environment.

   ```bash
   # If supported, install the forge package using the bun package manager
   bun add node-forge
   ```

   ```javascript
   const forge = require('node-forge');

   const cert = forge.pki.certificateFromPem(certificate);
   console.log(`Issuer: ${cert.issuer.attributes.map(attr => attr.value).join(', ')}`);
   ```

3. **Validate Certificate**

   Typically, validating involves checking the certificate chain against trusted root certificates, which would require additional processing and possibly external libraries.

While Bun's APIs and supported modules may evolve, keeping an eye on the Bun documentation and updates related to Node.js compatibility is essential. If specific libraries are not directly supported in Bun, consider implementing compatible alternatives or workarounds that align with Bun's capabilities at the time.

When implementing secure password storage in a Bun.js application, it's important to hash passwords using a library like `bcrypt`. Here's how you can accomplish that using Bun's JavaScript runtime:

First, you need to install the `bcrypt` package, which can be done via Bun's package manager as follows:

```bash
bun add bcrypt
```

Next, you can use `bcrypt` to hash and verify passwords in your application:

```javascript
import bcrypt from 'bcrypt';

// Function to hash a password
async function hashPassword(plainPassword) {
  const saltRounds = 10; // Recommended cost factor
  const hashedPassword = await bcrypt.hash(plainPassword, saltRounds);
  return hashedPassword;
}

// Function to verify a password
async function verifyPassword(plainPassword, hashedPassword) {
  const match = await bcrypt.compare(plainPassword, hashedPassword);
  return match;
}

// Example usage
(async () => {
  const plainPassword = 'securePassword123';
  
  // Hash the password
  const hashedPassword = await hashPassword(plainPassword);
  console.log('Hashed Password:', hashedPassword);
  
  // Verify the password
  const isMatch = await verifyPassword(plainPassword, hashedPassword);
  console.log('Password matches:', isMatch); // Should print: true
  
  // Attempting verification with an incorrect password
  const isMatchIncorrect = await verifyPassword('wrongPassword', hashedPassword);
  console.log('Password matches with wrong password:', isMatchIncorrect); // Should print: false
})();
```

Explanation:

1. **Hashing**: The `hashPassword` function uses `bcrypt` to hash a plain password. The `saltRounds` parameter defines the computational cost of hashing. A higher number increases security but also increases processing time.

2. **Verifying**: The `verifyPassword` function checks if a provided plain password matches a previously hashed password using `bcrypt.compare`.

This example demonstrates secure password storage, ensuring hashed passwords are stored and handled properly. Always store hashed passwords in your database, never plain text passwords.

Using the Bun JavaScript runtime, you can set up SSL/TLS for secure communication, usually through libraries that handle these protocols. Here's how you can use native modules or third-party packages to achieve SSL/TLS connections in Bun.

### Example: HTTPS Server Using Bun's Native `https` Module

To create a simple HTTPS server, you can utilize Bun's compatibility with the Node.js `https` module:

```javascript
import { readFileSync } from 'fs';
import { createServer } from 'https';

// Load your SSL/TLS certificate and key
const options = {
  key: readFileSync('./path/to/your/private-key.pem'),
  cert: readFileSync('./path/to/your/certificate.pem'),
};

// Create an HTTPS server
const server = createServer(options, (req, res) => {
  res.writeHead(200);
  res.end('Hello, Secure World!');
});

// Listen on port 443 (default HTTPS port)
server.listen(443, () => {
  console.log('HTTPS server listening on port 443');
});
```

### Example: HTTPS Client Request Using Bun's Native `https` Module

Similarly, you can make HTTPS requests:

```javascript
import { get } from 'https';

const options = {
  hostname: 'example.com',
  port: 443,
  path: '/',
  method: 'GET',
};

const req = get(options, (res) => {
  let data = '';

  // Collect response data
  res.on('data', (chunk) => {
    data += chunk;
  });

  // On end, output the data
  res.on('end', () => {
    console.log(data);
  });
});

req.on('error', (error) => {
  console.error('An error occurred:', error);
});

req.end();
```

### Using Third-Party Libraries for Enhanced Functionality

While native modules are sufficient for many use cases, you might want more features like better API ergonomics or additional security features. Libraries like `axios`, `got`, or `node-fetch` can be used. Here’s an example using `axios`, which should work in Bun given its Node.js compatibility:

Ensure you have `axios` installed:

```bash
bun add axios
```

Then use it as follows:

```javascript
import axios from 'axios';

axios.get('https://example.com')
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error('An error occurred:', error);
  });
```

These examples should give you a good starting point for using SSL/TLS in Bun for both server and client scenarios. Make sure to adapt file paths and options to your specific environment and security requirements.

Access Control Lists (ACLs) are used to specify which users or system processes are granted access to objects, as well as what operations are allowed on given objects. In the context of Bun, since Bun is primarily a JavaScript runtime, implementing ACLs would mostly relate to an application-level implementation where you might want to control access to resources like APIs, files, or other data.

Here's a basic example to demonstrate how you might implement a simple ACL system in a Bun application.

### Example: Simple ACL for an API

Imagine you have an API where you want to control which users can access certain endpoints. We'll use an ACL to manage this.

#### Step 1: Define Users and Roles

```javascript
const users = [
    { id: 1, name: 'Alice', roles: ['admin'] },
    { id: 2, name: 'Bob', roles: ['guest'] },
];

const roles = {
    admin: {
        permissions: ['read', 'write', 'delete'],
    },
    guest: {
        permissions: ['read'],
    },
};
```

#### Step 2: Middleware to Check ACL

Here's a simple middleware function that checks the user's permissions before allowing access to a route.

```javascript
function checkPermission(requiredPermission) {
    return (req, res, next) => {
        const userId = req.headers['x-user-id'];
        const user = users.find(u => u.id == userId);

        if (!user) {
            return res.status(403).send('Forbidden: User not found.');
        }

        const userPermissions = user.roles.reduce((perms, role) => {
            return perms.concat(roles[role].permissions);
        }, []);

        if (userPermissions.includes(requiredPermission)) {
            return next();
        }

        res.status(403).send('Forbidden: You do not have permission.');
    };
}
```

#### Step 3: Define Routes with ACL

Let's set up some routes using Bun's application serving capabilities (when integrated with a server like `express` or `bun-framework`).

```javascript
// Example using `express` or similar framework
const express = require('express');
const app = express();

app.use(express.json());

app.get('/data', checkPermission('read'), (req, res) => {
    res.send('This is data for users with read permission.');
});

app.post('/data', checkPermission('write'), (req, res) => {
    res.send('Data written successfully.');
});

app.delete('/data', checkPermission('delete'), (req, res) => {
    res.send('Data deleted successfully.');
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

### Run the Example with Bun

To run this example with Bun, make sure Bun is installed and you're using a server compatible with its modules, or adapt this for Bun's custom server APIs if necessary. The above example is a standard approach and would work with any Node.js environment that's compatible with Bun, including using Bun's build or script running features if `express` or similar is supported.

Remember, Bun aims to be a drop-in replacement for Node.js, so workflows involving Node.js can frequently be used with Bun. Make sure any external packages you're using are compatible or have been tested with Bun, as there's often ongoing development in these environments.

Testing and Debugging
When using the Bun JavaScript runtime, you can leverage its built-in test runner to write and execute unit tests efficiently. Below are examples of how you can write unit tests in Bun using its built-in testing capabilities.

### Example 1: Basic Test

```javascript
import { test, expect } from 'bun:test';

test('addition works correctly', () => {
  const sum = 1 + 2;
  expect(sum).toBe(3);
});
```

### Example 2: Testing Asynchronous Code

```javascript
import { test, expect } from 'bun:test';

function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve('hello world');
    }, 100);
  });
}

test('fetchData returns correct data', async () => {
  const data = await fetchData();
  expect(data).toBe('hello world');
});
```

### Example 3: Grouping Tests with Describe

If you prefer a structured approach by grouping related tests together, you can use `describe`.

```javascript
import { test, expect, describe } from 'bun:test';

describe('Math operations', () => {
  test('addition works correctly', () => {
    const result = 2 + 3;
    expect(result).toBe(5);
  });

  test('subtraction works correctly', () => {
    const result = 5 - 3;
    expect(result).toBe(2);
  });
});
```

### Example 4: Running Tests with Setup and Teardown

Just like other testing frameworks, you might need to perform setup and teardown for your tests. You can handle these manually in each test for now since Bun's test runner may not have explicit setup/teardown hooks.

```javascript
import { test, expect } from 'bun:test';

let counter = 0;

test('counter increment', () => {
  counter++;
  expect(counter).toBe(1);
});

// Resetting manually for the next test
counter = 0;

test('counter starts from zero again', () => {
  expect(counter).toBe(0);
});
```

### Running the Tests

To execute the tests, you can run the following command in the terminal:

```bash
bun test
```

Make sure you have `bun` installed and are in the root directory of your project.

These examples demonstrate the simplicity and effectiveness of using Bun's built-in testing framework to write and run unit tests in JavaScript.

In Bun, a JavaScript runtime like Deno and Node.js, you can write and execute test cases to ensure the correctness of your code. Testing in Bun can be conveniently achieved using its built-in testing facilities. Here’s a basic guide on how to work with test cases in Bun:

### Writing Tests

1. **Create a Test File**: 
   Create a JavaScript or TypeScript file where you will write your test cases. It's common to name this file with a `.test.js` or `.test.ts` extension.

2. **Using Bun's Test Functionality**:
   Bun provides a `bun:test` module that you can use to define your test cases.

   ```javascript
   import { describe, it, expect } from "bun:test";

   describe("Math operations", () => {
     it("should add two numbers correctly", () => {
       const result = 1 + 2;
       expect(result).toBe(3);
     });
   
     it("should subtract two numbers correctly", () => {
       const result = 5 - 2;
       expect(result).toBe(3);
     });
   });
   ```

   - **describe**: Groups a set of related tests. It usually takes a string description and a callback function.
   - **it**: Defines an individual test case. It also takes a description and a callback function.
   - **expect**: Used for making assertions about your code. The `toBe` function checks if the result matches the expected value.

### Running Tests

3. **Execute Your Tests**:
   To run your tests, use the Bun CLI to execute the test files. You can run all tests with the following command:

   ```bash
   bun test
   ```

   This command will automatically find files with common test file naming conventions like `.test.js`, `.spec.js`, etc., and execute them.

### Tips for Effective Testing

- **Use Mocks and Spies**: If you need to test functions that interact with databases or external services, use mocks to simulate these interactions.
  
- **Organize Tests Logically**: Use `describe` blocks to group related tests, making your test output easier to read and understand.

- **Use Setup and Teardown Functions**: If your tests require common setup or cleanup logic, use hooks like `beforeEach` or `afterEach` to handle this.

- **Run Tests Automatically**: Integrate your Bun tests into a CI/CD pipeline to ensure tests run automatically on every commit or pull request.

By following these steps and best practices, you can effectively use Bun to run and manage test cases, helping you maintain robust and error-free JavaScript applications.

In Bun's JavaScript runtime, you can use mock objects to simulate and test the behavior of certain parts of your application without relying on their real implementations. This is particularly useful in unit testing. Here's an example using a basic test framework approach, similar to how you might use Jest or another testing library that supports mocks.

First, let's create a simple example where we'll mock a dependency:

Suppose we have a module `mathOperations.js`:

```javascript
// mathOperations.js
export function add(a, b) {
  return a + b;
}

export function multiply(a, b) {
  return a * b;
}
```

Let's assume we have another module `calculator.js` that uses these operations:

```javascript
// calculator.js
import { add, multiply } from './mathOperations.js';

export function calculateSum(x, y) {
  return add(x, y);
}

export function calculateProduct(x, y) {
  return multiply(x, y);
}
```

Now, we want to test `calculateSum` function but mock `add` to always return a specific value. Using a simple test structure, you'd write something like:

```javascript
// calculator.test.js
import { vi } from 'bun:test'; // Assuming a Jest-like testing framework in Bun
import * as mathOperations from './mathOperations.js';
import { calculateSum } from './calculator.js';

// Create a mock for 'add' method
vi.spyOn(mathOperations, 'add');
// Alternatively, if vi is similar to jest, you can use jest-style mocking:
// jest.mock('./mathOperations.js', () => ({
//   add: vi.fn(),
// }));

describe('Calculator Module', () => {
  it('should return mocked value for calculateSum', () => {
    // Arrange: Set up mock
    mathOperations.add.mockImplementation((x, y) => 10); // Mock .add to always return 10

    // Act: Call the function that uses the mocked method
    const result = calculateSum(2, 3);

    // Assert: Verify the expected result
    expect(result).toBe(10);
    expect(mathOperations.add).toHaveBeenCalledWith(2, 3);
  });

  afterEach(() => {
    // Clean up mocks if necessary
    mathOperations.add.mockRestore();
  });
});
```

Here's a breakdown of what's happening:

- **Mock Creation**: We use `vi.spyOn()` to create a mock for `mathOperations.add`. This allows us to intercept and control calls to this method.
- **Mock Implementation**: We specify that whenever `add` is called during this test, it should return `10`.
- **Test Execution**: We call `calculateSum`, which internally calls our mocked `add` method.
- **Assertions**: We check if the result of `calculateSum` is `10` and verify that `add` was called with the arguments `2` and `3`.
- **Mock Cleanup**: After each test, we restore the original method to avoid side effects on other tests.

Note: This example assumes the presence of a Jest-like testing environment with mocking capabilities in Bun's runtime. If Bun introduces a specific testing library in the future, the syntax or approach might vary slightly.

Certainly! As of the last update, Bun has been rapidly evolving, so I encourage you to verify the latest features and tools available. However, here are some general examples and explanations on how you might use debugging tools within the Bun JavaScript runtime environment:

### Example 1: Using Bun's built-in Debugger

Bun includes built-in debugging capabilities. You can start your Bun project with the debugger enabled to step through your code:

1. **Run Bun with the `--inspect` flag:**

   You can start your Bun application with the `--inspect` flag, which allows you to connect a debugger:

   ```bash
   bun run --inspect your-script.ts
   ```

2. **Using a Debugger Client:**

   Once you've started Bun with inspection enabled, you can open developer tools in your preferred web browser (like Chrome) and connect to the Node.js debugging interface that Bun supports. You'll typically go to `chrome://inspect` and configure your target by adding a new connection using the appropriate port shown in your Bun terminal output.

### Example 2: Breakpoints in the Code

You can use breakpoints to pause your script execution at certain points, allowing you to inspect the state of your application:

1. **Add `debugger` Statements:**

   Add `debugger` statements in your JavaScript or TypeScript code:

   ```javascript
   function calculateSum(a, b) {
     let sum = a + b;
     debugger; // Execution will pause here
     return sum;
   }

   calculateSum(5, 10);
   ```

   When you run this code with the debugger attached, execution will pause at the `debugger` statement, allowing you to inspect variables like `sum`.

### Example 3: Logging and Conditional Breakpoints

1. **Console Logging:**

   Using `console.log` is a traditional and straightforward way to debug and inspect variable values:

   ```javascript
   function calculateProduct(x, y) {
     const product = x * y;
     console.log('Product:', product);
     return product;
   }

   calculateProduct(4, 5);
   ```

2. **Conditional Breakpoints:**

   In your debugging UI (e.g., Chrome DevTools), you can set breakpoints with conditions. This means that the execution will only pause if a specific condition is true.

   - Right-click on the line number where you'd set a breakpoint.
   - Select "Add Conditional Breakpoint" and enter a condition, like `sum > 10`.

### Example 4: Viewing Call Stack and Scopes

When execution is paused, you can navigate:

- **Call Stack:** To see the path your code took to reach the current line.
- **Scopes:** To view the variables currently in scope and their values.

By maintaining careful use of logging, breakpoints, and leveraging Bun's debugging capabilities, you can efficiently trace issues and optimize your JavaScript code.

Always keep an eye on Bun's official documentation for any updates or new features related to debugging and other runtime tools.

In the Bun JavaScript runtime, you can use logging frameworks like `bunyan`, `winston`, or `pino` to handle logging in a structured and efficient manner. Here are examples of how you can set up and use these logging frameworks in Bun:

### Example 1: Using `bunyan`

First, install Bunyan via npm:

```bash
bun add bunyan
```

Then, create a logging setup with Bunyan:

```javascript
import bunyan from 'bunyan';

// Create a logger instance
const logger = bunyan.createLogger({
  name: 'myapp',
  level: 'info', // Set default log level
});

// Example log statements
logger.info('This is an info message');
logger.warn('This is a warning message');
logger.error('This is an error message');
logger.debug('This debug message will only show if the level is set to debug');
```

### Example 2: Using `winston`

Install Winston with:

```bash
bun add winston
```

Set up Winston:

```javascript
import winston from 'winston';

// Create a logger instance
const logger = winston.createLogger({
  level: 'info', // Set the default logging level
  format: winston.format.json(), // Use JSON format
  transports: [
    new winston.transports.Console(), // Log to the console
  ],
});

// Example log statements
logger.info('This is an info message');
logger.warn('This is a warning message');
logger.error('This is an error message');
logger.debug('This debug message will not show unless the level is set to debug');
```

### Example 3: Using `pino`

Install Pino with:

```bash
bun add pino
```

Set up Pino for logging:

```javascript
import pino from 'pino';

// Create a logger instance
const logger = pino({
  level: 'info', // Set the default logging level
});

// Example log statements
logger.info('This is an info message');
logger.warn('This is a warning message');
logger.error('This is an error message');
logger.debug('This debug message will not show unless the level is configured to debug');
```

### Notes:

- Adjust logging levels according to your needs (`info`, `warn`, `error`, `debug`, etc.).
- These frameworks support various transport mediums (e.g., files, remote servers), but for simplicity, these examples log to the console.
- You can further configure formats, add custom transports, and support more advanced logging features by referring to each library's official documentation.

