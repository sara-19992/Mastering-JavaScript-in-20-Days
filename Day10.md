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
### 153.[Question 1](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%203/tasks.md#question-1)
#### My Solution
```javascript
const task1 = (cb) =>
  setTimeout(() => {
    const message = "Task 1 has executed successfully!";
    cb(message);
  }, 3000);

const task2 = (cb) =>
  setTimeout(() => {
    const message = "Task 2 has executed successfully!";
    cb(message);
  }, 0);

const task3 = (cb) =>
  setTimeout(() => {
    const message = "Task 3 has executed successfully!";
    cb(message);
  }, 1000);

const task4 = (cb) =>
  setTimeout(() => {
    const message = "Task 4 has executed successfully!";
    cb(message);
  }, 2000);

const task5 = (cb) =>
  setTimeout(() => {
    const message = "Task 5 has executed successfully!";
    cb(message);
  }, 4000);

const asyncTasks = [task1, task2, task3, task4, task5];

const executeInSequenceWithCBs = async (tasks, callback) => {
  const promiseArray = [];
  for (let task of tasks) {
    promiseArray.push(
      new Promise((resolve) => {
        task(resolve);
      })
    );
  }
  const messages = await Promise.all(promiseArray);
  callback(messages);
  return messages;
};

const print = (arr) => {
  for (a of arr) {
    console.log(a);
  }
};

executeInSequenceWithCBs(asyncTasks, print);
```
### 154.[Question 2](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%203/tasks.md#question-1)
#### My Solution
```javascript
const apis = [
  {
    apiName: "products",
    apiUrl: "https://dummyjson.com/products",
  },
  {
    apiName: "users",
    apiUrl: "https://dummyjson.com/users",
  },
  {
    apiName: "posts",
    apiUrl: "https://dummyjson.com/posts",
  },
  {
    apiName: "comments",
    apiUrl: "https://dummyjson.com/comments",
  },
];

const executeInParallelWithPromises = (apis) => {
  const results = [];
  for (let api of apis) {
    fetch(api.apiUrl).then((value) => {
      value.json().then((body) => {
        api.apiDate = body[api.apiName];
        results.push(api);
      });
    });
  }
  console.log(results);
  return results;
};

executeInParallelWithPromises(apis);
```
### 155.[Question 3](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week2%20-%20javaScript-the-hard-parts-v2/day%203/tasks.md#question-1)
#### My Solution
```javascript
const apis = [
  {
    apiName: "products",
    apiUrl: "https://dummyjson.com/products",
  },
  {
    apiName: "users",
    apiUrl: "https://dummyjson.com/users",
  },
  {
    apiName: "posts",
    apiUrl: "https://dummyjson.com/posts",
  },
  {
    apiName: "comments",
    apiUrl: "https://dummyjson.com/comments",
  },
];

const executeInSequenceWithPromises = async (apis) => {
  const results = [];
  for (let api of apis) {
    const response = await fetch(api.apiUrl);
    const body = await response.json();
    api.apiDate = body[api.apiName];
    results.push(api);
  }
  console.log(results);
  return results;
};

executeInSequenceWithPromises(apis);
```



  
