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

### Properties
two kinds of properties:
1. properties own properties are defined directly on the object instance itself.
2. prototype properties are defined on the prototype.

### Constructor property & instanceof
constructor property to find out what kind of object it is.there is one crucial side effect of manually setting the prototype to a new object. It erases the constructor property!, but since the property has been overwritten, it now gives false results, fix it by set the Constructor Property manually in prototype object.

instanceof use to check a kind of object, not effect of manually setting the prototype to a new object like constructor

### Object Inherits & Mixin
#### Inherits
- object inherits its prototype directly from the constructor function that created it.
- when an object inherits its prototype from another object, it also inherits the supertype's constructor property.
- override Inherited Methods.
#### Mixin  
- there are cases when inheritance is not the best solution. Inheritance does not work well for unrelated objects.
- for unrelated objects, it's better to use mixins. A mixin allows other objects to use a collection of functions.

### (IIFE) 
Immediately Invoked Function Expression (IIFE)
```javascript
(function() {
  console.log("Immediately");
})();
```
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
### 165.[Use Prototype Properties to Reduce Duplicate Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-prototype-properties-to-reduce-duplicate-code)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

Dog.prototype.numLegs = 2;

// Only change code above this line
let beagle = new Dog("Snoopy");

```
### 166.[Iterate Over All Properties](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/iterate-over-all-properties)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

Dog.prototype.numLegs = 4;

let beagle = new Dog("Snoopy");

let ownProps = [];
let prototypeProps = [];

// Only change code below this line
for(let prop in beagle){
  beagle.hasOwnProperty(prop) ? ownProps.push(prop) : prototypeProps.push(prop);
}

console.log('own property:' + ownProps);
console.log('prototype property:' + prototypeProps);
```
### 167.[Understand the Constructor Property](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/understand-the-constructor-property)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

// Only change code below this line
function joinDogFraternity(candidate) {
  return candidate.constructor === Dog ? true : false;
}
```
### 168.[Change the Prototype to a New Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/change-the-prototype-to-a-new-object)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

Dog.prototype = {
  // Only change code below this line
  numLegs: 2,
  eat: () => {
    console.log(`eat function`); 
  },
  describe: () => {
    console.log(`name is ${this.name}`);
  }
};
```
### 169.[Remember to Set the Constructor Property when Changing the Prototype](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/remember-to-set-the-constructor-property-when-changing-the-prototype)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

// Only change code below this line
Dog.prototype = {
  constructor: Dog,
  numLegs: 4,
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name);
  }
};

const d = new Dog('sd');
console.log(d.constructor === Dog);
```
### 170.[Understand Where an Object’s Prototype Comes From](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/understand-where-an-objects-prototype-comes-from)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

let beagle = new Dog("Snoopy");

// Only change code below this line
Dog.prototype.isPrototypeOf(beagle);
```
### 171.[Understand the Prototype Chain](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/understand-the-prototype-chain)
#### My Solution
```javascript
function Dog(name) {
  this.name = name;
}

let beagle = new Dog("Snoopy");

Dog.prototype.isPrototypeOf(beagle);  // yields true

// Fix the code below so that it evaluates to true
Object.prototype.isPrototypeOf(Dog.prototype);
```
### 172.[Use Inheritance So You Don't Repeat Yourself](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-inheritance-so-you-dont-repeat-yourself)
#### My Solution
```javascript
function Cat(name) {
  this.name = name;
}

function Bear(name) {
  this.name = name;
}

function Animal() { }

Animal.prototype = {
  constructor: Animal,
   eat: function() {
    console.log("nom nom nom");
  }

};
```
### 173.[Inherit Behaviors from a Supertype](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/inherit-behaviors-from-a-supertype)
#### My Solution
```javascript
function Animal() { }

Animal.prototype = {
  constructor: Animal,
  eat: function() {
    console.log("nom nom nom");
  }
};

// Only change code below this line

let duck = Object.create(Animal.prototype); // Change this line
let beagle = Object.create(Animal.prototype); // Change this line
```
### 174.[Set the Child's Prototype to an Instance of the Parent](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/set-the-childs-prototype-to-an-instance-of-the-parent)
#### My Solution
```javascript
function Animal() { }

Animal.prototype = {
  constructor: Animal,
  eat: function() {
    console.log("nom nom nom");
  }
};

function Dog() { }

// Only change code below this line

Dog.prototype = Object.create(Animal.prototype);

let beagle = new Dog();
```
### 175.[Reset an Inherited Constructor Property](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/reset-an-inherited-constructor-property)
#### My Solution
```javascript
function Animal() { }
function Bird() { }
function Dog() { }

Bird.prototype = Object.create(Animal.prototype);
Dog.prototype = Object.create(Animal.prototype);

// Only change code below this line
Bird.prototype.constructor = Bird;
Dog.prototype.constructor = Dog;


let duck = new Bird();
let beagle = new Dog();

console.log(duck.constructor, beagle.constructor);
```
### 176.[Add Methods After Inheritance](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/add-methods-after-inheritance)
#### My Solution
```javascript
function Animal() { }
Animal.prototype.eat = function() { console.log("nom nom nom"); };

function Dog() { }

// Only change code below this line
Dog.prototype = Object.create(Animal.prototype);

Dog.prototype.constructor = Dog;

Dog.prototype.bark = () => {
  console.log('Woof!');
}

// Only change code above this line

let beagle = new Dog();
```
### 177.[Override Inherited Methods](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/override-inherited-methods)
#### My Solution
```javascript
function Bird() { }

Bird.prototype.fly = function() { return "I am flying!"; };

function Penguin() { }
Penguin.prototype = Object.create(Bird.prototype);
Penguin.prototype.constructor = Penguin;

// Only change code below this line
Penguin.prototype.fly = () => 'Alas, this is a flightless bird.';


// Only change code above this line

let penguin = new Penguin();
console.log(penguin.fly());
```
### 178.[Use a Mixin to Add Common Behavior Between Unrelated Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-a-mixin-to-add-common-behavior-between-unrelated-objects)
#### My Solution
```javascript
let bird = {
  name: "Donald",
  numLegs: 2
};

let boat = {
  name: "Warrior",
  type: "race-boat"
};

// Only change code below this line
const glideMixin = (obj) => {
 obj.glide =  () => console.log('glide');
}

glideMixin(bird);
glideMixin(boat);
```
### 179.[Use Closure to Protect Properties Within an Object from Being Modified Externally](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-closure-to-protect-properties-within-an-object-from-being-modified-externally)
#### My Solution
```javascript
function Bird() {
  let weight = 15;
  
  this.getWeight = () => weight;

}

```
### 180.[Understand the Immediately Invoked Function Expression (IIFE)](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/understand-the-immediately-invoked-function-expression-iife)
#### My Solution
```javascript
(function() {
  console.log("A cozy nest is ready");
})();
```
### 181.[Use an IIFE to Create a Module](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/object-oriented-programming/use-an-iife-to-create-a-module)
#### My Solution
```javascript
let isCuteMixin = function(obj) {
  obj.isCute = function() {
    return true;
  };
};
let singMixin = function(obj) {
  obj.sing = function() {
    console.log("Singing to an awesome tune");
  };
};

const funModule = (function(){
  return {
    isCuteMixin: function(obj) {
       obj.isCute = function() {
        return true;
    };
  },
  singMixin: function(obj) {
    obj.sing = function() {
      console.log("Singing to an awesome tune");
    };
  }
 }
})();
```
## Asynchronicity Exercises
### 182.[CHALLENGE 1](http://csbin.io/async)
#### My Solution
```javascript
/* CHALLENGE 1 */

function sayHowdy() {
  console.log('Howdy');
}

function testMe() {
  setTimeout(sayHowdy, 0);
  console.log('Partnah');
}
// After thinking it through, uncomment the following line to check your guess!
testMe(); // what order should these log out? Howdy or Partnah first?
//log Partnah
//log Howdy
```
### 183.[CHALLENGE 2](http://csbin.io/async)
#### My Solution
```javascript
/* CHALLENGE 2 */

function delayedGreet() {
  // ADD CODE HERE
  setTimeout(() => console.log('welcome'), 3000);
}
// Uncomment the following line to check your work!
delayedGreet(); // should log (after 3 seconds): welcome
```
### 184.[CHALLENGE 3]()
#### My Solution
```javascript
/* CHALLENGE 3 */

function helloGoodbye() {
  // ADD CODE HERE
  console.log('hello');
  
  setTimeout(() => console.log('good bye'), 2000);
}
// Uncomment the following line to check your work!
helloGoodbye(); // should log: hello // should also log (after 3 seconds): good bye
```
### 185.[CHALLENGE 4](http://csbin.io/async)
#### My Solution
```javascript
/* CHALLENGE 4 */

function brokenRecord() {
  // ADD CODE HERE
  setInterval(() => console.log('hi again'), 1000);
}
// Uncomment the following line to check your work!
brokenRecord(); // should log (every second): hi again
```
### 186.[CHALLENGE 5](http://csbin.io/async)
#### My Solution
```javascript
/* CHALLENGE 5 */

function limitedRepeat() {
  // ADD CODE HERE
  let i = 0;
  const interval = setInterval(() => {
    i++ === 5 ? clearInterval(interval) : console.log('hi for now');
  }, 1000);
}
// Uncomment the following line to check your work!
limitedRepeat(); // should log (every second, for 5 seconds): hi for now
```
### 187.[](http://csbin.io/async)
#### My Solution
```javascript

```
### 188.[](http://csbin.io/async)
#### My Solution
```javascript

```
### 189.[]()
#### My Solution
```javascript

```
### 190.[]()
#### My Solution
```javascript

```
### 191.[]()
#### My Solution
```javascript

```

