## Asynchronous in JS 
JS is synchronous executed code after finish execute the line go to the next line 
but if there function take along time what JS do ?

Web Browser APIs
the feature of web browser inaddition to JS 
- HTML DOM (rendering html elements).
- Timer (setTimeOut).
- Console.
- Network request (fetch).
  
JS run on browser if we a setTimeOut function in code nothing to do in JS go to web browser features and refrence the function and time to execute and cheack if its complete if not go to next line of code, when time complete pack the function to JS and start execute automaticlly 

Web APIs Rules 

1. put the function completion on web browser features in a callback queue.
2. do Event Loop means keep checking if the global call stack is empty or not (no function running), if queue is not empty,delete function from queue and push function to stack.
3. all regular code executed first, after that start execute what deque from callback queue.
   
on completion run code 
is it complete ? 
go to next line code to execute 
and after time completet pack the function to js 
start executing automaticelly
