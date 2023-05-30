# Event Driven Applications

## Event Driven Programming
1. What native Node.js module allows us to get started with Event Driven Programming?
    - Event-driven programming in Node.js is facilitated through the `EventEmitter` class, which is part of the built-in `events` module. 
    - The EventEmitter allows us to create objects that emit named events whenever a particular action occurs in our application. 
    - Other parts of our application can then listen for these named events and run associated callback functions (known as "event handlers") when those events are detected. 
    - A simple example of this is a chat room scenario, where an event could be a new user joining a chat room. 

1. What is the value of Object Oriented Programming used in tandem with Event Driven Programming?

    - Combining Object-Oriented Programming (OOP) with Event-Driven Programming (EDP) can help to structure your code in a way that keeps related behavior and data together (in objects), and also allows these objects to react to events.
    - OOP promotes encapsulation, where an object's behavior is handled from code within that object. 
    - Meanwhile, EDP allows objects to emit events and other objects to react to those events. 
    - This can be very powerful, as objects don't need to know about each other's implementation details; they just need to know which events to emit or listen for.

1. Consider your knowledge of Event Driven Programming in the Web Browser, now explain to a non-technical friend how Event Driven Programming might be useful on the backend using Node.js.

    - Event-Driven Programming is similar to a series of reactions that are triggered by particular events. Take your daily routine: waking up in the morning triggers a series of actions like brushing your teeth, eating breakfast, etc. Think of these actions as event handlers and each of the events trigger its own set of actions like eating breakfast triggers cooking, doing dishes, etc. 

***

## Bookmark and Review
- [Node docs: events](https://nodejs.org/api/events.html)
- [Event Driven Programming Article](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)

***

## Cheat Sheet

**1. Importing EventEmitter**

```javascript
const EventEmitter = require('events').EventEmitter;
```

**2. Creating an instance of EventEmitter**

```javascript
const myEmitter = new EventEmitter;
```

**3. Defining an Event Listener**

Event listeners are functions that will be executed when a certain event is emitted. They can be added with `.on(eventName, listenerFunction)` or `.addListener(eventName, listenerFunction)`.

```javascript
myEmitter.on('someEvent', function() {
  console.log('someEvent occurred!');
});
```

**4. Emitting an Event**

Events can be emitted with `.emit(eventName)`.

```javascript
myEmitter.emit('someEvent'); // Logs 'someEvent occurred!' to the console
```

**5. Removing a Listener**

Event listeners can be removed with `.removeListener(eventName, listenerFunction)` or `.off(eventName, listenerFunction)`.

```javascript
function eventResponse() {
  console.log('someEvent occurred!');
}

myEmitter.on('someEvent', eventResponse);
myEmitter.removeListener('someEvent', eventResponse);
```

**6. Removing All Listeners for an Event**

All listeners for an event can be removed with `.removeAllListeners([eventName])`. If no event name is provided, all listeners for all events are removed.

```javascript
myEmitter.removeAllListeners('someEvent');
```

**7. Listening for an Event Only Once**

Listeners can be added that are triggered only once and then removed with `.once(eventName, listenerFunction)`.

```javascript
myEmitter.once('someEvent', function() {
  console.log('someEvent occurred once!');
});
```

**8. Getting the Count of Listeners for an Event**

The number of listeners listening to a particular event can be retrieved with `.listenerCount(eventName)`.

```javascript
console.log(EventEmitter.listenerCount(myEmitter, 'someEvent'));
```

Remember to replace `'someEvent'` and `eventResponse` with the names of your actual events and functions. These are just examples.

This should cover most of the common operations with `EventEmitters`. For more in-depth information, you can refer to the [Node.js EventEmitter documentation](https://nodejs.org/api/events.html).

***

## Reflection

1. I'm looking forward to learning about network events. 
2. My learning goals are understand and implement the Observer pattern using Publish/Subscribe and create a modular, event based system. 