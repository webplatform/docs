{{Note | Please note that this document is currently under development, if you have anything to add please use the Comments to share.''
}}
=== Next Release ===
ECMAScript 6 is the next draft version of the standard, code-named '''"Harmony"''' or '''"ES.next"'''. Draft 9 was released July 8, 2012.

=== Syntax ===
There has been a wide range of changes in regards to syntax, below are some examples of syntax additions and changes.

==== let ====
Let and const are new ways to declare variables, firstly <code>let</code> is exactly the same as <code>var</code> apart from it bounds the declared variable to the inner-most scope. example:

  //Testing var scope
  function scope()
  {
    for(var i = 0; i != 10; i++)
    {
       //(i) is available here
    }
    //(i) is also available here
  }

  //Testing let scope
  function scope()
  {
    for(let i = 0; i != 10; i++)
    {
       //(i) is available here
    }
    //(i) is *not* available here!
  }

This may not seem like a huge change but it's actually a much needed feature.
An example of ES3/5 would be:

  for(var i = 0; i < 10; i++)
  {
     setTimeout(function(){
       alert(i);
     }, 20);
  }

The above statement will alert the number 10, ten times. this is because the loop iterations finish before the execution of the time-out, so the value of <code>i</code> will be the last possible value in the loop.

Using <code>let</code> allows you to scope the variable to the '''current''' iteration scope, meaning that the example below act's like your creating an anonymous function for every iteration.

  for(let i = 0; i < 10; i++)
  {
     let k = i;
     setTimeout(function(){
       alert(k);
     });
  }

==== const ====
<code>const</code> is similar to <code>let</code> and <code>var</code> apart from the variable is marked as read-only.

==== for..of ====
<code>for(x of y)</code> loops allow you to iterate over arrays in the same way you iterate over object's key. an example usage would be:

  let array = [0,2,4,8,16,32,64];
  for(num of array)
  {
  }

=== Features ===
TODO: List some of the EMCAScript 6 features such as Syntax, Structures and Library implementations

=== Concepts ===
Describe concepts such as Classes, Private Names, Inheritance and Abstraction.

==References==
<references />