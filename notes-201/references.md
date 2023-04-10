# JavaScript Structure
1. Declare Global Variables
2. Declare Constructor functions - name should be capitalized!
3. Declare prototype methods
4. Declare regular functions
5. Add event listeners
6. Call functions

```javascript 
//declare global variables at the top of your file 

const globalVariable1 = ‘hello’; 
const globalVariable2 = [0, 1, 2]; 
const myForm = document.getElementById(‘my-form’);

//create an instance of PersonConstructor and save it to the sam variable (note that we can do this before the constructor function declaration)

const sam = new PersonConstructor(‘Sam’, ‘Hamm’); 

//now 

sam = { firstName: ‘Sam’, lastName: ‘Hamm’ }

//then put any object constructors 

function PersonConstructor(first, last) { 
    this.firstName = first; 
    this.lastName = last;
}

//then put any prototype functions that go with the object constructor 
//call this function on an instance of PersonConstructor

PersonConstructor.prototype.sayHello = function() { 
    console.log(‘Hello, my name is ‘ + this.firstName); 
}

//then put regular function declarations 

function firstFunction(parameter) { 
    console.log(parameter);
}

function secondFunction(myArray) { 
    for (i = 0; i < myArray.length; i++) { 
        console.log(myArray[i]); 
    }
}

function formHandler(event) { 
    console.log(event.target);
}

//then add any event listeners 

myForm.addEventListener(‘submit’, formHandler);

//finally, call your functions 

firstFunction(globalVariable1); //logs ‘hello’ 
secondFunction(globalVariable2); //logs 0 // 1 // 2 
sam.sayHello(); //logs ‘Hello, my name is Sam’

```

****

This is object-oriented programming in JavaScript at its most fundamental level.

1. The new keyword instantiates (i.e. creates) an object.
2. The constructor function initializes properties inside that object using the this variable.
3. The object is stored in a variable for later use.

### Domain Modeling Summary

Summary
Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

Here's some tips to follow when building your own domain models.

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.

***

### Prototypes

**Objects** 

* Objects are key/value pairs. The most common way to create an object is with curly braces {} and you add the properties and methods to an object using dot notation. 

**Functional Instantiation with Shared Methods** 

* By moving shared methods to their own object and refernce that object inside of our constructor function, we've now solved the problem of memory waste from overly large objects. 

**Object.create**
* `Object.create` allows you to create an object which will delegate to another object on failed lookups. Put differently, Object.create allows you to create an object and whenever there's a failed property lookup on that object, it can consult another object to see if that other object has the property. That was a lot of words. Let's see some code.


