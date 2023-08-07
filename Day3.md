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

```javascript
//declare array
const numbers = [1,2,3];

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

    
    
