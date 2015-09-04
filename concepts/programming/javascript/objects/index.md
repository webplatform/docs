---
title: objects
tags:
  - Tutorials
  - JavaScript
readiness: 'In Progress'
summary: "JavaScript is designed on a simple object-based paradigm. An object is a collection of properties, and a property is association between a name and a value. A value of property can be a function, which is then known as the object's method. In addition to objects that are predefined in the browser, you can define your own objects.\n"
uri: concepts/programming/javascript/objects
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/objects/js/statements
    - concepts/programming/javascript/objects/js/statements/for...in
    - concepts/programming/javascript/objects/js/objects/Object/keys
    - concepts/programming/javascript/objects/js/guides/JavaScript/Values
    - concepts/programming/javascript/objects/js/objects/Object/create
    - concepts/programming/javascript/objects/js/objects/Function/prototype
    - Obja.gif
    - concepts/programming/javascript/objects/js/objects/Object/defineProperty
    - concepts/programming/javascript/objects/js/objects/Object/defineGetter
    - concepts/programming/javascript/objects/guides/JavaScript/Functions
    - 'concepts/programming/javascript/objects/guides/JavaScript/Predefined Core Objects'
    - 'concepts/programming/javascript/objects/js/objects/Object/defineSetter defineSetter'
    - concepts/programming/javascript/objects/js/operators/get
    - concepts/programming/javascript/objects/js/operators/set

---
# objects

## Summary

JavaScript is designed on a simple object-based paradigm. An object is a collection of properties, and a property is association between a name and a value. A value of property can be a function, which is then known as the object's method. In addition to objects that are predefined in the browser, you can define your own objects.

This chapter describes how to use objects, properties, functions, and methods, and how to create your own objects.

## Objects overview

Objects in JavaScript, just as many other programming languages, can be compared to objects in real life. The concept of objects in JavaScript can be understood with real life, tangible objects.

In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup for example. A cup is an object, with properties. A cup has a colour, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

## Objects and properties

A JavaScript object has properties associated with it. A property of an object can be explained as variables that are attached to the object. Object properties are basically the same as ordinary JavaScript variables, except object properties are attached to objects. The properties of an object define the characteristics of the object. You access the properties of an object with a simple dot-notation:

    objectName.propertyName

Like all JavaScript variables, both the object name (which could be a normal variable) and property name are case sensitive. You define a property by assigning it a value. For example, let's create an object named `myCar` and give it properties named `make`, `model`, and `year` as follows:

    var myCar = new Object();
    myCar.make = "Ford";
    myCar.model = "Mustang";
    myCar.year = 1969;

Above we have used the key word `new` to create a new object named `myCar`. Then, using dot-notation, we added three properties to `myCar` and assigned them values. In addition to using dot-notation to access and set object property values, we may also use bracket-notation. So, for example, you could access the properties of the `myCar` object as follows:

    myCar["make"] = "Ford";
    myCar["model"] = "Mustang";
    myCar["year"] = 1969;

Objects are sometimes called *associative arrays*, since each property is associated with a string value that can be used to access it. Object property names can be valid JavaScript strings, or anything that can be converted to string, including the empty string. However, any property name that is not a valid JavaScript identifier (for example, a property name that has space or dash, or starts with a number) can only be accessed using bracket-notation. Bracket-notation is also very useful when property names are to be dynamically determined (when the property name is not determined until runtime). Examples are as follows:

    var myObj = new Object(),
        str = "myString",
        rand = Math.random(),
        obj = new Object();

    myObj.type              = "Dot syntax";
    myObj["date created"]   = "String with space";
    myObj[str]              = "String value";
    myObj[rand]             = "Random Number";
    myObj[obj]              = "Object";
    myObj[""]               = "Even an empty string";

    console.log(myObj);

You can also access properties by using a string value that is stored in a variable:

    var propertyName = "make";
    myCar[propertyName] = "Ford";

    propertyName = "model";
    myCar[propertyName] = "Mustang";

You can use bracket-notation with [for...in](/w/index.php?title=concepts/programming/javascript/objects/js/statements&action=edit&redlink=1) to iterate over all the enumerable properties of an object. To illustrate how this works, the following function displays the properties of the object when you pass the object and the object's name as arguments to the function:

    function showProps(obj, objName) {
      var result = "";
      for (var i in obj)
        result += objName + "." + i + " = " + obj[i] + "\n";
      return result;
    }

So, the function call `showProps(myCar, "myCar")` would return the following:

    myCar.make = Ford
    myCar.model = Mustang
    myCar.year = 1969

## Object everything

In JavaScript, almost everything is an object. All primitive types except `null` and `undefined` are treated as objects. They can be assigned properties (assigned properties of some types are not persistent), and they have all characteristics of objects. Even simple functions are objects in JavaScript.

## Enumerating all properties of an object

Starting with ECMAScript 5, there are three native ways to list/traverse object properties:

-   [for...in](/w/index.php?title=concepts/programming/javascript/objects/js/statements/for...in&action=edit&redlink=1) loops
     This method traverses all enumerable properties of an object and its prototype chain
-   [Object.keys(o)](/w/index.php?title=concepts/programming/javascript/objects/js/objects/Object/keys&action=edit&redlink=1)
     This method returns an array of Strings. Each string is a key in the object `o`. This array doesn't include keys that `o` inherited from it's prototype.
-   [Object.getOwnPropertyNames(o)](/concepts/programming/javascript/objects/js/objects/Object/getOwnPropertyNames)
     This method returns an array containing all own properties names (enumerable or not) of an object `o`.

In ECMAScript 5, there is no native way to list all properties of an object. However, this can be achieved with the following function:

    function listAllProperties(o){
        var objectToInspect;
        var result = [];

        for(objectToInspect = o; objectToInspect !== null; objectToInspect = Object.getPrototypeOf(objectToInspect)){
            result = result.concat(Object.getOwnPropertyNames(objectToInspect));
        }

        return result;
    }

This can be useful to reveal "hidden" properties (properties in the prototype chain which are not accessible through the object, because another property has the same name earlier in the prototype chain). Listing accessible properties only can easily be done by removing duplicates in the array.

## Creating new objects

JavaScript has a number of predefined objects. In addition, you can create your own objects. Starting in JavaScript 1.2, you can create an object using an object-literal. Alternatively, you can use a constructor function by calling the `new` operator on an existing function. Consider:

     var a = {};            //object-literal
     var b = new Object();  //constructor function

Both of these methods will get you a new object. Let's take a closer look at each of them.

### Using object literals

One way to create an object is to use object literals. Using object literals is sometimes referred to as creating objects with object-literal notation.

In it's most basic form, object literals are empty objects. To create one, do the following:

     var obj = {};

Since it might help to have an object with more substance, consider the following:

     var artist = {
         name : "Freddie Mercury",
         band : "Queen",
         rank : 1
     }

We now have an `artist` object. `artist` has a name, and band, and a rank of 1.

If an object is created with an object-literal in a top-level script, JavaScript interprets the object each time it evaluates an expression containing the object literal. In addition, an object literal used in a function is created each time the function is called.

The following statement creates an object and assigns it to the variable `x` if and only if the expression `cond` is true.

    if (cond) var x = {hi: "there"};

The following example creates `myHonda` with three properties. Note that the `engine` property is also an object with its own properties.

     var myHonda = {
         color: "red",
         wheels: 4,
         engine: {
             cylinders: 4,
             size: 2.2
         }
     };

You can also use object literals to create arrays and regular expressions. See [array](/w/index.php?title=concepts/programming/javascript/objects/js/guides/JavaScript/Values&action=edit&redlink=1) and [regular expression](/w/index.php?title=concepts/programming/javascript/objects/js/guides/JavaScript/Values&action=edit&redlink=1) literals.

In JavaScript 1.1 and earlier, you could not use object literals. You could create objects only using their constructor functions or using a function supplied by some other object for that purpose. See [Using a constructor function](http://docs.webplatform.org/wiki#Using_a_constructor_function).

### Using a constructor function

Alternatively, you can create an object with these two steps:

1.  Define the object type by writing a constructor function. There is a strong convention, with good reason, to use a capital initial letter.
2.  Create an instance of the object with `new`.

To define an object type, create a function for the object type that specifies its name, properties, and methods. For example, suppose you want to create an object type for cars. You want this type of object to be called `car`, and you want it to have properties for make, model, and year. To do this, you would write the following function:

    function Car(make, model, year) {
      this.make = make;
      this.model = model;
      this.year = year;
    }

Notice the use of `this` to assign values to the object's properties based on the values passed to the function.

Now you can create an object called `mycar` as follows:

    var mycar = new Car("Eagle", "Talon TSi", 1993);

This statement creates `mycar` and assigns it the specified values for its properties. Then the value of `mycar.make` is the string "Eagle", `mycar.year` is the integer 1993, and so on.

You can create any number of `car` objects by calls to `new`. For example,

    var kenscar = new Car("Nissan", "300ZX", 1992);
    var vpgscar = new Car("Mazda", "Miata", 1990);

An object can have a property that is itself another object. For example, suppose you define an object called `person` as follows:

    function Person(name, age, sex) {
      this.name = name;
      this.age = age;
      this.sex = sex;
    }

and then instantiate two new `person` objects as follows:

    var rand = new Person("Rand McKinnon", 33, "M");
    var ken = new Person("Ken Jones", 39, "M");

Then, you can rewrite the definition of `car` to include an `owner` property that takes a `person` object, as follows:

    function Car(make, model, year, owner) {
      this.make = make;
      this.model = model;
      this.year = year;
      this.owner = owner;
    }

To instantiate the new objects, you then use the following:

    var car1 = new Car("Eagle", "Talon TSi", 1993, rand);
    var car2 = new Car("Nissan", "300ZX", 1992, ken);

Notice that instead of passing a literal string or integer value when creating the new objects, the above statements pass the objects `rand` and `ken` as the arguments for the owners. Then if you want to find out the name of the owner of car2, you can access the following property:

    car2.owner.name

Note that you can always add a property to a previously defined object. For example, the statement

    car1.color = "black";

adds a property `color` to car1, and assigns it a value of "black." However, this does not affect any other objects. To add the new property to all objects of the same type, you have to add the property to the definition of the `car` object type.

### Using the Object.create method

Objects can also be created using the `Object.create` method. This method can be very useful, because it allows you to choose the prototype object for the object you want to create, without having to define a constructor function. For more detailed information on the method and how to use it, see [Object.create method](/w/index.php?title=concepts/programming/javascript/objects/js/objects/Object/create&action=edit&redlink=1)

### Inheritance

All objects in JavaScript inherit from at least one other object. The object being inherited from is known as the prototype, and the inherited properties can be found in the `prototype` object of the constructor.

### Indexing object properties

In JavaScript 1.0, you can refer to a property of an object either by its property name or by its ordinal index. In JavaScript 1.1 and later, however, if you initially define a property by its name, you must always refer to it by its name, and if you initially define a property by an index, you must always refer to it by its index.

This restriction applies when you create an object and its properties with a constructor function (as we did previously with the `Car` object type) and when you define individual properties explicitly (for example, `myCar.color = "red"`). If you initially define an object property with an index, such as `myCar[5] = "25 mpg"`, you can subsequently refer to the property only as `myCar[5]`.

The exception to this rule is objects reflected from HTML, such as the `forms` array. You can always refer to objects in these arrays by either their ordinal number (based on where they appear in the document) or their name (if defined). For example, if the second `<FORM>` tag in a document has a `NAME` attribute of "myForm", you can refer to the form as `document.forms[1]` or `document.forms["myForm"]` or `document.myForm`.

### Defining properties for an object type

You can add a property to a previously defined object type by using the `prototype` property. This defines a property that is shared by all objects of the specified type, rather than by just one instance of the object. The following code adds a `color` property to all objects of type `car`, and then assigns a value to the `color` property of the object `car1`.

    Car.prototype.color = null;
    car1.color = "black";

See the [`prototype` property](/w/index.php?title=concepts/programming/javascript/objects/js/objects/Function/prototype&action=edit&redlink=1) of the `Function` object in the JavaScript Reference for more information.

### Defining methods

A *method* is a function associated with an object, or, simply put, a method is a property of an object that is a function. Methods are defined the way normal functions are defined, except that they have to be assigned as the property of an object. Examples are:

    objectName.methodname = function_name;

    var myObj = {
      myMethod: function(params) {
        // ...do something
      }
    };

where `objectName` is an existing object, `methodname` is the name you are assigning to the method, and `function_name` is the name of the function.

You can then call the method in the context of the object as follows:

    object.methodname(params);

You can define methods for an object type by including a method definition in the object constructor function. For example, you could define a function that would format and display the properties of the previously-defined `car` objects; for example,

    function displayCar() {
      var result = "A Beautiful " + this.year + " " + this.make
        + " " + this.model;
      pretty_print(result);
    }

where `pretty_print` is a function to display a horizontal rule and a string. Notice the use of `this` to refer to the object to which the method belongs.

You can make this function a method of `car` by adding the statement

    this.displayCar = displayCar;

to the object definition. So, the full definition of `car` would now look like

    function Car(make, model, year, owner) {
      this.make = make;
      this.model = model;
      this.year = year;
      this.owner = owner;
      this.displayCar = displayCar;
    }

Then you can call the `displayCar` method for each of the objects as follows:

    car1.displayCar();
    car2.displayCar();

This produces the output shown in the following figure.

[Image:obja.gif](/w/index.php?title=Obja.gif&action=edit&redlink=1)

<small>**Figure 7.1: Displaying method output.**</small>

### Using this for object references

JavaScript has a special keyword, `this`, that you can use within a method to refer to the current object. For example, suppose you have a function called `validate` that validates an object's `value` property, given the object and the high and low values:

    function validate(obj, lowval, hival) {
      if ((obj.value < lowval);
    [object Object]
    js> o.a;
    7
    js> o.b;
    8
    js> o.c = 50;
    js> o.a;
    25

The `o` object's properties are:

-   `o.a` — a number
-   `o.b` — a getter that returns `o.a` plus 1
-   `o.c` — a setter that sets the value of `o.a` to half of the value `o.c` is being set to

Please note that function names of getters and setters defined in an object literal using "[gs]et *property*()" (as opposed to `__define[GS]etter__` below) are not the names of the getters themselves, even though the `[gs]et propertyName(){ }` syntax may mislead you to think otherwise. To name a function in a getter or setter using the "[gs]et *property*()" syntax, define an explicitly named function programmatically using `Object.defineProperty` (or the `Object.prototype.__defineGetter__` legacy fallback).

This JavaScript shell session illustrates how getters and setters can extend the `Date` prototype to add a `year` property to all instances of the predefined `Date` class. It uses the `Date` class's existing `getFullYear` and `setFullYear` methods to support the `year` property's getter and setter.

These statements define a getter and setter for the year property:

    js> var d = Date.prototype;
    js> d.__defineGetter__("year", function() { return this.getFullYear(); });
    js> d.__defineSetter__("year", function(y) { this.setFullYear(y); });

These statements use the getter and setter in a `Date` object:

    js> var now = new Date;
    js> print(now.year);
    2000
    js> now.year = 2001;
    987617605170
    js> print(now);
    Wed Apr 18 11:13:25 GMT-0700 (Pacific Daylight Time) 2001

#### Obsolete syntaxes

In the past, JavaScript supported several other syntaxes for defining getters and setters. None of these syntaxes were supported by other engines, and support has been removed in recent versions of JavaScript. See [this dissection of the removed syntaxes](http://whereswalden.com/2010/04/16/more-spidermonkey-changes-ancient-esoteric-very-rarely-used-syntax-for-creating-getters-and-setters-is-being-removed/) for further details on what was removed and how to adapt to those removals.

#### Summary

In principle, getters and setters can be either

-   defined using [object initializers](#Using_object_initializers), or
-   added later to any object at any time using a getter or setter adding method.

When defining getters and setters using [object initializers](#Using_object_initializers) all you need to do is to prefix a getter method with `get` and a setter method with `set`. Of course, the getter method must not expect a parameter, while the setter method expects exactly one parameter (the new value to set). For instance:

    var o = {
      a: 7,
      get b() { return this.a + 1; },
      set c(x) { this.a = x / 2; }
    };

Getters and setters can also be added to an object at any time after creation using two special methods called `__defineGetter__` and `__defineSetter__`. Both methods expect the name of the getter or setter as their first parameter, in the form of a string. The second parameter is the function to call as the getter or setter. For instance (following the previous example):

    o.__defineGetter__("b", function() { return this.a + 1; });
    o.__defineSetter__("c", function(x) { this.a = x / 2; });

Which of the two forms to choose depends on your programming style and task at hand. If you already go for the object initializer when defining a prototype you will probably most of the time choose the first form. This form is more compact and natural. However, if you need to add getters and setters later — because you did not write the prototype or particular object — then the second form is the only possible form. The second form probably best represents the dynamic nature of JavaScript — but it can make the code hard to read and understand.

Prior to Firefox 3.0, getter and setter are not supported for DOM Elements. Older versions of Firefox silently fail. If exceptions are needed for those, changing the prototype of HTMLElement `(HTMLElement.prototype.__define[SG]etter__)` and throwing an exception is a workaround.

With Firefox 3.0, defining getter or setter on an already-defined property will throw an exception. The property must be deleted beforehand, which is not the case for older versions of Firefox.

### Deleting properties

You can remove a property by using the `delete` operator. The following code shows how to remove a property.

    //Creates a new object, myobj, with two properties, a and b.
    var myobj = new Object;
    myobj.a = 5;
    myobj.b = 12;

    //Removes the a property, leaving myobj with only the b property.
    delete myobj.a;

You can also use `delete` to delete a global variable if the `var` keyword was not used to declare the variable:

    g = 17;
    delete g;

See `[/guides/JavaScript/Expressions#delete|delete]]` for more information.

<span style="float: left">[« Previous](/w/index.php?title=concepts/programming/javascript/objects/guides/JavaScript/Functions&action=edit&redlink=1)</span>[Next »](/w/index.php?title=concepts/programming/javascript/objects/guides/JavaScript/Predefined_Core_Objects&action=edit&redlink=1)

}}

## See also

### Other articles

-   `__defineGetter__`
-   `/js/objects/Object/defineSetter __defineSetter__`
-   `get`
-   `set`

### External resources

-   [ECMAScript 5.1 spec: Language Overview](http://es5.github.com/#x4.2)
-   [JavaScript. The core. (Dmitry A. Soshnikov ECMA-262 article series)](http://dmitrysoshnikov.com/ecmascript/javascript-the-core)

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Working_with_Objects)

