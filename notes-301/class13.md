# CRUD Basics

1. Which HTTP method would you use to update a record through an API?

    To update a record through an API, you would use the HTTP `PUT` method. 

2. Which REST methods require an ID parameter?

    The REST methods that require an ID parameter are `GET`, `PUT`, `DELETE`. 

***

## Videos
[Speed Coding: Building a CRUD API](https://www.youtube.com/watch?v=EzNcBhSv1Wo) (Watch a Twitch streamer code an Express API in 20 minutes!)

1. What’s the relationship between REST and CRUD?

    `CRUD` (Create, Read, Update, Delete) is a set of basic operations used to manage data in a database. `REST` (Representational State Transfer) is an architectural style that is used to design web services. The relationship between REST and CRUD is that CRUD operations can be mapped to RESTful HTTP methods, where each operation maps to a specific HTTP method.

2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?

    1. Identify the resources that will be exposed by the API.
    2. Define the endpoints (URLs) that will be used to access each resource.
    3. Determine the HTTP methods that will be used to perform operations on each resource (`GET`, `POST`, `PUT`, `DELETE`).
    4. Design the data model that will be used to represent each resource.
    5. Implement the API using a web framework or library (such as Express for Node.js) and test it using tools like Postman or curl.

***

