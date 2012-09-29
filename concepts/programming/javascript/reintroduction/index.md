{{Page_Title|A re-introduction to JavaScript}}
{{Flags
|Content=Outdated
|Editorial notes=Update to cover ES5
}}
{{Summary_Section|Why a re-introduction? Because JavaScript has a reasonable claim to being the world's most misunderstood programming language. While often derided as a toy, beneath its deceptive simplicity lie some powerful language features. Deeper knowledge of this technology is an important skill for any web developer.}}
{{Guide
|Content=It's useful to start with an idea of the language's history. JavaScript was created in 1995 by Brendan Eich, an engineer at Netscape, and first released with Netscape 2 early in 1996. It was originally going to be called LiveScript, but was renamed in an ill-fated marketing decision to try to capitalize on the popularity of Sun Microsystem's Java language — despite the two having very little in common. This has been a source of confusion ever since.

Microsoft released a mostly-compatible version of the language called JScript with IE 3 several months later. Netscape submitted the language to [http://www.ecma-international.org/ Ecma International], a European standards organization, which resulted in the first edition of the ECMAScript standard in 1997. The standard received a significant update as [http://www.ecma-international.org/publications/standards/Ecma-262.htm ECMAScript edition 3] in 1999, and has stayed pretty much stable ever since. The fourth edition was abandoned, due to political differences concerning language complexity. Many parts of the fourth edition formed a basis of the new ECMAScript edition 5, published in December of 2009.

This stability is great news for developers, as it's given the various implementations plenty of time to catch up. I'm going to focus almost exclusively on the edition 3 dialect. For familiarity, I will stick with the term JavaScript throughout.

Unlike most programming languages, the JavaScript language has no concept of input or output. It is designed to run as a scripting language in a host environment, and it is up to the host environment to provide mechanisms for communicating with the outside world. The most common host environment is the browser, but JavaScript interpreters can also be found in Adobe Acrobat, Photoshop, Yahoo!'s Widget engine, and even server side environments.

==Overview==

JavaScript is an object oriented dynamic language; it has types and operators, core objects, and methods. Its syntax comes from the Java and C languages, so many structures from those languages apply to JavaScript as well. One of the key differences is that JavaScript does not have classes; instead, the class functionality is accomplished by object prototypes. The other main difference is that functions are objects, giving functions the capacity to hold executable code and be passed around like any other object.

Let's start off by looking at the building block of any language: the types. JavaScript programs manipulate values, and those values all belong to a type. JavaScript's types are:

* [[/js/objects/Number|Numbers]]
* [[/js/objects/String|Strings]]
* [[/js/objects/Boolean|Booleans]]
* [[/js/objects/Function|Functions]]
* [[/js/objects/Object|Objects]]

... oh, and Undefined and Null, which are slightly odd. And [[/js/objects/Array|Arrays]], which are a special kind of object. And [[/js/objects/Date|Dates]] and [[/js/objects/RegExp|Regular Expressions]], which are objects that you get for free. And to be technically accurate, functions are just a special type of object. So the type diagram looks more like this:

* Number
* String
* Boolean
* Object
** Function
** Array
** Date
** RegExp
* Null
* Undefined

And there are some built in [[/js/objects/Error|Error]] types as well. Things are a lot easier if we stick with the first diagram, though.

==Numbers==

Numbers in JavaScript are "double-precision 64-bit format IEEE 754 values", according to the spec. This has some interesting consequences. There's no such thing as an integer in JavaScript, so you have to be a little careful with your arithmetic if you're used to math in C or Java. Watch out for stuff like:

 0.1 + 0.2 == 0.30000000000000004

In practice, integer values are treated as 32-bit ints (and are stored that way in some browser implementations), which can be important for bit-wise operations. For details, see [http://www.hunlock.com/blogs/The_Complete_Javascript_Number_Reference The Complete JavaScript Number Reference].

The standard [[/js/objects/operators/Arithmetic_Operators|numeric operators]] are supported, including addition, subtraction, modulus (or remainder) arithmetic and so forth. There's also a built-in object that I forgot to mention earlier called [[/js/objects/objects/Math|Math]] to handle more advanced mathematical functions and constants:

 Math.sin(3.5);
 var d = Math.PI * r * r;

You can convert a string to an integer using the built-in <code>[[/js/objects/objects/parseInt|parseInt()]]</code> function. This takes the base for the conversion as an optional second argument, which you should always provide:

 > parseInt("123", 10)
 123
 > parseInt("010", 10)
 10

If you don't provide the base, you can get surprising results:

 > parseInt("010")
 8

That happened because the <code>parseInt</code> function decided to treat the string as octal due to the leading 0.

If you want to convert a binary number to an integer, just change the base:

 > parseInt("11", 2)
 3

Similarly, you can parse floating point numbers using the built-in <code>[[/js/objects/parseFloat|parseFloat()]]</code> function which uses base 10 always unlike its [[/js/objects/parseInt|<code>parseInt()</code>]] cousin.

You can also use the unary <code>+</code> operator to convert values to numbers:

 > + "42"
 42 

A special value called <code>[[/js/objects/NaN|NaN]]</code> (short for "Not a Number") is returned if the string is non-numeric:

 > parseInt("hello", 10)
 NaN

<code>NaN</code> is toxic: if you provide it as an input to any mathematical operation the result will also be <code>NaN</code><nowiki>:</nowiki>

 > NaN + 5
 NaN

You can test for <code>NaN</code> using the built-in <code>[[/js/objects/isNaN|isNaN()]]</code> function:

 > isNaN(NaN)
 true

JavaScript also has the special values <code>[[/js/objects/Infinity|Infinity]]</code> and <code>-Infinity</code><nowiki>:</nowiki>

 > 1 / 0
 Infinity
 > -1 / 0
 -Infinity

You can test for <code>Infinity</code>, <code>-Infinity</code> and <code>NaN</code> values using the built-in <code>[[/js/objects/isFinite|isFinite()]]</code> function:

 > isFinite(1/0)
 false
 > isFinite(-Infinite)
 false
 > isFinite(NaN)
 false

{{Note|The [[/js/objects/parseInt|<code>parseInt()</code>]] and <code>[[/js/objects/parseFloat|parseFloat()]]</code> functions parse a string until they reach a character that isn't valid for the specified number format, then return the number parsed up to that point. However the "+" operator simply converts the string to <code>NaN</code> if there is any invalid character in it. Just try parsing the string "10.2abc" with each method by yourself in the console and you'll understand the differences better.</div>

==Strings==

Strings in JavaScript are sequences of characters. More accurately, they're sequences of [http://unicode.org/charts/ Unicode characters], with each character represented by a 16-bit number. This should be welcome news to anyone who has had to deal with internationalisation.

If you want to represent a single character, you just use a string of length 1.

To find the length of a string, access its <code>[[/js/objects/String/length|length]]</code> property:

 > "hello".length
 5

There's our first brush with JavaScript objects! Did I mention that strings are objects too? They have [[/js/objects/String#Methods|methods]] as well:

 > "hello".charAt(0)
 h
 > "hello, world".replace("hello", "goodbye")
 goodbye, world
 > "hello".toUpperCase()
 HELLO

==Other types==

JavaScript distinguishes between <code>null</code>, which is an object of type 'object' that indicates a deliberate non-value, and <code>undefined</code>, which is an object of type 'undefined' that indicates an uninitialized value — that is, a value hasn't even been assigned yet. We'll talk about variables later, but in JavaScript it is possible to declare a variable without assigning a value to it. If you do this, the variable's type is <code>undefined</code>.

JavaScript has a boolean type, with possible values <code>true</code> and <code>false</code> (both of which are keywords). Any value can be converted to a boolean according to the following rules:

# <code>false</code>, <code>0</code>, the empty string (<code>""</code>), <code>NaN</code>, <code>null</code>, and <code>undefined</code> all become <code>false</code>
# all other values become <code>true</code>

You can perform this conversion explicitly using the <code>Boolean()</code> function:

 > Boolean("")
 false
 > Boolean(234)
 true

However, this is rarely necessary, as JavaScript will silently perform this conversion when it expects a boolean, such as in an <code>if</code> statement (see below). For this reason, we sometimes speak simply of "true values" and "false values," meaning values that become <code>true</code> and <code>false</code>, respectively, when converted to booleans. Alternatively, such values can be called "truthy" and "falsy", respectively.

Boolean operations such as <code>&amp;&amp;</code> (logical ''and''), <code><nowiki>{{!}}{{!}}</nowiki></code> (logical ''or''), and <code><nowiki>!</nowiki></code> (logical ''not'') are supported; see below.

==Variables==

New variables in JavaScript are declared using the <code>[[/js/statements/var|var]]</code> keyword:

 var a;
 var name = "simon";

If you declare a variable without assigning any value to it, its type is <code>undefined</code>.

An important difference from other languages like Java is that in JavaScript, blocks do not have scope; only functions have scope. So if a variable is defined using <code>var</code> in a compound statement (for example inside an <code>if</code> control structure), it will be visible to the entire function.

==Operators==

JavaScript's numeric operators are <code>+</code>, <code>-</code>, <code><nowiki>*</nowiki></code>, <code>/</code> and <code>%</code> &mdash; which is the remainder operator. Values are assigned using <code><nowiki>=</nowiki></code>, and there are also compound assignment statements such as <code>+=</code> and <code>-=</code>. These extend out to <code>x = x ''operator'' y</code>.

 x += 5
 x = x + 5

You can use <code>++</code> and <code>--</code> to increment and decrement respectively. These can be used as prefix or postfix operators.

The [[/js/objects/perators/String_Operators|<code>+</code> operator]] also does string concatenation:

 > "hello" + " world"
 hello world

If you add a string to a number (or other value) everything is converted in to a string first. This might catch you out:

 > "3" + 4 + 5
 345
 > 3 + 4 + "5"
 75

Adding an empty string to something is a useful way of converting it.

[[/js/obperators/Comparison_Operators|Comparisons]] in JavaScript can be made using <code>&lt;</code>, <code>&gt;</code>, <code>&lt;=</code> and <code>&gt;=</code>. These work for both strings and numbers. Equality is a little less straightforward. The double-equals operator performs type coercion if you give it different types, with sometimes interesting results:

 > "dog" == "dog"
 true
 > 1 == true
 true

To avoid type coercion, use the triple-equals operator:

 > 1 === true
 false
 > true === true
 true

There are also <code><nowiki>!=</nowiki></code> and <code><nowiki>!==</nowiki></code> operators.

JavaScript also has [[/js/operators/Bitwise_Operators|bitwise operations]]. If you want to use them, they're there.

==Control structures==

JavaScript has a similar set of control structures to other languages in the C family. Conditional statements are supported by <code>if</code> and <code>else</code><nowiki>; you can chain them together if you like:</nowiki>

 var name = "kittens";
 if (name == "puppies") {
   name += "!";
 } else if (name == "kittens") {
   name += "!!";
 } else {
   name = "!" + name;
 }
 name == "kittens!!"

JavaScript has <code>while</code> loops and <code>do-while</code> loops. The first is good for basic looping; the second for loops where you wish to ensure that the body of the loop is executed at least once:

 while (true) {
   // an infinite loop!
 }
 
 var input;
 do {
   input = get_input();
 } while (inputIsNotValid(input))

JavaScript's <code>for</code> loop is the same as that in C and Java: it lets you provide the control information for your loop on a single line.

 for (var i = 0; i &lt; 5; i++) {
   // Will execute 5 times
 }

The <code>&amp;&amp;</code> and <code><nowiki>{{!}}{{!}}</nowiki></code> operators use short-circuit logic, which means whether they will execute their second operand is dependent on the first. This is useful for checking for null objects before accessing their attributes:

 var name = o &amp;&amp; o.getName();

Or for setting default values:

 var name = otherName {{!}}{{!}} "default";

JavaScript has a ternary operator for conditional expressions:

 var allowed = (age &gt; 18) ? "yes" : "no";

The switch statement can be used for multiple branches based on a number or string:

 switch(action) {
     case 'draw':
         drawit();
         break;
     case 'eat':
         eatit();
         break;
     default:
         donothing();
 }

If you don't add a <code>break</code> statement, execution will "fall through" to the next level. This is very rarely what you want &mdash; in fact it's worth specifically labelling deliberate fallthrough with a comment if you really meant it to aid debugging:

 switch(a) {
     case 1: // fallthrough
     case 2:
         eatit();
         break;
     default:
         donothing();
 }

The default clause is optional. You can have expressions in both the switch part and the cases if you like; comparisons take place between the two using the <code><nowiki>===</nowiki></code> operator:

 switch(1 + 3) {
     case 2 + 2:
         yay();
         break;
     default:
         neverhappens();
 }

==Objects==

JavaScript objects are simply collections of name-value pairs. As such, they are similar to:

* Dictionaries in Python
* Hashes in Perl and Ruby
* Hash tables in C and C++
* HashMaps in Java
* Associative arrays in PHP

The fact that this data structure is so widely used is a testament to its versatility. Since everything (bar core types) in JavaScript is an object, any JavaScript program naturally involves a great deal of hash table lookups. It's a good thing they're so fast!

The "name" part is a JavaScript string, while the value can be any JavaScript value &mdash; including more objects. This allows you to build data structures of arbitrary complexity.

There are two basic ways to create an empty object:

 var obj = new Object();

And:

 var obj = {};

These are semantically equivalent; the second is called object literal syntax, and is more convenient. This syntax is also the core of JSON format and should be preferred at all times.

Once created, an object's properties can again be accessed in one of two ways:

 obj.name = "Simon";
 var name = obj.name;

And...

 obj["name"] = "Simon";
 var name = obj["name"];

These are also semantically equivalent. The second method has the advantage that the name of the property is provided as a string, which means it can be calculated at run-time though using this method prevents some JavaScript engine and minifier optimizations being applied. It can also be used to set and get properties with names that are [[/js/reserved_words|reserved words]]<nowiki>:</nowiki>

 obj.for = "Simon"; // Syntax error, because 'for' is a reserved word
 obj["for"] = "Simon"; // works fine

Object literal syntax can be used to initialise an object in its entirety:

 var obj = {
     name: "Carrot",
     "for": "Max",
     details: {
         color: "orange",
         size: 12
     }
 }

Attribute access can be chained together:

 > obj.details.color
 orange
 > obj["details"]["size"]
 12

==Arrays==

Arrays in JavaScript are actually a special type of object. They work very much like regular objects (numerical properties can naturally be accessed only using [] syntax) but they have one magic property called '<code>length</code>'. This is always one more than the highest index in the array.

The old way of creating arrays is as follows:

 > var a = new Array();
 > a[0] = "dog";
 > a[1] = "cat";
 > a[2] = "hen";
 > a.length
 3

A more convenient notation is to use an array literal:

 > var a = ["dog", "cat", "hen"];
 > a.length
 3

Leaving a trailing comma at the end of an array literal is inconsistent across browsers, so don't do it.

Note that <code>array.length</code> isn't necessarily the number of items in the array. Consider the following:

 > var a = ["dog", "cat", "hen"];
 > a[100] = "fox";
 > a.length
 101

Remember &mdash; the length of the array is one more than the highest index.

If you query a non-existent array index, you get <code>undefined</code><nowiki>:</nowiki>

 > typeof a[90]
 undefined

If you take the above into account, you can iterate over an array using the following:

 for (var i = 0; i &lt; a.length; i++) {
     // Do something with a[i]
 }

This is slightly inefficient as you are looking up the length property once every loop. An improvement is this:

 for (var i = 0, len = a.length; i &lt; len; i++) {
     // Do something with a[i]
 }

An even nicer idiom is:

 for (var i = 0, item; item = a[i++];) {
     // Do something with item
 }

Here we are setting up two variables. The assignment in the middle part of the <code>for</code> loop is also tested for truthfulness &mdash; if it succeeds, the loop continues. Since <code>i</code> is incremented each time, items from the array will be assigned to item in sequential order. The loop stops when a "falsy" item is found (such as <code>undefined</code>).

Note that this trick should only be used for arrays which you know do not contain "falsy" values (arrays of objects or [[/DOM|DOM]] nodes for example). If you are iterating over numeric data that might include a 0 or string data that might include the empty string you should use the <code>i, len</code> idiom instead.

Another way to iterate is to use the <code>[[/js/statements/for...in|for...in]]</code> loop. Note that if someone added new properties to <code>Array.prototype</code>, they will also be iterated over by this loop:

 for (var i in a) {
   // Do something with a[i]
 }

If you want to append an item to an array, the safest way to do it is like this:

 a[a.length] = item;                 // same as a.push(item);

Since <code>a.length</code> is one more than the highest index, you can be assured that you are assigning to an empty position at the end of the array.

Arrays come with a number of methods:

{{{!}}
! scope="col" {{!}} Method name
! scope="col" {{!}} Description
{{!}}-
{{!}} <code>a.toString()</code>
{{!}}
{{!}}-
{{!}} <code>a.toLocaleString()</code>
{{!}}
{{!}}-
{{!}} <code>a.concat(item[, itemN])</code>
{{!}} Returns a new array with the items added on to it.
{{!}}-
{{!}} <code>a.join(sep)</code>
{{!}}
{{!}}-
{{!}} <code>a.pop()</code>
{{!}} Removes and returns the last item.
{{!}}-
{{!}} <code>a.push(item[, itemN])</code>
{{!}} <code>Push</code> adds one or more items to the end.
{{!}}-
{{!}} <code>a.reverse()</code>
{{!}}
{{!}}-
{{!}} <code>a.shift()</code>
{{!}}
{{!}}-
{{!}} <code>a.slice(start, end)</code>
{{!}} Returns a sub-array.
{{!}}-
{{!}} <code>a.sort([cmpfn])</code>
{{!}} Takes an optional comparison function.
{{!}}-
{{!}} <code>a.splice(start, delcount[, itemN])</code>
{{!}} Lets you modify an array by deleting a section and replacing it with more items.
{{!}}-
{{!}} <code>a.unshift([item])</code>
{{!}} Prepends items to the start of the array.
{{!}}}

==Functions==

Along with objects, functions are the core component in understanding JavaScript. The most basic function couldn't be much simpler:

 function add(x, y) {
     var total = x + y;
     return total;
 }

This demonstrates everything there is to know about basic functions. A JavaScript function can take 0 or more named parameters. The function body can contain as many statements as you like, and can declare its own variables which are local to that function. The <code>return</code> statement can be used to return a value at any time, terminating the function. If no return statement is used (or an empty return with no value), JavaScript returns <code>undefined</code>.

The named parameters turn out to be more like guidelines than anything else. You can call a function without passing the parameters it expects, in which case they will be set to <code>undefined</code>.

 > add()
 NaN // You can't perform addition on undefined

You can also pass in more arguments than the function is expecting:

 > add(2, 3, 4)
 5 // added the first two; 4 was ignored

That may seem a little silly, but functions have access to an additional variable inside their body called [[/js/functions/arguments|<code>arguments</code>]], which is an array-like object holding all of the values passed to the function. Let's re-write the add function to take as many values as we want:

 function add() {
     var sum = 0;
     for (var i = 0, j = arguments.length; i &lt; j; i++) {
         sum += arguments[i];
     }
     return sum;
 }
 
 &gt; add(2, 3, 4, 5)
 14

That's really not any more useful than writing <code>2 + 3 + 4 + 5</code> though. Let's create an averaging function:

 function avg() {
     var sum = 0;
     for (var i = 0, j = arguments.length; i &lt; j; i++) {
         sum += arguments[i];
     }
     return sum / arguments.length;
 }
 &gt; avg(2, 3, 4, 5)
 3.5

This is pretty useful, but introduces a new problem. The <code>avg()</code> function takes a comma separated list of arguments &mdash; but what if you want to find the average of an array? You could just rewrite the function as follows:

 function avgArray(arr) {
     var sum = 0;
     for (var i = 0, j = arr.length; i &lt; j; i++) {
         sum += arr[i];
     }
     return sum / arr.length;
 }
 > avgArray([2, 3, 4, 5])
 3.5

But it would be nice to be able to reuse the function that we've already created. Luckily, JavaScript lets you call a function and call it with an arbitrary array of arguments, using the [[/js/function/apply|<code>apply()</code>]] method of any function object.

 > avg.apply(null, [2, 3, 4, 5])
 3.5

The second argument to <code>apply()</code> is the array to use as arguments; the first will be discussed later on. This emphasizes the fact that functions are objects too.

JavaScript lets you create anonymous functions.

 var avg = function() {
     var sum = 0;
     for (var i = 0, j = arguments.length; i &lt; j; i++) {
         sum += arguments[i];
     }
     return sum / arguments.length;
 }

This is semantically equivalent to the <code>function avg()</code> form. It's extremely powerful, as it lets you put a full function definition anywhere that you would normally put an expression. This enables all sorts of clever tricks. Here's a way of "hiding" some local variables — like block scope in C:

 > var a = 1;
 > var b = 2;
 > (function() {
     var b = 3;
     a += b;
 })();
 > a
 4
 > b
 2

JavaScript allows you to call functions recursively. This is particularly useful for dealing with tree structures, such as you get in the browser [http://docs.webplatform.org/en/DOM DOM].

 function countChars(elm) {
     if (elm.nodeType == 3) { // TEXT_NODE
         return elm.nodeValue.length;
     }
     var count = 0;
     for (var i = 0, child; child = elm.childNodes[i]; i++) {
         count += countChars(child);
     }
     return count;
 }

This highlights a potential problem with anonymous functions: how do you call them recursively if they don't have a name? The answer lies with the <strike><code>arguments</code> object, which in addition to acting as a list of arguments also provides a property called <code>arguments.callee</code></strike>. The <code>arguments.callee</code> usage is deprecated and even disallowed in strict mode. Instead, you should use "named anonymous functions" as below:

 var charsInBody = (function counter(elm) {
     if (elm.nodeType == 3) { // TEXT_NODE
         return elm.nodeValue.length;
     }
     var count = 0;
     for (var i = 0, child; child = elm.childNodes[i]; i++) {
         count += counter(child);
     }
     return count;
 })(document.body);

The name provided to an anonymous function as above is(or at least should be) only available to the function's own scope. This both allows more optimizations to be done by the engine and a more readable code.

==Custom objects==

{{Note|For a more detailed discussion of object-oriented programming in JavaScript, see [[/tutorials/JavaScript/OOJ|Introduction to Object Oriented JavaScript]].}}

In classic Object Oriented Programming, objects are collections of data and methods that operate on that data. JavaScript is a prototype-based language which contains no class statement, such as is found in C++ or Java. (This is sometimes confusing for programmers accustomed to languages with a class statement.) Instead, JavaScript uses functions as classes. Let's consider a person object with first and last name fields. There are two ways in which the name might be displayed: as "first last" or as "last, first". Using the functions and objects that we've discussed previously, here's one way of doing it:

 function makePerson(first, last) {
     return {
         first: first,
         last: last
     }
 }
 function personFullName(person) {
     return person.first + ' ' + person.last;
 }
 function personFullNameReversed(person) {
     return person.last + ', ' + person.first
 }
 > s = makePerson("Simon", "Willison");
 > personFullName(s)
 Simon Willison
 > personFullNameReversed(s)
 Willison, Simon

This works, but it's pretty ugly. You end up with dozens of functions in your global namespace. What we really need is a way to attach a function to an object. Since functions are objects, this is easy:

 function makePerson(first, last) {
     return {
         first: first,
         last: last,
         fullName: function() {
             return this.first + ' ' + this.last;
         },
         fullNameReversed: function() {
             return this.last + ', ' + this.first;
         }
     }
 }
 > s = makePerson("Simon", "Willison")
 > s.fullName()
 Simon Willison
 > s.fullNameReversed()
 Willison, Simon

There's something here we haven't seen before: the '<code>[[/js/operators/this|this]]</code>' keyword. Used inside a function, '<code>this</code>' refers to the current object. What that actually means is specified by the way in which you called that function. If you called it using [/js/operators/member_operators|dot notation or bracket notation]] on an object, that object becomes '<code>this</code>'. If dot notation wasn't used for the call, '<code>this</code>' refers to the global object. This is a frequent cause of mistakes. For example:

 > s = makePerson("Simon", "Willison")
 > var fullName = s.fullName;
 > fullName()
 undefined undefined

When we call <code>fullName()</code>, '<code>this</code>' is bound to the global object. Since there are no global variables called <code>first</code> or <code>last</code> we get <code>undefined</code> for each one.

We can take advantage of the '<code>this</code>' keyword to improve our <code>makePerson</code> function:

 function Person(first, last) {
     this.first = first;
     this.last = last;
     this.fullName = function() {
         return this.first + ' ' + this.last;
     }
     this.fullNameReversed = function() {
         return this.last + ', ' + this.first;
     }
 }
 var s = new Person("Simon", "Willison");

We've introduced another keyword: '<code>[[/js/operators/new|new]]</code>'. <code>new</code> is strongly related to '<code>this</code>'. What it does is it creates a brand new empty object, and then calls the function specified, with '<code>this</code>' set to that new object. Functions that are designed to be called by '<code>new</code>' are called constructor functions. Common practise is to capitalise these functions as a reminder to call them with <code>new</code>.

Our person objects are getting better, but there are still some ugly edges to them. Every time we create a person object we are creating two brand new function objects within it &mdash; wouldn't it be better if this code was shared?

 function personFullName() {
     return this.first + ' ' + this.last;
 }
 function personFullNameReversed() {
     return this.last + ', ' + this.first;
 }
 function Person(first, last) {
     this.first = first;
     this.last = last;
     this.fullName = personFullName;
     this.fullNameReversed = personFullNameReversed;
 }

That's better: we are creating the method functions only once, and assigning references to them inside the constructor. Can we do any better than that? The answer is yes:

 function Person(first, last) {
     this.first = first;
     this.last = last;
 }
 Person.prototype.fullName = function() {
     return this.first + ' ' + this.last;
 }
 Person.prototype.fullNameReversed = function() {
     return this.last + ', ' + this.first;
 }

<code>Person.prototype</code> is an object shared by all instances of <code>Person</code>. It forms part of a lookup chain (that has a special name, "prototype chain"): any time you attempt to access a property of <code>Person</code> that isn't set, JavaScript will check <code>Person.prototype</code> to see if that property exists there instead. As a result, anything assigned to <code>Person.prototype</code> becomes available to all instances of that constructor via the <code>this</code> object.

This is an incredibly powerful tool. JavaScript lets you modify something's prototype at any time in your program, which means you can add extra methods to existing objects at runtime:

 > s = new Person("Simon", "Willison");
 > s.firstNameCaps();
 TypeError on line 1: s.firstNameCaps is not a function
 > Person.prototype.firstNameCaps = function() {
     return this.first.toUpperCase()
 }
 > s.firstNameCaps()
 SIMON

Interestingly, you can also add things to the prototype of built-in JavaScript objects. Let's add a method to <code>String</code> that returns that string in reverse:

 > var s = "Simon";
 > s.reversed()
 TypeError on line 1: s.reversed is not a function
 > String.prototype.reversed = function() {
     var r = "";
     for (var i = this.length - 1; i &gt;= 0; i--) {
         r += this[i];
     }
     return r;
 }
 > s.reversed()
 nomiS

Our new method even works on string literals!

 > "This can now be reversed".reversed()
 desrever eb won nac sihT

As I mentioned before, the prototype forms part of a chain. The root of that chain is <code>Object.prototype</code>, whose methods include <code>toString()</code> — it is this method that is called when you try to represent an object as a string. This is useful for debugging our <code>Person</code> objects:

 > var s = new Person("Simon", "Willison");
 > s
 [object Object]
 > Person.prototype.toString = function() {
     return '&lt;Person: ' + this.fullName() + '&gt;';
 }
 > s
 <Person: Simon Willison>;

Remember how <code>avg.apply()</code> had a null first argument? We can revisit that now. The first argument to <code>apply()</code> is the object that should be treated as '<code>this</code>'. For example, here's a trivial implementation of '<code>new</code>':

 function trivialNew(constructor) {
     var o = {}; // Create an object
     constructor.apply(o, arguments);
     return o;
 }

This isn't an exact replica of <code>new</code> as it doesn't set up the prototype chain. <code>apply()</code> is difficult to illustrate &mdash; it's not something you use very often, but it's useful to know about.

<code>apply()</code> has a sister function named [[/js/Function/call|<code>call</code>]], which again lets you set '<code>this</code>' but takes an expanded argument list as opposed to an array.

 function lastNameCaps() {
     return this.last.toUpperCase();
 }
 var s = new Person("Simon", "Willison");
 lastNameCaps.call(s);
 // Is the same as:
 s.lastNameCaps = lastNameCaps;
 s.lastNameCaps();

==Inner functions==

JavaScript function declarations are allowed inside other functions. We've seen this once before, with an earlier <code>makePerson()</code> function. An important detail of nested functions in JavaScript is that they can access variables in their parent function's scope:

 function betterExampleNeeded() {
     var a = 1;
     function oneMoreThanA() {
         return a + 1;
     }
     return oneMoreThanA();
 }

This provides a great deal of utility in writing more maintainable code. If a function relies on one or two other functions that are not useful to any other part of your code, you can nest those utility functions inside the function that will be called from elsewhere. This keeps the number of functions that are in the global scope down, which is always a good thing.

This is also a great counter to the lure of global variables. When writing complex code it is often tempting to use global variables to share values between multiple functions — which leads to code that is hard to maintain. Nested functions can share variables in their parent, so you can use that mechanism to couple functions together when it makes sense without polluting your global namespace &mdash; 'local globals' if you like. This technique should be used with caution, but it's a useful ability to have.

==Closures==

This leads us to one of the most powerful abstractions that JavaScript has to offer &mdash; but also the most potentially confusing. What does this do?

 function makeAdder(a) {
     return function(b) {
         return a + b;
     }
 }
 x = makeAdder(5);
 y = makeAdder(20);
 x(6)
 ?
 y(7)
 ?

The name of the <code>makeAdder</code> function should give it away: it creates new 'adder' functions, which when called with one argument add it to the argument that they were created with.

What's happening here is pretty much the same as was happening with the inner functions earlier on: a function defined inside another function has access to the outer function's variables. The only difference here is that the outer function has returned, and hence common sense would seem to dictate that its local variables no longer exist. But they ''do'' still exist &mdash; otherwise the adder functions would be unable to work. What's more, there are two different "copies" of <code>makeAdder</code>'s local variables &mdash; one in which <code>a</code> is 5 and one in which <code>a</code> is 20. So the result of those function calls is as follows:

 x(6) // returns 11
 y(7) // returns 27

Here's what's actually happening. Whenever JavaScript executes a function, a 'scope' object is created to hold the local variables created within that function. It is initialised with any variables passed in as function parameters. This is similar to the global object that all global variables and functions live in, but with a couple of important differences: firstly, a brand new scope object is created every time a function starts executing, and secondly, unlike the global object (which in browsers is accessible as window) these scope objects cannot be directly accessed from your JavaScript code. There is no mechanism for iterating over the properties of the current scope object for example.

So when <code>makeAdder</code> is called, a scope object is created with one property: <code>a</code>, which is the argument passed to the <code>makeAdder</code> function. <code>makeAdder</code> then returns a newly created function. Normally JavaScript's garbage collector would clean up the scope object created for <code>makeAdder</code> at this point, but the returned function maintains a reference back to that scope object. As a result, the scope object will not be garbage collected until there are no more references to the function object that <code>makeAdder</code> returned.

Scope objects form a chain called the scope chain, similar to the prototype chain used by JavaScript's object system.

A closure is the combination of a function and the scope object in which it was created.

Closures let you save state &mdash; as such, they can often be used in place of objects.

===Memory leaks===

An unfortunate side effect of closures is that they make it trivially easy to leak memory in Internet Explorer. JavaScript is a garbage collected language &mdash; objects are allocated memory upon their creation and that memory is reclaimed by the browser when no references to an object remain. Objects provided by the host environment are handled by that environment.

Browser hosts need to manage a large number of objects representing the HTML page being presented &mdash; the objects of the [[/DOM|DOM]]. It is up to the browser to manage the allocation and recovery of these.

Internet Explorer uses its own garbage collection scheme for this, separate from the mechanism used by JavaScript. It is the interaction between the two that can cause memory leaks.

A memory leak in IE occurs any time a circular reference is formed between a JavaScript object and a native object. Consider the following:

 function leakMemory() {
     var el = document.getElementById('el');
     var o = { 'el': el };
     el.o = o;
 }

The circular reference formed above creates a memory leak; IE will not free the memory used by <code>el</code> and <code>o</code> until the browser is completely restarted.

The above case is likely to go unnoticed; memory leaks only become a real concern in long running applications or applications that leak large amounts of memory due to large data structures or leak patterns within loops.

Leaks are rarely this obvious &mdash; often the leaked data structure can have many layers of references, obscuring the circular reference.

Closures make it easy to create a memory leak without meaning to. Consider this:

 function addHandler() {
     var el = document.getElementById('el');
     el.onclick = function() {
         this.style.backgroundColor = 'red';
     }
 }

The above code sets up the element to turn red when it is clicked. It also creates a memory leak. Why? Because the reference to <code>el</code> is inadvertently caught in the closure created for the anonymous inner function. This creates a circular reference between a JavaScript object (the function) and a native object (<code>el</code>).

 <font size="16px">needsTechnicalReview();
 </font>

There are a number of workarounds for this problem. The simplest is not to use the <code>el</code> variable:

 function addHandler(){
     document.getElementById('el').onclick = function(){
         this.style.backgroundColor = 'red';
     }
 }

Surprisingly, one trick for breaking circular references introduced by a closure is to add another closure:

 function addHandler() {
     var clickHandler = function() {
         this.style.backgroundColor = 'red';
     };
     (function() {
         var el = document.getElementById('el');
         el.onclick = clickHandler;
     })();
 }

The inner function is executed straight away, and hides its contents from the closure created with <code>clickHandler</code>.

Another good trick for avoiding closures is breaking circular references during the <code>window.onunload</code> event. Many event libraries will do this for you. Note that doing so disables [http://developer.mozilla.org/docs/Using_Firefox_1.5_caching bfcache in Firefox 1.5], so you should not register an <code>unload</code> listener in Firefox, unless you have other reasons to do so.

<div class="originaldocinfo">

==Original Document Information==

* Author: [http://simon.incutio.com/ Simon Willison]
* Original publication date: March 7, 2006
* Copyright: &copyr; 2006 Simon Willison, contributed under the Creative Commons: Attribute-Sharealike 2.0 license.
* More information: For more information about this tutorial (and for links to the original talk's slides), see Simon's [http://simon.incutio.com/archive/2006/03/07/etech Etech weblog post].

</div>
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/A_re-introduction_to_JavaScript
|MSDN_link=
|HTML5Rocks_link=
}}