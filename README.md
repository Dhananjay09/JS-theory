# JS-theory
# Primitive vs Non Primitive
In primitive type of values comarission is done based on value but in case of Non Primitive it is done base on refrence.
# Primitive Types in Js
- String
- Number
- Boolean
- NUll
- Undefined
# Expression 
- Piece of code which produce a value.
# Statement 
Piece of code which does something.
# Number
- Number datatype in js has only one type that is double. Every value is stored as double. It has 2 more values Infinity and NAN.
- var x = Number(''); // x= 0
- var x = Number(null); // x= 0
- var x = Number(undefined);// x= NAN
- var x = Number(Infinity); // x = Infinity
- var x = Number(false); // x= 0
- var x = Number(true); // x= 1
- var x = Number(NaN); // x=NaN
# NAN
- It stand for Not A Number, it is considered as error.
- Equality is not valid for NaN. NaN === NaN will give false result.
# Static vs Dynamic
- If type is known at the time of Compiling it is Static.
- If type is known at run time, it is Dynamic.
# Static Type vs Dynamic Type
- If types are specified at compile time and vice versa in case of Dynamic.
# Static Type Cheching vs Dynamic Type Checking
- To perform the operations in case of the being the type same is Static else Dynamic.
# JS Types
- Js has 5 primitive type and one Object type.
# Coercion or TypeCasting
- Converting the data types of the variables.
# Implicit Type Casting vs Explicit type Casting
- Type getting converted automatically is Implicit but doing by own is explicit.
# Autoboxing 
- Changing the type and then making it same as earlier.
Example : console.log('djcnfv'.length); length is there in object not in string but it gets converetd into object and then back to string.
# Type checking
- console.log(typeof(undefined), typeof(null)); // undefined object
- console.log(undefined == null ); // True
- console.log(undefined === null ); // False
- console.log(''===false); // false
- console.log(''==false); // True

# Closures
- Closure is a function that returns a function by wrapping the variables.
- It refers to ability of a function to remember and modify the variables of parent, grandparent...... scope.

# use of Closures
- Creating Encaptulation, Event Handler, Callbacks, etc because these need to remenber their parents scope.

# Methods
- Methods are functions which are always called with objects.
# this keywork
- 'this' is run time binding.
- this completly depends on how the function has been called.
# Default binding
- When neither class not object is associated with this keyword, this refers to window.
# Implicit bindng
- Passing object imlicitly for this.
# Explicit Binding
- Call, bind, apply
# Bind
- Bind is a function called with an object to specify the this keyword. It is permanetly binded to the object pass.
- const antmethod(a,b)
- const bindedfunction = anymethod.bind(null, a);
- bindedfunction(b); //Will work 
# Call
- It does not return a function, but works simmilarily. This is not permanently binded.
# Apply
- It is same as call but arguments are called as array. It is used if we don't amount of arguments are given.
- We can call Math.max.apply(null, [2,3,2,5]); 
- It will not work as Math.max([1,3,4,2,5])
# use strict
- By writing that we execute our code in strict mode.
- It does not silently ignore the ignorable errors.
- use strict makes the code more efficient.
# new
- new keyword is used when we want to make a function behave like constructor method.
- in this case value of this becomes {}.
# Objects
- Everything in js is object except primitives.
- Array, functions and objects itself are objects.
- Object is collection of properties[key-value pair].
- Every ken of js property should be string, value can be anything.
# Creating objects
- const obj = {};
- const obj = new Object();//do not use
- const obj = Object.create(Object.prototype);https://github.com/Dhananjay09/JS-theory/blob/main/Screenshot%20from%202022-02-21%2019-40-24.png
- Deletion can be done using delete obj.property.
# obj.hasOwnProperty() showld be used to check if a property exist or not. Because 'prop' in obj given the property that are accessible to obj.
# Object.keys(obj)
- To get all the keys of object only, exclusing the symbols.
# Reflect.ownKeys() 
- To get all the keys of object obly with symbol.
# Object.values(obj)
- To get all the values in the object only.
# Object.entries(obj) 
- to get all the value, key - value pair in obj.
# Charecterstics of Prototypal Language
- Classes are not present.
- Everything is public. No private or protected.
- Object inherits Objects.
- Not traditibal Oops language.
# Prototype
- Prototype is working object instance.
- Every object in js has one parent by default until it is difined to be null.
- Every object has an property Prototype and every instance of a function is also said prototype.
# Prototype-based Programming Language
- Method of reusing the functionality in js is known as Prototype based programming language where objects are linked with each other using their prototypes. It is also calles instance based, classless, prototypal, prototype-based language.
# Delegation 
- Searching the property to parent or in grandparent is called delegation.
# Any object has only read access to protype chain.
# Accessing the prototype
# Object.getPrototypeOf()
- const obj1 = {name : 'dj'};
- const obj2 = Object.create(obj1);
- console.log(Object.getPrototypeOf(obj2)); // {name : dj}
- console.log(obj2.name); // dj
# Object.setPrototypeOf(child, parent);
- Modifyting prototype of child to point another object as its parent.
# child.__proto__ = obj
- To point the parent as obj.
# prototype function
- Any function executed with new keyword is called constructor function.
- It return this if nothing is retuned or non object value is returned.
# Diffrent between .prototype and [[prototype]]
- [[prototype]] is an internal property present in all objects.
- Its value can be refrence of another object or null. like parent.
- .prototype is an present only inside the function, not inside arrow functions.
- It contains value or methods that are shared amoung all the objects of that class.
- [[prototype]] can't be modified but .prototype can be modified.

# Prototypes 
function Person(){
}
const p = new Person()
- Object.getPrototypeof(p) => Person.prototype
- Object.getPrototypeof(Person) => Function.prototype
- Object.getPrototypeof(Object) => Function.prototype
- Object.getPrototypeof(Function.prototype) => Object.prototype
- Object.getPrototypeof(Object.prototype) => null

# ES6 introduces class which are syntactic sugar of the function.
- class Dj{
    constructor(name){
        this.name = name
    }
    getName(){
        return this.name
    }
    setName(name){
        this.name = name
    }
}

class Dhananjay extends Dj{
    constructor(name, id){
        super(name)
        this.id=id
    }
    getName(){
        return super.getName()
    }
}

# Type of Properties in Js
- There are three types of property
- Data Property
- Internal Property
- Accessor Property

# Data Property
- Most commonly used property. 
- For example  const data = {  name :  "Dhananajay"}

# Internal property
- [[prototype]] these properties can't be directly accessed/modified, to modify them we need some js apis.

# Accessor properties
- These properties look likes to be data properties but they are not actually.
- const data = {
- nm = "Dhananjay",
- get name(){
- return this.nm;
- }
- set name(name){
- this.nm = name;
- }
- }
- Now we can use them as data.name, or data.name= "Ajay". 

# Buildinhg blocks of js are not the properties but building blocks are attributes. 
- Each property {name : 'dj'} has four attributes, 
- [[value]], [[writable]], [[Enumerable]], [[Configurable]], which are building block of the js.

# Descriptor
- Descriptor is set of properties.

# Object.getOwnPropertyDescriptor(obj)
- This will retuen all the four building blocks of each property in teh object.

# [[writable]] 
- Can we modify or not.
# [[Enumerable]]
- We can enumerate over the property through for in or not.
# [[Configurable]]
- It tells that we can delete or not, we can change the property type or not elc.

# Accessor Properties building block
- These are [[Get]], [[Set]], [[Enumerable]], [[Configurable]]

# Setting these Properties
- Object.defineProperty(obj, 'name' , { value : "Dhananjay" })
- This will make the object as obj = {name : "Dhananjay"}, 
- By this way all the other 3 properties will be false.
- ![Accessing properties](https://github.com/Dhananjay09/JS-theory/blob/main/Screenshot%20from%202022-02-21%2019-40-24.png)

# Protecting Objects
- Preventing Extensions
- Sealing
- Freezing

# Preventing Extensions
- Object.preventExtentions(obj) => Can't add extra properties to any object.
- Object.isExtensible()

# Sealing
- Same as Extensible but added configurable as true. So we can't delete the property.

# Freezing
- Same as Sealing but now can't delete also, in this writable is false.
# Descriptor
![](https://github.com/Dhananjay09/JS-theory/blob/main/Screenshot%20from%202022-02-21%2019-58-41.png)

# Js is non blocking language, it does not wait instead it start executing further.
- This os possible with the help of callbacks.

# Disadvantage of callbacks
- Readability, complexity and debugging becomes very tough, loss of control flow.
- Result of the callback stroed in the variable would become undefined.
- Callback can't be wraped in try/catch.
- Can't decide weather the callback is habdled as sunc or insync way.

# Promises(Future)
- Promise is an object which represents eventual completion of some task.
- There are three states of Promise.
- Pending.
- Fulfilled.
- Rejected
# Promiss Fulfilment
- After fulfilment is one time process, if it is fulfilled it can't be rejected and vice ver...
const pms = new Promise((resolve, reject)=>{
   resolve(10);
})

# Consuming of Promises
- .then, .catch, .finally

# .then
- It takes two functions one for resolved and one for rejected.
- pms.then((res) => console.log(`Resolved ${res}`), (err) => console.error(err));

# .catch
- It has only one function that execreed on rejected.
- It promise is rejected nearest catch block is called.
# .finally 
- It is called on the Promise fulfilment
pms.finally(()=> {});
