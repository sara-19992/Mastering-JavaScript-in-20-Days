## Asynchronous in JS 
JS is synchronous executed code after finish execute the line go to the next line 
but if there function take along time what JS do ?

### Web Browser APIs
JS run on browser  
the feature of web browser in addition to JS 
- HTML DOM (rendering html elements).
- Timer (setTimeOut).
- Console.
- Network request (fetch).
  
if a setTimeOut function in the code nothing to do in JS go to web browser features and reference the function and time to execute and check if its complete if not go to next line of code, after time complete pack the function to JS and start execute automatically.

### Web APIs Rules 
1. put the function completion on web browser features in a callback queue.
2. do Event Loop means keep checking if the global call stack is empty (no function running), if queue is not empty,delete function from queue and push it to stack.
3. all regular code executed first, after that start execute what deque from callback queue.

   
