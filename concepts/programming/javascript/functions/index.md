{{Page_Title|Functions}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|Functions are one of the fundamental building blocks in JavaScript. A function is a JavaScript procedure—a set of statements that performs a task or calculates a value. To use a function, you must define it somewhere in the scope from which you wish to call it.}}
{{Tutorial
|Content===Defining functions==

A '''function definition''' (also called a '''function declaration''') consists of the <code>[[/js/statements/function|function]]</code> keyword, followed by

* The name of the function.
* A list of arguments to the function, enclosed in parentheses and separated by commas.
* The JavaScript statements that define the function, enclosed in curly braces, <code>{ }</code>.

For example, the following code defines a simple function named <code> square</code>:

<div style="margin-right: 270px">

 function square(number) {
   return number * number;
 }

</div>

The function <code>square</code> takes one argument, called <code>number</code>. The function consists of one statement that says to return the argument of the function (that is, <code>number</code>) multiplied by itself. The <code>[[/js/statements/return|return]]</code> statement specifies the value returned by the function.

 return number * number;

Primitive parameters (such as a number) are passed to functions '''by value'''; the value is passed to the function, but if the function changes the value of the parameter, this change is not reflected globally or in the calling function.

If you pass an object (i.e. a [[/glossary/non-primitive value|non-primitive value]], such as <code>[[/js/objects/Array|Array]]</code> or a user-defined object) as a parameter, and the function changes the object's properties, that change is visible outside the function, as shown in the following example:

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

Note that assigning a new object to the parameter will '''not''' have any effect outside the function, because this is changing the value of the parameter rather than the value of one of the object's properties:

 function myFunc(theObject) {
   theObject = {make: "Ford", model: "Focus", year: 2006};
 }
 
 var mycar = {make: "Honda", model: "Accord", year: 1998},
     x,
     y;
 
 x = mycar.make;     // x gets the value "Honda"
 
 myFunc(mycar);
 y = mycar.make;     // y still gets the value "Honda" 

In the first case, the object <code>mycar</code> was passed to the function <code>myFunc</code>, which altered it. In the second case, the function did not alter the object that was passed; instead, it created a new local variable that happens to have the same name as the global object passed in, so there is no effect on the global object that was passed in.

In JavaScript, a function can be defined based on a condition. For example, the following function definition defines <code>myFunc</code> only if <code>num</code> equals 0:

 if (num == 0){
   function myFunc(theObject) {
     theObject.make = "Toyota"
   }
 }

If <code>num</code> does not equal 0, the function is not defined, and any attempt to execute it will fail.

Note that ECMAScript does not allow functions to appear in such contexts such as this, only directly inside other functions or at the top level of a program, so this example is invalid as ECMAScript.

{{Note|Different implementations of JavaScript handle this non-standard construct differently, so it is best avoided when writing portable code. Otherwise, your code may work in some browsers but not in others.}}

In addition to defining functions as described here, you can also use the  <code>[[js/objects/Function_Object|Function]]</code> constructor to create functions from a string at runtime, much like <code>[[js/Functions#eval_Function|eval()]]</code>.

A '''method''' is a function that is a property of an object. Read more about objects and methods in [[/guides/JavaScript/Working_with_Objects|Working with Objects]].

While the function declarations above are all syntactically statements, functions can also be created by a '''function expression'''. Such a function can be '''anonymous'''<nowiki>; it does not have to have a name. For example, the function </nowiki><code>square</code> could have been defined as:

 var square = function(number) {return number * number};

However, a name can be provided with a function expression, and can be used inside the function to refer to itself, or in a debugger to identify the function in stack traces:

 var factorial = function fac(n) {return n<2 ? 1 : n*fac(n-1)};
 
 print(factorial(3));

Function expressions are convenient when passing a function as an argument to another function. The following example shows a <code>map</code> function being defined and then called with an anonymous function as its first parameter:

 function map(f,a) {
   var result = [], // Create a new Array
       i;
   for (i = 0; i != a.length; i++)
     result[i] = f(a[i]);
   return result;
 }

The following code:

 map(function(x) {return x * x * x}, [0, 1, 2, 5, 10]);

returns [0, 1, 8, 125, 1000].

==Calling functions==

Defining a function does not execute it. Defining the function simply names the function and specifies what to do when the function is called. '''Calling''' the function actually performs the specified actions with the indicated parameters. For example, if you define the function <code>square</code>, you could call it as follows:

 square(5);

The preceding statement calls the function with an argument of 5. The function executes its statements and returns the value 25.

Functions must be in scope when they are called, but the function declaration can be below the call, as in this example:

 print(square(5));
 /* ... */
 function square(n){return n*n} 

The scope of a function is the function in which it is declared, or the entire program if it is declared at the top level. Note that this works only when defining the function using the above syntax (i.e. <code>function funcName(){}</code>). The code below will not work.

 print(square(5));
 square = function (n) {
   return n * n;
 }

The arguments of a function are not limited to strings and numbers. You can pass whole objects to a function, too. The <code>show_props</code> function (defined in [[/guides/JavaScript/Working_with_Objects#Objects_and_Properties|Working with Objects]]) is an example of a function that takes an object as an argument.

A function can be recursive; that is, it can call itself. For example, here is a function that computes factorials recursively:

 function factorial(n){
   if ((n == 0) {{!}}{{!}} (n == 1))
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

There are other ways to call functions. There are often cases where a function needs to be called dynamically, or the number of arguments to a function vary, or in which the context of the function call needs to be set to a specific object determined at runtime. It turns out that functions are, themselves, objects, and these objects in turn have methods (see the <code>[[/js/objects/Function_Object|Function]]</code> object). One of these, the  <code>[[/js/objects/Function/apply|apply()]]</code> method, can be used to achieve this goal.

==Function scope==

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

==Closures==

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
       if(typeof newSex == "string" && (newSex.toLowerCase() == "male" {{!}}{{!}} newSex.toLowerCase() == "female")) {
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

In the codes above, the <code>name</code> variable of the outer function is accessible to the inner functions, and there is no other way to access the inner variables except through the inner functions. The inner variables of the inner function act as safe stores for the inner functions. They hold "persistent", yet secure, data for the inner functions to work with. The functions do not even have to be assigned to a variable, or have a name.

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
       name = name;               // ??? How do we access the "name" defined by the outer function ???
     }
   }
 }

The magical <code>this</code> variable is very tricky in closures. They have to be used carefully, as what <code>this</code> refers to depends completely on where the function was called, rather than where it was defined. An excellent and elaborate article on closures can be found [http://jibbering.com/faq/notes/closures/ here].

==Using the arguments object==

The arguments of a function are maintained in an array-like object. Within a function, you can address the arguments passed to it as follows:

 arguments[i]

where <code>i</code> is the ordinal number of the argument, starting at zero. So, the first argument passed to a function would be <code>arguments[0]</code>. The total number of arguments is indicated by <code>arguments.length</code>.

Using the <code>arguments</code> object, you can call a function with more arguments than it is formally declared to accept. This is often useful if you don't know in advance how many arguments will be passed to the function. You can use <code>arguments.length</code> to determine the number of arguments actually passed to the function, and then access each argument using the <code>arguments</code> object.

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

Please note that the <code>arguments</code> variable is "array-like", but not an array. It is array-like in that is has a numbered index and a <code>length</code> property. However, it does not possess all of the array-manipulation methods.

See the  <code>[[/js/objects/Function|Function]]</code> object in the JavaScript Reference for more information.

==Predefined functions==

JavaScript has several top-level predefined functions:

* [[#eval_function|eval]]
* [[#isFinite_function|isFinite]]
* [[#isNaN_function|isNaN]]
* [[#parseInt_and_parseFloat_functions|parseInt and parseFloat]]
* [[#Number_and_String_functions|Number and String]]
* [[#escape_and_unescape_functions|encodeURI, decodeURI, encodeURIComponent, and decodeURIComponent]] (all available with Javascript 1.5 and later).

The following sections introduce these functions. See the [[/js|JavaScript Reference]] for detailed information on all of these functions.

===eval Function===

The <code>eval</code> function evaluates a string of JavaScript code without reference to a particular object. The syntax of <code>eval</code> is:

 eval(expr);

where <code>expr</code> is a string to be evaluated.

If the string represents an expression, <code>eval</code> evaluates the expression. If the argument represents one or more JavaScript statements, eval performs the statements. The scope of <code>eval</code> code is identical to the scope of the calling code. Do not call <code>eval</code> to evaluate an arithmetic expression; JavaScript evaluates arithmetic expressions automatically.

===isFinite function===

The <code>isFinite</code> function evaluates an argument to determine whether it is a finite number. The syntax of <code>isFinite</code> is:

 isFinite(number);

where <code>number</code> is the number to evaluate.

If the argument is <code>NaN</code>, positive infinity or negative infinity, this method returns <code>false</code>, otherwise it returns <code>true</code>.

The following code checks client input to determine whether it is a finite number.

 if(isFinite(ClientInput)){
    /* take specific steps */
 }

===isNaN function===

The <code>isNaN</code> function evaluates an argument to determine if it is "NaN" (not a number). The syntax of <code>isNaN</code> is:

 isNaN(testValue);

where <code>testValue</code> is the value you want to evaluate.

The <code>parseFloat</code> and <code>parseInt</code> functions return "NaN" when they evaluate a value that is not a number. <code>isNaN</code> returns true if passed "NaN," and false otherwise.

The following code evaluates <code>floatValue</code> to determine if it is a number and then calls a procedure accordingly:

 var floatValue = parseFloat(toFloat);
 
 if (isNaN(floatValue)) {
    notFloat();
 } else {
    isFloat();
 }

===parseInt and parseFloat functions===

The two "parse" functions, <code>parseInt</code> and <code>parseFloat</code>, return a numeric value when given a string as an argument.

The syntax of <code>parseFloat</code> is

 parseFloat(str);

where <code>parseFloat</code> parses its argument, the string <code>str</code>, and attempts to return a floating-point number. If it encounters a character other than a sign (+ or -), a numeral (0-9), a decimal point, or an exponent, then it returns the value up to that point and ignores that character and all succeeding characters. If the first character cannot be converted to a number, it returns "NaN" (not a number).

The syntax of <code>parseInt</code> is

 parseInt(str [, radix]);

<code>parseInt</code> parses its first argument, the string <code>str</code>, and attempts to return an integer of the specified <code>radix</code> (base), indicated by the second, optional argument, <code>radix</code>. For example, a radix of ten indicates to convert to a decimal number, eight octal, sixteen hexadecimal, and so on. For radixes above ten, the letters of the alphabet indicate numerals greater than nine. For example, for hexadecimal numbers (base 16), A through F are used.

If <code>parseInt</code> encounters a character that is not a numeral in the specified radix, it ignores it and all succeeding characters and returns the integer value parsed up to that point. If the first character cannot be converted to a number in the specified radix, it returns "NaN." The <code>parseInt</code> function truncates the string to integer values.

===Number and String functions===

The <code>Number</code> and <code>String</code> functions let you convert an object to a number or a string. The syntax of these functions is:

 var objRef;
 objRef = Number(objRef);
 objRef = String(objRef);

where <code>objRef</code> is an object reference. Number uses the valueOf() method of the object; String uses the toString() method of the object.

The following example converts the <code>[http://docs.webplatform.org/en-US/docs/JavaScript/Reference/Global_Objects/Date Date]</code> object to a readable string.

 var D = new Date(430054663215),
     x;
 x = String(D); // x equals "Thu Aug 18 04:37:43 GMT-0700 (Pacific Daylight Time) 1983"

The following example converts the <code>[/js/objects/String|String]]</code> object to <code>[/js/objects/Number|Number]]</code> object.

 var str = "12",
     num;
 num = Number(str);

You can check it. Use DOM method <code>write()</code> and JavaScript <code>typeof</code> operator.

 var str = "12",
     num;
 document.write(typeof str);
 document.write("<br/>");
 num = Number(str);
 document.write(typeof num);

===escape and unescape functions===

The <code>escape</code> and <code>unescape</code> functions do not work properly for non-ASCII characters and have been deprecated. In JavaScript 1.5 and later, use <code>[[/js/objects/encodeURI|encodeURI]]</code>, <code>[[/js/objects/decodeURI|decodeURI]]</code>, <code>[[/js/objects/encodeURIComponent|encodeURIComponent]]</code>, and <code>[[/js/objects/decodeURIComponent|decodeURIComponent]]</code>.

The <code>escape</code> and <code>unescape</code> functions let you encode and decode strings. The <code>escape</code> function returns the hexadecimal encoding of an argument in the ISO Latin character set. The <code>unescape</code> function returns the ASCII string for the specified hexadecimal encoding value.

The syntax of these functions is:

 escape(string);
 unescape(string);

These functions are used primarily with server-side JavaScript to encode and decode name/value pairs in URLs.

<div>

<span style="float: left">[[/guides/JavaScript/Statements|&laquo; Previous]]</span>[[/guides/JavaScript/Working_with_Objects|Next &raquo;]]

</div>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Functions
|MSDN_link=
|HTML5Rocks_link=
}}