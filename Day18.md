## Coding Exercises
### 245.[Sum All Numbers in a Range](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/sum-all-numbers-in-a-range)
#### My Solution
```javascript
function sumAll(arr) {
  let [min, max] = arr;
  if(min > max){
    [min, max] = [max, min];
  }
  let sum = 0;
   for(let i = min; i <= max; i++){
    sum += i;
   }  
  return sum;
}


sumAll([1, 4]);
```
### 246.[Diff Two Arrays](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/diff-two-arrays)
#### My Solution
```javascript
function diffArray(arr1, arr2) {
  const newArr = [];
  for(let i = 0; i < arr1.length; i++){
    if(arr2.indexOf(arr1[i]) == -1)newArr.push(arr1[i]);
  }
  for(let i = 0; i < arr2.length; i++){
    if(arr1.indexOf(arr2[i]) == -1)newArr.push(arr2[i]);
  }
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```
