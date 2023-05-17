# Express REST API

Review: ES6 Classes

1. Classes are a template for creating ____.
    objects or instances 

2. Can a class declaration be hoisted?
    No you have to declare the class before using it in your code. 

3. How would you describe a constructor and contextual “this” to a non-technical friend?
    A constructor sets up the initial state of the object and "this" is a way to point to the object itself and allows you to modify its properties and methods. 

Using Express Routing

1. Within Express, what does routing refer to?
    Routing refers to the process of taking an incoming request and routing or passing it to the correct handler function or code to process the request and return a response. 

2. What is the difference between a route path and a route method?
    Route path defines the URL pattern for a specific route and contains placeholders, parameters, and optional segments like `/task/:id`. Route method is the HTTP method associated with a route like GET, POST, PUT, DELETE, etc. 


3. When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?
    It's appropiate to use `next` as a parameter to route handler when you need to do some initial processing in your middleware and then pass it on to the next handler for further processing. You need to invoke it in order to pass to your middleware with `next()`. 

Express Routing

1. What is an Express Router?
    A router allows you to create resuable and modular sets of routes. 

2. By what mean do we initialize express.Router() in an express server?

    ```
    const express = require('express');
    const router = express.Router();
    ```

3. What do we use route middleware for?
    Route middleware is used for inital processing on an incoming request or response before they reach the final route handler. Common use cases include authentication, data validation, error handling, logging, etc. 



Reflection
- Learn syntax and familiarize myself with external (modular) routing with Express 
