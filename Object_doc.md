# Objects in JavaScript

## What is an object?
[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

>An **object** is an unordered list of  properties, methods, and attributes which are made up of a key and a value associated with it.

>Example: Car is the object 

    let car = {
     // Properties and methods go here
    }
You can identify an a object being declared by the binding name being set equal a set of curly braces like the example above.

----
There are properties and/or methods associated with that object.

>**Properties** are the specific characteristics of the object. It is what differentiates two or more objects from each other. 

>Example: If a car is the object. The properties could be the model, the color, the brand or the weight. 

    let car = {

      model: 'sedan'
      color: 'red'
      brand: 'Lexus'

    }
>**Methods** defines the actions/behavior of the object.

>Example: If a car is the object. The one of those methods could be the calculating speed of the car.

    let car = {

          speed: function(){
             // Function statement goes here

          }
    }
## How are objects useful in JavaScript?

>JavaScript objects can be created by simply setting their properties within a pair of curly braces: {...}. Each property is a # key/value pair (A key points to a value stored in memory). This is called an object literal. The advantage is that the things that belong together are put together in code. Such as anything key/value pair associated with the object “car” should be in that object.

*Objects allows for leeway to be creative. Nothing is definite.

What allows this leeway is the concept of object-orientated programming (OOP)

>**Object-Oriented Programming (OOP)** refers to a type of computer programming where the programmer defines the data type of a data structure, its operations (functions) that can be applied.


There are four principles of object-oriented programming:

- [**Encapsulation**]([https://developer.mozilla.org/en-US/docs/Glossary/Encapsulation])
-  [**Abstraction**]([https://developer.mozilla.org/en-US/docs/Glossary/Abstraction])
-  [**Inheritance**]([https://developer.mozilla.org/en-US/docs/Glossary/Inheritance])
- [**Polymorphism**]([https://developer.mozilla.org/en-US/docs/Glossary/Polymorphism])

Once you understand these concepts the world of OOP comes alive.

## How Do You Create New Objects?

1. Use an object initializer
	- Simply setting its value in a set of curly braces

2. Create a **constructor function**  ( there are two methods)
	>A **constructor function** is a way to create an object using a function to create a new instance of a class with given parameters.
		There are two ways to create a instance of a new object
	
      ##### Method 1 ( the old way: prototype-based inheritance)
       function Car = {
       
				//instance of object properties
				constructor (height, width) {
				    this.height = height;
				    this.width = width;
				  }

			///Methods used
			  speed() {
		    //Calculate Speed
		  }

    ##### Method 2 ( Classes, introduced in ECMAScript 2015)
       class Car = {
       
				//instance of object properties
				
				constructor (height, width) {
				    this.height = height;
				    this.width = width;
				  }

			///Methods used
			
			  speed() {
		    //Calculate Speed
		  }

		}
And by using the keyword **new** you can create an new instance of that object with the it properties and methods.

### How to access the properties and methods in objects?

Let's look at built-in JavaScript properties and methods

Array.isArray- method best fit for identifying arrays

You can assign numbers, strings, and even other objects to property

