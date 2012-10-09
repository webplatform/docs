{{Page_Title|Iterators and generators}}
{{Flags
|Content=Not Neutral
|Editorial notes=Remove XUL-specific info.
}}
{{Summary_Section|Processing each of the items in a collection is a very common operation. JavaScript provides a number of ways of iterating over a collection, from simple <code>[[/js/reference/statements/for|for]]</code> and <code>[[/js/reference/statements/for_each...in|for each]]</code> loops to <code>[[/js/reference/objects/Array/map|map()]]</code>, <code>[[/js/reference/objects/Array/filter|filter()]]</code> and [[/guides/JavaScript/objects#Array_comprehensions|array comprehensions]]. Iterators and Generators, introduced in JavaScript 1.7, bring the concept of iteration directly into the core language and provide a mechanism for customizing the behavior of <code>[[/js/reference/statements/for...in|for...in]]</code> and <code>[[/js/reference/statements/for_each...in|for each]]</code> loops.}}

===Iterators==

An Iterator is an object that knows how to access items from a collection one at a time, while keeping track of its current position within that sequence. In JavaScript an iterator is an object that provides a <code>next()</code> method which returns the next item in the sequence. This method can optionally raise a <code>StopIteration</code> exception when the sequence is exhausted.

Once created, an iterator object can be used either explicitly by repeatedly calling <code>next()</code>, or implicitly using JavaScript's <code>[[/js/reference/statements/for...in|for...in]]</code> and <code>[[/js/reference/statements/for_each...in|for each]]</code> constructs.

Simple iterators for objects and arrays can be created using the <code>Iterator()</code> function:

 var lang = { name: 'JavaScript', birthYear: 1995 };
 var it = Iterator(lang);

Once initialized, the <code>next()</code> method can be called to access key-value pairs from the object in turn:

 var pair = it.next(); // Pair is ["name", "JavaScript"]
 pair = it.next(); // Pair is ["birthYear", 1995]
 pair = it.next(); // A StopIteration exception is thrown

A <code>for...in</code> loop can be used instead of calling the <code>next()</code> method directly. The loop will automatically terminate when the <code>StopIteration</code> exception is raised.

 var it = Iterator(lang);
 for (var pair in it)
   print(pair); // prints each [key, value] pair in turn

If we just want to iterate over the object's keys, we can pass a second argument of <code>true</code> to the <code>Iterator()</code> function:

 var it = Iterator(lang, true);
 for (var key in it)
   print(key); // prints each key in turn

One advantage of using <code>Iterator()</code> to access the contents of an object is that custom properties that have been added to <code>Object.prototype</code> will not be included in the sequence.

<code>Iterator()</code> can be used with arrays as well:

 var langs = ['JavaScript', 'Python', 'C++'];
 var it = Iterator(langs);
 for (var pair in it)
   print(pair); // prints each [index, language] pair in turn

As with objects, passing <code>true</code> as the second argument will result in iteration occurring over the array indices:

 var langs = ['JavaScript', 'Python', 'C++'];
 var it = Iterator(langs, true);
 for (var i in it)
   print(i); // prints 0, then 1, then 2

It is also possible to assign block scoped variables to both index and value within the for loop using the <code>let</code> keyword and a destructuring assignment:

 var langs = ['JavaScript', 'Python', 'C++'];
 var it = Iterator(langs);
 for (let [i, lang] in it)
  print(i + ': ' + lang); // prints "0: JavaScript" etc.

==Defining custom iterators==

Some objects represent collections of items that should be iterated over in a specific way.

* Iterating over a range object should return the numbers in that range one by one.
* The leaves in a tree can be visited using depth-first or breadth-first traversal.
* Iterating over an object representing the results from a database query should return rows one by one, even if the entire result set has not been loaded in to a single array.
* An iterator on an infinite mathematical sequence (such as the Fibonacci sequence) should be able to return results one by one without creating an infinite length data structure.

JavaScript lets you write code that represents custom iteration logic and link it to an object.

We'll create a simple <code>Range</code> object which stores a low and high value.

 function Range(low, high){
   this.low = low;
   this.high = high;
 }

Now we'll create a custom iterator that can return a sequence of inclusive integers from that range. The iterator interface requires that we provide a <code>next()</code> method which either returns an item from the sequence or throws a <code>StopIteration</code> exception.

 function RangeIterator(range){
   this.range = range;
   this.current = this.range.low;
 }
 RangeIterator.prototype.next = function(){
   if (this.current > this.range.high)
     throw StopIteration;
   else
     return this.current++;
 };

Our <code>RangeIterator</code> is instantiated with a range instance, and maintains its own <code>current</code> property to track how far along in the sequence it has got.

Finally, to associate our <code>RangeIterator</code> with the <code>Range</code> object we need to add a special <code>__iterator__</code> method to <code>Range</code>. This will be called when we attempt to iterate over a <code>Range</code> instance, and should return an instance of <code>RangeIterator</code>, which implements the iterator logic.

 Range.prototype.__iterator__ = function(){
   return new RangeIterator(this);
 };

Having hooked in our custom iterator, we can iterate over a range instance with the following:

 var range = new Range(3, 5);
 for (var i in range)
   print(i); // prints 3, then 4, then 5 in sequence

==Generators: a better way to build Iterators==

While custom iterators are a useful tool, their creation requires careful programming due to the need to explicitly maintain their internal state. Generators provide a powerful alternative: they allow you to define an iterative algorithm by writing a single function which can maintain its own state.

A generator is a special type of function that works as a factory for iterators. A function becomes a generator if it contains one or more <code>yield</code> expressions.


The <code>yield</code> keyword is only available to code blocks in HTML wrapped in a <code>script</code> element with attribute <code> type=&quot;application/javascript;version=1.7&quot;</code>  (or higher version). XUL script tags have access to these features without needing this special block.

When a generator function is called the body of the function does not execute straight away; instead, it returns a generator-iterator object. Each call to the generator-iterator's <code>next()</code> method will execute the body of the function up to the next <code>yield</code> expression and return its result. When either the end of the function or a <code>return</code> statement is reached, a <code>StopIteration</code> exception is thrown.

This is best illustrated with an example:

 function simpleGenerator(){
   yield "first";
   yield "second";
   yield "third";
   for (var i = 0; i < 3; i++)
     yield i;
 }
 
 var g = simpleGenerator();
 print(g.next()); // prints "first"
 print(g.next()); // prints "second"
 print(g.next()); // prints "third"
 print(g.next()); // prints 0
 print(g.next()); // prints 1
 print(g.next()); // prints 2
 print(g.next()); // StopIteration is thrown

A generator function can be used directly as the <code>__iterator__</code> method of a class, greatly reducing the amount of code needed to create custom iterators. Here is our <code>Range</code> rewritten to use a generator:

 function Range(low, high){
   this.low = low;
   this.high = high;
 }
 Range.prototype.__iterator__ = function(){
   for (var i = this.low; i <= this.high; i++)
     yield i;
 };
 var range = new Range(3, 5);
 for (var i in range)
   print(i); // prints 3, then 4, then 5 in sequence

Not all generators terminate; it is possible to create a generator that represents an infinite sequence. The following generator implements the Fibonacci sequence, where each element is the sum of the two previous elements:

 function fibonacci(){
   var fn1 = 1;
   var fn2 = 1;
   while (1){
     var current = fn2;
     fn2 = fn1;
     fn1 = fn1 + current;
     yield current;
   }
 }
 
 var sequence = fibonacci();
 print(sequence.next()); // 1
 print(sequence.next()); // 1
 print(sequence.next()); // 2
 print(sequence.next()); // 3
 print(sequence.next()); // 5
 print(sequence.next()); // 8
 print(sequence.next()); // 13

Generator functions can take arguments, which are bound the first time the function is called. Generators can be terminated (causing them to raise a <code>StopIteration</code> exception) using a <code>return</code> statement. The following <code>fibonacci()</code> variant takes an optional limit argument, and will terminate once that limit has been passed.

 function fibonacci(limit){
   var fn1 = 1;
   var fn2 = 1;
   while (1){
     var current = fn2;
     fn2 = fn1;
     fn1 = fn1 + current;
     if (limit && current > limit)
       return;
     yield current;
   }
 }

==Advanced generators==

Generators compute their yielded values on demand, which allows them to efficiently represent sequences that are expensive to compute, or even infinite sequences as demonstrated above.

In addition to the <code>next()</code> method, generator-iterator objects also have a <code>send()</code> method which can be used to modify the internal state of the generator. A value passed to <code>send()</code> will be treated as the result of the last <code>yield</code> expression that paused the generator. You must start a generator by calling <code>next()</code> at least once before you can use <code>send()</code> to pass in a specific value.

Here is the fibonacci generator using <code>send()</code> to restart the sequence:

 function fibonacci(){
   var fn1 = 1;
   var fn2 = 1;
   while (1){
     var current = fn2;
     fn2 = fn1;
     fn1 = fn1 + current;
     var reset = yield current;
     if (reset){
         fn1 = 1;
         fn2 = 1;
     }
   }
 }
 
 var sequence = fibonacci();
 print(sequence.next());     // 1
 print(sequence.next());     // 1
 print(sequence.next());     // 2
 print(sequence.next());     // 3
 print(sequence.next());     // 5
 print(sequence.next());     // 8
 print(sequence.next());     // 13
 print(sequence.send(true)); // 1
 print(sequence.next());     // 1
 print(sequence.next());     // 2
 print(sequence.next());     // 3

<div class="note">'''Note:''' As a point of interest, calling <code>send(undefined)</code> is equivalent to calling <code>next()</code>. However, starting a newborn generator with any value other than undefined when calling <code>send()</code> will result in a <code>TypeError</code> exception.</div>

You can force a generator to throw an exception by calling its <code>throw()</code> method and passing the exception value it should throw. This exception will be thrown from the current suspended context of the generator, as if the <code>yield</code> that is currently suspended were instead a <code>throw ''value''</code> statement.

If a yield is not encountered during the processing of the thrown exception, then the exception will propagate up through the call to <code>throw()</code>, and subsequent calls to <code>next()</code> will result in <code>StopIteration</code> being thrown.

Generators have a <code>close()</code> method that forces the generator to close itself. The effects of closing a generator are:

# Any <code>finally</code> clauses active in the generator function are run.
# If a <code>finally</code> clause throws any exception other than <code>StopIteration</code>, the exception is propagated to the caller of the <code>close()</code> method.
# The generator terminates.

==Generator expressions==

{{Note|Introduced in JavaScript 1.8}}

A significant drawback of [[/guides/js/objects#Array_comprehensions|array comprehensions]] is that they cause an entire new array to be constructed in memory. When the input to the comprehension is itself a small array the overhead involved is insignificant &mdash; but when the input is a large array or an expensive (or indeed infinite) generator the creation of a new array can be problematic.

Generators enable lazy computation of sequences, with items calculated on-demand as they are needed. ''Generator expressions'' are syntactically almost identical to array comprehensions &mdash; they use parenthesis instead of braces (and <code>for...in</code> instead of <code>for each...in</code>) &mdash; but instead of building an array they create a generator that can execute lazily. You can think of them as short hand syntax for creating generators.

Suppose we have an iterator <code>it</code> which iterates over a large sequence of integers. We want to create a new iterator that will iterate over their doubles. An array comprehension would create a full array in memory containing the doubled values:

 var doubles = [i * 2 for (i in it)];

A generator expression on the other hand would create a new iterator which would create doubled values on demand as they were needed:

 var it2 = (i * 2 for (i in it));
 print(it2.next()); // The first value from it, doubled
 print(it2.next()); // The second value from it, doubled

When a generator expression is used as the argument to a function, the parenthesis used for the function call means that the outer parenthesis can be omitted:

 var result = doSomething(i * 2 for (i in it));

<span style="float: left">[[/guides/js/inheritance|&laquo; Previous]]</span>[[/guides/JavaScript/Closures|Next &raquo]]

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
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Iterators_and_Generators
|MSDN_link=
|HTML5Rocks_link=
}}