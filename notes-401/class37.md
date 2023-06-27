# Redux - Combined Reducers

## [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)

**1. Why create multiple reducers?**

Creating multiple reducers helps in managing complex applications by segregating different parts of the application's state. It makes your codebase easier to maintain and understand because each reducer is responsible for managing a specific slice of the state.

**2. How would you combine multiple reducers?**

In Redux, multiple reducers can be combined using the `combineReducers` utility function. This function takes an object whose values are different reducing functions and turns it into a single reducing function that can be passed to the Redux `createStore` method.

Example:
```javascript
import { combineReducers } from 'redux';
import reducerA from './reducerA';
import reducerB from './reducerB';

const rootReducer = combineReducers({
  a: reducerA,
  b: reducerB
});

export default rootReducer;
```

**3. How will you manage state as an immutable object? Why?**

In Redux, we manage state as an immutable object by returning a new state object from our reducers whenever the state changes, rather than modifying the existing state object. This is important because it makes complex state updates easier to reason about, enables powerful debugging and developer tools like time-travel debugging, and helps to prevent difficult-to-track bugs caused by shared, mutable state.

## [Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)


**4. Redux Docs: Using Combined Reducers**

The sentence completion would be: "combineReducers is a utility function to simplify the most common use case when writing Redux reducers."

**5. Explain how combineReducers assembles the new state tree.**

The `combineReducers` function generates a function that calls your reducers with the slices of state selected according to their keys, and combines their results into a single state object. The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by `combineReducers()` namespaces the states of each reducer under their keys as passed to `combineReducers()`.

## [Redux Docs: Combined Reducers Syntax](https://redux.js.org/api/combinereducers/)

**6. How would you define initial state in an app using combineReducers?**

When you use `combineReducers`, you would define the initial state in the individual reducers. Each reducer defines its own slice of the initial state. The `combineReducers` function will call each reducer with `undefined` as the state, and whatever action you choose, in order to populate the state with the initial values.

**7. Redux Docs: Combined Reducer Syntax**

The sentence completion would be: "The `combineReducers` helper function turns an object whose values are different reducing functions into a single reducing function you can pass to `createStore`."

**8. What is a popular convention when naming reducers?**

A popular convention when naming reducers is to use the slice of state that they manage as their name. For example, a reducer managing the 'user' slice of state might be named 'userReducer'. This convention helps to keep the code base organized and clear about which reducer is managing which part of the state.