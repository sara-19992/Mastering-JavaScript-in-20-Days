## Promise
- added in ES6
- return a promise object immediately and set value after web browser completion
- after promise completion set the value automatically to response object 
- can use it to error handling on Rejection

### .then ()
code that run on data when returnans the promise object save this code (function) to hidden property onFulfilment and run automatically when data return.

### Microtask queue & Callback queue
web browser features after completion functions put it on: 
1. microtask queue for promise functions. 
2. callback queue for other callback functions.
    
when global code finish running go to Event loop and first check microtask queue then callback queue.

  
