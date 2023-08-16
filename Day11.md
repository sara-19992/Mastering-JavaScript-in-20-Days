## Classes & Prototypes


1. generate object using a function (copies of object, don't repeat yourself, can't add new functionality).
2. Prototype chain
3. classes

Prototype chain 
when assign object create a link to functions stored and store in hidden property proto,
when call function search on the object if can't find it go to link and search. 
 
1. chain conenction a link a refrence to that function.
2. when create object using Object.create() methode return empty object.
3. all object in js has proto property link to Object.prototype. 
4 Object.prototype is big object which proto link to Null.
