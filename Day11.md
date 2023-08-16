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
### 159.[Make Code More Reusable with the this Keyword](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/make-code-more-reusable-with-the-this-keyword)
#### My Solution
```javascript
let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs: function() {return "This dog has " + this.numLegs + " legs.";}
};

dog.sayLegs();
```
### 160.[Define a Constructor Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/define-a-constructor-function)
#### My Solution
```javascript
function Dog(){
  this.name = 'dfg';
  this.color = 'red';
  this.numLegs = 4;
}
```
### 161.[Use a Constructor to Create Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-a-constructor-to-create-objects)
#### My Solution
```javascript
function Dog() {
  this.name = "Rupert";
  this.color = "brown";
  this.numLegs = 4;
}
// Only change code below this line
const hound = new Dog();
```
### 162.[Extend Constructors to Receive Arguments](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/extend-constructors-to-receive-arguments)
#### My Solution
```javascript
function Dog(name, color) {
  this.name = name;
  this.color = color;
  this.numLegs = 4;
}

const terrier = new Dog('terr','brown');
```
### 163.[Verify an Object's Constructor with instanceof](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/verify-an-objects-constructor-with-instanceof)
#### My Solution
```javascript
function House(numBedrooms) {
  this.numBedrooms = numBedrooms;
}

// Only change code below this line
const myHouse = new House(10);

console.log(myHouse instanceof House);
```
### 164.[Understand Own Properties](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/understand-own-properties)
#### My Solution
```javascript
function Bird(name) {
  this.name = name;
  this.numLegs = 2;
}

let canary = new Bird("Tweety");
let ownProps = [];
// Only change code below this line
for(let prop in canary){
  if(canary.hasOwnProperty(prop))ownProps.push(prop);
}

console.log(ownProps);
```
### 165.[]()
#### My Solution
```javascript

```
### 166.[]()
#### My Solution
```javascript

```
### 167.[]()
#### My Solution
```javascript

```
### 168.[]()
#### My Solution
```javascript

```
### 169.[]()
#### My Solution
```javascript

```
### 170.[]()
#### My Solution
```javascript

```
### 171.[]()
#### My Solution
```javascript

```
### 172.[]()
#### My Solution
```javascript

```
### 173.[]()
#### My Solution
```javascript

```
### 174.[]()
#### My Solution
```javascript

```
### 175.[]()
#### My Solution
```javascript

```
### 176.[]()
#### My Solution
```javascript

```
### 177.[]()
#### My Solution
```javascript

```
### 78.[]()
#### My Solution
```javascript

```
