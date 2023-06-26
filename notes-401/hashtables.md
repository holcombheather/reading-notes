# Hash Tables Cheat Sheet

[Video](https://www.youtube.com/watch?v=MfhjkfocRR0)

**Definition:**
A hash table (also known as a hash map) is a data structure that implements an associative array abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index into an array of buckets or slots, from which the desired value can be found.

**Hash Table Basics in JavaScript:**

JavaScript doesn't have a built-in Hash Table class, its built-in Object data type is essentially a hash table.

1. **Create a new hash table:**

```javascript
let hashTable = {};
// or
let hashTable = new Object();
```

2. **Insert a new key-value pair:**

```javascript
hashTable["key"] = "value";
// or
hashTable.key = "value";
```

3. **Retrieve a value by its key:**

```javascript
let value = hashTable["key"];
// or
let value = hashTable.key;
```

4. **Check if a key exists in the hash table:**

```javascript
if ("key" in hashTable) {
  // do something
}
// or
if (hashTable.hasOwnProperty("key")) {
  // do something
}
```

5. **Delete a key-value pair:**

```javascript
delete hashTable["key"];
// or
delete hashTable.key;
```

6. **Iterate over keys in the hash table:**

```javascript
for (let key in hashTable) {
  if (hashTable.hasOwnProperty(key)) {
    console.log(key + " -> " + hashTable[key]);
  }
}
```

7. **Get all keys:**

```javascript
let keys = Object.keys(hashTable);
```

8. **Get all values:**

```javascript
let values = Object.values(hashTable);
```

9. **Get the size of the hash table:**

```javascript
let size = Object.keys(hashTable).length;
```

**Methods**

Methods
For the hashtable to work there are a few methods that we should implement:
1. `add()`: This method should hash the key and add the key and value pair to the table.
2. `get()`: This method should hash the key, locate the correct bucket, and retrieve the value associated with that key.
3. `contains()`: This checks if a key is in the table.
4. `hash()`: This method should conduct the actual hashing of the key.

Here's an implementation example for these methods:

```javascript
class Hashtable {
  constructor(size = 53) {
    this.keyMap = new Array(size);
  }

  _hash(key) {
    let total = 0;
    let WEIRD_PRIME = 31;
    for (let i = 0; i < Math.min(key.length, 100); i++) {
      let char = key[i];
      let value = char.charCodeAt(0) - 96
      total = (total * WEIRD_PRIME + value) % this.keyMap.length;
    }
    return total;
  }

  set(key,value){
    let index = this._hash(key);
    if(!this.keyMap[index]){
      this.keyMap[index] = [];
    }
    this.keyMap[index].push([key, value]);
  }

  get(key){
    let index = this._hash(key);
    if(this.keyMap[index]) {
      for(let i = 0; i < this.keyMap[index].length; i++){
        if(this.keyMap[index][i][0] === key) {
          return this.keyMap[index][i][1]
        }
      }
    }
    return undefined;
  }

  contains(key) {
    let index = this._hash(key);
    if(this.keyMap[index]) {
      for(let i = 0; i < this.keyMap[index].length; i++){
        if(this.keyMap[index][i][0] === key) {
          return true
        }
      }
    }
    return false;
  }
}
```

With this basic Hashtable, you can create a hashtable, add key-value pairs to the table, retrieve the value for a given key, and check if a key exists in the table. This is a basic implementation, in a real-world scenario, you would also have to deal with collision resolution strategies such as chaining (as is done here) or open addressing and potentially resizing the hashtable when it gets too full or sparse. 

It's also worth noting that JavaScript's built-in objects are basically hash tables, as they are collections of key-value pairs. For instance, the methods `Object.hasOwnProperty`, `Object.keys`, and `Object.values` all work in O(1) time on average.

**Time Complexity:**

- Insertion: O(1)
- Retrieval: O(1)
- Deletion: O(1)

The time complexity is constant time for the average case for each of these operations, but keep in mind that in the worst-case scenario (when all keys hash to the same index), the complexity could be as bad as O(n), where n is the number of keys in the table. 

The JavaScript engine tries to manage this for you, but it's still good to be aware of the potential performance implications.

**Note:**
Remember that the property keys of objects are always strings. If you use any other type as a key, it will be converted to a string.
For example, if you use a number, boolean, or even another object as a key, it will be converted to a string before it is used.

For a more complex and customizable hash table, you'd likely need to create your own implementation with arrays and a hashing function.