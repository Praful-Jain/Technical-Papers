# Promises
- A JavaScript Promise is an object that can be used to get the outcome of an asynchronous operation when that result is not instantly available.
- A JavaScript Promise object can be in one of three states: **pending**, **resolved**, or **rejected**.
  1. Pending - The initial state - the operation has not completed yet.
  2. Resolved/Fulfilled - The operation has completed successfully and the promise now has a resolved value.
  3. Rejected - The operation has failed and the promise has a reason for the failure.

```javascript
const promise = new Promise((resolve, reject) => {
  const res = true;
  // An asynchronous operation.
  if (res) {
    resolve('Resolved!');
  } else {
    reject(Error('Error'));
  }
});

promise.then((res) => console.log(res), (err) => alert(err));
```

## Creating a JavaScript Promise object
- An instance of a JavaScript Promise object is created using the `new` keyword.
- The constructor of the Promise object takes a function, known as the executor function, as the argument. This function is responsible for resolving or rejecting the promise.

```javascript
const executorFn = (resolve, reject) => {
  console.log('The executor function of the promise!');
};

const promise = new Promise(executorFn);
```

## The Promise Object
- A Promise is an object that can be used to get the outcome of an asynchronous operation when that result is not instantly available.
- Since JavaScript code runs in a non-blocking manner, promises become essential when we have to wait for some asynchronous operation without holding back the execution of the rest of the code.

## Executor function of JavaScript Promise object
- It is passed as argument to the **Promise constructor**.
- The execution funcion is responsible for performing some asynchronous operation and determine whether the promise should be resolved or rejected.
- **Promise constructor** - It is used to return a promise object.
- A JavaScript promise’s executor function takes two functions as its arguments. The first parameter represents the function that should be called to resolve the promise and the other one is used when the promise should be rejected.
- A Promise object may use any one or both of them inside its executor function.

```javascript
const executorFn = (resolve, reject) => {
  resolve('Resolved!');
};

const promise = new Promise(executorFn);
```

## `setTimeout()`
- `setTimeout()` is an asynchronous JavaScript function that executes a code block or evaluates an expression through a callback function after a delay set in milliseconds.

```javascript
const loginAlert = () => {
  alert('Login');
};

setTimeout(loginAlert, 6000);
```

## `.then()` method of a JavaScript Promise object
- The `.then()` method of a JavaScript Promise object is a higher-order functions, can be used to get the eventual result (or error) of the asynchronous operation.
- `.then()` accepts two function arguments. We refer to these callbacks as handlers.
  1. The first handler supplied to it will be called if the promise is resolved.
  2. The second one will be called if the promise is rejected.

```javascript
const promise = new Promise((resolve, reject) => {    
  setTimeout(() => {
    resolve('Result');
  }, 200);
});

promise.then((res) => {
  console.log(res);
}, (err) => {
  alert(err);
});
```

## The `.catch()` method for handling rejection
- The `.catch()` method takes only one argument, which is failure callback function.
- In case of a rejected promise, this failure handler will be invoked with the reason for rejection.
  
```javascript
const promise = new Promise((resolve, reject) => {  
  setTimeout(() => {
    reject(Error('Promise Rejected Unconditionally.'));
  }, 1000);
});

promise.then((res) => {
  console.log(value);
});

promise.catch((err) => {
  alert(err);
});
```

## JavaScript `Promise.all()`
- `Promise.all()` accepts an array of promises as its argument and returns a single promise.
  1. **Case-1:** If every promise in the argument array resolves, the single promise will be an array containing the resolve value from each promise in the argument array.
  2. **Case-2:** If any promise from the argument array rejects, the single promise will immediately reject with the reason that promise rejected.
     
```javascript
//In the code block, 3 and 2 will be printed respectively even though `promise1` will be resolved after `promise2`.

const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve(3);
  }, 300);
});

const promise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve(2);
  }, 200);
});

Promise.all([promise1, promise2]).then((res) => {
  console.log(res[0]);
  console.log(res[1]);
});
```

## Chaining multiple `.then()` methods
- The `.then()` method returns a Promise, even if one or both of the handler functions are absent. Because of this, multiple `.then()` methods can be chained together. This is known as composition.
- In the code block, a couple of `.then()` methods are chained together. Each method deals with the resolved value of their respective promises.

```javascript
const promise = new Promise((resolve, reject) => {  
  setTimeout(() => {
    resolve('*');
  }, 1000);
});

const twoStars = (star) => {  
  return (star + star);
};

const oneDot = (star) => {  
  return (star + '.');
};

const print = (val) => {
  console.log(val);
};

// Chaining them all together
promise.then(twoStars).then(oneDot).then(print);
```

## Avoiding nested Promise and `.then()`
- In JavaScript, when performing multiple asynchronous operations in a sequence, promises should be composed by chaining multiple `.then()` methods. This is better practice than nesting.
- Chaining helps streamline the development process because it makes the code more readable and easier to debug.

