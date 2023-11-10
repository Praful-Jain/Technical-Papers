# JAVASCRIPT
- JavaScript is a high-level, interpreted programming language.
- It is primarily known for adding interactivity to web pages, allowing dynamic content and behavior.
- JavaScript is a core technology for building modern, interactive, and dynamic web applications.

## Loops
1. for Loop: Used when you know the number of iterations.
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```
2. for ...in: Used when you want to iterate over the properties of an object.
```javascript
const obj = { a: 1, b: 2, c: 3 };

for (let key in obj) {
    console.log(key, obj[key]);
}
```
3. for ...of: Used when you want to iterate over the values of an iterable object like an array.
```javascript
const array = [1, 2, 3, 4, 5];

for (let value of array) {
    console.log(value);
}
```
4. while loop: Used when you don't know how many times you want to iterate beforehand, and the loop continues as long as the specified condition is true.
```javascript
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```


## Mutable and Immutable Methods (in strings and arrays)
In JavaScript, strings are immutable and arrays are mutable.

1. Strings:
-Strings in JavaScript are immutable, meaning that their values cannot be changed once they are created.
- Operations on strings, such as concatenation or substring extraction, return new strings rather than modifying the original string.
```javascript
let str = "Hello";
let newStr = str + " World"; // Concatenation creates a new string
console.log(newStr); // Output: Hello World
console.log(str); // Output: Hello (original string remains unchanged)
```

2. String Methods:
- Methods like concat, slice, and substring return new strings without modifying the original.
```javascript
let original = "Hello";
let concatenated = original.concat(" World");
let sliced = original.slice(0, 3);

console.log(original); // Output: Hello (unchanged)
console.log(concatenated); // Output: Hello World
console.log(sliced); // Output: Hel
```

3. Arrays:
- Arrays in JavaScript are mutable, meaning that you can change their contents by adding or removing elements.
```javascript
let arr = [1, 2, 3];
arr.push(4); // Adds an element, modifying the original array
console.log(arr); // Output: [1, 2, 3, 4]
```

4. Array Methods:
- Methods like push, pop, shift, and splice modify the original array.
```javascript
let array = [1, 2, 3];
array.push(4); // Modifies the original array
array.pop(); // Modifies the original array by removing the last element

console.log(array); // Output: [1, 2, 3]
```

- Methods like concat, slice, and filter return new arrays without modifying the original.
```javascript
let originalArray = [1, 2, 3];
let newArray = originalArray.concat(4);

console.log(originalArray); // Output: [1, 2, 3] (unchanged)
console.log(newArray); // Output: [1, 2, 3, 4]
```


## Pass by Reference and Pass by Value
- There are two types of datatypes in JS-
  1. **Primitive Datatypes (Pre-defined):** 
  - Objects of primitive type (built-in objects) are immutable and hence we can't add/modify/delete properties and methods of them.
  - Built-in objects - Object, Array, String, NUmber, Boolean, Function, Date. 
  ```javascript
  let num1 = 10;
  let num2 = num1;  // Pass by value - num1 id copied to num2
  num1 = 20;
  console.log(num1);  // output - 20  
  console.log(num2);  // output - 10
  ```
  
  2. **Non-Primitive/Referenced Datatypes:** 
  - Reference types are mutable, and when you assign a variable to a reference type, you're actually creating a reference to the object in memory.
  - We can't add/modify/delete properties and methods of them.
  ```javascript
  let obj1 = {number:10};
  let obj2 = obj1;  // Pass by reference - obj1 & obj2 pointing to same memory location.
  obj1.number = 20;  // it will make changes in both the objects
  console.log(obj1.number);  // output - 20
  console.log(obj2.number);  // output - 20
  ```


## Array methods

### Mutating Methods:
1. **Array.pop:**
   - Removes the last element from an array.
   - Mutable.
   ```javascript
   let array = [1, 2, 3];
   let lastElement = array.pop(); // Removes 3 from the array
   console.log(array); // Output: [1, 2]
   console.log(lastElement); // Output: 3
   ```

2. **Array.push:**
   - Adds one or more elements to the end of an array.
   - Mutable.
   ```javascript
   let array = [1, 2];
   array.push(3, 4); // Adds 3 and 4 to the end of the array
   console.log(array); // Output: [1, 2, 3, 4]
   ```

4. **Array.concat:**
   - Combines two or more arrays and returns a new array.
   - Immutable.
   ```javascript
   let array1 = [1, 2];
   let array2 = [3, 4];
   let newArray = array1.concat(array2);
   console.log(newArray); // Output: [1, 2, 3, 4]
   ```

5. **Array.slice:**
   - Returns a shallow copy of a portion of an array into a new array.
   - Immutable.
   ```javascript
   let array = [1, 2, 3, 4, 5];
   let slicedArray = array.slice(1, 4); // Creates a new array [2, 3, 4]
   console.log(slicedArray);
   ```

6. **Array.splice:**
   - Changes the contents of an array by removing or replacing existing elements and/or adding new elements.
   - Mutable.
   ```javascript
   let array = [1, 2, 3, 4, 5];
   array.splice(2, 1, 6); // Removes 1 element at index 2 and inserts 6
   console.log(array); // Output: [1, 2, 6, 4, 5]
   ```

7. **Array.join:**
   - Joins all elements of an array into a string.
   - Immutable.
   ```javascript
   let array = ['Hello', 'World'];
   let joinedString = array.join(' '); // Joins elements with a space
   console.log(joinedString); // Output: Hello World
   ```

8. **Array.flat:**
   - Creates a new array with all sub-array elements concatenated into it recursively.
   - Immutable.
   ```javascript
   let nestedArray = [1, 2, [3, 4, [5, 6]]];
   let flatArray = nestedArray.flat(2); // Flattens the nested array
   console.log(flatArray); // Output: [1, 2, 3, 4, 5, 6]
   ```

### Finding Elements:
1. **Array.find:**
   - Returns the first element in an array that satisfies a provided testing function.
   - Immutable.
   ```javascript
   let array = [10, 20, 30, 40];
   let result = array.find(element => element > 25); // Finds the first element greater than 25
   console.log(result); // Output: 30
   ```

2. **Array.indexOf:**
   - Returns the first index at which a given element can be found in the array.
   - Immutable.
   ```javascript
   let array = [10, 20, 30, 40];
   let index = array.indexOf(30); // Finds the index of 30
   console.log(index); // Output: 2
   ```

3. **Array.includes:**
    - Determines whether an array includes a certain element, returning `true` or `false`.
    - Immutable.
    ```javascript
    let array = [10, 20, 30, 40];
    let isIncluded = array.includes(30); // Checks if 30 is in the array
    console.log(isIncluded); // Output: true
    ```

4. **Array.findIndex:**
    - Returns the index of the first element in an array that satisfies a provided testing function.
    - Immutable.
    ```javascript
    let array = [10, 20, 30, 40];
    let index = array.findIndex(element => element > 25); // Finds the index of the first element greater than 25
    console.log(index); // Output: 2
    ```

### Higher Order Functions:
- Higher Order Functions are functions that can take other functions as input.

1. **Array.forEach:**
    - Executes a provided function once for each array element.
    - Mutable.
    ```javascript
    let array = [1, 2, 3];
    array.forEach(element => console.log(element)); // Prints each element
    ```

2. **Array.filter:**
    - Creates a new array with all elements that pass the test implemented by the provided function.
    - Immutable.
    ```javascript
    let array = [1, 2, 3, 4, 5];
    let filteredArray = array.filter(element => element > 2); // Filters elements greater than 2
    console.log(filteredArray); // Output: [3, 4, 5]
    ```

3. **Array.map:**
    - Creates a new array with the results of calling a provided function on every element in the array.
    - Immutable.
    ```javascript
    let array = [1, 2, 3];
    let squaredArray = array.map(element => element ** 2); // Squares each element
    console.log(squaredArray); // Output: [1, 4, 9]
    ```

4. **Array.reduce:**
    - Applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.
    - Immutable.
    ```javascript
    let array = [1, 2, 3, 4];
    let sum = array.reduce((accumulator, currentValue) => accumulator + currentValue, 0); // Calculates the sum
    console.log(sum); // Output: 10
    ```

5. **Array.sort:**
    - Sorts the elements of an array in place.
    - Mutable.
    ```javascript
    let array = [3, 1, 4, 1, 5, 9, 2, 6];
    array.sort((a, b) => a - b); // Sorts the array in ascending order
    console.log(array); // Output: [1, 1, 2, 3, 4, 5, 6, 9]
    ``` 

## Array methods chaining
- Array methods chaining is a powerful technique in JavaScript that involves chaining multiple array methods together to perform a series of operations on an array in a concise and readable manner.
- Each method in the chain operates on the result of the previous method, and the final result is often a transformed or filtered version of the original array.
  ```javascript
  const numbers = [1, 2, 3, 4, 5];
    
  const result = numbers
      .filter(num => num % 2 === 0)   // Keep only even numbers
      .map(num => num * 2)            // Double each remaining number
      .reduce((acc, num) => acc + num, 0);  // Sum the doubled numbers

  console.log(result); // Output: 12
  ```

## String methods
- All string methods are immutable.

1. **`length`:**
   - Returns the length of the string.
   ```javascript
   let str = "Hello, World!";
   console.log(str.length); // Output: 13
   ```

2. **`charAt(index)`:**
   - Returns the character at the specified index in the string.
   ```javascript
   let str = "Hello";
   console.log(str.charAt(1)); // Output: e
   ```

3. **`charCodeAt(index)`:**
   - Returns the Unicode value of the character at the specified index.
   ```javascript
   let str = "Hello";
   console.log(str.charCodeAt(1)); // Output: 101 (Unicode value for 'e')
   ```

4. **`concat(string1, string2, ..., stringN)`:**
   - Concatenates two or more strings.
   ```javascript
   let str1 = "Hello";
   let str2 = "World";
   let result = str1.concat(", ", str2, "!");
   console.log(result); // Output: Hello, World!
   ```

5. **`indexOf(searchValue, startIndex)`:**
   - Returns the index of the first occurrence of a specified value in a string.
   ```javascript
   let str = "Hello, World!";
   console.log(str.indexOf("World")); // Output: 7
   ```

6. **`lastIndexOf(searchValue, startIndex)`:**
   - Returns the index of the last occurrence of a specified value in a string.
   ```javascript
   let str = "Hello, World!";
   console.log(str.lastIndexOf("o")); // Output: 8
   ```

7. **`slice(startIndex, endIndex)`:**
   - Extracts a section of a string and returns it as a new string.
   ```javascript
   let str = "Hello, World!";
   let sliced = str.slice(0, 5);
   console.log(sliced); // Output: Hello
   ```

8. **`substring(startIndex, endIndex)`:**
   - Similar to `slice`, extracts a section of a string and returns it as a new string.
   ```javascript
   let str = "Hello, World!";
   let subString = str.substring(7, 12);
   console.log(subString); // Output: World
   ```

9. **`substr(startIndex, length)`:**
   - Extracts a specified number of characters from a string, starting at a specified index.
   ```javascript
   let str = "Hello, World!";
   let subStr = str.substr(7, 5);
   console.log(subStr); // Output: World
   ```

10. **`toUpperCase()`:**
    - Converts a string to uppercase.
    ```javascript
    let str = "hello";
    console.log(str.toUpperCase()); // Output: HELLO
    ```

11. **`toLowerCase()`:**
    - Converts a string to lowercase.
    ```javascript
    let str = "WORLD";
    console.log(str.toLowerCase()); // Output: world
    ```

12. **`replace(searchValue, replaceValue)`:**
    - Replaces a specified value with another value in a string.
    ```javascript
    let str = "Hello, World!";
    let newStr = str.replace("World", "Universe");
    console.log(newStr); // Output: Hello, Universe!
    ```

13. **`trim()`:**
    - Removes whitespace from both ends of a string.
    ```javascript
    let str = "   Hello, World!   ";
    let trimmedStr = str.trim();
    console.log(trimmedStr); // Output: Hello, World!
    ```

14. **`split(separator)`:**
    - Splits a string into an array of substrings based on a specified separator.
    ```javascript
    let str = "apple,orange,banana";
    let fruitsArray = str.split(",");
    console.log(fruitsArray); // Output: ["apple", "orange", "banana"]
    ```

15. **`startsWith(searchString, position)`:**
    - Checks if a string starts with a specified value.
    ```javascript
    let str = "Hello, World!";
    console.log(str.startsWith("Hello")); // Output: true
    ```

16. **`endsWith(searchString, length)`:**
    - Checks if a string ends with a specified value.
    ```javascript
    let str = "Hello, World!";
    console.log(str.endsWith("World")); // Output: true
    ```

## Object methods
- Examples of common object methods and operations in JavaScript.
### Creating Objects:

1. **Object Literal:**
   - Creates an object using the literal notation.

    ```javascript
    let person = { name: "John", age: 30 };
    ```

2. **Object Constructor:**
   - Creates an object using the `Object` constructor.

    ```javascript
    let person = new Object();
    person.name = "John";
    person.age = 30;
    ```

### Accessing and Modifying Properties:

3. **Dot Notation:**
   - Accesses and modifies object properties using dot notation.

    ```javascript
    let person = { name: "John", age: 30 };
    console.log(person.name); // Output: John
    person.age = 31; // Mutable: Changes the value of 'age'
    ```

4. **Bracket Notation:**
   - Accesses and modifies object properties using bracket notation.

    ```javascript
    let person = { name: "John", age: 30 };
    console.log(person["name"]); // Output: John
    person["age"] = 31; // Mutable: Changes the value of 'age'
    ```

### Object Methods:

5. **Object.keys:**
   - Returns an array of a given object's own enumerable property names.

    ```javascript
    let person = { name: "John", age: 30 };
    let keys = Object.keys(person);
    console.log(keys); // Output: ["name", "age"]
    ```

6. **Object.values:**
   - Returns an array of a given object's own enumerable property values.

    ```javascript
    let person = { name: "John", age: 30 };
    let values = Object.values(person);
    console.log(values); // Output: ["John", 30]
    ```

7. **Object.entries:**
   - Returns an array of a given object's own enumerable property [key, value] pairs.

    ```javascript
    let person = { name: "John", age: 30 };
    let entries = Object.entries(person);
    console.log(entries); // Output: [["name", "John"], ["age", 30]]
    ```

### Object Spread Operator (ES6):

8. **Object Spread Operator:**
   - Creates a shallow copy of an object with additional or modified properties.

    ```javascript
    let person = { name: "John", age: 30 };
    let updatedPerson = { ...person, age: 31 }; // Immutable: Creates a new object
    console.log(updatedPerson); // Output: { name: "John", age: 31 }
    console.log(person); // Output: { name: "John", age: 30 } (unchanged)
    ```

### Deleting Properties:

9. **delete:**
   - Deletes a property from an object.

    ```javascript
    let person = { name: "John", age: 30 };
    delete person.age; // Mutable: Removes the 'age' property
    console.log(person); // Output: { name: "John" }
    ```
## Hoisting
- Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase. 
- This means that you can use a variable or call a function before it is declared in the code.
- **Note-** Only the declarations are hoisted, not the initializations.
 

## Scopes
- Scope refers to the context in which variables are declared and the extent of their visibility.
- There are two main types of scope: global scope and local scope.

1. **Global Scope:**
- Variables declared outside of any function or block have global scope.
2. **Local Scope:**
- Variables declared inside a function or block have local scope.
3. **Block Scope (let and const):**
- Variables declared with let and const have block scope.



## Higher Order Functions
- Higher-order functions are functions that can take other functions as arguments or return them as results.
- Example of Higher Order Functions : **map, filter, reduce, forEach, etc**
  


## Best Practices

### 1. Best Practices: Indentation

Ensure that your code indentation is good. Submitting code that looks like the example given is unprofessional and makes it difficult to read for you as well as anyone who has to work with your code.

**Bad indentation:**
```javascript
function problem1(inventory, passid) {
if(Array.isArray(inventory)){
return inventory;}
else{
    return [];
}
}
module.exports=problem1;
```

**Good indentation:**
```javascript
function problem1(inventory, passid) {
    if (Array.isArray(inventory) && passid < 50) {
        return inventory;
    } else {
        return [];
    }
}
module.exports = problem1;
```

An easy way to indent your code is to press `Ctrl + Shift + I` in VSCode.

If you are on a Mac, try `Cmd + Shift + I`.

### 2. Best Practices: Variable Naming

Ensure that your variable names are descriptive. Variable names that look like the examples below are unprofessional and make it difficult to read for you as well as anyone who has to work with your code.

**Bad Naming:**
```javascript
const a = [1, 2, 3, 4, 5];
const a1 = [1, 4, 9, 16, 25];
```

**Good Naming:**
```javascript
const numbers = [1, 2, 3, 4, 5];
const squares = [1, 4, 9, 16, 25];
```

This also applies to functions.

**Bad Naming:**
```javascript
const numbers = [1, 2, 3, 4, 5];
function calc(n) {
    return n * n;
}
const squares = numbers.map(calc);
```

**Good Naming:**
```javascript
const numbers = [1, 2, 3, 4, 5];
function squareNumber(number) {
    return number * number;
}
const squares = numbers.map(squareNumber);
```

Naming is tricky for every engineer. But that does not mean you don't do it. It means you think about what to name it while you are writing code, not after you have finished.

### 3. Best Practices: if else

Keeping your code as readable as possible will ensure that you don't run into issues later on. One way to ensure this with `if-else` is to always use `{}` with the statements.

**Bad Usage:**
```javascript
let sum = 10;
if(value %2 == 0)
    sum += value;
else if(value == 0)
    sum += 1;
else
    sum += -1;
```

**Good Usage:**
```javascript
let sum = 10;
if(value %2 == 0) {
    sum += value;
} else if(value == 0) {
    sum += 1;
} else {
    sum += -1;
}
```

This ensures that there is never any confusion about which code runs and when.

It also ensures that there will be no chance of code not getting executed because it was placed on an adjacent line and is missed by the interpreter.


## Debugging
Debugging is a crucial skill in software development that involves identifying and fixing errors, or bugs, in your code. Here are some general debugging techniques and tools commonly used in JavaScript:

### 1. **Console.log:**
- Inserting `console.log` statements in your code to print out variable values, check the flow of execution, and identify where issues might be occurring.

     ```javascript
     let x = 5;
     console.log('The value of x is:', x);
     ```

### 2. **Debugger Statement:**
- Placing the `debugger` statement in your code to pause execution and enter the browser's debugging environment.
     ```javascript
     let y = 10;
     debugger;
     ```
     
### 3. **Browser Developer Tools:**
- Most modern browsers come with built-in developer tools that allow you to inspect and debug your JavaScript code. You can set breakpoints, step through code, and inspect variable values.
- Right-click on a webpage, select "Inspect" or "Inspect Element," and navigate to the "Console" or "Sources" tab.


### 4. **Browser Console:**
- Utilizing the browser's console to interactively test code snippets, log values, and identify errors.
- Open the browser console (usually by pressing `F12` or `Ctrl+Shift+J`), and start typing JavaScript commands.


### 5. **Breakpoints:**
- Placing breakpoints in your code using the browser's developer tools to pause execution at specific points and inspect the program state.
- In the "Sources" tab of the browser's developer tools, click on the line number to set a breakpoint.


### 6. **Logging and Error Handling:**
- Implementing structured logging and appropriate error handling in your code to catch and report errors.
     ```javascript
     try {
         // Code that might throw an error
     } catch (error) {
         console.error('An error occurred:', error);
     }
     ```
