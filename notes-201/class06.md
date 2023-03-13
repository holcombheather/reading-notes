## JavaScript Object Basics:

#### How would you describe an object to a non-technical friend you grew up with?
- An object can be compared to a real-world object with different properties that describe its characteristics.
#### What are some advantages to creating object literals?
- Object literals are a convenient way to define objects with properties and methods.
#### How do objects differ from arrays?
- Objects are unordered collections of key-value pairs, while arrays are ordered lists of data.
# 
#### Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
- Bracket notation is used to access an object's property when the property name contains spaces or special characters or when the property name is stored as a variable.
##### Evaluate the code below. What does the term this refer to and what is the advantage to using this?

    const dog = {
    name: 'Spot',
    age: 2,
    color: 'white with black spots',
    humanAge: function (){
        console.log(`${this.name} is ${this.age*7} in human years`);
    }
    }

- Using this in a method allows for dynamic access to an object's properties.

## Introduction to the DOM:

#### What is the DOM?
- The DOM is a programming interface for HTML and XML documents, representing the structure of a web page as a tree of nodes.
#### Briefly describe the relationship between the DOM and JavaScript.
- JavaScript can be used to manipulate the elements and content of a web page by interacting with the DOM. 
- The DOM provides a way for JavaScript to access and manipulate the structure and content of a web page, making it a powerful tool for web development.