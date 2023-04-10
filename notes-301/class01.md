# Introduction to React and Components

## Component-Based Architecture

1. What is a “component”?

    A "component" is a modular and independent unit of software that can be used and reused in various systems or applications. It is a software element that encapsulates certain functionalities and properties that can be utilized by other components or systems.


2. What are the characteristics of a component?

    - Encapsulation: components have clearly defined boundaries and only expose necessary interfaces to interact with other components or systems.
    - Reusability: components are designed to be easily used and reused in different contexts.
    - Replaceability: components can be replaced or updated without affecting the entire system or other components.
    - Independent deployment: components can be deployed independently from other components, allowing for easier maintenance and updates.
    - Composability: components can be combined or composed to form larger, more complex systems or applications.


3. What are the advantages of using component-based architecture?

    - Increased productivity: components can be reused, saving time and effort in development.
    - Improved maintainability: components can be updated or replaced independently, without affecting the rest of the system or other components.
    - Higher quality: components are designed to be modular and independent, which can lead to higher quality code.
    - Flexibility: components can be easily composed or decomposed, allowing for greater flexibility in system design.
    - Better collaboration: components can be developed and tested independently, allowing for easier collaboration between teams or developers.

***

### What is Props and How to Use it in React

1. What is “props” short for?

    "Props" is short for "properties" and refers to a way of passing data from a parent component to a child component in React.

2. How are props used in React?

    Props are used in React by passing data or values as attributes to a child component within the parent component's JSX. The child component can then access and use these props as necessary. For example, in the parent component's JSX, the child component might be written as `<ChildComponent prop1="value1" prop2="value2" />`. Within the child component, the props can be accessed using `props.prop1` and `props.prop2`.

3. What is the flow of props?

    The flow of props is unidirectional, meaning they are passed from parent components to child components, but cannot be passed back up to the parent. This helps to maintain the encapsulation and modularity of each component.


***

## Bookmark and Review
- React Tutorial through ‘Passing Data Through Props’
- React Docs - Hello world
- React Docs - Introducing JSX
- React Docs - Rendering elements
- React Docs - Components and props