# CRUD 

## Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:
    - 100's = Informational codes, used to indicate that the request has been received and understood by the server and that the client should continue with the request.
    - 200's = Success codes, used to indicate that the request has been successfully processed by the server.
    - 300's = Redirection codes, used to indicate that the requested resource is no longer available at the requested URL and has been moved to a new location.
    - 400's = Client error codes, used to indicate that there is a problem with the client's request, such as missing or invalid parameters.
    - 500's = Server error codes, used to indicate that there is a problem with the server's ability to process the request.

2. What is a status code 202?
    - Status code 202 means that the request has been accepted for processing, but the processing has not been completed yet.

3. What is a status code 308?
    - Status code 308 means that the requested resource has been permanently moved to a new URL, and the client should update its links to use the new URL.

4. What code would you use if an update didn’t return data to a client?
    - If an update didn't return data to a client, you would use the status code 204 No Content.

5. What code would you use if a resource used to exist but no longer does?
    - If a resource used to exist but no longer does, you would use the status code 410 Gone.

6. What is the ‘Forbidden’ status code?
    - The 'Forbidden' status code is 403, which is used when the server understands the request, but is refusing to fulfill it because the client does not have appropriate permissions.

***

## Build A REST API with Node.js, Express, & MongoDB - Quick
[Video](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
    - We need to pull our MongoDB database string out of our server and put it into our .env for security reasons, so that we can keep sensitive information separate from our codebase.

2. What is middleware?
    - Middleware is a function that sits between the request and the response, allowing us to modify the request or response as needed.

3. What does app.use(express.json()) do?
    - app.use(express.json()) is a middleware function that allows us to parse incoming JSON data in our requests.

4. What does the /:id mean in a route?
    - The /:id in a route is a URL parameter that allows us to dynamically specify the ID of a resource we want to manipulate.

5. What is the difference between PUT and PATCH?
    - The main difference between PUT and PATCH is that PUT is used to completely replace an existing resource with a new one, while PATCH is used to update an existing resource.

6. How do you make a default value in a schema?
    - To make a default value in a schema, we can use the 'default' keyword in the schema definition.

7. What does a 500 error status code mean?
    - A 500 error status code means that there was an internal server error, indicating that something went wrong on the server side.

8. What is the difference between a status 200 and a status 201?
    - The difference between a status 200 and a status 201 is that a status 200 means that the request has been successfully processed, while a status 201 means that a new resource has been created as a result of the request.
