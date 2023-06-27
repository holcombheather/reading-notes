# React - Context API

[**Choosing the State Structure**](https://react.dev/learn/choosing-the-state-structure)

When structuring state in your applications, the following five principles can guide you:

  1. **Colocate state as much as possible**: Keep state as close as possible to where it's being used. This makes your code easier to maintain because it's clear where the state is coming from and how it's being used.

  2. **Normalize complex state**: If your state has a complex structure, such as a deeply nested object or an array of objects, it can be beneficial to normalize it. Normalizing state often involves flattening it and removing redundancies, making it easier to manage and update.

  3. **Avoid duplicate state**: Redundancy in state can lead to inconsistencies and bugs. Each piece of data should be stored once and computed everywhere else it's needed.

  4. **Keep state read-only**: State should be treated as immutable. Instead of mutating state directly, create a copy of the state, make changes to the copy, and then replace the old state with the new one.

  5. **Think in state transitions**: Instead of mutating state based on its current value, think of state changes as transitions from one state to another based on actions.

[**Passing State Deeply with Context**](https://react.dev/learn/passing-data-deeply-with-context)

1. What problem do Contexts aim to solve? 
Contexts in React aim to solve the problem of "prop drilling" - passing down data through many layers of components. This can be cumbersome and makes your code hard to maintain, especially for global state that many components might need to access.

2. What is one technique to try before useContext? 
Before using `useContext`, consider if lifting the state up might solve the problem. Sometimes, you can move the state to a common ancestor component of the components that need the data, and pass the state down only a few levels.

3. What hook complements useContext for complex applications? 
For complex applications, the `useReducer` hook complements `useContext` well. `useReducer` allows you to manage complex state logic in a more manageable way by defining a reducer function to handle state transitions, which can be especially useful when there are complex state transitions or when the new state depends on the old one. Using `useContext` with `useReducer` allows you to provide the state and dispatch function throughout your component tree, enabling any component to read the state or dispatch actions.


## Helpful Links
- [Sharing State Between Components](https://react.dev/learn/sharing-state-between-components)
- [Preserving and Resetting State](https://react.dev/learn/preserving-and-resetting-state)