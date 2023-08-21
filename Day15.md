## Equality 

### Loose Equality vs Strict Equality 

#### Loose Equality 
double equal (==):
1. check value
2. allows coercion (different types)
3. prefer to numeric comparison (ToNumber)
4. invoke coercion if type is different
5. if non-primitive ToPrimitive
6. algorithm repeat itself
#### Coding Examples
```javascript
console.log(null == undefined);
//log true

console.log(42 == [42]); 
convert [42] ToPrimitive to "42"
prefer numeric and convert string to 42
//log true

console.log([] == ![]); 
//[] == false 
//"" == false
//0 == false
//0 == 0 
//log true

//log true

```

   
#### Strict Equality 
triple equal (===):
1. check value and type
2. disallows coercion (same types)


