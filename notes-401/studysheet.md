Stacks
```
class Stack {
  constructor() {
    this.stack = [];
  }

  // Push an element to the top of the stack
  push(element) {
    this.stack.push(element);
  }

  // Remove and return the top element of the stack
  pop() {
    if(this.isEmpty()) {
      throw new Error("Stack is empty");
    }
    return this.stack.pop();
  }

  // Get the top element of the stack
  peek() {
    if(this.isEmpty()) {
      throw new Error("Stack is empty");
    }
    return this.stack[this.stack.length - 1];
  }

  // Check if the stack is empty
  isEmpty() {
    return !this.stack.length;
  }

  // Get the size of the stack
  size() {
    return this.stack.length;
  }
}
```

Queues
```
class Queue {
  constructor() {
    this.queue = [];
  }

  // Add an element to the end of the queue
  enqueue(element) {
    this.queue.push(element);
  }

  // Remove and return the first element of the queue
  dequeue() {
    if(this.isEmpty()) {
      throw new Error("Queue is empty");
    }
    return this.queue.shift();
  }

  // Get the first element of the queue
  front() {
    if(this.isEmpty()) {
      throw new Error("Queue is empty");
    }
    return this.queue[0];
  }

  // Check if the queue is empty
  isEmpty() {
    return !this.queue.length;
  }

  // Get the size of the queue
  size() {
    return this.queue.length;
  }
}

```

HashTable

```
class HashTable {
  constructor(size=53) {
    this.keyMap = new Array(size);
  }

  _hash(key) {
    let total = 0;
    let PRIME_NUMBER = 31;
    for (let i = 0; i < Math.min(key.length, 100); i++) {
      let char = key[i];
      let value = char.charCodeAt(0) - 96;
      total = (total * PRIME_NUMBER + value) % this.keyMap.length;
    }
    return total;
  }

  set(key, value) {
    let index = this._hash(key);
    if(!this.keyMap[index]) {
      this.keyMap[index] = [];
    }
    this.keyMap[index].push([key, value]);
  }

  get(key) {
    let index = this._hash(key);
    if(this.keyMap[index]) {
      for(let i = 0; i < this.keyMap[index].length; i++) {
        if(this.keyMap[index][i][0] === key) {
          return this.keyMap[index][i][1];
        }
      }
    }
    return undefined;
  }
}

```

[link](/Users/heathergallagher/projects/courses/code-102/reading-notes/notes-401/studysheet.md)