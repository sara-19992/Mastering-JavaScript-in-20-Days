## Classes & Prototypes
1. generate object using a function (copies of object, don't repeat yourself, can't add new functionality).
2. Prototype chain.
3. new keyword.
4. classes.

### Prototype chain 

when assign object create a link to functions stored and store in hidden property proto, when call function search on the object if can't find it go to link and search. 
 
1. chain connection a link a reference to object functions.
2. when create object using Object.create() method return empty object.
3. all object in JS has proto property link to Object.prototype as default (proto link to object stored function).
4. Object.prototype is big object which proto link to Null.
5. when creating a function, a property object called prototype is being created automatically and is being attached to the function object.  

## Coding Exercises
### 156.[Create a Basic JavaScript Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/create-a-basic-javascript-object)
#### My Solution
```javascript
let dog = {
  name: "sds",
  numLegs: 4
};
```
### 157.[Use Dot Notation to Access the Properties of an Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-dot-notation-to-access-the-properties-of-an-object)
#### My Solution
```javascript
let dog = {
  name: "Spot",
  numLegs: 4
};
// Only change code below this line
console.log(dog.name, dog.numLegs);
```
### 158.[Create a Method on an Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/create-a-method-on-an-object)
#### My Solution
```javascript
let dog = {
  name: "Spot",
  numLegs: 4,

  sayLegs: () => `This dog has ${dog.numLegs} legs.`

};

dog.sayLegs();
```
### 159.[]()
#### My Solution
```javascript

```
### 160.[]()
#### My Solution
```javascript

```
