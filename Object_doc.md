
# Objects in JavaScript

## [](https://github.com/zjacobsdev/Object_Documention-/blob/master/Object_doc.md#what-is-an-object)What is an object?

> Its one of JavaScript's data types . Its an unordered list of properties, methods, and attributes which are made up of a key and a value associated with it. Its one of JavaScript's data types.

> Example: Car is the object

```javascript
let car = {

 // Properties and methods go here
 
}

```

You can identify an a object being declared by the binding name being set equal a set of curly braces like the example above.

----------

There are properties and/or methods associated with that object.

> **Properties**  are the specific characteristics of the object. It is what differentiates two or more objects from each other.

***Example 1:*** If a car is the object. The properties could be the model, the color, the brand or the weight.

```javascript
let Car = {

  model: 'sedan'
  color: 'red'
  brand: 'Lexus'

}

```

You can assign numbers, strings, and even other objects a property.

> **Methods**  defines the actions/behavior of the object.

 ***Example 2:*** If a car is the object. The one of these methods could be the calculating speed of the car.

```javascript
let Car = {

      speed: function(){
         // Function statement goes here

      }
}

```

## [](https://github.com/zjacobsdev/Object_Documention-/blob/master/Object_doc.md#how-are-objects-useful-in-javascript)How are objects useful in JavaScript?

> JavaScript objects can be created by simply setting their properties within a pair of curly braces: {...}. Each property is a key/value pair (A key points to a value stored in memory). This is called an object literal. The advantage is that the things that belong together are put together in code. Such as anything key/value pair associated with the object “car” should be in that object.

What allows this leeway is the concept of object-orientated programming (OOP)

> **Object-Oriented Programming (OOP)**  refers to a type of computer programming where the programmer defines the data type of a data structure, its operations (functions) that can be applied.

There are four principles of object-oriented programming:

1. [Encapsulation](https://developer.mozilla.org/en-US/docs/Glossary/Encapsulation)
2. [Abstraction](https://developer.mozilla.org/en-US/docs/Glossary/Abstraction)
3. [Inheritance](https://developer.mozilla.org/en-US/docs/Glossary/Inheritance)
4. [Polymorphism](https://developer.mozilla.org/en-US/docs/Glossary/Polymorphism)

Once you understand these concepts the world of OOP comes alive.

## [](https://github.com/zjacobsdev/Object_Documention-/blob/master/Object_doc.md#how-do-you-create-new-objects)How Do You Create New Objects?

1.  Use an object initializer
    
    -   Simply setting its value in a set of curly braces refer to **Example 1**

2. Create  a  constructor with a function or classes to create an instance of an object.
    
    > A  **constructor **  is a way to create an object using a function to create a new instance of a class with given parameters.  It is like a blueprint for making multiple objects with the same properties and methods. There are two ways to create a instance of a new object.
    
  ##### [](https://github.com/zjacobsdev/Object_Documention-/blob/master/Object_doc.md#method-1--the-old-way-prototype-based-inheritance)Method 1 ( using a function )
  
```javascript
  function Car(model, color, brand) = {

//instance of object properties in a constructor.
  this.model: model,
  this.color: color,
  this.brand : brand,
  
///Methods used
  this.speed: function {
  
    //Calculates and returns the speed
    
  }
}
```
    
 What makes this constructor over a normal function is the that the first letter when naming the constructor must be *capitalization*.

##### [](https://github.com/zjacobsdev/Object_Documention-/blob/master/Object_doc.md#method-2--classes-introduced-in-ecmascript-2015)Method 2 ( using a class, introduced in ECMAScript 2015)
```javascript
    class Car = {
    
     		//instance of object properties
     		
     		constructor (model, color, brand) {
     		    this.model: model;
     		    this.color: color;
     		    this.brand: brand;
     		  }
     		  }
    
     	///Methods used
     	
     	  speed() {
     	  
         //Calculates and returns the speed
       }
    
     }
    
   ```
   
And by using the keyword  ```new```  you can create an new instance of that object with the it properties and methods.

***Example 3:***
```javascript     
function Car(model, color, brand) = {

//instance of object properties in a constructor.
  this.model: model,
  this.color: color,
  this.brand : brand,
}

let newCar1 = new Car('sedan','red','Buick')
let newCar2 = new Car('coupe','green','Mercedes')

console.log(newCar1)
// Outputs the new instance of the object Car under the variable name newCar1 
```

## [](https://github.com/zjacobsdev/Object_Documention-/blob/master/Object_doc.md#how-to-access-the-properties-and-methods-in-objects)How to access the properties and methods  of an object?

Let's look some of JavaScript's built-in properties and methods:
```javascript
Math.random()   
```
The Math object is holding the method random().

```javascript 
let Math = {

	///Some properties.....
	
	///Some other methods.......
	
	random: function(){
	
	/// Returns a random number between 0-1
	
	}

}
```

If you use Math.random() before then you have already been accessing the method random() from the Math object which returns an random number between 0 and 1. Let'd try this with our own custom object.

To use and get a return from that method use either dot notation ( **.** ) or bracket notation( {} ).

***Example 4:***
To access the properties and methods from the Car object:
```javascript
//Dot notation
let carColor = Car.color     // The carCar variable now holds the value'red' from the color property in the Car object.
let carSpeed = Car.speed()    // The carSpeed variable now holds the value of the return of the speed method in the Car object.

//Bracket Notation 
let carColor = Car['color']  // Same as above
let carSpeed = Car.['speed()']  // Same as above

console.log (carColor)  
// Output: 'red'

console.log (carSpeed) 
// Output: 39 mph <-- Calulated by the speed() method.
```
Dot notation is more commonly used than bracket notation.

## How to change, add, and delete an object's properties and methods?  

***Example 5:***

If you want to change a value of a property, just reassign it like you would do a variable.

```javascript
let Car = {

  model: 'sedan'
  color: 'red'     // Initial color property
  brand: 'Lexus'

}

Car.color = 'purple'  // Changes color property to purple.

console.log(Car.color)
// Outputs : 'purple'  
```

#### What if you want the same properties from an object but what to add/ delete some of its properties and methods for a new object?
In this case, we can use a concept of prototypal inherience using prototypes within JavaScript.

>  Every object in Javascript has a  **prototype**. It is simply a reference to another object and contains common   characteristics across all instances of an object. An object’s prototype characteristics specifies the object from which it inherits those  characteristic. In other words, when a messages reaches an object, JavaScript will attempt to find a property in that object first, if it cannot find it then the message will be sent to the object’s prototype (the parent object)  and so on. 

>   
***Example 6:***
```javascript
function Car(model, color, brand) = {

//instance of object properties in a constructor.
  this.model: model,
  this.color: color,
  this.brand : brand,
}

let newCar1 = new Car('sedan','red','Buick')
let newCar2 = new Car('coupe','green','Mercedes')

newCar2.prototype.hasRadio= true  // now newCar2 also has an additional property of hasRadio but this new property does not get added the parent object Car

console.log(newCar2)
// Outputs: The properties and methods based around the Car object and the corresponding values for newCar2 and a new property of hasRadio.
```
To delete properties of methods use the keyword ```delete```

***Example 7:***
```javascript 
function Car(model, color, brand) = {

//instance of object properties in a constructor.
  this.model: model,
  this.color: color,
  this.brand : brand,
}

let newCar1 = new Car('sedan','red','Buick')
let newCar2 = new Car('coupe','green','Mercedes')

delete newCar1.brand

console.log(newCar)
// Outputs: undefinded

```

## What other things you can do to objects?

This document just goes over of the basic concepts about objects in JavaScript, if you want more check the sources below. 

## Other Sources and Documentation

[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

[Understanding Classes in JavaScript](https://www.digitalocean.com/community/tutorials/understanding-classes-in-javascript)

[Understanding "Prototypes" in JavaScript](https://yehudakatz.com/2011/08/12/understanding-prototypes-in-javascript/)

[Prototypal inheritance](https://www.digitalocean.com/community/tutorials/understanding-classes-in-javascript)

[Object prototypes (MDN)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)

[JavaScript | Object Constructors](https://www.geeksforgeeks.org/javascript-object-constructors/)






