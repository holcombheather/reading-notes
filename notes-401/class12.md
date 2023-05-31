# Socket.io

## Quick Links & Bookmarks
- [Socket.io Documentation](https://socket.io/docs/)

- [Socket.io Server API](https://socket.io/docs/server-api)

- [Socket.io Client API](https://socket.io/docs/client-api)

- [Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)

## Web Sockets

1. What is a Web Socket?

  Web Sockets are a protocol for two-way communication between a client and a server over a single, long-lived connection. They're part of the HTML5 specification and allow for messages to be passed back and forth while keeping the connection open, providing a mechanism to establish a persistent connection for real-time applications.

1. Describe the Web Socket request/response handshake and what happens once the connection is established.

  The handshake process for a WebSocket connection starts with an HTTP request-response. The client sends an HTTP request to the server with an "Upgrade: websocket" header. If the server supports WebSockets, it responds with an "HTTP/1.1 101 Switching Protocols" status code, effectively transforming the connection from HTTP to WebSocket. Once this handshake process is complete, the connection remains open for the duration of the client-server interaction, allowing two-way communication without the need for repeated request-response pairs.

1. Web Sockets provide a standardized way for the server to send content to a client without first receiving a ____ from that client.

  Web Sockets provide a standardized way for the server to send content to the client without first receiving a request from that client. This capability enables the server to push updates to the client as soon as they are available, creating opportunities for real-time applications such as chat systems, online gaming, live data feeds, etc.

## Socket.io Tutorial

1. What does the event handler io.on() do?

  The io.on() function in Socket.io is an event handler that listens for specific events. This function usually takes two arguments: the name of the event to listen for, and a callback function that is triggered when that event is detected.

1. Describe some possible proof of life or proof that the code works as expected

  To test and demonstrate that your Socket.io code is working as expected, you could write a series of tests that simulate different events and check if the appropriate responses are triggered. You can also use logging or console outputs to see when certain events are being triggered or certain states are reached.

1. What does socket.emit() do?

  The socket.emit() function in Socket.io is used to emit events from the server to the client or vice versa. It typically takes two arguments: the name of the event to emit, and data to send with the event.


## Socket.io vs Web Sockets

1. What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).

  Socket.IO and WebSockets serve similar purposes, but Socket.IO is more like a library that uses WebSockets under the hood, among other transport protocols, for real-time communication. Comparing them to Git and GitHub or OAuth and Auth0, WebSockets is like Git or OAuth -- it's a protocol or a technology. Socket.IO, like GitHub or Auth0, is a framework or a service that leverages that technology, but provides a lot of additional features and ease of use.

1. When would you use Socket.IO?

  You might choose to use Socket.IO when you need real-time functionality but also require a higher-level API with features like broadcasting, namespaces, and room-based segregation of connections. Socket.IO also provides fallback options for browsers that do not support WebSockets.

1. When would you use WebSockets?

  On the other hand, you might opt to use plain WebSockets when you need real-time functionality, but your use case is simple and does not require the extra features provided by Socket.IO. WebSockets might also be the choice if you need to use less data and have fewer dependencies, or if you are working with platforms where Socket.IO isn't available.

## [OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)

1. What are a couple of key takeaways from this video?

  The Open Systems Interconnection (OSI) model is a conceptual model used to understand and describe how different network protocols interact and work together to provide network services. The model has seven layers, each representing a specific network function. These are, from top to bottom:

  - Application
  - Presentation
  - Session
  Transport
  Network
  Data Link
  Physical

## [TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)

1. Translate the gist of this video to a non-technical friend