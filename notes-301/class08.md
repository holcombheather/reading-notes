# API Design Best Practices

1. REST stands for Representational State Transfer.
2. REST APIs are designed around a resource, which can be anything that can be represented in a web application, such as a user, a blog post, or an image.
3. An identifier of a resource is a unique URI (Uniform Resource Identifier) that identifies the resource. For example, in a blog application, the identifier of a blog post resource could be `/posts/1234`, where `1234` is the ID of the blog post.
4. The most common HTTP verbs are `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`.
5. URIs should be based on the resources they represent, not the actions that can be performed on those resources. For example, a URI should be `/posts/1234` instead of `/get_post?id=1234`.
6. A good URI should be descriptive, unique, and consistent with the naming conventions used throughout the API. For example, `/users/1234` is a good URI for the user with ID 1234.
7. Having a 'chatty' web API means that the API requires multiple requests to perform a single operation. This is generally a bad thing as it can increase the latency and decrease the performance of the API.
8. A successful GET request returns a status code of `200 OK`.
9. An unsuccessful GET request returns a status code of `404 Not Found`.
10. A successful POST request returns a status code of `201 Created`.
11. A successful DELETE request returns a status code of `204 No Content`.
