{{Flags}}
{{Summary_Section|JavaScript is designed on a simple object-based paradigm. An object is a collection of properties, and a property is association between a name and a value. A value of property can be a function, which is then known as the object's method. In addition to objects that are predefined in the browser, you can define your own objects.

This chapter describes how to use objects, properties, functions, and methods, and how to create your own objects.
}}
{{Guide
|Content=<h2 id="Objects_overview">Objects overview</h2>
<p>Objects in JavaScript, just as many other programming languages, can be compared to objects in real life. The concept of objects in JavaScript can be understood with real life, tangible objects.</p>
<p>In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup for example. A cup is an object, with properties. A cup has a colour, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.</p>
<h2 id="Objects_and_properties">Objects and properties</h2>
<p>A JavaScript object has properties associated with it. A property of an object can be explained as variables that are attached to the object. Object properties are basically the same with ordinary JavaScript variables, except for the attachment to objects. The properties of an object define the characteristics of the object. You access the properties of an object with a simple dot-notation:</p>
<div style="margin-right: 270px;">
  <pre class="brush: js">objectName.propertyName
</pre>
</div>
<p>Like all JavaScript variables, both the object name (which could be a normal variable) and property name are case sensitive. You define a property by assigning it a value. For example, let's create an object named <code>myCar</code> and give it properties named <code>make</code>, <code>model</code>, and <code>year</code> as follows:</p>
<pre class="brush: js">var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";
myCar.year = 1969;
</pre>
<p>Properties of JavaScript objects can also be accessed or set using a bracket notation. Objects are sometimes called <em>associative arrays</em>, since each property is associated with a string value that can be used to access it. So, for example, you could access the properties of the <code>myCar</code> object as follows:</p>
<pre class="brush: js">myCar["make"] = "Ford";
myCar["model"] = "Mustang";
myCar["year"] = 1969;
</pre>
<p>Object properties names can be valid JavaScript string, or anything that can be converted to string, including the empty string. However, any property name that is not a valid JavaScript identifier (for example, a property name that has space or dash, or starts with a number) can only be accessed using the square bracket notation. This notation is also very useful when property names are to be dynamically determined (when the property name is not determined until runtime). Examples are as follows:</p>
<pre class="brush: js">var myObj = new Object(),
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
</pre>
<p>You can also access properties by using a string value that is stored in a variable:</p>
<div style="width: auto;">
  <pre class="brush: js">var propertyName = "make";
myCar[propertyName] = "Ford";

propertyName = "model";
myCar[propertyName] = "Mustang";
</pre>
</div>
<p>You can use the bracket notation with <a class="internal" href="/en-US/docs/JavaScript/Guide/Statements#for...in_Statement" title="en-US/docs/JavaScript/Guide/Statements#for...in Statement">for...in</a> to iterate over all the enumerable properties of an object. To illustrate how this works, the following function displays the properties of the object when you pass the object and the object's name as arguments to the function:</p>
<pre class="brush: js">function showProps(obj, objName) {
  var result = "";
  for (var i in obj)
    result += objName + "." + i + " = " + obj[i] + "\n";
  return result;
}
</pre>
<p>So, the function call <code>showProps(myCar, "myCar")</code> would return the following:</p>
<pre>myCar.make = Ford
myCar.model = Mustang
myCar.year = 1969</pre>
<h2 id="Object_everything">Object everything</h2>
<p>In JavaScript, almost everything is an object. All primitive types except <code>null</code> and <code>undefined</code> are treated as objects. They can be assigned properties (assigned properties of some types are not persistent), and they have all characteristics of objects.</p>
<h2 id="Enumerating_all_properties_of_an_object">Enumerating all properties of an object</h2>
<p>Starting with <a href="/en-US/docs/JavaScript/ECMAScript_5_support_in_Mozilla" title="en-US/docs/JavaScript/ECMAScript 5 support in Mozilla">ECMAScript 5</a>, there are three native ways to list/traverse object properties:</p>
<ul>
  <li><a href="/en-US/docs/JavaScript/Reference/Statements/for...in" title="en-US/docs/JavaScript/Reference/Statements/for...in">for...in</a> loops<br>
    This method traverses all enumerable properties of an object and its prototype chain</li>
  <li><a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/keys" title="en-US/docs/JavaScript/Reference/Global Objects/Object/keys">Object.keys(o)</a><br>
    This method returns an array with all the own (not in the prototype chain) enumerable properties names ("keys") of an object <code>o</code>.</li>
  <li><a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/getOwnPropertyNames" title="en-US/docs/JavaScript/Reference/Global Objects/Object/getOwnPropertyNames">Object.getOwnPropertyNames(o)</a><br>
    This method returns an array containing all own properties names (enumerable or not) of an object <code>o</code>.</li>
</ul>
<p>In ECMAScript 5, there is no native way to list all properties of an object. However, this can be achieved with the following function:</p>
<pre class="brush: js">function listAllProperties(o){     
	var objectToInspect;     
	var result = [];
	
	for(objectToInspect = o; objectToInspect !== null; objectToInspect = Object.getPrototypeOf(objectToInspect)){  
		result = result.concat(Object.getOwnPropertyNames(objectToInspect));  
	}
	
	return result; 
}
</pre>
<p>This can be useful to reveal "hidden" properties (properties in the prototype chain which are not accessible through the object, because another property has the same name earlier in the prototype chain). Listing accessible properties only can easily be done by removing duplicates in the array.</p>
<h2 id="Creating_new_objects">Creating new objects</h2>
<p>JavaScript has a number of predefined objects. In addition, you can create your own objects. In JavaScript 1.2 and later, you can create an object using an object initializer. Alternatively, you can first create a constructor function and then instantiate an object using that function and the <code>new</code> operator.</p>
<h3 id="Using_object_initializers">Using object initializers</h3>
<p>In addition to creating objects using a constructor function, you can create objects using an object initializer. Using object initializers is sometimes referred to as creating objects with literal notation. "Object initializer" is consistent with the terminology used by C++.</p>
<p>The syntax for an object using an object initializer is:</p>
<pre class="brush: js">var obj = { property_1:   value_1,   // property_# may be an identifier...
            2:            value_2,   // or a number...
            // ...,
            "property n": value_n }; // or a string
</pre>
<p>where <code>obj</code> is the name of the new object, each <code>property_<em>i</em></code> is an identifier (either a name, a number, or a string literal), and each <code>value_<em>i</em></code> is an expression whose value is assigned to the <code>property_<em>i</em></code>. The <code>obj</code> and assignment is optional; if you do not need to refer to this object elsewhere, you do not need to assign it to a variable. (Note that you may need to wrap the object literal in parentheses if the object appears where a statement is expected, so as not to have the literal be confused with a block statement.)</p>
<p>If an object is created with an object initializer in a top-level script, JavaScript interprets the object each time it evaluates an expression containing the object literal. In addition, an initializer used in a function is created each time the function is called.</p>
<p>The following statement creates an object and assigns it to the variable <code>x</code> if and only if the expression <code>cond</code> is true.</p>
<pre class="brush: js">if (cond) var x = {hi: "there"};
</pre>
<p>The following example creates <code>myHonda</code> with three properties. Note that the <code>engine</code> property is also an object with its own properties.</p>
<pre class="brush: js">var myHonda = {color: "red", wheels: 4, engine: {cylinders: 4, size: 2.2}};
</pre>
<p>You can also use object initializers to create arrays. See <a href="Values%2C_variables%2C_and_literals#Array_literals">array literals</a>.</p>
<p>In JavaScript 1.1 and earlier, you cannot use object initializers. You can create objects only using their constructor functions or using a function supplied by some other object for that purpose. See <a href="#Using_a_constructor_function">Using a constructor function</a>.</p>
<h3 id="Using_a_constructor_function">Using a constructor function</h3>
<p>Alternatively, you can create an object with these two steps:</p>
<ol>
  <li>Define the object type by writing a constructor function. There is a strong convention, with good reason, to use a capital initial letter.</li>
  <li>Create an instance of the object with <code>new</code>.</li>
</ol>
<p>To define an object type, create a function for the object type that specifies its name, properties, and methods. For example, suppose you want to create an object type for cars. You want this type of object to be called <code>car</code>, and you want it to have properties for make, model, and year. To do this, you would write the following function:</p>
<pre class="brush: js">function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
</pre>
<p>Notice the use of <code>this</code> to assign values to the object's properties based on the values passed to the function.</p>
<p>Now you can create an object called <code>mycar</code> as follows:</p>
<pre class="brush: js">var mycar = new Car("Eagle", "Talon TSi", 1993);
</pre>
<p>This statement creates <code>mycar</code> and assigns it the specified values for its properties. Then the value of <code>mycar.make</code> is the string "Eagle", <code>mycar.year</code> is the integer 1993, and so on.</p>
<p>You can create any number of <code>car</code> objects by calls to <code>new</code>. For example,</p>
<pre class="brush: js">var kenscar = new Car("Nissan", "300ZX", 1992);
var vpgscar = new Car("Mazda", "Miata", 1990);
</pre>
<p>An object can have a property that is itself another object. For example, suppose you define an object called <code>person</code> as follows:</p>
<pre class="brush: js">function Person(name, age, sex) {
  this.name = name;
  this.age = age;
  this.sex = sex;
}
</pre>
<p>and then instantiate two new <code>person</code> objects as follows:</p>
<pre class="brush: js">var rand = new Person("Rand McKinnon", 33, "M");
var ken = new Person("Ken Jones", 39, "M");
</pre>
<p>Then, you can rewrite the definition of <code>car</code> to include an <code>owner</code> property that takes a <code>person</code> object, as follows:</p>
<pre class="brush: js">function Car(make, model, year, owner) {
  this.make = make;
  this.model = model;
  this.year = year;
  this.owner = owner;
}
</pre>
<p>To instantiate the new objects, you then use the following:</p>
<pre class="brush: js">var car1 = new Car("Eagle", "Talon TSi", 1993, rand);
var car2 = new Car("Nissan", "300ZX", 1992, ken);
</pre>
<p>Notice that instead of passing a literal string or integer value when creating the new objects, the above statements pass the objects <code>rand</code> and <code>ken</code> as the arguments for the owners. Then if you want to find out the name of the owner of car2, you can access the following property:</p>
<pre class="brush: js">car2.owner.name
</pre>
<p>Note that you can always add a property to a previously defined object. For example, the statement</p>
<pre class="brush: js">car1.color = "black";
</pre>
<p>adds a property <code>color</code> to car1, and assigns it a value of "black." However, this does not affect any other objects. To add the new property to all objects of the same type, you have to add the property to the definition of the <code>car</code> object type.</p>
<h3 id="Using_the_Object.create_method">Using the Object.create method</h3>
<p>Objects can also be created using the <code>Object.create</code> method. This method can be very useful, because it allows you to choose the prototype object for the object you want to create, without having to define a constructor function. For more detailed information on the method and how to use it, see <a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/create">Object.create method</a></p>
<h3 id="Inheritance">Inheritance</h3>
<p>All objects in JavaScript inherit from at least one other object. The object being inherited from is known as the prototype, and the inherited properties can be found in the <code>prototype</code> object of the constructor.</p>
<h3 id="Indexing_object_properties">Indexing object properties</h3>
<p>In JavaScript 1.0, you can refer to a property of an object either by its property name or by its ordinal index. In JavaScript 1.1 and later, however, if you initially define a property by its name, you must always refer to it by its name, and if you initially define a property by an index, you must always refer to it by its index.</p>
<p>This restriction applies when you create an object and its properties with a constructor function (as we did previously with the <code>Car</code> object type) and when you define individual properties explicitly (for example, <code>myCar.color = "red"</code>). If you initially define an object property with an index, such as <code>myCar[5] = "25 mpg"</code>, you can subsequently refer to the property only as <code>myCar[5]</code>.</p>
<p>The exception to this rule is objects reflected from HTML, such as the <code>forms</code> array. You can always refer to objects in these arrays by either their ordinal number (based on where they appear in the document) or their name (if defined). For example, if the second <code>&lt;FORM&gt;</code> tag in a document has a <code>NAME</code> attribute of "myForm", you can refer to the form as <code>document.forms[1]</code> or <code>document.forms["myForm"]</code> or <code>document.myForm</code>.</p>
<h3 id="Defining_properties_for_an_object_type">Defining properties for an object type</h3>
<p>You can add a property to a previously defined object type by using the <code>prototype</code> property. This defines a property that is shared by all objects of the specified type, rather than by just one instance of the object. The following code adds a <code>color</code> property to all objects of type <code>car</code>, and then assigns a value to the <code>color</code> property of the object <code>car1</code>.</p>
<pre class="brush: js">Car.prototype.color = null;
car1.color = "black";
</pre>
<p>See the <a href="/en-US/docs/JavaScript/Reference/Global_Objects/Function/prototype" title="en-US/docs/JavaScript/Reference/Global Objects/Function/prototype"><code>prototype</code> property</a> of the <code>Function</code> object in the <a href="/en-US/docs/JavaScript/Reference" title="en-US/docs/JavaScript/Reference">JavaScript Reference</a> for more information.</p>
<h3 id="Defining_methods">Defining methods</h3>
<p>A <em>method</em> is a function associated with an object, or, simply put, a method is a property of an object that is a function. Methods are defined the way normal functions are defined, except that they have to be assigned as the property of an object. Examples are:</p>
<pre class="brush: js">objectName.methodname = function_name;

var myObj = {
  myMethod: function(params) {
    // ...do something
  }
};
</pre>
<p>where <code>objectName</code> is an existing object, <code>methodname</code> is the name you are assigning to the method, and <code>function_name</code> is the name of the function.</p>
<p>You can then call the method in the context of the object as follows:</p>
<pre class="brush: js">object.methodname(params);
</pre>
<p>You can define methods for an object type by including a method definition in the object constructor function. For example, you could define a function that would format and display the properties of the previously-defined <code>car</code> objects; for example,</p>
<pre class="brush: js">function displayCar() {
  var result = "A Beautiful " + this.year + " " + this.make
    + " " + this.model;
  pretty_print(result);
}
</pre>
<p>where <code>pretty_print</code> is a function to display a horizontal rule and a string. Notice the use of <code>this</code> to refer to the object to which the method belongs.</p>
<p>You can make this function a method of <code>car</code> by adding the statement</p>
<pre class="brush: js">this.displayCar = displayCar;
</pre>
<p>to the object definition. So, the full definition of <code>car</code> would now look like</p>
<pre class="brush: js">function Car(make, model, year, owner) {
  this.make = make;
  this.model = model;
  this.year = year;
  this.owner = owner;
  this.displayCar = displayCar;
}
</pre>
<p>Then you can call the <code>displayCar</code> method for each of the objects as follows:</p>
<pre class="brush: js">car1.displayCar();
car2.displayCar();
</pre>
<p>This produces the output shown in the following figure.</p>
<p><img alt="Image:obja.gif" class="internal" src="/@api/deki/files/786/=Obja.gif"></p>
<p><small><strong>Figure 7.1: Displaying method output.</strong></small></p>
<h3 id="Using_this_for_object_references">Using <code>this</code> for object references</h3>
<p>JavaScript has a special keyword, <code>this</code>, that you can use within a method to refer to the current object. For example, suppose you have a function called <code>validate</code> that validates an object's <code>value</code> property, given the object and the high and low values:</p>
<pre class="brush: js">function validate(obj, lowval, hival) {
  if ((obj.value &lt; lowval) || (obj.value &gt; hival))
    alert("Invalid Value!");
}
</pre>
<p>Then, you could call <code>validate</code> in each form element's <code>onchange </code> event handler, using <code>this</code> to pass it the element, as in the following example:</p>
<pre class="brush: html">&lt;input type="text" name="age" size="3"
  onChange="validate(this, 18, 99)"&gt;
</pre>
<p>In general, <code>this</code> refers to the calling object in a method.</p>
<p>When combined with the <code>form</code> property, <code>this</code> can refer to the current object's parent form. In the following example, the form <code>myForm</code> contains a <code>Text</code> object and a button. When the user clicks the button, the value of the <code>Text</code> object is set to the form's name. The button's <code>onclick</code> event handler uses <code>this.form</code> to refer to the parent form, <code>myForm</code>.</p>
<pre class="brush: html">&lt;form name="myForm"&gt;
&lt;p&gt;&lt;label&gt;Form name:&lt;input type="text" name="text1" value="Beluga"&gt;&lt;/label&gt;
&lt;p&gt;&lt;input name="button1" type="button" value="Show Form Name"
     onclick="this.form.text1.value = this.form.name"&gt;
&lt;/p&gt;
&lt;/form&gt;</pre>
<h3 id="Defining_getters_and_setters">Defining getters and setters</h3>
<p>A <em>getter</em> is a method that gets the value of a specific property. A <em>setter</em> is a method that sets the value of a specific property. You can define getters and setters on any predefined core object or user-defined object that supports the addition of new properties. The syntax for defining getters and setters uses the object literal syntax.</p>
<p></p><div class="blockIndicator standardNote standardNoteBlock"> 
<p><a href="http://developer.mozilla.org/en-US/docs/JavaScript/New_in_JavaScript/1.8.1">JavaScript 1.8.1</a> note</p> 
<p style="font-weight: 400;">Starting in JavaScript 1.8.1, setters are no longer called when setting properties in object and array initializers.</p> 
</div><p></p>
<p>The following <a href="/en-US/docs/SpiderMonkey/Introduction_to_the_JavaScript_shell" title="en-US/docs/SpiderMonkey/Introduction to the JavaScript shell">JS shell</a> session illustrates how getters and setters could work for a user-defined object <code>o</code>. The JS shell is an application that allows developers to test JavaScript code in batch mode or interactively.</p>
<pre class="brush: js">js&gt; var o = {a: 7, get b() {return this.a + 1;}, set c(x) {this.a = x / 2}};
[object Object]
js&gt; o.a;
7
js&gt; o.b;
8
js&gt; o.c = 50;
js&gt; o.a;
25
</pre>
<p>The <code>o</code> object's properties are:</p>
<ul>
  <li><code>o.a</code> — a number</li>
  <li><code>o.b</code> — a getter that returns <code>o.a</code> plus 1</li>
  <li><code>o.c</code> — a setter that sets the value of <code>o.a</code> to half of the value <code>o.c</code> is being set to</li>
</ul>
<p>Please note that function names of getters and setters defined in an object literal using "[gs]et <em>property</em>()" (as opposed to <code>__define[GS]etter__</code> below) are not the names of the getters themselves, even though the <code>[gs]et <em>propertyName</em>(){ }</code> syntax may mislead you to think otherwise. To name a function in a getter or setter using the "[gs]et <em>property</em>()" syntax, define an explicitly named function programmatically using <code><a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/defineProperty" title="en-US/docs/Core JavaScript 1.5 Reference/Global
Objects/Object/defineProperty">Object.defineProperty</a></code> (or the <code><a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/defineGetter" title="en-US/docs/Core JavaScript 1.5 Reference/Global
Objects/Object/defineGetter">Object.prototype.__defineGetter__</a></code> legacy fallback).</p>
<p>This JavaScript shell session illustrates how getters and setters can extend the <code>Date</code> prototype to add a <code>year</code> property to all instances of the predefined <code>Date</code> class. It uses the <code>Date</code> class's existing <code>getFullYear</code> and <code>setFullYear</code> methods to support the <code>year</code> property's getter and setter.</p>
<p>These statements define a getter and setter for the year property:</p>
<pre class="brush: js">js&gt; var d = Date.prototype;
js&gt; d.__defineGetter__("year", function() { return this.getFullYear(); });
js&gt; d.__defineSetter__("year", function(y) { this.setFullYear(y); });
</pre>
<p>These statements use the getter and setter in a <code>Date</code> object:</p>
<pre class="brush: js">js&gt; var now = new Date;
js&gt; print(now.year);
2000
js&gt; now.year = 2001;
987617605170
js&gt; print(now);
Wed Apr 18 11:13:25 GMT-0700 (Pacific Daylight Time) 2001
</pre>
<h4 id="Obsolete_syntaxes">Obsolete syntaxes</h4>
<p>In the past, JavaScript supported several other syntaxes for defining getters and setters. None of these syntaxes were supported by other engines, and support has been removed in recent versions of JavaScript. See <a class="external" href="http://whereswalden.com/2010/04/16/more-spidermonkey-changes-ancient-esoteric-very-rarely-used-syntax-for-creating-getters-and-setters-is-being-removed/" title="http://whereswalden.com/2010/04/16/more-spidermonkey-changes-ancient-esoteric-very-rarely-used-syntax-for-creating-getters-and-setters-is-being-removed/">this dissection of the removed syntaxes</a> for further details on what was removed and how to adapt to those removals.</p>
<h4 id="Summary">Summary</h4>
<p>In principle, getters and setters can be either</p>
<ul>
  <li>defined using <a href="#Using_object_initializers">object initializers</a>, or</li>
  <li>added later to any object at any time using a getter or setter adding method.</li>
</ul>
<p>When defining getters and setters using <a href="#Using_object_initializers">object initializers</a> all you need to do is to prefix a getter method with <code>get</code> and a setter method with <code>set</code>. Of course, the getter method must not expect a parameter, while the setter method expects exactly one parameter (the new value to set). For instance:</p>
<pre class="brush: js">var o = {
  a: 7,
  <strong>get</strong> b() { return this.a + 1; },
  <strong>set</strong> c(x) { this.a = x / 2; }
};
</pre>
<p>Getters and setters can also be added to an object at any time after creation using two special methods called <code>__defineGetter__</code> and <code>__defineSetter__</code>. Both methods expect the name of the getter or setter as their first parameter, in the form of a string. The second parameter is the function to call as the getter or setter. For instance (following the previous example):</p>
<pre class="brush: js">o.__defineGetter__("b", function() { return this.a + 1; });
o.__defineSetter__("c", function(x) { this.a = x / 2; });
</pre>
<p>Which of the two forms to choose depends on your programming style and task at hand. If you already go for the object initializer when defining a prototype you will probably most of the time choose the first form. This form is more compact and natural. However, if you need to add getters and setters later — because you did not write the prototype or particular object — then the second form is the only possible form. The second form probably best represents the dynamic nature of JavaScript — but it can make the code hard to read and understand.</p>
<div class="tip">
  <p>Prior to Firefox 3.0, getter and setter are not supported for DOM Elements. Older versions of Firefox silently fail. If exceptions are needed for those, changing the prototype of HTMLElement <code>(HTMLElement.prototype.__define[SG]etter__)</code> and throwing an exception is a workaround.</p>
  With Firefox 3.0, defining getter or setter on an already-defined property will throw an exception. The property must be deleted beforehand, which is not the case for older versions of Firefox.</div>
<h4 id="See_also">See also</h4>
<ul>
  <li><code><a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/defineGetter" title="en-US/docs/JavaScript/Reference/Global_Objects/Object/defineGetter">__defineGetter__</a></code></li>
  <li><code><a href="/en-US/docs/JavaScript/Reference/Global_Objects/Object/defineSetter" title="en-US/docs/JavaScript/Reference/Global_Objects/Object/defineSetter">__defineSetter__</a></code></li>
  <li><code><a href="/en-US/docs/JavaScript/Reference/Operators/get" title="en-US/docs/JavaScript/Reference/Operators/Special Operators/get Operator">get</a></code></li>
  <li><code><a href="/en-US/docs/JavaScript/Reference/Operators/set" title="en-US/docs/JavaScript/Reference/Operators/Special Operators/set Operator">set</a></code></li>
</ul>
<h3 id="Deleting_properties">Deleting properties</h3>
<p>You can remove a property by using the <code>delete</code> operator. The following code shows how to remove a property.</p>
<pre class="brush: js">//Creates a new object, myobj, with two properties, a and b.
var myobj = new Object;
myobj.a = 5;
myobj.b = 12;

//Removes the a property, leaving myobj with only the b property.
delete myobj.a;
</pre>
<p>You can also use <code>delete</code> to delete a global variable if the <code>var</code> keyword was not used to declare the variable:</p>
<pre class="brush: js">g = 17;
delete g;
</pre>
<p>See <code><a href="Expressions_and_operators#delete">delete</a></code> for more information.</p>
<h2 id="See_also">See also</h2>
<ul>
  <li><a class="external" href="http://es5.github.com/#x4.2" title="http://es5.github.com/#x4.2">ECMAScript 5.1 spec: Language Overview</a></li>
  <li><a class="external" href="http://dmitrysoshnikov.com/ecmascript/javascript-the-core" title="http://dmitrysoshnikov.com/ecmascript/javascript-the-core">JavaScript. The core. (Dmitry A. Soshnikov ECMA-262 article series)</a></li>
</ul>
<div>
  <p style="text-align: right;"><span style="float: left;"><a href="/en-US/docs/JavaScript/Guide/Functions" title="Functions">« Previous</a></span><a href="/en-US/docs/JavaScript/Guide/Predefined_Core_Objects" title="Predefined Core Objects">Next »</a></p></div>
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Working_with_Objects
|MSDN_link=
|HTML5Rocks_link=
}}