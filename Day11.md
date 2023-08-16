## Classes & Prototypes


1. generate object using a function (copies of object, don't repeat yourself, can't add new functionality).
2. Prototype chain
3. classes

Prototype chain 
when assign object create a link to functions stored and store in hidden property proto, when call function search on the object if can't find it go to link and search. 

When creating a function, a property object called prototype is being created automatically (you didn't create it yourself) and is being attached to the function object. 
 
1. chain connection a link a reference to object functions.
2. when create object using Object.create() method return empty object.
3. all object in JS has proto property link to Object.prototype as default (proto link to object stored function).
4 Object.prototype is big object which proto link to Null.

