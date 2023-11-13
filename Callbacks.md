# Callbacks
- A function that is passed to another function as a parameter is a callback function.
- Callback functions are commonly used in asynchronous programming, such as handling events, making API requests, and dealing with timeouts.

```javascript
// Example 1: Callback function as an argument
function doSomethingAsync(callback) {
  // Simulate an asynchronous operation (e.g., API request, setTimeout)
  setTimeout(function () {
    console.log("Async operation completed");
    // Call the callback function
    callback();
  }, 1000);
}

// Callback function
function onComplete() {
  console.log("Callback function executed");
}

// Call the function with the callback
doSomethingAsync(onComplete);
```

## Need of Callback functions
- Callback functions are essential in JavaScript for handling asynchronous operations, events, and for enabling better control over the flow of your code.
- In summary, callback functions in JavaScript are crucial for managing asynchronous code, handling events, and providing a way to structure code execution in a non-blocking manner.
- Callback functions enhance the flexibility and efficiency of your programs, particularly in scenarios where timing and order of execution are important.
- JavaScript runs code sequentially in top-down order. However, there are some cases that code runs (or must run) after something else happens and also not sequentially. This is called asynchronous programming.
- Callbacks make sure that a function is not going to run before a task is completed but will run right after the task has completed. It helps us develop asynchronous JavaScript code and keeps us safe from problems and errors.

1. **Asynchronous Operations:**
  - An asynchronous operation is one that allows the computer to move on to other tasks while waiting for the asynchronous operation to complete.
  - Callback functions allow you to specify what should happen once the asynchronous operation is completed.
  - Many operations in JavaScript are asynchronous, such as fetching data from an API, reading a file, or making a database query. 
   
   ```javascript
   function fetchData(callback) {
     // Simulate asynchronous operation
     setTimeout(function () {
       var data = { message: "Data fetched successfully" };
       callback(data);
     }, 1000);
   }

   // Using callback for handling asynchronous operation
   fetchData(function (result) {
     console.log(result.message);
   });
   ```

2. **Event Handling:**
   - Callbacks are commonly used to handle events in the browser, such as button clicks, form submissions, or key presses.
   - Event listeners take a callback function as an argument, and this function is executed when the corresponding event occurs.

   ```javascript
   // Event handling with callback
   document.getElementById("myButton").addEventListener("click", function () {
     console.log("Button clicked");
   });
   ```

3. **Timeouts and Intervals:**
   - Functions like `setTimeout` and `setInterval` allow you to execute code after a specified delay or at regular intervals.
   - Callback functions are used to define what should happen when the timer expires.

   ```javascript
   // Timeout with callback
   setTimeout(function () {
     console.log("Delayed operation");
   }, 2000);

   // Interval with callback
   setInterval(function () {
     console.log("Repeated operation");
   }, 1000);
   ```

4. **Control Flow:**
   - Callbacks enable better control over the flow of your code, especially in scenarios where certain tasks depend on the completion of others.
   - Callbacks can be used to sequence operations or handle results based on previous computations.

   ```javascript
   function stepOne(callback) {
     console.log("Step One");
     callback();
   }

   function stepTwo() {
     console.log("Step Two");
   }

   // Sequencing operations with callbacks
   stepOne(function () {
     stepTwo();
   });
   ```

## Anonymous Function :
- An anonymous function in JavaScript is a function without a name.
- Anonymous functions are often used as arguments to other functions, especially in scenarios where a function is only needed temporarily and doesn't need a formal declaration.

```javascript
// Example 2: Anonymous function as a callback
function doSomethingAsync(callback) {
  setTimeout(function () {
    console.log("Async operation completed");
    callback();
  }, 1000);
}

// Call the function with an anonymous callback function
doSomethingAsync(function () {
  console.log("Anonymous callback function executed");
});
```

## How to create a Callback?
- Let's say we want to log a message to the console but it should be there after 3 seconds.
```javascript
const message = function() {
    console.log("This message is shown after 3 seconds");
}

setTimeout(message, 3000);
```

## setTimeout() Function
- setTimeout() is a function that uses callback functions to schedule task to be performed after a delay.
- setTimeout() has two parameters: a callback function and a delay in millisecond.

## Callback as an Arrow Function
- Callback function as an ES6 arrow function, which is a newer type of function in JavaScript:
```javascript
setTimeout(() => {
    console.log("This message is shown after 3 seconds");
}, 3000);
```
