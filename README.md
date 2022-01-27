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
- It refers to ability of a function to remember and modify the variables of parent, grandparent...... scope.
# use of Closures
- Event Handler, Callbacks, etc because these need to remenber their parents scope.

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
