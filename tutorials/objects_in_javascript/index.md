---
title: Objects in JavaScript
notes:
  - 'Links should be changed to WPD articles when they become available.'
readiness: 'Almost Ready'
summary: 'This article takes the concept of functions further, looking at how you can encapsulate functions and variables into reusable packages of functionality called objects.'
tags:
  - Tutorials
  - JavaScript
uri: 'tutorials/objects in javascript'

---
## Summary

This article takes the concept of functions further, looking at how you can encapsulate functions and variables into reusable packages of functionality called objects.

## Introduction

The [functions article](http://www.w3.org/wiki/JavaScript_functions) that this follows introduced the concept of functions, teaching you how to better organize and reuse your code by grouping individual activities into logical chunks that you can call whenever you like. Now that you’re comfortable with these essential components of JavaScript programming, I’d like to expand upon their application by introducing **objects**. Objects enable you to gather together the related bundles of functionality you define as functions, and bind them into a coherent package that you can pass around and refer to as a *single item*. This ability has very practical impacts upon the code you’re able to write, even if it sounds a little abstract at the moment.

You might not have noticed it, but you’ve been implicitly exposed to objects throughout this series; at this point in the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum), I’ll give you a more explicit understanding of how objects work in JavaScript, and explain how you can increase the expressiveness and reusability of your code by exploiting them.

Note: There is an example available for you to download or run live, which contains code to calculate the area of a triangle, both with and without objects. This code is built up in the explanations below. Run the [triangle objects example](http://dev.opera.com/articles/view/objects-in-javascript/triangle_area.html).

## Why objects?

The single most important reason to care about objects is their capacity to improve your code’s representation of the data and processes you’re implementing. As a trivial example, consider how you’d write code that did some sort of work with a triangle. You know that triangles in general have three sides, so to deal with a specific triangle the obvious thing to do is to create three variables:

``` js
// This is a triangle.
var sideA = 3;
var sideB = 4;
var sideC = 5;
```

 And there you go, you’ve got a triangle! But not *really*, right? You’ve really just created three variables that you need to keep track of separately, and a comment to remind yourself what you were thinking. This simply isn’t as clear or as usable as it could be. But no matter, let’s continue on and consider how you’d build some calculations around this “triangle”. To find its area, you might write the function as follows:

``` js
function getArea( a, b, c ) {
  // Return the area of a triangle using Heron's formula

  var semiperimeter   =   (a + b + c) / 2;
  var calculation     =   semiperimeter * (semiperimeter - a) * (semiperimeter - b) * (semiperimeter - c);
  return Math.sqrt( calculation );
}

alert( getArea( sideA, sideB, sideC ) );
```

 You’ll notice that you have to pass all the information about the triangle into the function in order for it to do any calculation. The activities related to triangles are *completely* decoupled from the triangle’s data, even though they don’t really make sense in isolation.

Further, I’ve used a nicely generic name for the function and each of the variables: `getArea`, `sideA`, etc. What happens when I find out next week that I need to extend my program to include a rectangle? I’d *like* to use `sideA` and `sideB` for the square's data, but those variable names are already taken. I could use `side1` and `side2`, but I bet you can see why that’s a recipe for confusion and disaster. I’d probably end up using `rectangleSideA` and `rectangleSideB`, and to stay consistent, I’d also have to go back and change all the code that’s already written for triangles to use `triangleSideA` and so on, which introduces some potential for error. The same goes of course for the function name: I’d like to use `getArea` for both shapes, as it’s *conceptually* the same calculation, but I can’t. There must be a better way to represent my data!

In the same way that it makes sense to create a function that bundles up a series of commands into a single, well-named activity, it makes sense here to create an object that brings each “thing” together into a single unit. Instead of being limited to JavaScript’s natively-supported primitive data types (strings, numbers, booleans, etc.), objects enable you to build your own amalgamation of any number of variables of any type. This free-form flexibility enables you to build structures that map quite directly to the “things” you’re concerned with when writing your programs, and to use them directly in your code just like you’d use native primitives. Here, I should build triangle and rectangle objects, each containing all the data necessary to deal intelligently with the shape, as well as all the activities I might want to perform with it. With that goal in mind, let’s get into some syntax.

## Familiar territory

If you look back to the [final functions example from the previous article](http://devfiles.myopera.com/articles/616/functions_4.html), you’ll see code snippets like:

``` js
var obj = document.getElementById( elementID );
```

 and:

``` js
obj.style.background = 'rgb('+red+','+green+','+blue')';
```

 Surprise! You’ve been using objects without even knowing it! Let’s explore these two snippets in some detail to start piecing together JavaScript’s object syntax.

The code `var obj = document.getElementById( elementID )` should look somewhat familiar. You know that parentheses at the end of a command mean that a function of some sort is being executed, and you can see that the result of the function call is being stored in a variable named `obj`. The only piece here that’s really *new* is the dot in the middle. As it turns out, this **dot notation** is how JavaScript grants access to the data inside an object. The dot (.) is simply an operator that sits between its operands, just like + and -.

By convention, the variables stored in an object that we access via the dot operator are generically called **properties**. Properties that happen to be functions are called **methods**. There’s no magic to either of those words; methods are just functions, properties are just variables.

The dot operator expects an object on its left, and a property name on its right; applying this to the code snippet, you can tell that I’m accessing the `getElementById` method of the built in `document` object (which you’ll read *much* more about in the upcoming [article on traversing the DOM](http://dev.opera.com/articles/view/45-traversing-the-dom/).

The next snippet is a little more interesting: it has *two* dots. One of the really exciting things about JavaScript’s object support is the notion of **chaining** dots together to dive down into complex structures. In short, you can chain objects together the same way that you can execute `var x = 2 + 3 + 4 + 5;` and expect a resulting 14; the object references simply resolve themselves, left to right (you can impress your friends by explaining that this makes the JavaScript dot operator into a “left-associative infix operator”). In this case, `obj.style` is evaluated, resolving to an object whose `background` property is then accessed. If you like, you can make this explicit in your code by adding parentheses: `(obj.style).background`.

## Creating objects

To build my own triangle object, I’ll create it explicitly using the following syntax:

``` js
var triangle = new Object();
```

`triangle` is now a blank foundation, waiting for you to construct some soaring three-sided edifice. You can do so by adding properties to your object using the dot operator:

``` js
triangle.sideA  =   3;
triangle.sideB  =   4;
triangle.sideC  =   5;
```

 You don’t actually have to do anything special to add new properties to an object. When JavaScript evaluates the dot operator, it’s quite forgiving indeed. If you attempt to set a property that doesn’t exist, JavaScript creates it for you. If you try to read a property that isn’t there, JavaScript returns “undefined”. This is convenient, but can mask errors if you’re not careful, so watch out for typos!

Adding methods works similarly — here’s an example:

``` js
triangle.getArea    =   function ( a, b, c ) {
  // Return the area of a triangle using Heron's formula

  var semiperimeter   =   (a + b + c) / 2;
  var calculation     =   semiperimeter * (semiperimeter - a) *
                                (semiperimeter - b) * (semiperimeter - c);
  return Math.sqrt( calculation );

};      // Note the semi-colon here; it’s mandatory.
```

 If you’re thinking that this looks a *lot* like defining a function, you’re spot on: I’ve simply left off the function’s name entirely. JavaScript has the concept of an *anonymous* function that doesn’t have a name of its own, but is instead stored in a variable just like any other value. In this code, I’m creating an anonymous function, and storing it in the `triangle` object’s `getArea` property. The object then carries that function around with it, just like it carries any other property.

## Self-reference

One of the goals of creating the `triangle` object was to create a bond between the triangle’s data and the actions I can perform on the data. I haven’t accomplished that yet, however. You’ll notice right away that the `triangle.getArea` method still requires that the side length data be passed in when it’s executed, resulting in code that looks like this:

``` js
triangle.getArea( triangle.sideA, triangle.sideB, triangle.sideC );
```

 I think this is better than the code I had at the beginning of the article, as it clearly expresses a *relationship* between the data and the activity. That relationship, however, means that we shouldn’t have to tell the method what values to work with. It should be able to gather data about the object on which it lives, and use that data without asking you to input it manually.

The secret lies in the `this` keyword, which you can use inside a method’s definition to refer back to other properties and methods on the same object. Rewriting the `getArea` method to use `this`, we end up with the following code:

``` js
triangle.getArea    =   function () {
  // Return the area of a triangle using Heron's formula

  var semiperimeter   =   (this.sideA + this.sideB + this.sideC) / 2;
  var calculation     =   semiperimeter * (semiperimeter - this.sideA) * (semiperimeter - this.sideB) * (semiperimeter - this.sideC);

  return Math.sqrt( calculation );

};      // Note the semi-colon here, it's mandatory.
```

 As you can see, `this` works somewhat like a mirror. When the `getArea` method is executed, it takes a long look at its reflection to read its `sideA`, `sideB`, and `sideC` properties. It’s able to use those in its calculation, instead of relying on input from outside.

Note: This is a bit of an oversimplification. `this` doesn’t *always* refer to the object on which a method is defined, but instead can change based on specific contexts. Sorry for the obscurity here, but it’s a bit beyond the scope of this article. That said, you can rest assured that in the context I’m using it here, `this` will always refer to the `triangle` object.

## Objects as associative arrays

The dot operator isn’t the only way to access an object’s properties and methods; they can also be accessed quite efficiently using the **subscript** notation**you’ll probably be familiar with from the earlier [discussion of arrays](http://www.w3.org/wiki/Programming_-_the_real_basics#Arrays). In short, you can treat an object as an**associative array**that maps a string to a value in the same way that a typical** array maps a number to a value. Using this notation, you could rewrite `triangle` a second way:

``` js
var triangle = new Object();
triangle['sideA']   =   3;
triangle['sideB']   =   4;
triangle['sideC']   =   5;
triangle['getArea'] =   function ( a, b, c ) {
  // Return the area of a triangle using Heron's formula

  var semiperimeter   =   (a + b + c) / 2;
  var calculation     =   semiperimeter * (semiperimeter - a) * (semiperimeter - b) * (semiperimeter - c);
  return Math.sqrt( calculation );

};      // Note the semi-colon here, it's mandatory.
```

 At first glance, this might appear superfluous. Why not just use dot notation? The benefit of this new syntax is that the property name isn’t hard-coded into your program. You can use variables to specify the property names, which means you can build truly flexible commands that do different things based on context. For example, you could build a function that compared two objects to see if they share a common property:

``` js
function isPropertyShared( objectA, objectB, propertyName ) {
  if (
     typeof objectA[ propertyName ] !== undefined
     &&
     typeof objectB[ propertyName ] !== undefined
     ) {
         alert("Both objects have a property named " + propertyName + "!");
       }
}
```

 This function would be simply impossible to write in a generic way using dot notation, as I’d have to explicitly write the property names to test in the program's code. You’ll use this syntax a *lot*.

Note: An associative array is called a “hash” in Perl, a “hashtable” in C\#, a “map” in C++, a “hashmap” in Java, a “dictionary” in Python, and so on. It’s a very powerful and foundational concept in programming, and you might already know it under a different name.

## The object literal

Let’s take a close look at some code that’s probably quite familiar:

``` js
alert("Hello world");
```

 You can identify `alert` right away as a function that’s being called with a single argument: the string “Hello world”. What I’d like you to note here is that you *didn’t* have to write:

``` js
var temporaryString = "Hello world";
alert(temporaryString);
```

 JavaScript simply understands that anything contained inside a pair of double-quotes (" ") should be treated as a string, and does whatever background magic is necessary to make that work wherever you write it. The string is created and passed right into the function all at once. Formally, `"Hello world"`\` is referred to as a **string literal**; you’ve literally typed out everything that’s going into the string in order to create it.

JavaScript has a similar syntax for “object literals” that allows you to create your own object without any syntactical overhead. Let’s rewrite the object I created above yet a third way, this time as an object literal:

``` js
var triangle = {
  sideA:      3,
  sideB:      4,
  sideC:      5,
  getArea:    function ( a, b, c ) {
    // Return the area of a triangle using Heron's formula

    var semiperimeter   =   (a + b + c) / 2;
    var calculation     =   semiperimeter * (semiperimeter - a) * (semiperimeter - b) * (semiperimeter - c);
    return Math.sqrt( calculation );

  }
};
```

 The syntax is clear: the object literal uses curly-braces to demarcate the beginning and end of the object, which contain an arbitrary number of “`propertyName: propertyValue`” pairs separated by commas. This makes it quite easy to build up structures for use in your programs without tedious repetition of the object name on every line.

One thing to watch out for, though: it's a very common mistake to put a comma after the last item in the object literal’s list of properties (in this case, after the `getArea` definition). Only put commas *between* properties — an extra comma at the end will cause errors. Especially when coming back to code later to insert or remove values, you’ll need to be very careful to keep commas in the right places.

## Summary — there’s much more to learn

This is really just scratching the surface of object capabilities and limitations in JavaScript. After reading through, you should be comfortable creating your own objects, adding properties and methods, and using them in simple self-referential ways. There’s a lot more out there, but none of it is *essential* for you in your explorations. This article is meant to start you down the path, and give you the tools you need to understand code you’ll be exposed to as you delve deeper into the subject.

## See also

### External resources

-   [Object Oriented JavaScript](http://nefariousdesigns.co.uk/archive/2006/05/object-oriented-javascript/): A good introduction to more advanced object-oriented concepts in JavaScript.
-   [Private Members in JavaScript](http://javascript.crockford.com/private.html): Douglas Crockford’s seminal discussion of implementing encapsulation in JavaScript.
-   [Scope in JavaScript](http://www.digital-web.com/articles/scope_in_javascript/): A more advanced discussion of the intricacies of the `this` keyword in various contexts.

### Exercise questions

-   When might you want to use subscript notation instead of dot notation when referencing an object’s properties?
-   How can an object refer to itself? Why is this valuable?
-   What is an object literal? When creating an object literal, where do the commas go?
-   I built an object to represent a triangle, and calculate its area. I’d like you to do the same for a rectangle. Use `this` in the rectangle’s `getArea` method to avoid passing its data around unnecessarily.
