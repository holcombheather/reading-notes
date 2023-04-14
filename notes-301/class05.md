# Putting it all together


## React Docs - Thinking in React

1. The single responsibility principle is a software development principle that states that a component should have only one reason to change. In other words, a component should have only one job or responsibility. This applies to components in React because it helps keep them simple, reusable, and maintainable.

2. Building a "static" version of your application means creating a version of your application that doesn't have any interactivity or dynamic behavior. It's a version of your application that just displays the data that you pass into it.

3. Once you have a static application, you need to add interactivity by adding stateful behavior to your components. This involves identifying which components need to be stateful, and determining what kind of state they need to manage.

4. The three questions you can ask to determine if something is state are:

    1. Is it passed in from a parent via props? If so, it probably isn't state.
    2. Does it remain unchanged over time? If so, it probably isn't state.
    3. Can you compute it based on any other state or props in your component? If so, it probably isn't state.

5. You can identify where state needs to live by following these steps:
    - Identify every component that renders something based on that state.
    - Find a common owner component (a single component above all the components that need the state in the hierarchy).
    - Either the common owner or another component higher up in the hierarchy should own the state.
    - If you can't find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

*** 

## Higher-Order Functions:

1. A "higher-order function" is a function that takes one or more functions as arguments, and/or returns a function as its result.

2. The `greaterThan` function defined in the reading takes a number as an argument and returns a new function. Line 2 of the function is creating a new function that takes a single argument `n`, and returns `n > number`. This new function is then returned by the `greaterThan` function, effectively creating a new function that can be used to test if a number is greater than the original number passed in as an argument.

3. `map` and `reduce` are higher-order functions that operate on arrays. `map` takes a function as an argument and applies that function to each element of the array, returning a new array with the results. `reduce` takes a function as an argument that combines each element of the array into a single value, and returns that value. Both `map` and `reduce` allow you to write more concise and expressive code by abstracting away common array operations into higher-order functions.