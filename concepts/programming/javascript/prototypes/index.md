---
title: Prototypes
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Inheritance_and_the_prototype_chain)'
readiness: 'Not Ready'
summary: "JavaScript is a little confusing for developers experienced in class-based languages (like Java or C++), as it's dynamic and does not provide a class implementation (although the keyword class is a reserved keyword and cannot be used as a variable name).\n"
tags:
  - Inheritance
  - JavaScript
uri: concepts/programming/javascript/prototypes

---
## Summary

JavaScript is a little confusing for developers experienced in class-based languages (like Java or C++), as it's dynamic and does not provide a class implementation (although the keyword class is a reserved keyword and cannot be used as a variable name).

JavaScript is still an Object Orientated Language (OOP), meaning you can construct class like structures and instantiate them into objects that are used in the same way as class-based languages.

An object has an internal link to another object (or `null`) called its **prototype**. This object has a prototype as well and so on, until one object has `null` as its prototype. This *chain* of objects being prototypes of one another is called the **prototype chain**.

## Inheritance with the prototype chain

### Inheriting properties

JavaScript objects are dynamic "bags" of properties (referred as **own properties**) and have a link to a prototype object (or `null`). Here is what happens when trying to access a property:

    // Let's assume we have an object o with its prototype chain looking like:
     // {a:1, b:2} ---> {b:3, c:4} ---> null
     // 'a' and 'b' are o own properties.

     // In this example, someObject.[[Prototype]] will designate the prototype of someObject.
     // This is a pure notation (based on the one used in the ECMAScript standard) and cannot be used in scripts

     console.log(o.a); // 1
     // Is there an 'a' own property on o? Yes and its value is 1

     console.log(o.b); // 2
     // Is there a 'b' own property on o? Yes and its value is 2
     // The prototype also has a 'b' property, but it's not visited. This is called "property shadowing"

     console.log(o.c); // 4
     // Is there a 'c' own property on o? No, check its prototype
     // Is there a 'c' own property on o.[[Prototype]]? Yes, its value is 4

     console.log(o.d); // undefined
     // Is there a 'd' own property on o? No, check its prototype
     // Is there a 'd' own property on o.[[Prototype]]? No, check it prototype
     // o.[[Prototype]].[[Prototype]] is null, stop searching, no property found, return undefined


Setting a property to an object creates an own property. The only exception to the getting and setting behavior rules is when there is an inherited property with a [defining getters and setters](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Working_with_Objects#Defining_getters_and_setters) getter or a setter.

### Inheriting "methods"

JavaScript does not have "methods" per se. JavaScript has functions and these functions can be used as property values. The inheritance of functions works the same way that any value, including property shadowing as shown above (which is a form of *method overriding*).

The only thing that changes when functions are object properties (own or inherited) is the value of [`this`](http://docs.webplatform.org/en/JavaScript/Reference/Operators/this) when the function is executed.

    var o = {
       a: 2,
       m: function(b){
         return this.a + 1;
       }
     };

     console.log(o.m()); // 3
     // When calling o.m in this case, 'this' refers to o.

     var p = Object.create(o);
     // p is an object and p.[[Prototype]] is o

     p.a = 12; // creates an own 'a' property on p.
     console.log(p.m()); // 13
     // when p.m is called, 'this' refers to p. 'this.a' is p own property


## Different ways to create objects and the resulting prototype chain

### Objects created with syntax constructs

    var o = {a: 1};

     // This object is created with Object.prototype as its [[Prototype]]
     // This is what allows to call o.hasOwnProperty('a').
     // hasOwnProperty is an own property of Object.prototype
     // Object.prototype has null as its prototype.
     // o ---> Object.prototype ---> null

     var a = ["yo", "whadup", "?"];

     // Arrays inherits from Array.prototype (which has methods like indexOf, forEach, etc.).
     // The prototype chain looks like:
     // a ---> Array.prototype ---> Object.prototype ---> null

     function f(){
       return 2;
     }

     // Functions inherit from Function.prototype (which has methods like call, bind, etc.):
     // f ---> Function.prototype ---> Object.prototype ---> null


### With a constructor

A "constructor" in JavaScript is "just" a function that happens to be called with the [new operator](http://docs.webplatform.org/en/JavaScript/Reference/Operators/new).

    function Graph() {
       this.vertexes = [];
       this.edges = [];
     }

     Graph.prototype = {
       addVertex: function(v){
         this.vertexes.push(v);
       }
     };

     var g = new Graph();
     // g is an object with own properties 'vertexes' and 'edges'.
     // g.[[Prototype]] is value of Graph.prototype at time of instantiation.


### With Object.create

ECMAScript 5 introduced a new method: [Object.create](http://docs.webplatform.org/en/JavaScript/Reference/Global_Objects/Object/create). Calling this method creates a new object. The prototype of this object is the first argument of the function:

    var a = {a: 1};
    // a ---> Object.prototype ---> null

    var b = Object.create(a);
    // b ---> a ---> Object.prototype ---> null
    console.log(b.a); // 1 (inherited)

    var c = Object.create(b);
    // c ---> b ---> a ---> Object.prototype ---> null

    var d = Object.create(null);
    // d ---> null
    console.log(d.hasOwnProperty); // undefined, because d doesn't inherit from Object.prototype
