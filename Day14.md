### Abstract Operations (ToPremitive)

### Coercion
converts of values from one data type to another
### Coding Examples
```javascript
var x = 10 + '30';
console.log(x);
//log 1030

console.log("ahmade" + 25)
//log ahmade25

console.log("ahmade" + true)
//log ahmadetrue
```

#### ToString
```javascript

null      //"null"
undefined //"undifined"
true      //"true"
false     //"false"
0         //"0"
-0        //"0"
30        //"30"
[]        //""
[1,3]     //"1,3"
{}        //[object Object] 
```
#### ToNumber
```javascript
null      //0
undefined //NaN
true      //1
false     //0
"0"       //0
"-0"      //-0
"0."      //0
"003"     //3
"30.12"   //30.12
[]        //0
[1,3]     //NaN
```
#### ToBoolean
```javascript
null      //false
undefined //false
true      //true
false     //false
0         //false
-0        //false
20        //true 
"30.12"   //true
[1,3]     //true
```
