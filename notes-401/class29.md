# Advanced State with Reducers

## [Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)

1. **What is the motivation for adding a reducer?**

   - Reducers are used to handle complex state logic that involves multiple sub-values or when the next state depends on the previous one. They also allow for more predictable and testable state updates by centralizing the state update logic.

2. **What are actions in the context of a reducer? How are they different than setting state directly?**

   - In the context of a reducer, actions are objects that contain information about what happened and what needs to change. They typically have a `type` property that indicates the type of action to be performed, and other properties to carry any additional information required for the update.

   - This approach is different from setting state directly because actions provide a clear, predictable way of describing state changes. Rather than directly mutating state, you're dispatching actions that describe the mutation, which are then handled by the reducer function.

3. **What common list operation is useReduce named for, and why?**

   - `useReducer` is named after the `reduce` method available on JavaScript arrays. The `reduce` method takes a list (array) and reduces it down to a single value by applying a function (the reducer) to each element of the array. Similarly, `useReducer` takes a series of actions (analogous to the array) and a reducer function and applies the reducer to each action to produce a single state value.

4. **When should you switch from useState to useReducer?**

   - It's often beneficial to switch to `useReducer` when the state logic becomes complex, when you have multiple sub-values to handle, or when the next state depends on the previous one. 

   - It's also useful when you need to pass down the state-updating function deep into the component hierarchy, as dispatching actions with `useReducer` can make the code easier to understand and maintain than callbacks to `setState`.
