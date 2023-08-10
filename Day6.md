## Data Fetching & Promises
  - APIs provide URL that point to certain resource (data).
  - fetch() use to load data from APIs.

### Promises  
promises represent the value that don't have yet promises take time so its asynchronous ,JS add this task to list and keep running code but if we need data from promise, can stop JS execute and wait to for promise to resolve.

- fetch() take time to get data because its return a promise.
- await keyword stop JS and wait to finish asynchronous operation. 

promises states
  1. pending: still waiting, I promise to get value.
  2. fulfilled: get the value.
  3. reject: can't get the value.
     

step fetch data:
  1. use fetch(URL) with await.
  2. the browser send a request.
  3. receive a response object.
  4. use json() to parse body of response object.
  5.  use await with json (return another promise).
      
### Coding Examples
```javascript

```
## Destructuring Objects & Arrays
   to break down an object and extract values from object and assign it to multiple variables.

   object
   - use { }
   - use property name
   - omit property name that don't need
   - order not matter
   array
   - use [ ]
   - use comma to skip value 
   - order is matter
     
split() split string on delimiting char
trim() remove spaces from start and end of str 

## Async   
in async functons can use await 

render mean display it on the page
Document.createElement() create element
appendChile append child to element
