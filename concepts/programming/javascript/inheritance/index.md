{{Page_Title|Inheritance revisited}}
{{Flags
}}
{{Byline}}
{{Summary_Section|Inheritance has always been available in JavaScript, but the examples on this page use some methods introduced in ECMAScript 5.}}
{{Tutorial
|Content===Example==

<code>B</code> shall inherit from <code>A</code><nowiki>:</nowiki>

 function A(a){
   this.varA = a;
 }
 A.prototype = {
   varA : null,
   doSomething : function(){
     // ...
   }
 }
 function B(a, b){
   A.call(this, a);
   this.varB = b;
 }
 B.prototype = Object.create(A.prototype, {
   varB : { value: null, enumerable: true, configurable: true, writable: true },
   doSomething : { value: function(){ // override
        A.prototype.doSomething.apply(this, arguments); // call super
        // ...
     }, enumerable: true, configurable: true, writable: true }
 })
 
 var b = new B();
 b.doSomething();

The important parts are:

* Types are defined in <code>.prototype</code>
* You use <code>Object.create()</code> to inherit

==<code>prototype</code> and Object.getPrototypeOf==

JavaScript is a bit confusing for developers coming from Java or C++, as it's all dynamic, all runtime, and it has no classes at all. It's all just instances (objects). Even the "classes" we simulate are just a function object.

You probably already noticed that our <code>function A</code> has a special property called <code>prototype</code>. This special property works with the JavaScript <code>new </code>operator. The reference to the prototype object is copied to the internal <code><nowiki>[[Prototype]]</nowiki></code> property of the new instance. For example, when you do <code>var a1 = new A()</code>, JavaScript (after creating the object in memory and before running function <code>A()</code> with <code>this</code> defined to it) sets <code><nowiki>a1.[[Prototype]] = A.prototype</nowiki></code>. When you then access properties of the instance, JavaScript first checks whether they exist on that object directly, and if not, it looks in <code><nowiki>[[Prototype]]</nowiki></code>. This means that all the stuff you define in <code>prototype</code> is effectively shared by all instances, and you can even later change parts of <code>prototype</code> and have the changes appear in all existing instances, if you wanted to.

If, in the example above, you do <code>var a1 = new A(); var a2 = new A();</code> then <code>a1.doSomething</code> would actually refer to <code>Object.getPrototypeOf(a1).doSomething</code>, which is the same as the <code>A.prototype.doSomething</code> you defined, i.e. <code>Object.getPrototypeOf(a1).doSomething == Object.getPrototypeOf(a2).doSomething == A.prototype.doSomething</code>.

In short, <code>prototype</code> is for types, while <code>Object.getPrototypeOf()</code> is the same for instances.

<code><nowiki>[[Prototype]]</nowiki></code> is looked at ''recursively'', i.e. <code>a1.doSomething</code>, <code>Object.getPrototypeOf(a1).doSomething</code>, <code>Object.getPrototypeOf(Object.getPrototypeOf(a1)).doSomething</code> etc., until it's found or <code>Object.getPrototypeOf </code>returns null.

So, when you call

 var o = new Foo();

JavaScript actually just does

 <nowiki>var o = new Object();
 o.[[Prototype]] = Foo.prototype;
 o.Foo();</nowiki>

(or something like that) and when you later do

 o.someProp;

it checks whether <code>o</code> has a property <code>someProp</code>. If not it checks <code>Object.getPrototypeOf(o).someProp</code> and if that doesn't exist it checks <code>Object.getPrototypeOf(Object.getPrototypeOf(o)).someProp</code> and so on.

<div>

<span style="float: left">[http://docs.webplatform.org/en-US/docs/JavaScript/Guide/Details_of_the_Object_Model &laquo; Previous]</span>[http://docs.webplatform.org/en-US/docs/JavaScript/Guide/Iterators_and_Generators Next &raquo;]

</div>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript, Inheritance}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Inheritance_Revisited
|MSDN_link=
|HTML5Rocks_link=
}}