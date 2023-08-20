## Types
in JS everything is object is false, the true is in JS most things are object.
in JS variables don't have types, value do.

### Primitive Type
- null
- undefined
- boolean
- string
- number
- symbol
- bigint
- object
### Subtype of a object type
- array
- functions
  
### typeof  
typeof operator return string that indicate the type 

null in typeof operator return 'object' is a bug 
### Coding Examples
```javascript
console.log(typeof "ahmade");
//log 'string'

console.log(typeof null);
//log 'object'
```

### undefined vs undeclared
1. undefined means there is a variable but at the moment  has no value.
2. undeclared means never been created.
3. uninitialized means have a variable never be initialized (not allow to touch these variable).

### NaN  
NaN is a invalid number

so we use isNaN to check if not anumbr 

NaN with any operation, output always NaN

NaN its only value that is not equal to itself (not have identity property)

triple equal (===) in NaN and negative zero its lies
