## Coding Exercises
### 118.[Create a JavaScript Promise](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/create-a-javascript-promise)
#### My Solution
```javascript
const makeServerRequest = new Promise((resolve, reject) => {

});
```
### 119.[Complete a Promise with resolve and reject](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/complete-a-promise-with-resolve-and-reject)
#### My Solution
```javascript

```
### 120.[Complete a Promise with resolve and reject](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/complete-a-promise-with-resolve-and-reject)
#### My Solution
```javascript
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer represents a response from a server
  let responseFromServer;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
});
```
### 121.[Handle a Fulfilled Promise with then](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/handle-a-fulfilled-promise-with-then)
#### My Solution
```javascript
const makeServerRequest = new Promise((resolve, reject) => {
  // responseFromServer is set to true to represent a successful response from a server
  let responseFromServer = true;
    
  if(responseFromServer) {
    resolve("We got the data");
  } else {  
    reject("Data not received");
  }
}).then(result => {
  console.log(result);
});
```
