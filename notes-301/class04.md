# React and Forms

***

## React Docs - Forms:

1. A controlled component is a form input element whose value is controlled by React's state. When the user interacts with a controlled component, the value of the input is updated through a change handler, which updates the component's state, and then the updated state is passed down as props to the controlled component. This ensures that the React component always has the current value of the input element.

2. It's generally best to update the state with the user's responses as soon as they enter them, rather than waiting until they submit the form. This allows for immediate validation and feedback to the user, which can improve the user experience. It also makes it easier to implement features such as real-time form validation and conditional rendering of form elements.

3. We can target what the user is entering by accessing the value property of the event target, which represents the input element that triggered the event. For example, if we have an event handler on an input field with the name "username", we can target what the user is entering like this:

      ```handleInputChange(event) {
        const target = event.target;
        const name = target.name;
        const value = target.value;
        this.setState({
          [name]: value
        });
      }
***

## The Conditional (Ternary) Operator Explained:

1. We use the ternary operator to write concise and readable conditional statements. It's often used as a shorthand for an if/else statement.

2. The statement using a ternary operator would be:

      `console.log(x === y ? true : false);`

    This is equivalent to the original if/else statement. If x is equal to y, the ternary operator will evaluate to true, and if they are not equal, it will evaluate to false. 