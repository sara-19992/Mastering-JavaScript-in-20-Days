## Promise
- ES6
- return a promise object immediatly and set value after completeion
- after propmise completeion set the value to response object
- can use it to error handling on Rejection

  ### Microstack queue & Callback queue
  web browser features after completion functions put it on: 
  1. microstack queue for promise functions 
  2. callback queue for other callback functions
      
  when global code finsh running go to eventloop and check the callback queue and
microstak queue

event loop check microstak queue then go to callback queue
  
