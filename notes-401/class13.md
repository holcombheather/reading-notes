# Message Queues

## Quick Links
- [Socket.io Emit Cheatsheet](https://socket.io/docs/v4/emit-cheatsheet/)

## [Socket.io Chat Example](https://socket.io/get-started/chat/)

1. Explain to a non-technical recruiter what the Chat Example (above) does.

It is a demo of a chat application built using Socket.IO, a JavaScript library for real-time web applications. It allows users to communicate with each other in real-time by sending and receiving messages instantly.

1. What proof of life are we getting on the backend from the above app?

Proof of life on the backend in this context refers to receiving data or events from the frontend. In the Chat Example, the backend receives messages from the frontend when a user sends a chat message. This serves as proof that the backend server is actively running and capable of handling incoming events.

1. Socket.IO gives us the i0.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?



## [Rooms](https://socket.io/docs/v4/rooms)

1. What is a room and how might a room be useful?

  To send a message to everyone except for a certain emitting socket, you can use the `io.to(room).emit()` method instead of `io.emit()`. By specifying a room as an argument, the message will be broadcast to all sockets in that room except the emitting socket.

1. How do you join a room?

  `socket.join(room)`

1. How do you leave a room?

  `socket.leave(room)`


## [Namespaces](https://socket.io/docs/v4/namespaces/)

1. What is a Namespace and what does it allow you to do?

A Namespace in Socket.IO is a separate communication channel that allows you to segment the application's functionality or separate different groups of clients. It allows you to create isolated communication contexts within the same server instance.

1. Each namespace potentially has its own what? (hint: 3 things)

Each Namespace potentially has its own events, rooms, and connected clients. This means you can define different events, create separate rooms, and have distinct sets of clients connected within each Namespace.

1. Discuss a possible use case for separate namespaces

A possible use case for separate namespaces could be building a multi-tenant application where different organizations or user groups require their own isolated communication channels. Each Namespace could represent a different organization or user group, enabling separate communication and event handling for each group within the same application.

