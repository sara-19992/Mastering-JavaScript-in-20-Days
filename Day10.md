## Promise
- added in ES6
- return a promise object immediately and set value after web browser completion
- after promise completion set the value automatically to response object 
- can use it to error handling on Rejection

### .then ( )
code that run on data when returnans the promise object save this code (function) to hidden property onFulfilment and run automatically when data return.

### Microtask queue & Callback queue
after web browser features completion, functions put it on: 
1. microtask queue for promise functions. 
2. callback queue for other callback functions.
    
when global code finish running go to Event loop and first check microtask queue then callback queue.

## Coding Exercises
### 154.[]()
#### My Solution
```javascript
const task1 = (cb) => setTimeout(() => {
  const message = "Task 1 has executed successfully!";
  cb(message);
}, 3000)

const task2 = (cb) => setTimeout(() => {
  const message = "Task 2 has executed successfully!";
  cb(message);
}, 0)

const task3 = (cb) => setTimeout(() => {
  const message = "Task 3 has executed successfully!";
  cb(message);
}, 1000)

const task4 = (cb) => setTimeout(() => {
  const message = "Task 4 has executed successfully!";
  cb(message);
}, 2000)

const task5 = (cb) => setTimeout(() => {
  const message = "Task 5 has executed successfully!";
  cb(message);
}, 4000)

const asyncTasks = [task1, task2, task3, task4, task5];

const executeInSequenceWithCBs = (tasks, callback) => {
    for(let task of tasks){
       task();
     }

}
```
### 155.[]()
#### My Solution
```javascript
```
### 156.[]()
#### My Solution
```javascript
```
### 157.[]()
#### My Solution
```javascript
```


  
