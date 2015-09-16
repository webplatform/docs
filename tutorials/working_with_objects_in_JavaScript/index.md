---
title: 'Working with objects in JavaScript'
notes:
  - "Is marked as needing a technical review in MDN.\nLinks need to be changed to point to the WPD JS reference, once it's created"
readiness: 'Almost Ready'
summary: 'Objects are integral to javascript development and understanding how objects are generated and used is essential.'
tags:
  - Tutorials
uri: 'tutorials/working with objects in JavaScript'

---
## Summary

Objects are integral to javascript development and understanding how objects are generated and used is essential.

JavaScript is designed on a simple object-based paradigm: An object represents a collection of properties; each property is an association between a name/value pair. A value of property can be a function, which is then known as the object's *method*. In addition to objects that are predefined in the browser, you can define your own objects.

This chapter describes how to use objects, properties, functions, and methods, and how to create your own objects.

## Objects overview

Objects in JavaScript, just as many other programming languages, can be compared to objects in real life. The concept of objects in JavaScript can be understood with real life, tangible objects.

In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup for example. A cup is an object, with properties. A cup has a colour, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

## Objects and properties

A JavaScript object has properties associated with it. A property of an object can be explained as variables that are attached to the object. Object properties are basically the same with ordinary JavaScript variables, except for the attachment to objects. The properties of an object define the characteristics of the object. You access the properties of an object with a simple dot-notation:

``` js
 objectName.propertyName
```

 Like all JavaScript variables, both the object name (which could be a normal variable) and property name are case sensitive. You define a property by assigning it a value. For example, let's create an object named `myCar` and give it properties named `make`, `model`, and `year` as follows:

``` js
 var myCar = new Object();
 myCar.make = "Ford";
 myCar.model = "Mustang";
 myCar.year = 1969;
```

 Properties of JavaScript objects can also be accessed or set using a bracket notation. Objects are sometimes called *associative arrays*, since each property is associated with a string value that can be used to access it. So, for example, you could access the properties of the `myCar` object as follows:

``` js
 myCar["make"] = "Ford";
 myCar["model"] = "Mustang";
 myCar["year"] = 1969;
```

 Object properties names can be valid JavaScript string, or anything that can be converted to string, including the empty string. However, any property name that is not a valid JavaScript identifier (for example, a property name that has space or dash, or starts with a number) can only be accessed using the square bracket notation. This notation is also very useful when property names are to be dynamically determined (when the property name is not determined until runtime). Examples are as follows:

``` js
 var myObj = new Object(),
     str = "myString",
     rand = Math.random(),
     obj = new Object();

 myObj.type = "Dot syntax";
 myObj["date created"] = "String with space";
 myObj[str] = "String value";
 myObj[rand] = "Random Number";
 myObj[obj] = "Object";
 myObj[""] = "Even an empty string";

 console.log(myObj);
```

 You can also access properties by using a string value that is stored in a variable:

``` js
 var propertyName = "make";
 myCar[propertyName] = "Ford";

 propertyName = "model";
 myCar[propertyName] = "Mustang";
```

 You can use the bracket notation with [for...in](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Statements/for...in) to iterate over all the enumerable properties of an object. To illustrate how this works, the following function displays the properties of the object when you pass the object and the object's name as arguments to the function:

``` js
 function showProps(obj, objName) {
   var result = "";
   for (var i in obj) {
     if (obj.hasOwnProperty(i)) {
         result += objName + "." + i + " = " + obj[i] + "\n";
     }
   }
   return result;
 }
```

 So, the function call `showProps(myCar, "myCar")` would return the following:

``` js
 myCar.make = Ford
 myCar.model = Mustang
 myCar.year = 1969
```

## Object everything

In JavaScript, almost everything is an object. All primitive types except `null` and `undefined` are treated as objects. They can be assigned properties (assigned properties of some types are not persistent), and they have all characteristics of objects.

## Enumerating all properties of an object

Starting with ECMAScript 5, there are three native ways to list/traverse object properties:

-   [for...in](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Statements/for...in) loops: this method traverses all enumerable properties of an object and its prototype chain
-   [Object.keys(o)](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Object/keys): this method returns an array with all the own (not in the prototype chain) enumerable properties names ("keys") of an object `o`.
-   [Object.getOwnPropertyNames(o)](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Object/getOwnPropertyNames): this method returns an array containing all own properties names (enumerable or not) of an object `o`.

In ECMAScript 5, there is no native way to list all properties of an object. However, this can be achieved with the following function:

``` js
 function listAllProperties(o){
    var objectToInspect;
    var result = [];

    for(objectToInspect = o; objectToInspect !== null; objectToInspect = Object.getPrototypeOf(objectToInspect)){
        result = result.concat(Object.getOwnPropertyNames(objectToInspect));
    }

    return result;
 }
```

 This can be useful to reveal "hidden" properties (properties in the prototype chain which are not accessible through the object, because another property has the same name earlier in the prototype chain). Listing accessible properties only can easily be done by removing duplicates in the array.

## Creating new objects

JavaScript has a number of predefined objects. In addition, you can create your own objects. In JavaScript 1.2 and later, you can create an object using an object initializer. Alternatively, you can first create a constructor function and then instantiate an object using that function and the `new` operator.

### Using object initializers

In addition to creating objects using a constructor function, you can create objects using an object initializer. Using object initializers is sometimes referred to as creating objects with literal notation. "Object initializer" is consistent with the terminology used by C++.

The syntax for an object using an object initializer is:

``` js
 var obj = { property_1:   value_1,   // property_# may be an identifier...
             2:            value_2,   // or a number...
             // ...,
             "property n": value_n }; // or a string
```

 where `obj` is the name of the new object, each `property_i` is an identifier (either a name, a number, or a string literal), and each `value_i` is an expression whose value is assigned to the `property_i`. The `obj` and assignment is optional; if you do not need to refer to this object elsewhere, you do not need to assign it to a variable. (Note that you may need to wrap the object literal in parentheses if the object appears where a statement is expected, so as not to have the literal be confused with a block statement.)

If an object is created with an object initializer in a top-level script, JavaScript interprets the object each time it evaluates an expression containing the object literal. In addition, an initializer used in a function is created each time the function is called.

The following statement creates an object and assigns it to the variable `x` if and only if the expression `cond` is true.

``` js
 if (cond) var x = {hi: "there"};
```

 The following example creates `myHonda` with three properties. Note that the `engine` property is also an object with its own properties.

``` js
 var myHonda = {color: "red", wheels: 4, engine: {cylinders: 4, size: 2.2}};
```

 You can also use object initializers to create arrays. See [array literals](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Values%2C_variables%2C_and_literals#Array_literals).

In JavaScript 1.1 and earlier, you cannot use object initializers. You can create objects only using their constructor functions or using a function supplied by some other object for that purpose. See [Using a constructor function](#Using_a_constructor_function).

### Using a constructor function

Alternatively, you can create an object with these two steps:

1.  Define the object type by writing a constructor function. There is a strong convention, with good reason, to use a capital initial letter.
2.  Create an instance of the object with `new`.

To define an object type, create a function for the object type that specifies its name, properties, and methods. For example, suppose you want to create an object type for cars. You want this type of object to be called `car`, and you want it to have properties for make, model, and year. To do this, you would write the following function:

``` js
 function Car(make, model, year) {
   this.make = make;
   this.model = model;
   this.year = year;
 }
```

 Notice the use of `this` to assign values to the object's properties based on the values passed to the function.

Now you can create an object called `mycar` as follows:

``` js
 var mycar = new Car("Eagle", "Talon TSi", 1993);
```

 This statement creates `mycar` and assigns it the specified values for its properties. Then the value of `mycar.make` is the string "Eagle", `mycar.year` is the integer 1993, and so on.

You can create any number of `car` objects by calls to `new`. For example,

``` js
 var kenscar = new Car("Nissan", "300ZX", 1992);
 var vpgscar = new Car("Mazda", "Miata", 1990);
```

 An object can have a property that is itself another object. For example, suppose you define an object called `person` as follows:

``` js
 function Person(name, age, sex) {
   this.name = name;
   this.age = age;
   this.sex = sex;
 }
```

 and then instantiate two new `person` objects as follows:

``` js
 var rand = new Person("Rand McKinnon", 33, "M");
 var ken = new Person("Ken Jones", 39, "M");
```

 Then, you can rewrite the definition of `car` to include an `owner` property that takes a `person` object, as follows:

``` js
 function Car(make, model, year, owner) {
   this.make = make;
   this.model = model;
   this.year = year;
   this.owner = owner;
 }
```

 To instantiate the new objects, you then use the following:

``` js
 var car1 = new Car("Eagle", "Talon TSi", 1993, rand);
 var car2 = new Car("Nissan", "300ZX", 1992, ken);
```

 Notice that instead of passing a literal string or integer value when creating the new objects, the above statements pass the objects `rand` and `ken` as the arguments for the owners. Then if you want to find out the name of the owner of car2, you can access the following property:

``` js
 car2.owner.name
```

 Note that you can always add a property to a previously defined object. For example, the statement

``` js
 car1.color = "black";
```

 adds a property `color` to car1, and assigns it a value of "black." However, this does not affect any other objects. To add the new property to all objects of the same type, you have to add the property to the definition of the `car` object type.

### Using the Object.create method

Objects can also be created using the `Object.create` method. This method can be very useful, because it allows you to choose the prototype object for the object you want to create, without having to define a constructor function. For more detailed information on the method and how to use it, see [Object.create method](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Object/create)

### Inheritance

All objects in JavaScript inherit from at least one other object. The object being inherited from is known as the prototype, and the inherited properties can be found in the `prototype` object of the constructor.

### Indexing object properties

In JavaScript 1.0, you can refer to a property of an object either by its property name or by its ordinal index. In JavaScript 1.1 and later, however, if you initially define a property by its name, you must always refer to it by its name, and if you initially define a property by an index, you must always refer to it by its index.

This restriction applies when you create an object and its properties with a constructor function (as we did previously with the `Car` object type) and when you define individual properties explicitly (for example, `myCar.color = "red"`). If you initially define an object property with an index, such as `myCar[5] = "25 mpg"`, you can subsequently refer to the property only as `myCar[5]`.

The exception to this rule is objects reflected from HTML, such as the `forms` array. You can always refer to objects in these arrays by either their ordinal number (based on where they appear in the document) or their name (if defined). For example, if the second `<FORM>` tag in a document has a `NAME` attribute of "myForm", you can refer to the form as `document.forms[1]` or `document.forms["myForm"]` or `document.myForm`.

### Defining properties for an object type

You can add a property to a previously defined object type by using the `prototype` property. This defines a property that is shared by all objects of the specified type, rather than by just one instance of the object. The following code adds a `color` property to all objects of type `car`, and then assigns a value to the `color` property of the object `car1`.

``` js
 Car.prototype.color = null;
 car1.color = "black";
```

 See the [`prototype` property](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Function/prototype) of the `Function` object for more information.

### Defining methods

A *method* is a function associated with an object, or, simply put, a method is a property of an object that is a function. Methods are defined the way normal functions are defined, except that they have to be assigned as the property of an object. Examples are:

``` js
 objectName.methodname = function_name;

 var myObj = {
   myMethod: function(params) {
     // ...do something
   }
 };
```

 where `objectName` is an existing object, `methodname` is the name you are assigning to the method, and `function_name` is the name of the function.

You can then call the method in the context of the object as follows:

``` js
 object.methodname(params);
```

 You can define methods for an object type by including a method definition in the object constructor function. For example, you could define a function that would format and display the properties of the previously-defined `car` objects; for example,

``` js
 function displayCar() {
   var result = "A Beautiful " + this.year + " " + this.make
     + " " + this.model;
   pretty_print(result);
 }
```

 where `pretty_print` is a function to display a horizontal rule and a string. Notice the use of `this` to refer to the object to which the method belongs.

You can make this function a method of `car` by adding the statement

``` js
 this.displayCar = displayCar;
```

 to the object definition. So, the full definition of `car` would now look like

``` js
 function Car(make, model, year, owner) {
   this.make = make;
   this.model = model;
   this.year = year;
   this.owner = owner;
   this.displayCar = displayCar;
 }
```

 Then you can call the `displayCar` method for each of the objects as follows:

``` js
 car1.displayCar();
 car2.displayCar();
```

 This produces the output shown in the following figure.

![Two lines saying: "a beautiful 1993 Eagle Talon TSi" and "a beautiful 1992 Nissan 300ZX"](/assets/public/d/dd/obja.gif)

<small>**Figure 7.1: Displaying method output.**</small>

### Using `this` for object references

JavaScript has a special keyword, `this`, that you can use within a method to refer to the current object. For example, suppose you have a function called `validate` that validates an object's `value` property, given the object and the high and low values:

``` js
 function validate(obj, lowval, hival) {
   if ((obj.value < lowval) || (obj.value > hival))
     alert("Invalid Value!");
 }
```

 Then, you could call `validate` in each form element's `onchange ` event handler, using `this` to pass it the element, as in the following example:

``` html
 <input type="text" name="age" size="3"
   onChange="validate(this, 18, 99)">
```

 In general, `this` refers to the calling object in a method.

When combined with the `form` property, `this` can refer to the current object's parent form. In the following example, the form `myForm` contains a `Text` object and a button. When the user clicks the button, the value of the `Text` object is set to the form's name. The button's `onclick` event handler uses `this.form` to refer to the parent form, `myForm`.

``` html
 <form name="myForm">
 <p><label>Form name:<input type="text" name="text1" value="Beluga"></label>
 <p><input name="button1" type="button" value="Show Form Name"
      onclick="this.form.text1.value = this.form.name">
 </p>
 </form>
```

### Defining getters and setters

A *getter* is a method that gets the value of a specific property. A *setter* is a method that sets the value of a specific property. You can define getters and setters on any predefined core object or user-defined object that supports the addition of new properties. The syntax for defining getters and setters uses the object literal syntax.

**Note**: Starting in [JavaScript 1.8.1](https://developer.mozilla.org/en-US/docs/JavaScript/New_in_JavaScript/1.8.1), setters are no longer called when setting properties in object and array initializers.

 The following [JS shell](https://developer.mozilla.org/en-US/docs/SpiderMonkey/Introduction_to_the_JavaScript_shell) session illustrates how getters and setters could work for a user-defined object `o`. The JS shell is an application that allows developers to test JavaScript code in batch mode or interactively.

``` js
 js> var o = {a: 7, get b() {return this.a + 1;}, set c(x) {this.a = x / 2}};
 [object Object]
 js> o.a;
 7
 js> o.b;
 8
 js> o.c = 50;
 js> o.a;
 25
```

 The `o` object's properties are:

-   `o.a` — a number
-   `o.b` — a getter that returns `o.a` plus 1
-   `o.c` — a setter that sets the value of `o.a` to half of the value `o.c` is being set to

Please note that function names of getters and setters defined in an object literal using "[gs]et *property*()" (as opposed to `__define[GS]etter__` below) are not the names of the getters themselves, even though the `[gs]et propertyName(){ }` syntax may mislead you to think otherwise. To name a function in a getter or setter using the "[gs]et *property*()" syntax, define an explicitly named function programmatically using `Object.defineProperty` (or the `Object.prototype.__defineGetter__` legacy fallback).

This JavaScript shell session illustrates how getters and setters can extend the `Date` prototype to add a `year` property to all instances of the predefined `Date` class. It uses the `Date` class's existing `getFullYear` and `setFullYear` methods to support the `year` property's getter and setter.

These statements define a getter and setter for the year property:

``` js
 js> var d = Date.prototype;
 js> d.__defineGetter__("year", function() { return this.getFullYear(); });
 js> d.__defineSetter__("year", function(y) { this.setFullYear(y); });
```

 These statements use the getter and setter in a `Date` object:

``` js
 js> var now = new Date;
 js> print(now.year);
 2000
 js> now.year = 2001;
 987617605170
 js> print(now);
 Wed Apr 18 11:13:25 GMT-0700 (Pacific Daylight Time) 2001
```

#### Obsolete syntaxes

In the past, JavaScript supported several other syntaxes for defining getters and setters. None of these syntaxes were supported by other engines, and support has been removed in recent versions of JavaScript. See [this dissection of the removed syntaxes](http://bugsalert.com/Jeff-Walden-SpiderMonkey-ancient-esoteric-rarely-syntax-creating-getters-setters-removed_46423.html) for further details on what was removed and how to adapt to those removals.

#### Summary

In principle, getters and setters can be either

-   defined using [object initializers](#Using_object_initializers), or
-   added later to any object at any time using a getter or setter adding method.

When defining getters and setters using [object initializers](#Using_object_initializers) all you need to do is to prefix a getter method with `get` and a setter method with `set`. Of course, the getter method must not expect a parameter, while the setter method expects exactly one parameter (the new value to set). For instance:

``` js
 var o = {
   a: 7,
   '''get''' b() { return this.a + 1; },
   '''set''' c(x) { this.a = x / 2; }
 };
```

 Getters and setters can also be added to an object at any time after creation using two special methods called `__defineGetter__` and `__defineSetter__`. Both methods expect the name of the getter or setter as their first parameter, in the form of a string. The second parameter is the function to call as the getter or setter. For instance (following the previous example):

``` js
 o.__defineGetter__("b", function() { return this.a + 1; });
 o.__defineSetter__("c", function(x) { this.a = x / 2; });
```

 Which of the two forms to choose depends on your programming style and task at hand. If you already go for the object initializer when defining a prototype you will probably most of the time choose the first form. This form is more compact and natural. However, if you need to add getters and setters later — because you did not write the prototype or particular object — then the second form is the only possible form. The second form probably best represents the dynamic nature of JavaScript — but it can make the code hard to read and understand.

**Note**: Prior to Firefox 3.0, getter and setter are not supported for DOM Elements. Older versions of Firefox silently fail. If exceptions are needed for those, changing the prototype of HTMLElement `(HTMLElement.prototype.__define[SG]etter__)` and throwing an exception is a workaround.

With Firefox 3.0, defining getter or setter on an already-defined property will throw an exception. The property must be deleted beforehand, which is not the case for older versions of Firefox.

#### See also

-   `__defineGetter__`
-   `__defineSetter__`
-   `get`
-   `set`

### Deleting properties

You can remove a property by using the `delete` operator. The following code shows how to remove a property.

``` js
 //Creates a new object, myobj, with two properties, a and b.
 var myobj = new Object;
 myobj.a = 5;
 myobj.b = 12;

 //Removes the a property, leaving myobj with only the b property.
 delete myobj.a;
```

 You can also use `delete` to delete a global variable if the `var` keyword was not used to declare the variable:

``` js
 g = 17;
 delete g;
```

 See ` delete` for more information.

## See also

-   [ECMAScript 5.1 spec: Language Overview](http://es5.github.com/#x4.2)
-   [JavaScript. The core. (Dmitry A. Soshnikov ECMA-262 article series)](http://dmitrysoshnikov.com/ecmascript/javascript-the-core)

