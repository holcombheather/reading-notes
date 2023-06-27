# Application State with Redux

## [Dan Abramov Redux Tutorials]()

**1. First Principle of Redux:**

The first principle of Redux is that the entire state of your application is stored in a single JavaScript object, which we call the state or the state tree.

**2. Redux Store and Reducers:**

A Redux Store is an object that brings together the state of your application, the action(s) that change the state, and the reducer(s) which control how state changes in response to an action. A store holds and manages the entire state tree of your application.

Reducers are functions that determine how the application's state changes in response to an action sent to the store. In essence, actions describe what happened, but they don't specify how the application's state changes in response; this is the job of reducers. Reducers take the current state and an action as arguments, and return a new state as a result.

**3. Three Redux Store Methods:**

The `createStore` function provided by Redux gives us access to several methods:

- `getState`: This method is used to access the current state held in the Redux store.

- `dispatch`: This method is used to dispatch actions to the Redux store. These dispatched actions are processed by the reducer to produce a new state.

- `subscribe`: This method adds a change listener function that will be called any time an action is dispatched, allowing you to react to the current state of the store. This is often used to trigger re-renders of your UI when the state changes.

**4. Explanation of combineReducers():**

Let's say our app is a big party, and the state of our app is like a big party planning checklist. combineReducers() is like our event coordinator. The event coordinator doesn't do all the jobs herself but delegates them to different teams. Each team focuses on their specific task, like catering, entertainment, or decorations. 

In our app, the state checklist is broken down into smaller parts (like 'user', 'posts', 'comments'). Each part is managed by a specific reducer (or team). The combineReducers() function is the event coordinator that brings all these teams together. It takes an object whose properties are different reducing functions (teams), and merges them into a single reducing function (the event coordinator). 

This is helpful because it allows us to split a complex reducer into smaller, more manageable reducers, each handling a specific part of the state. And that makes our app's code easier to understand and maintain.

## Links
- [Worlds easiest guide to redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)
- [Testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)
- [Redux Docs](https://redux.js.org/)