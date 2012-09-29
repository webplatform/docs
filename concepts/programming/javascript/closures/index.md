{{Page_Title|About closures}}
{{Flags}}
{{Summary_Section|Closures are often considered an advanced feature in JavaScript, but understanding them is essential to mastering the language.}}
{{Guide
|Content=Consider the following function:

<div style="width: auto; overflow: hidden">

 function init() {
   var name = "Hello world!";
   function displayName() {
     alert(name);
   }
   displayName();
 }
 init(); 

</div>

The <code>init()</code> function creates a local variable called <code>name</code>, and then defines a function called <code>displayName()</code>. <code>displayName()</code> is an inner function &mdash; it is defined inside <code>init()</code>, and is only available within the body of that function. <code>displayName()</code> has no local variables of its own, but reuses the <code>name</code> variable declared in the outer function.

This works just fine &mdash; try running the code to see what happens. This is an example of ''functional'' ''scoping'': in JavaScript, the scope of a variable is defined by its location within the source code, and nested functions have access to variables declared in their outer scope.

Now consider the following example:

 function makeFunc() {
   var name = "Hello world!";
   function displayName() {
     alert(name);
   }
   return displayName;
 }
 
 var myFunc = makeFunc();
 myFunc();

If you run this code it will have exactly the same effect as the previous <code>init()</code> example: the string "Hello world!" will be displayed in a JavaScript alert box. What's different &mdash; and interesting &mdash; is that the <code>displayName()</code> inner function was returned from the outer function before being executed.

That the code still works may seem unintuitive. Normally, the local variables within a function only exist for the duration of that function's execution. Once <code>makeFunc()</code> has finished executing, it is reasonable to expect that the name variable will no longer be necessary. Since the code still works as expected, this is obviously not the case.

The solution to this puzzle is that <code>myFunc</code> has become a ''closure''. A closure is a special kind of object that combines two things: a function, and the environment in which that function was created. The environment consists of any local variables that were in-scope at the time that the closure was created. In this case, <code>myFunc</code> is a closure that incorporates both the <code>displayName</code> function and the "Hello world!" string that existed when the closure was created.

Here's a slightly more interesting example &mdash; a <code>makeAdder</code> function:

 function makeAdder(x) {
   return function(y) {
     return x + y;
   };
 }
 
 var add5 = makeAdder(5);
 var add10 = makeAdder(10);
 
 print(add5(2));  // 7
 print(add10(2)); // 12

In this example, we have defined a function <code>makeAdder(x)</code> which takes a single argument <code>x</code> and returns a new function. The function it returns takes a single argument <code>y</code>, and returns the sum of <code>x</code> and <code>y</code>.

In essence, <code>makeAdder</code> is a function factory &mdash; it creates functions which can add a specific value to their argument. In the above example we use our function factory to create two new functions &mdash; one that adds 5 to its argument, and one that adds 10.

<code>add5</code> and <code>add10</code> are both closures. They share the same function body definition, but store different environments. In <code>add5</code>'s environment, <code>x</code> is 5. As far as <code>add10</code> is concerned, <code>x</code> is 10.

==Practical closures==

That's the theory out of the way &mdash; but are closures actually useful? Let's consider their practical implications. A closure lets you associate some data (the environment) with a function that operates on that data. This has obvious parallels to object oriented programming, where objects allow us to associate some data (the object's properties) with one or more methods.

Consequently, you can use a closure anywhere that you might normally use an object with only a single method.

Situations where you might want to do this are particularly common on the web. Much of the code we write in web JavaScript is event-based &mdash; we define some behavior, then attach it to an event that is triggered by the user (such as a click or a keypress). Our code is generally attached as a callback: a single function which is executed in response to the event.

Here's a practical example: suppose we wish to add some buttons to a page that adjust the text-size. One way of doing this is to specify the font-size of the body element in pixels, then set the size of the other elements on the page (such as headers) using the relative em unit:

 body {
   font-family: Helvetica, Arial, sans-serif;
   font-size: 12px;
 }
 
 h1 {
   font-size: 1.5em;
 }
 h2 {
   font-size: 1.2em;
 }

Our interactive text size buttons can change the font-size property of the body element, and the adjustments will be picked up by other elements on the page thanks to the relative units.

Here's the JavaScript:

 function makeSizer(size) {
   return function() {
     document.body.style.fontSize = size + 'px';
   };
 }
 
 var size12 = makeSizer(12);
 var size14 = makeSizer(14);
 var size16 = makeSizer(16);

<code>size12</code>, <code>size14</code> and <code>size16</code> are now functions which will resize the body text to 12, 14, and 16 pixels, respectively. We can attach them to buttons (in this case links) as follows:

 document.getElementById('size-12').onclick = size12;
 document.getElementById('size-14').onclick = size14;
 document.getElementById('size-16').onclick = size16;

 <a href="#" id="size-12">12</a>
 <a href="#" id="size-14">14</a>
 <a href="#" id="size-16">16</a> 

[http://jsfiddle.net/vnkuZ View on jsFiddle]

==Emulating private methods with closures==

Languages such as Java provide the ability to declare methods private, meaning that they can only be called by other methods in the same class.

JavaScript does not provide a native way of doing this, but it is possible to emulate private methods using closures. Private methods aren't just useful for restricting access to code: they also provide a powerful way of managing your global namespace, keeping non-essential methods from cluttering up the public interface to your code.

Here's how to define some public functions that can access private functions and variables, using closures which is also known as the [http://www.google.com/search?q=javascript+module+pattern module pattern]:

 var Counter = (function() {
   var privateCounter = 0;
   function changeBy(val) {
     privateCounter += val;
   }
   return {
     increment: function() {
       changeBy(1);
     },
     decrement: function() {
       changeBy(-1);
     },
     value: function() {
       return privateCounter;
     }
   }   
 })();
 
 alert(Counter.value()); /* Alerts 0 */
 Counter.increment();
 Counter.increment();
 alert(Counter.value()); /* Alerts 2 */
 Counter.decrement();
 alert(Counter.value()); /* Alerts 1 */

There's a lot going on here. In previous examples each closure has had its own environment; here we create a single environment which is shared by three functions: <code>Counter.increment</code>, <code>Counter.decrement</code> and <code>Counter.value</code>.

The shared environment is created in the body of an anonymous function, which is executed as soon as it has been defined. The environment contains two private items: a variable called <code>privateCounter</code> and a function called <code>changeBy</code>. Neither of these private items can be accessed directly from outside the anonymous function. Instead, they must be accessed by the three public functions that are returned from the anonymous wrapper.

Those three public functions are closures that share the same environment. Thanks to JavaScript's lexical scoping, they each have access to the <code>privateCounter</code> variable and <code>changeBy</code> function.

You'll notice we're defining an anonymous function that creates a counter, and then we call it immediately and assign the result to the <code>Counter</code> variable. We could store this function into a separate variable and use it to create several counters.

 var makeCounter = function() {
   var privateCounter = 0;
   function changeBy(val) {
     privateCounter += val;
   }
   return {
     increment: function() {
       changeBy(1);
     },
     decrement: function() {
       changeBy(-1);
     },
     value: function() {
       return privateCounter;
     }
   }  
 };
 
 var Counter1 = makeCounter();
 var Counter2 = makeCounter();
 alert(Counter1.value()); /* Alerts 0 */
 Counter1.increment();
 Counter1.increment();
 alert(Counter1.value()); /* Alerts 2 */
 Counter1.decrement();
 alert(Counter1.value()); /* Alerts 1 */
 alert(Counter2.value()); /* Alerts 0 */

Notice how each of the two counters maintains its independence from the other. Its environment during the call of the <code>makeCounter()</code> function is different each time. The closure variable <code>privateCounter </code>contains a different instance each time.

Using closures in this way provides a number of benefits that are normally associated with object oriented programming, in particular data hiding and encapsulation.

==Creating closures in loops: A common mistake==

Prior to the introduction of the [[/js/reference/statements/let|<code>let</code> keyword]] in JavaScript 1.7, a common problem with closures occurred when they were created inside a loop. Consider the following example:
<syntaxhighlight>
 <p id="help">Helpful notes will appear here</p>
 <p>E-mail: <input type="text" id="email" name="email"></p>
 <p>Name: <input type="text" id="name" name="name"></p>
 <p>Age: <input type="text" id="age" name="age"></p>
</syntaxhighlight>
 function showHelp(help) {
   document.getElementById('help').innerHTML = help;
 }
 
 function setupHelp() {
   var helpText = [
       {'id': 'email', 'help': 'Your e-mail address'},
       {'id': 'name', 'help': 'Your full name'},
       {'id': 'age', 'help': 'Your age (you must be over 16)'}
     ];
 
   for (var i = 0; i < helpText.length; i++) {
     var item = helpText[i];
     document.getElementById(item.id).onfocus = function() {
       showHelp(item.help);
     }
   }
 }
 
 setupHelp(); 

[http://jsfiddle.net/v7gjv View on jsFiddle]

The <code>helpText</code> array defines three helpful hints, each associated with the ID of an input field in the document. The loop cycles through these definitions, hooking up an onfocus event to each one that shows the associated help method.

If you try this code out, you'll see that it doesn't work as expected. No matter what field you focus on, the message about your age will be displayed.

The reason for this is that the functions assigned to onfocus are closures; they consist of the function definition and the captured environment from the <code>setupHelp</code> function's scope. Three closures have been created, but each one shares the same single environment. By the time the onfocus callbacks are executed, the loop has run its course and the item variable (shared by all three closures) has been left pointing to the last entry in the <code>helpText</code> list.

One solution in this case is to use more closures: in particular, to use a function factory as described earlier on:

 function showHelp(help) {
   document.getElementById('help').innerHTML = help;
 }
 
 function makeHelpCallback(help) {
   return function() {
     showHelp(help);
   };
 }
 
 function setupHelp() {
   var helpText = [
       {'id': 'email', 'help': 'Your e-mail address'},
       {'id': 'name', 'help': 'Your full name'},
       {'id': 'age', 'help': 'Your age (you must be over 16)'}
     ];
 
   for (var i = 0; i < helpText.length; i++) {
     var item = helpText[i];
     document.getElementById(item.id).onfocus = makeHelpCallback(item.help);
   }
 }
 
 setupHelp(); 

[http://jsfiddle.net/v7gjv/1 View on jsFiddle]

This works as expected. Rather than the callbacks all sharing a single environment, the <code>makeHelpCallback</code> function creates a new environment for each one in which <code>help</code> refers to the corresponding string from the <code>helpText</code> array.

==Performance considerations==

It is unwise to unnecessarily create functions within other functions if closures are not needed for a particular task as it will negatively affect script performance both in terms of processing speed and memory consumption.

For instance, when creating a new object/class, methods should normally be associated to the object's prototype rather than defined into the object constructor. The reason is that whenever the constructor is called the methods would get reassigned (that is, for every object creation).

Consider the following impractical but demonstrative case:

 function MyObject(name, message) {
   this.name = name.toString();
   this.message = message.toString();
   this.getName = function() {
     return this.name;
   };
 
   this.getMessage = function() {
     return this.message;
   };
 }

The previous code does not take advantage of the benefits of closures and thus should instead be formulated:

 function MyObject(name, message) {
   this.name = name.toString();
   this.message = message.toString();
 }
 MyObject.prototype = {
   getName: function() {
     return this.name;
   },
   getMessage: function() {
     return this.message;
   }
 };

Or as follows:

 function MyObject(name, message) {
   this.name = name.toString();
   this.message = message.toString();
 }
 MyObject.prototype.getName = function() {
   return this.name;
 };
 MyObject.prototype.getMessage = function() {
   return this.message;
 };

In the two previous examples, the inherited prototype can be shared by all objects and the method definitions need not occur at every object creation. See [[guides/JavaScript/objects|Details of the Object Model]] for more details.

<span style="float: left">[[/guides/JavaScript/iterators|&laquo; Previous]]</span>[[guides/JavaScript/LiveConnect|Next &raquo;]]
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
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Closures
|MSDN_link=
|HTML5Rocks_link=
}}