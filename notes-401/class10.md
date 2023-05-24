# Stacks and Queues Cheat Sheet

## Stacks
- A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
- **Common Terminology:**
  - **Push:** Add nodes or items into the stack.
  - **Pop:** Remove nodes or items from the stack. Raises an exception when stack is empty.
  - **Top:** The top of the stack.
  - **Peek:** View the value of the top Node in the stack. Raises an exception when stack is empty.
  - **IsEmpty:** Returns true when stack is empty, otherwise returns false.
- **Key Concepts:** FILO (First In Last Out), LIFO (Last In First Out).
- Operations are typically O(1) since they depend only on the top element, not on the number of elements in the stack.

## Queues
- A queue is a data structure where the first element inserted is the first one to be removed (FIFO).
- **Common Terminology:**
  - **Enqueue:** Add nodes or items to the queue.
  - **Dequeue:** Remove nodes or items from the queue. Raises an exception when the queue is empty.
  - **Front:** The first Node of the queue.
  - **Rear:** The last Node of the queue.
  - **Peek:** View the value of the front Node in the queue. Raises an exception when the queue is empty.
  - **IsEmpty:** Returns true when queue is empty, otherwise returns false.
- **Key Concepts:** FIFO (First In First Out), LILO (Last In Last Out).
- Operations are typically O(1) as they deal with either the front or rear of the queue, regardless of the number of elements in the queue.

## Pseudocode Examples

- **Push onto Stack**
```
ALGORITHM push(value)
    node = new Node(value)
    node.next <-- Top
    top <-- Node
```
- **Pop from Stack**
```
ALGORITHM pop()
    Node temp <-- top
    top <-- top.next
    temp.next <-- null
    return temp.value
```
- **Peek at Stack**
```
ALGORITHM peek()
    return top.value
```
- **Check if Stack is Empty**
```
ALGORITHM isEmpty()
    return top = NULL
```
- **Enqueue to Queue**
```
ALGORITHM enqueue(value)
    node = new Node(value)
    rear.next <-- node
    rear <-- node
```
- **Dequeue from Queue**
```
ALGORITHM dequeue()
    Node temp <-- front
    front <-- front.next
    temp.next <-- null
    return temp.value
```
- **Peek at Queue**
```
ALGORITHM peek()
    return front.value
```
- **Check if Queue is Empty**
```
ALGORITHM isEmpty()
    return front = NULL
```
