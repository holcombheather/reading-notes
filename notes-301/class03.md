# Passing Functions as Props

## Lists and Keys

1. .map() returns a new array with the results of calling a provided function on every element in the original array.
2. To loop through an array and display each value in JSX, you can use the .map() method in combination with JSX syntax.
3. Each list item needs a unique "key".
4. The purpose of a key is to help React identify which items in a list have changed, been added, or been removed. Keys should be unique to each item in the list.

## The Spread Operator

1. The spread operator is a syntax for expanding an iterable (e.g., an array, string, or object) into a list of arguments.
2. The spread operator can be used to: copy arrays, merge arrays, add items to arrays, pass arguments to functions, and copy objects.
3. Example of using the spread operator to combine two arrays:

        const arr1 = [1, 2, 3];
        const arr2 = [4, 5, 6];
        const combinedArr = [...arr1, ...arr2];
        console.log(combinedArr); // [1, 2, 3, 4, 5, 6]
        
4. Example of using the spread operator to add a new item to an array:

        const oldArr = [1, 2, 3];
        const newArr = [...oldArr, 4];
        console.log(newArr); // [1, 2, 3, 4]
5. Example of using the spread operator to combine two objects into one:

        const obj1 = { name: 'John', age: 30 };
        const obj2 = { gender: 'male', profession: 'developer' };
        const combinedObj = { ...obj1, ...obj2 };
        console.log(combinedObj); // { name: 'John', age: 30, gender: 'male', profession: 'developer' }

## How to Pass Functions Through Components 

1. The first step that the developer does to pass functions between components is to define the function in the parent component and pass it as a prop to the child component.
2. The increment function in the video increases a counter variable by 1 each time it is called.
3. You can pass a method from a parent component into a child component by defining the method in the parent component, passing it as a prop to the child component, and then invoking it in the child component.
4. The child component can invoke a method that was passed to it from a parent component by calling it using the props object and passing any necessary arguments.