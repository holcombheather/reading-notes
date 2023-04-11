# React: State and Props

## React Lifecycle:

1. The very first thing to happen in the lifecycle of React is the 'constructor' method.
2. The 'render' method comes after the 'constructor' method, but before the 'componentDidMount' method.
3. The order of the React lifecycle methods is: constructor, render, componentDidMount, React Updates, componentWillUnmount.
4. The 'componentDidMount' method is called once the component is mounted or rendered on the DOM. This method is commonly used to fetch data or set up event listeners.

***

## React State Vs Props:

1. Props can be used to pass any type of data (strings, numbers, arrays, objects, functions, etc.) from a parent component to a child component.
2. The big difference between props and state is that props are immutable and are passed down from parent to child components, while state is mutable and is managed within a component.
3. We re-render our application when the state or props of a component change.
4. Some examples of things that we could store in state are: user input values, fetched data, loading status, error messages, and UI flags.
