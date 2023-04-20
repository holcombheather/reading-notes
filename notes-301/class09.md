# Functional Programming

# Functional Programming Concepts

## What is functional programming?
Functional programming is a programming paradigm that emphasizes on the use of pure functions and immutable data structures to perform computations. In functional programming, functions are treated as first-class citizens and are used to represent and manipulate data.

## What is a pure function and how do we know if something is a pure function?
A pure function is a function that always returns the same output for a given input and does not have any side effects. Side effects refer to any modification of a variable outside the scope of the function, such as I/O operations, mutation of state or modifying the DOM. We can identify whether a function is pure or not by checking if it satisfies the above conditions.

## What are the benefits of a pure function?
The benefits of using pure functions are that they are easier to reason about, test and debug. Since they always produce the same output for a given input, they make the code more predictable and easier to maintain.

## What is immutability?
Immutability refers to the property of a data structure that once it is created, it cannot be modified. In functional programming, immutable data structures are preferred over mutable data structures as they allow for safer and more predictable code.

## What is Referential transparency?
Referential transparency is a property of a function that states that it can be replaced with its output without changing the behavior of the program. This means that given the same input, the function will always produce the same output and can be used anywhere in the program without any side effects.

*** 

## Node JS Tutorial for Beginners #6 - Modules and require()

### What is a module?
A module is a file containing JavaScript code that can be used in other files. Modules help to organize code into reusable and maintainable pieces.

### What does the word ‘require’ do?
‘require’ is a built-in Node.js function that allows us to load modules into our program. It searches for a module with the given name and returns the object exported by that module.

### How do we bring another module into the file that we are working in?
We can use the ‘require’ function followed by the name of the module we want to import. For example, to import a module named ‘math.js’, we can write ‘const math = require(‘./math’);’ in our JavaScript file.

### What do we have to do to make a module available?
To make a module available, we need to export it. We can export a module by assigning an object to the `module.exports` property or by exporting individual functions or objects using the `exports` object.
