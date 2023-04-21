# In memory stage

## Understanding the JavaScript Call Stack

### What is a ‘call’?
In JavaScript, a 'call' refers to the process of invoking a function. When a function is called, it is added to the call stack, which keeps track of where the program is in its execution.

### How many ‘calls’ can happen at once?
JavaScript is single-threaded, meaning that only one call can be processed at a time. Calls are processed in the order they are added to the call stack, and each call must complete before the next one can be processed.

### What does LIFO mean?
LIFO stands for "Last In, First Out". In the context of the call stack, LIFO means that the most recently added call is the first one to be removed. In other words, the call stack operates like a stack of plates - the last one added is the first one removed.

### Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

Assume we have three functions, `a()`, `b()`, and `c()`, where `a()` calls `b()`, and `b()` calls `c()`.

        Call stack:
        c()
        b()
        a()


### What causes a Stack Overflow?
A stack overflow occurs when the call stack becomes too large, typically due to an infinite or excessively recursive function call. When this happens, the browser or runtime environment will throw a "Maximum call stack size exceeded" error.

### JavaScript error messages

#### What is a ‘reference error’?
A 'reference error' occurs when you try to access a variable or function that doesn't exist. This can happen if you misspell the name of the variable or function, or if it hasn't been declared yet.

#### What is a ‘syntax error’?
A 'syntax error' occurs when you write code that doesn't follow the syntax rules of the JavaScript language. This can happen if you forget a semicolon, use the wrong type of quotes, or write an invalid keyword.

#### What is a ‘range error’?
A 'range error' occurs when you try to use a value that is outside the range of acceptable values. For example, if you try to create an array with a negative length, or use a negative index to access an array element.

#### What is a ‘type error’?
A 'type error' occurs when you try to use a value of the wrong type. For example, if you try to call a method on a variable that isn't an object, or try to access a property on a string.

#### What is a breakpoint?
A 'breakpoint' is a point in your code where execution will pause when you run your program in a debugger. This allows you to step through your code line by line and inspect the values of variables at each step.

#### What does the word ‘debugger’ do in your code?
The 'debugger' statement is a keyword in JavaScript that tells the browser or runtime environment to pause execution at that point in the code. This allows you to inspect the call stack, variables, and other program state to help identify and fix bugs.
