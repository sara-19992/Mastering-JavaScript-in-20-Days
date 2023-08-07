## Arrays
array is a object data type contains items can be in different types.

each item in array pointed to index to accesses it 

 ### Coding Examples

```javascript
//declare empty array
const days = [];

//array of diffrent item type
const arr = ["Ahmade",45,true];

console.log(arr[0]);
//log "Ahmade" to the console
```

### Array methode
 some of array methods:
  - push (append item to array and return the new length of array)
  - pop (remove the last item of array and return it)
  - sort (sort the array in alphabetical order)
  - join (join the item of array by a string)
  - concat (create a new array and concatenate the two array together)
  - includes (if array contains a given item)

 ### Coding Examples
```javascript
//declare array
const numbers = [1,2,3,7];

let num=numbers.pop()
console.log(num)
//log 7

console.log(numbers)
//log [1,2,3]

numbers.push(4);
console.log(numbers);
//log [1,2,3,4]

const arr=numbers.concat([5,6]);
console.log(arr);
//arr = [1,2,3,4,5,6]

const names = ["aseel","nour","alaa"];
console.log(names.join(" , "));
//log "aseel , nour , alaa"

```    

### immutable vs mutable
there are two type of data:
  1. immutable cant be change (always stay the same)
  2. mutable cne be change

for variable
- let and var is a mutable can change it (reassign)
- const is immutable (declare and assign in the same time and can't change it)

for data type  
- array is a mutable can change the items
- string is immutable can't change the items as array but can reassign the value of it

if declare a const array we can't reassign it but we can change the items in array because array is mutable  
  
### Coding Examples

```javascript

const names = ["Ahmade","aseel","alaa"];
names[0] = "wael";
conole.log(names[0]);
//log a new value "wael"

let str = "duaa fd";
str[0] = "a";
console.log(str[0]);
//log "d" because string is immutable  

```

    
    
