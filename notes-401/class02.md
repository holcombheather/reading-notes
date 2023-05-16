# Express, NPM, TDD, CI/CD

## Quick Links & Resources
- nodeJS docs
- npm docs
- express docs
- http status codes
- supertest

***

### An Intro to NodeJS and Express

1. Explain middleware, answer as though I were a non-technical recruiter.

    Middleware is like a series of checkpoints that requests and responses pass through in an application. These checkpoints can perform various tasks, like checking if a user is logged in, validating data, or logging information for debugging purposes. Middleware helps to manage and streamline the flow of data between different parts of an application.

2. Express the most popular __ __ ____.

    **web application framework for Node.js**

3. Express is “unopinionated.” What does that mean?

    Being "unopinionated" means that Express does not force you to follow specific guidelines or conventions when building your application. This provides developers with the flexibility to choose how they structure their projects, which tools they use, and how they implement features.

4. What is a module and why is modularity useful to us as developers?

    A module is a self-contained piece of code that performs a specific function and can be easily integrated into a larger application. Modularity is useful because it helps us to organize code into smaller, reusable components, making the overall application easier to maintain, troubleshoot, and scale.

### What is NPM?

1. What version of npm are you running on your machine?

    9.6.4

2. What command would you type to install a library/package called ‘jshint’ into your node project?

    `npm install jshint` 

### What is TDD?

1. Explain why tests are important. Please explain as though I were your non technical elder.

    Tests are important because they ensure that the various parts of a software program work correctly and as expected. By writing tests, developers can catch errors early in the development process, making it easier to fix problems before they become more serious. This ultimately leads to more reliable software and a better user experience.

2. What are three expected benefits of testing

    - Improved code quality: Testing helps identify and fix issues early in the development process, resulting in more reliable and efficient code.
    - Easier maintenance: Well-tested code is easier to understand and modify, making it simpler to maintain and update in the future.
    - Faster development: Catching and fixing issues early on can save time and effort, allowing developers to focus on adding new features and functionality.

3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.

    - Individual pitfalls:
        - Writing tests after the code has been written, making it more difficult to catch issues early on.
        - Focusing on testing edge cases rather than the most common use cases, leading to less effective testing.

    - Team pitfalls:
        - Inconsistent testing methodologies across team members, leading to confusion and a lack of cohesion.
        - Insufficient communication about testing strategies and expectations, resulting in gaps in test coverage and potential issues being overlooked.


### CI/CD

1. What are three benefits of Continuous Integration?

    - Early error detection: By integrating code frequently, issues are identified and resolved early in the development process.
    - Improved collaboration: Continuous Integration encourages better communication and collaboration among team members.
    - Faster development cycles: The process of integrating and testing code becomes more efficient, allowing for quicker releases and updates.

2. What is the difference between Continuos Delivery and Continuous Deployment?

    Continuous Delivery is the practice of ensuring that code is always in a releasable state, while Continuous Deployment is the automated process of deploying code to production once it passes all required tests. Continuous Delivery prepares the code for deployment, but the actual deployment may still require manual approval. Continuous Deployment, on the other hand, automates

3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background

    In the context of Continuous Integration and Continuous Deployment, GitHub plays a crucial role by providing a centralized location for the code. Developers can push their changes to GitHub, which then triggers automated testing and, if applicable, deployment processes. This ensures that the latest code changes are always tested and, if they pass all the tests, can be automatically deployed to the production environment.

    GitHub serves as the hub for code collaboration, version control, and integration with CI/CD tools.



***

## Reflection

1. What are your learning goals after reading and reviewing the class README?
    - Successfully incorporate application level middleware
    - Familiarize myself with the concepts and syntax for express routing

