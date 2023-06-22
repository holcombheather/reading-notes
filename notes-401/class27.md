# useState() Hook

## [Thinking in React](https://react.dev/learn/thinking-in-react)

1. **Summarize the five steps of thinking in React**:

   - **Step One: Break The UI Into A Component Hierarchy**: The first step is to draw boxes around every component and subcomponent in the mock and give them all names.

   - **Step Two: Build A Static Version in React**: Build a version that takes your data model and renders the UI but has no interactivity.

   - **Step Three: Identify The Minimal (but complete) Representation Of UI State**: Identify the minimal set of mutable state your application needs.

   - **Step Four: Identify Where Your State Should Live**: Identify which component mutates, or owns, this state.

   - **Step Five: Add Inverse Data Flow**: If you're trying to change a component's state from another component, pass a function from the state-owning component to the component that triggers the change.


## [State: A component's memory](https://react.dev/learn/state-a-components-memory)


2. **What is one reason a local variable isn’t sufficient for managing a React component?**

   - A local variable wouldn't cause a component to re-render when its value changes. State variables in React, however, trigger a re-render when their values are updated.

3. **What is the argument to the useState hook, and what are the two parts of its return array?**

   - The argument to the `useState` hook is the initial state. This can be any data type (number, string, object, array, etc.).

   - The hook returns an array with two elements. The first element is the current state value, and the second element is a function to update the current state value.

4. **How can Component A access state from Component B?**

   - Generally, React components cannot directly access the state of other components. However, there are a few ways to share state:

     - Lift the state up: The most common way is to move the state to a shared parent component, and then pass the state and state updating function down to both Component A and Component B as props.

     - Use context: If the components are deeply nested and passing props is getting too complex, you could use the Context API to create a shared state for all components in a component tree.

     - Use Redux or similar state management libraries: For even more complex applications, you could use a library like Redux to manage global application state and allow any component to access or update any piece of state.


