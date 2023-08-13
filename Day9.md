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

## Coding Exercises
### 145.[Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)
#### My Solution
```javascript
const squareList = arr => {
  // Only change code below this line
  const positveInteger =arr.filter(x => x > 0 && Math.floor(x) === x);
  const sqList =positveInteger.map(x => x*x);
  return sqList;
  // Only change code above this line
};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);
```
### 146.[Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)
#### My Solution
```javascript
// Only change code below this line
function urlSlug(title) {

 const str = title.toLowerCase().trim().split(' ').filter(x => x!=='').map(x => x.trim()).join('-');

 return str; 

}
// Only change code above this line
urlSlug(" Winter Is  Coming");
```

### 147.[Functions and Callbacks]()
#### My Solution
```javascript
function mapAsync(arr, func){
	
  return async function(){
    return await arr.map( x => func(x)); 
	} 

}

const arrayMap = mapAsync(['nour','alaa','weal'], (str) =>  str.toUpperCase());
console.log(arrayMap());
```
### 148.[]()
#### My Solution
```javascript
function sumRange(n1, n2){
  if(n2 === n1)return n1;
  return n2 + sumRange(n1, n2 - 1);
}

console.log(sumRange(4,7)); //log 22
```  
