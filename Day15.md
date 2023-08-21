## Equality 

### Loose Equality vs Strict Equality 

#### Loose Equality (==)
1. check value.
2. allows coercion (different types).
3. prefer to numeric comparison (ToNumber).
4. invoke coercion if type is different.
5. if non-primitive ToPrimitive.
6. algorithm repeat itself.
7. comparison with known types.
#### Coding Examples.
```javascript
console.log(null == undefined);
//log true

console.log(42 == [42]); 
//convert [42] ToPrimitive to "42"
//prefer numeric and convert string to 42
//log true

console.log([] == ![]); 
//[] == false 
//"" == false
//0 == false
//0 == 0 
//log true
```
#### Avoid loose equal 
1. with non-primitive.
2. with true and false.
3. with 0 or "".

#### Strict Equality 
triple equal (===):
1. check value and type
2. disallows coercion (same types)

#### The Case of Double equal
not knowing a types means not fully understand the code

  => if the same types prefer use == over === (== faster).
  
  => if types are different use === be broken, prefer use == or not compare.
  
  => if know the types whether it's match or not, == is more sensible choice.
  
  => if don't know the types, === is the reasonable choice (not knowing types should be obvious to reader).


### Static Typing


