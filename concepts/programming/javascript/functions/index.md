---
title: 'JavaScript Functions'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Functions)'
notes:
  - 'It is not clear whether this article describes functions as a language construct in JS (as suggested by the beginning of the article) or if it is meant to be a reference (suggested by the parts at the end)'
readiness: 'Almost Ready'
summary: 'Functions are one of the fundamental building blocks in JavaScript. A function is a JavaScript procedure—a set of statements that performs a task or calculates a value. To use a function, you must define it somewhere in the scope from which you wish to call it.'
tags:
  - Tutorials
  - JavaScript
  - Merge_Candidate
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/functions/js/statements/function
    - concepts/programming/javascript/functions/js/statements/return
    - 'concepts/programming/javascript/functions/glossary/non-primitive value'
    - concepts/programming/javascript/functions/js/objects/Array
    - 'js/objects/Function Object'
    - js/Functions
    - 'concepts/programming/javascript/functions/guides/JavaScript/Working with Objects'
    - 'concepts/programming/javascript/functions/js/objects/Function Object'
    - concepts/programming/javascript/functions/js/objects/Function/apply
    - concepts/programming/javascript/functions/js/objects/Function
    - concepts/programming/javascript/functions/js
uri: concepts/programming/javascript/functions

---
## Summary

Functions are one of the fundamental building blocks in JavaScript. A function is a JavaScript procedure—a set of statements that performs a task or calculates a value. To use a function, you must define it somewhere in the scope from which you wish to call it.

## Defining functions

A **function definition** (also called a **function declaration**) consists of the `function` keyword, followed by

-   The name of the function.
-   A list of arguments to the function, enclosed in parentheses and separated by commas.
-   The JavaScript statements that define the function, enclosed in curly braces, `{ }`.

For example, the following code defines a simple function named ` square`:

    function square(number) {
      return number * number;
    }

The function `square` takes one argument, called `number`. The function consists of one statement that says to return the argument of the function (that is, `number`) multiplied by itself. The `return` statement specifies the value returned by the function.

    return number * number;

Primitive parameters (such as a number) are passed to functions **by value**; the value is passed to the function, but if the function changes the value of the parameter, this change is not reflected globally or in the calling function.

If you pass an object (i.e. a [non-primitive value](/w/index.php?title=concepts/programming/javascript/functions/glossary/non-primitive_value&action=edit&redlink=1), such as `Array` or a user-defined object) as a parameter, and the function changes the object's properties, that change is visible outside the function, as shown in the following example:

    function myFunc(theObject) {
      theObject.make = "Toyota";
    }

    var mycar = {make: "Honda", model: "Accord", year: 1998},
        x,
        y;

    x = mycar.make;     // x gets the value "Honda"

    myFunc(mycar);
    y = mycar.make;     // y gets the value "Toyota"
                        // (the make property was changed by the function)

Note that assigning a new object to the parameter will **not** have any effect outside the function, because this is changing the value of the parameter rather than the value of one of the object's properties:

    function myFunc(theObject) {
      theObject = {make: "Ford", model: "Focus", year: 2006};
    }

    var mycar = {make: "Honda", model: "Accord", year: 1998},
        x,
        y;

    x = mycar.make;     // x gets the value "Honda"

    myFunc(mycar);
    y = mycar.make;     // y still gets the value "Honda"

In the first case, the object `mycar` was passed to the function `myFunc`, which altered it. In the second case, the function did not alter the object that was passed; instead, it created a new local variable that happens to have the same name as the global object passed in, so there is no effect on the global object that was passed in.

In JavaScript, a function can be defined based on a condition. For example, the following function definition defines `myFunc` only if `num` equals 0:

    if (num == 0){
      function myFunc(theObject) {
        theObject.make = "Toyota"
      }
    }

If `num` does not equal 0, the function is not defined, and any attempt to execute it will fail.

Note that ECMAScript does not allow functions to appear in such contexts such as this, only directly inside other functions or at the top level of a program, so this example is invalid as ECMAScript.

**Note**: Different implementations of JavaScript handle this non-standard construct differently, so it is best avoided when writing portable code. Otherwise, your code may work in some browsers but not in others.

 In addition to defining functions as described here, you can also use the `Function` constructor to create functions from a string at runtime, much like `eval()`.

A **method** is a function that is a property of an object. Read more about objects and methods in [Working with Objects](/w/index.php?title=concepts/programming/javascript/functions/guides/JavaScript/Working_with_Objects&action=edit&redlink=1).

While the function declarations above are all syntactically statements, functions can also be created by a **function expression**. Such a function can be **anonymous**; it does not have to have a name. For example, the function `square` could have been defined as:

    var square = function(number) {return number * number};

However, a name can be provided with a function expression, and can be used inside the function to refer to itself, or in a debugger to identify the function in stack traces:

    var factorial = function fac(n) {return n<2 ? 1 : n*fac(n-1)};

    print(factorial(3));

Function expressions are convenient when passing a function as an argument to another function. The following example shows a `map` function being defined and then called with an anonymous function as its first parameter:

    function map(f,a) {
      var result = [], // Create a new Array
          i;
      for (i = 0; i != a.length; i++)
        result[i] = f(a[i]);
      return result;
    }

The following code:

    map(function(x) {return x * x * x}, [0, 1, 2, 5, 10]);

returns [0, 1, 8, 125, 1000].

## Calling functions

Defining a function does not execute it. Defining the function simply names the function and specifies what to do when the function is called. **Calling** the function actually performs the specified actions with the indicated parameters. For example, if you define the function `square`, you could call it as follows:

    square(5);

The preceding statement calls the function with an argument of 5. The function executes its statements and returns the value 25.

Functions must be in scope when they are called, but the function declaration can be below the call, as in this example:

    print(square(5));
    /* ... */
    function square(n){return n*n}

The scope of a function is the function in which it is declared, or the entire program if it is declared at the top level. Note that this works only when defining the function using the above syntax (i.e. `function funcName(){}`). The code below will not work.

    print(square(5));
    square = function (n) {
      return n * n;
    }

The arguments of a function are not limited to strings and numbers. You can pass whole objects to a function, too. The `show_props` function (defined in [Working with Objects](/w/index.php?title=concepts/programming/javascript/functions/guides/JavaScript/Working_with_Objects&action=edit&redlink=1)) is an example of a function that takes an object as an argument.

A function can be recursive; that is, it can call itself. For example, here is a function that computes factorials recursively:

    function factorial(n){
      if ((n == 0) || (n == 1))
        return 1;
      else
        return (n * factorial(n - 1));
    }

You could then compute the factorials of one through five as follows:

    var a, b, c, d, e;
    a = factorial(1); // a gets the value 1
    b = factorial(2); // b gets the value 2
    c = factorial(3); // c gets the value 6
    d = factorial(4); // d gets the value 24
    e = factorial(5); // e gets the value 120

There are other ways to call functions. There are often cases where a function needs to be called dynamically, or the number of arguments to a function vary, or in which the context of the function call needs to be set to a specific object determined at runtime. It turns out that functions are, themselves, objects, and these objects in turn have methods (see the `Function` object). One of these, the `apply()` method, can be used to achieve this goal.

## Function scope

Like Scheme, JavaScript has lexical scoping, meaning the scope of variables is restricted and determined by their placement. Additionally, in the case of JavaScript, only function definitions will create new scopes. The behavior of variables, therefore, may be determined by simply reading the code because the scope is entirely independent of the runtime (unlike dynamic scoping).

Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined. In other words, a function defined in the global scope can only access variables defined in the global scope (i.e. global variables). A function defined inside another function can also access all variables defined in its parent function and any other variable to which the parent function has access.

    // The following variables are defined in the global scope
    var num1 = 20,
        num2 = 3,
        name = "Chamahk";

    // This function is defined in the global scope
    function multiply() {
      return num1 * num2;
    }

    multiply(); // Returns 60

    // A nested function example
    function getScore () {
      var num1 = 2,
          num2 = 3;

      function add() {
        return name + " scored " + (num1 + num2);
      }

      return add();
    }

    getScore(); // Returns "Chamahk scored 5"

## Closures

Closures are one of the most powerful features of JavaScript. JavaScript allows for the nesting of functions and, in addition, grants the inner function full access to all the variables and functions defined inside the outer function (and all other variables and functions that the outer function has access to). However, the outer function does not have access to the variables and functions defined inside the inner function. This provides a sort of security for the variables of the inner function. Also, since the inner function has access to the scope of the outer function, the variables and functions defined in the outer function will live longer than the outer function itself, if the inner function manages to survive beyond the life of the outer function. A closure is created when the inner function is somehow made available to any scope outside the outer function.

    var pet = function(name) {          // The outer function defines a variable called "name"
          var getName = function() {
            return name;                // The inner function has access to the "name" variable of the outer function
          }

          return getName;               // Return the inner function, thereby exposing it to outer scopes
        },
        myPet = pet("Vivie");

    myPet();                            // Returns "Vivie"

It can be much more complex than the code above. An object containing methods for manipulating the inner variables of the outer function can be returned.

    var createPet = function(name) {
      var sex;

      return {
        setName: function(newName) {
          name = newName;
        },

        getName: function() {
          return name;
        },

        getSex: function() {
          return sex;
        },

        setSex: function(newSex) {
          if(typeof newSex == "string" && (newSex.toLowerCase() == "male" || newSex.toLowerCase() == "female")) {
            sex = newSex;
          }
        }
      }
    }

    var pet = createPet("Vivie");
    pet.getName();                  // Vivie

    pet.setName("Oliver");
    pet.setSex("male");
    pet.getSex();                   // male
    pet.getName();                  // Oliver

In the codes above, the `name` variable of the outer function is accessible to the inner functions, and there is no other way to access the inner variables except through the inner functions. The inner variables of the inner function act as safe stores for the inner functions. They hold "persistent", yet secure, data for the inner functions to work with. The functions do not even have to be assigned to a variable, or have a name.

    var getCode = (function(){
      var secureCode = "0]Eal(eh&2";    // A code we do not want outsiders to be able to modify...

      return function () {
        return secureCode;
      };
    })();

    getCode();    // Returns the secret code

There are, however, a number of pitfalls to watch out for when using closures. If an enclosed function defines a variable with the same name as the name of a variable in the outer scope, there is no way to refer to the variable in the outer scope again.

    var createPet = function(name) {  // Outer function defines a variable called "name"
      return {
        setName: function(name) {    // Enclosed function also defines a variable called "name"
          name = name;               // ??? How do we access the "name" defined by the outer function ???
        }
      }
    }

The magical `this` variable is very tricky in closures. They have to be used carefully, as what `this` refers to depends completely on where the function was called, rather than where it was defined. An excellent and elaborate article on closures can be found [here](http://jibbering.com/faq/notes/closures/).

## Using the arguments object

The arguments of a function are maintained in an array-like object. Within a function, you can address the arguments passed to it as follows:

    arguments[i]

where `i` is the ordinal number of the argument, starting at zero. So, the first argument passed to a function would be `arguments[0]`. The total number of arguments is indicated by `arguments.length`.

Using the `arguments` object, you can call a function with more arguments than it is formally declared to accept. This is often useful if you don't know in advance how many arguments will be passed to the function. You can use `arguments.length` to determine the number of arguments actually passed to the function, and then access each argument using the `arguments` object.

For example, consider a function that concatenates several strings. The only formal argument for the function is a string that specifies the characters that separate the items to concatenate. The function is defined as follows:

    function myConcat(separator) {
       var result = "", // initialize list
           i;
       // iterate through arguments
       for (i = 1; i < arguments.length; i++) {
          result += arguments[i] + separator;
       }
       return result;
    }

You can pass any number of arguments to this function, and it concatenates each argument into a string "list":

    // returns "red, orange, blue, "
    myConcat(", ", "red", "orange", "blue");

    // returns "elephant; giraffe; lion; cheetah; "
    myConcat("; ", "elephant", "giraffe", "lion", "cheetah");

    // returns "sage. basil. oregano. pepper. parsley. "
    myConcat(". ", "sage", "basil", "oregano", "pepper", "parsley");

Please note that the `arguments` variable is "array-like", but not an array. It is array-like in that is has a numbered index and a `length` property. However, it does not possess all of the array-manipulation methods.

See the `Function` object in the JavaScript Reference for more information.

## Predefined functions

JavaScript has several top-level predefined functions:

-   [eval](#eval_function)
-   [isFinite](#isFinite_function)
-   [isNaN](#isNaN_function)
-   [parseInt and parseFloat](#parseInt_and_parseFloat_functions)
-   [Number and String](#Number_and_String_functions)
-   [encodeURI, decodeURI, encodeURIComponent, and decodeURIComponent](#escape_and_unescape_functions) (all available with Javascript 1.5 and later).

The following sections introduce these functions. See the [JavaScript Reference](/w/index.php?title=concepts/programming/javascript/functions/js&action=edit&redlink=1) for detailed information on all of these functions.

### eval Function

The `eval` function evaluates a string of JavaScript code without reference to a particular object. The syntax of `eval` is:

    eval(expr);

where `expr` is a string to be evaluated.

If the string represents an expression, `eval` evaluates the expression. If the argument represents one or more JavaScript statements, eval performs the statements. The scope of `eval` code is identical to the scope of the calling code. Do not call `eval` to evaluate an arithmetic expression; JavaScript evaluates arithmetic expressions automatically.

### isFinite function

The `isFinite` function evaluates an argument to determine whether it is a finite number. The syntax of `isFinite` is:

    isFinite(number);

where `number` is the number to evaluate.

If the argument is `NaN`, positive infinity or negative infinity, this method returns `false`, otherwise it returns `true`.

The following code checks client input to determine whether it is a finite number.

    if(isFinite(ClientInput)){
       /* take specific steps */
    }

### isNaN function

The `isNaN` function evaluates an argument to determine if it is "NaN" (not a number). The syntax of `isNaN` is:

    isNaN(testValue);

where `testValue` is the value you want to evaluate.

The `parseFloat` and `parseInt` functions return "NaN" when they evaluate a value that is not a number. `isNaN` returns true if passed "NaN," and false otherwise.

The following code evaluates `floatValue` to determine if it is a number and then calls a procedure accordingly:

    var floatValue = parseFloat(toFloat);

    if (isNaN(floatValue)) {
       notFloat();
    } else {
       isFloat();
    }

### parseInt and parseFloat functions

The two "parse" functions, `parseInt` and `parseFloat`, return a numeric value when given a string as an argument.

The syntax of `parseFloat` is

    parseFloat(str);

where `parseFloat` parses its argument, the string `str`, and attempts to return a floating-point number. If it encounters a character other than a sign (+ or -), a numeral (0-9), a decimal point, or an exponent, then it returns the value up to that point and ignores that character and all succeeding characters. If the first character cannot be converted to a number, it returns "NaN" (not a number).

The syntax of `parseInt` is

    parseInt(str [, radix]);

`parseInt` parses its first argument, the string `str`, and attempts to return an integer of the specified `radix` (base), indicated by the second, optional argument, `radix`. For example, a radix of ten indicates to convert to a decimal number, eight octal, sixteen hexadecimal, and so on. For radixes above ten, the letters of the alphabet indicate numerals greater than nine. For example, for hexadecimal numbers (base 16), A through F are used.

If `parseInt` encounters a character that is not a numeral in the specified radix, it ignores it and all succeeding characters and returns the integer value parsed up to that point. If the first character cannot be converted to a number in the specified radix, it returns "NaN." The `parseInt` function truncates the string to integer values.

### Number and String functions

The `Number` and `String` functions let you convert an object to a number or a string. The syntax of these functions is:

    var objRef;
    objRef = Number(objRef);
    objRef = String(objRef);

where `objRef` is an object reference. Number uses the valueOf() method of the object; String uses the toString() method of the object.

The following example converts the `Date` object to a readable string.

    var D = new Date(430054663215),
        x;
    x = String(D); // x equals "Thu Aug 18 04:37:43 GMT-0700 (Pacific Daylight Time) 1983"

The following example converts the `[/js/objects/String`

