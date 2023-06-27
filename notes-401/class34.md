# API Integration

## [Review API Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/)

**Difference Between Query String Parameter and Path Parameter**:

Query string parameters and path parameters are two ways to pass information from the client to the server in a HTTP request.

1. **Path Parameter**: Path parameters are part of the URL itself. They're typically used to identify a specific resource or a group of resources. For example, in the URL "http://our-site.com/users/123", "123" is a path parameter that likely identifies a user with ID 123.

2. **Query String Parameter**: Query string parameters are appended to the end of the URL, following a question mark. They're usually used to sort/filter resources or to provide additional context. For example, in the URL "http://our-site.com/users?sort=asc", "sort=asc" is a query string parameter that might sort the users in ascending order.

**API URL with Path ID Parameter**:

Given the provided information, your API URL would look like this:

```
http://our-site.com/v3/stuff/things
```

Here "v3" indicates the version of the API, "stuff" is the model name and "things" is the id of a specific resource.

**Explaining Interface of a Dynamic API to a Non-Technical Friend**:

Imagine you have a large box filled with a lot of smaller boxes, each with a unique label. You want to find a specific small box, but you don't want to dig through all the other boxes to find it. That's where the 'interface' comes in. It's like a tool or assistant that can quickly find the box you want. You just tell the interface what you're looking for (like the label of the box), and it does the work for you.

## [Review Auth Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/)

**Using Middleware for Basic and Bearer Auth**:

Middleware in the context of web servers is software that sits in-between the client's request and the server's response.

- For Basic Auth, the client sends a username and password with each request. The server then verifies these credentials before responding. Middleware can be created to intercept these requests, verify the username and password, and then either continue the request to the intended route (if credentials are valid) or send an error response.

- Bearer Auth is a bit more complex. Here, the client first authenticates with the server (often using Basic Auth) and receives a token. This token is sent with all future requests as proof of authentication. Again, middleware can intercept requests, verify the token, and then either continue the request or send an error response.

**Handshake for Implementing OAuth**:

OAuth is a protocol that allows a user to grant a third-party website or application access to their information, without sharing their password. Here's a simplified version of the "handshake" process:

1. The third-party app redirects the user to the service provider (like Google or Facebook).
2. The user logs in to the service provider and authorizes the third-party app.
3. The service provider redirects the user back to the third-party app, along with a special code.
4. The third-party app uses this code to request an access token from the service provider.
5. The service provider sends back the access token, which the third-party app can use to access the user's information.

**Explaining Role Based Access Control to a Non-Technical Friend**:

Imagine a security system at a large company. Every employee has an ID card that they swipe to enter different rooms. Not all employees can enter every room - the CEO can go anywhere, a manager might have access to certain strategic rooms, and a regular employee may only have access to the work floors and cafeteria.

This is similar to how role-based access control (RBAC) works in a computer system. When you log in

, you are assigned a role (like employee, manager, or CEO). Depending on your role, you can access different parts of the system (like viewing, creating, or deleting data). The system checks your "ID card" (role) every time you try to do something, to make sure you have the right access.


