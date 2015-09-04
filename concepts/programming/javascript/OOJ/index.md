---
title: OOJ
tags:
  - Inheritance
  - JavaScript
readiness: 'Not Ready'
summary: "JavaScript has strong object-oriented programming capabilities, even though some debates have taken place due to the differences in object-oriented JavaScript compared to other languages.\n"
uri: concepts/programming/javascript/OOJ
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/OOJ/tutorials/JavaScript/reintroduction
    - concepts/programming/javascript/OOJ/guides/JavaScript
    - concepts/programming/javascript/OOJ/js/objects
    - concepts/programming/javascript/OOJ/js/objects/Object/create
    - concepts/programming/javascript/OOJ/js/objects/Function/call
    - concepts/programming/javascript/OOJ/js/objects/Function/apply
    - concepts/programming/javascript/OOJ/js/objects/Object/prototype

---
# Introduction to object-oriented JavaScript

## Summary

JavaScript has strong object-oriented programming capabilities, even though some debates have taken place due to the differences in object-oriented JavaScript compared to other languages.

This article starts with an introduction to object-oriented programming, then reviews the JavaScript object model, and finally demonstrates concepts of object-oriented programming in JavaScript.

## JavaScript review

If you don't feel confident about JavaScript concepts such as variables, types, functions, and scope you can read about those topics in [A re-introduction to JavaScript](/w/index.php?title=concepts/programming/javascript/OOJ/tutorials/JavaScript/reintroduction&action=edit&redlink=1). You can also consult the [JavaScript Guide](/w/index.php?title=concepts/programming/javascript/OOJ/guides/JavaScript&action=edit&redlink=1).

## Object-oriented programming

Object-oriented programming is a programming paradigm that uses abstraction to create models based on the real world. It uses several techniques from previously established paradigms, including modularity, polymorphism, and encapsulation. Today, many popular programming languages (such as Java, JavaScript, C\#, C++, Python, PHP, Ruby and Objective-C) support object-oriented programming (OOP).

Object-oriented programming may be seen as the design of software using a collection of cooperating objects, as opposed to a traditional view in which a program may be seen as a collection of functions, or simply as a list of instructions to the computer. In OOP, each object is capable of receiving messages, processing data, and sending messages to other objects. Each object can be viewed as an independent little machine with a distinct role or responsibility.

Object-oriented programming is intended to promote greater flexibility and maintainability in programming, and is widely popular in large-scale software engineering. By virtue of its strong emphasis on modularity, object oriented code is intended to be simpler to develop and easier to understand later on, lending itself to more direct analysis, coding, and understanding of complex situations and procedures than less modular programming methods.<sup>[1](#Reference)</sup>

## Terminology

 Class
:   Defines the characteristics of the Object.
 Object
:   An Instance of a Class.
 Property
:   An Object characteristic, such as color.
 Method
:   An Object capability, such as walk.
 Constructor
:   A method called at the moment of instantiation.
 Inheritance
:   A Class can inherit characteristics from another Class.
 Encapsulation
:   A Class defines only the characteristics of the Object, a method defines only how the method executes.
 Abstraction
:   The conjunction of complex inheritance, methods, properties of an Object must be able to simulate a reality model.
 Polymorphism
:   Different Classes might define the same method or property.

For a more extensive description of object-oriented programming, see [Object-oriented programming](http://en.wikipedia.org/wiki/Object_oriented_programming) at Wikipedia.

## Prototype-based programming

Prototype-based programming is a style of object-oriented programming in which classes are not present, and behavior reuse (known as inheritance in class-based languages) is accomplished through a process of decorating existing objects which serve as prototypes. This model is also known as class-less, prototype-oriented, or instance-based programming.

The original (and most canonical) example of a prototype-based language is the programming language Self developed by David Ungar and Randall Smith. However, the class-less programming style has recently grown increasingly popular, and has been adopted for programming languages such as JavaScript, Cecil, NewtonScript, Io, MOO, REBOL, Kevo, Squeak (when using the Viewer framework to manipulate Morphic components), and several others.<sup>[1](#References)</sup>

## JavaScript Object Oriented Programming

### Core Objects

JavaScript has several objects included in its core; for example, there are objects like Math, Object, Array, and String. The example below shows how to use the Math object to get a random number by using its `random()` method.

    alert(Math.random());

**Note**: This and all further examples presume a function named `alert` (such as the one included in web browsers) is defined globally. The `alert` function is not actually a part of JavaScript itself.

 See [JavaScript objects](/w/index.php?title=concepts/programming/javascript/OOJ/js/objects&action=edit&redlink=1) for a list of the core objects in JavaScript.

Every object in JavaScript is an instance of the object `Object` and therefore inherits all its properties and methods.

### Custom Objects

#### The Class

JavaScript is a prototype-based language which contains no class statement, such as is found in C++ or Java. This is sometimes confusing for programmers accustomed to languages with a class statement. Instead, JavaScript uses functions as classes. Defining a class is as easy as defining a function. In the example below we define a new class called Person.

    function Person() { }

#### The Object (Class Instance)

To create a new instance of an object *`obj`* we use the statement `new obj`, assigning the result (which is of type *`obj`*) to a variable to access it later.

In the example below we define a class named `Person` and we create two instances (`person1` and `person2`).

    function Person() { }
    var person1 = new Person();
    var person2 = new Person();

**Note**: Please also see [Object.create](/w/index.php?title=concepts/programming/javascript/OOJ/js/objects/Object/create&action=edit&redlink=1) for a new and alternative instantiation method.

#### The Constructor

The constructor is called at the moment of instantiation (the moment when the object instance is created). The constructor is a method of the class. In JavaScript, the function serves as the constructor of the object; therefore, there is no need to explicitly define a constructor method. Every action declared in the class gets executed at the time of instantiation.

The constructor is used to set the object's properties or to call methods to prepare the object for use. Adding class methods and their definitions occurs using a different syntax described later in this article.

In the example below, the constructor of the class `Person` displays an alert when a `Person` is instantiated.

    function Person() {
      alert('Person instantiated');
    }

    var person1 = new Person();
    var person2 = new Person();

#### The Property (object attribute)

Properties are variables contained in the class; every instance of the object has those properties. Properties should be set in the prototype property of the class (function) so that inheritance works correctly.

Working with properties from within the class is done by the keyword `this`, which refers to the current object. Accessing (reading or writing) a property outside of the class is done with the syntax: `InstanceName.Property`; this is the same syntax used by C++, Java, and a number of other languages. (Inside the class the syntax `this.Property` is used to get or set the property's value.)

In the example below we define the `gender` property for the `Person` class and we define it at instantiation.

    function Person(gender) {
      this.gender = gender;
      alert('Person instantiated');
    }

    var person1 = new Person('Male');
    var person2 = new Person('Female');

    //display the person1 gender
    alert('person1 is a ' + person1.gender); // person1 is a Male

#### The methods

Methods follow the same logic as properties; the difference is that they are functions and they are defined as functions. Calling a method is similar to accessing a property, but you add `()` at the end of the method name, possibly with arguments. To define a method, assign a function to a named property of the class's `prototype` property; the name that the function is assigned to is the name that the method is called by on the object.

In the example below we define and use the method `sayHello()` for the `Person` class.

    function Person(gender) {
      this.gender = gender;
      alert('Person instantiated');
    }

    Person.prototype.sayHello = function()
    {
      alert ('hello');
    };

    var person1 = new Person('Male');
    var person2 = new Person('Female');

    // call the Person sayHello method.
    person1.sayHello(); // hello

In JavaScript methods are regular function objects that are bound to a class/object as a property which means they can be invoked "out of the context". Consider the following example code:

    function Person(gender) {
      this.gender = gender;
    }

    Person.prototype.sayGender = function()
    {
      alert(this.gender);
    };

    var person1 = new Person('Male');
    var genderTeller = person1.sayGender;

    person1.sayGender(); // alerts 'Male'
    genderTeller(); // alerts undefined
    alert(genderTeller === person1.sayGender); // alerts true
    alert(genderTeller === Person.prototype.sayGender); // alerts true

This example demonstrates many concepts at once. It shows that there are no "per-object methods" in JavaScript since all references to the method point to the exact same function, the one we have defined in the first place on the prototype. JavaScript "binds" the current "object context" to the special "this" variable when a function is invoked as a method(or property to be exact) of an object. This is equal to calling the function object's "call" method as follows:

    genderTeller.call(person1); //alerts 'Male'

See more about this on [Function.call](/w/index.php?title=concepts/programming/javascript/OOJ/js/objects/Function/call&action=edit&redlink=1) and [Function.apply](/w/index.php?title=concepts/programming/javascript/OOJ/js/objects/Function/apply&action=edit&redlink=1)

#### Inheritance

Inheritance is a way to create a class as a specialized version of one or more classes (*JavaScript only supports single class inheritance*). The specialized class is commonly called the *child*, and the other class is commonly called the parent. In JavaScript you do this by assigning an instance of the parent class to the child class, and then specializing it.

**Note**: JavaScript does not detect the child class `prototype.constructor` see [Object:prototype](/w/index.php?title=concepts/programming/javascript/OOJ/js/objects/Object/prototype&action=edit&redlink=1) property, so we must state that manually.

 In the example below, we define the class `Student` as a child class of `Person`. Then we redefine the `sayHello()` method and add the `sayGoodBye()` method.

    // define the Person Class
    function Person() {}

    Person.prototype.walk = function(){
      alert ('I am walking!');
    };
    Person.prototype.sayHello = function(){
      alert ('hello');
    };

    // define the Student class
    function Student() {
      // Call the parent constructor
      Person.call(this);
    }

    // inherit Person
    Student.prototype = new Person();

    // correct the constructor pointer because it points to Person
    Student.prototype.constructor = Student;

    // replace the sayHello method
    Student.prototype.sayHello = function(){
      alert('hi, I am a student');
    }

    // add sayGoodBye method
    Student.prototype.sayGoodBye = function(){
      alert('goodBye');
    }

    var student1 = new Student();
    student1.sayHello();
    student1.walk();
    student1.sayGoodBye();

    // check inheritance
    alert(student1 instanceof Person); // true
    alert(student1 instanceof Student); // true

#### Encapsulation

In the previous example, `Student` does not need to know how the `Person` class's `walk()` method is implemented, but still can use that method; the `Student` class doesn't need to explicitly define that method unless we want to change it. This is called **encapsulation**, by which every class inherits the methods of its parent and only needs to define things it wishes to change.

#### Abstraction

Abstraction is a mechanism that permits modeling the current part of the working problem. This can be achieved by inheritance (specialization), or composition. JavaScript achieves specialization by inheritance, and composition by letting instances of classes be the values of attributes of other objects.

The JavaScript Function class inherits from the Object class (this demonstrates specialization of the model). and the Function.prototype property is an instance of Object (this demonstrates composition)

    var foo = function(){};
    alert( 'foo is a Function: ' + (foo instanceof Function) );
    alert( 'foo.prototype is an Object: ' + (foo.prototype instanceof Object) );

#### Polymorphism

Just like all methods and properties are defined inside the prototype property, different classes can define methods with the same name; methods are scoped to the class in which they're defined. This is only true when the two classes do not hold a parent-child relation (when one does not inherit from the other in a chain of inheritance).

## Notes

The techniques presented in this article to implement object-oriented programming are not the only ones that can be used in JavaScript, which is very flexible in terms of how object-oriented programming can be performed.

Similarly, the techniques shown here do not use any language hacks, nor do they mimic other languages' object theory implementations.

There are other techniques that make even more advanced object-oriented programming in JavaScript, but those are beyond the scope of this introductory article.

## References

1.  Wikipedia. "Prototype-based programming", [http://en.wikipedia.org/wiki/Prototype-based\_programming](http://en.wikipedia.org/wiki/Prototype-based_programming)

<span id="Original_Document_Information">**Original Document Information**</span>

-   Author(s): Fernando Trasviña \<f\_trasvina at hotmail dot com\>

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Introduction_to_Object-Oriented_JavaScript)

