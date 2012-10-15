{{Flags}}
{{Summary_Section|This chapter discusses values that JavaScript recognizes and describes the fundamental building blocks of JavaScript expressions: variables, constants, and literals.}}
<h2 id="Values">Values</h2>
<p>JavaScript recognizes the following '''primitive''' types of values:</p>
<ul>
  <li>[[/js/data-types/number|Numbers]], such as 42 or 3.14159</li>
  <li>[[/js/data-types/boolean|Logical (Boolean)]] values, either <code>true</code> or <code>false</code></li>
  <li>[[/js/data-types/string|Strings]], such as "Howdy!"</li>
  <li><code>null</code>, a special keyword denoting a null value. Because JavaScript is case-sensitive, <code>null</code> is not the same as <code>Null</code>, <code>NULL</code>, or any other variant</li>
  <li><code>[[/js/objects/undefined|undefined]]</code>, a top-level property whose value is undefined.</li>
</ul>
<p>This relatively small set of types of values, or <em>data types</em>, enables you to perform useful functions with your applications. There is no explicit distinction between integer and real-valued numbers. Nor is there an explicit date data type in JavaScript. However, you can use the <code>[[/js/objects/Date|Date]]</code> object and its methods to handle dates.</p>
<p>[[/js/objects/Object|Objects]] and [[/js/objects/Function|functions]] are the other fundamental elements in the language. You can think of objects as named containers for values, and functions as procedures that your application can perform.</p>
<h3 id="Data_type_conversion">Data type conversion</h3>
<p>JavaScript is a dynamically typed language. That means you do not have to specify the data type of a variable when you declare it, and data types are converted automatically as needed during script execution. So, for example, you could define a variable as follows:</p>
<div style="overflow:hidden;">
  <syntaxhighlight lang="JavaScript>
var answer = 42;
</syntaxhighlight>
</div>
<p>And later, you could assign the same variable a string value, for example:</p>
<div style="overflow:hidden;">
  <pre class="brush: js">
answer = "Thanks for all the fish...";
</pre>
</div>
<p>Because JavaScript is dynamically typed, this assignment does not cause an error message.</p>
<p>In expressions involving numeric and string values with the + operator, JavaScript converts numeric values to strings. For example, consider the following statements:</p>
<pre class="brush: js">
x = "The answer is " + 42 // returns "The answer is 42"
y = 42 + " is the answer" // returns "42 is the answer"
</pre>
<p>In statements involving other operators, JavaScript does not convert numeric values to strings. For example:</p>
<pre class="brush: js">
"37" - 7 // returns 30
"37" + 7 // returns "377"
</pre>
<h3 id="Converting_strings_to_numbers">Converting strings to numbers</h3>
<p>In the case that a value representing a number is in memory as a string, there are methods for conversion.</p>
<h4 id="parseInt()_and_parseFloat()"><code>parseInt()</code> and <code>parseFloat()</code></h4>
<p>See: <code>[[/js/functions/parseInt|parseInt()]]</code> and <code>[[/js/functions/parseFloat|parseFloat()]]</code> pages.</p>
<p><code>parseInt</code> will only return whole numbers, so its use is diminished for decimals. Additionally, a best practice for <code>parseInt</code> is to always include the radix parameter. That's because of strings with leading zeroes (like <code>parseInt('016')</code>) which will be treated as octal numbers by default.</p>
<h4 id="Plus_operator">Plus operator</h4>
<p>An alternative method of retrieving a number from a string is with the <code>+</code> operator.</p>
<pre class="brush: js">
"1.1" + "1.1" = "1.11.1"
(+"1.1") + (+"1.1") = 2.2   // Note: the parentheses are added for clarity, not required.</pre>
<p>The pitfall here is when trying to convert a string <code>'1 some'</code> to a number using plus operator result in a <code>NaN</code> while <code>parseInt</code> is working correctly.</p>
<h2 id="Variables">Variables</h2>
<p>You use variables as symbolic names for values in your application. The names of variables, called <em>identifiers</em>, conform to certain rules.</p>
<p>A JavaScript identifier must start with a letter, underscore (_), or dollar sign ($); subsequent characters can also be digits (0-9). Because JavaScript is case sensitive, letters include the characters "A" through "Z" (uppercase) and the characters "a" through "z" (lowercase).</p>
<p>Starting with JavaScript 1.5, you can use ISO 8859-1 or Unicode letters such as å and ü in identifiers. You can also use the \uXXXX [[#Unicode escape sequences|Unicode escape sequences]] as characters in identifiers.</p>
<p>Some examples of legal names are <code>Number_hits</code>, <code>temp99</code>, and <code>_name</code>.</p>
<h3 id="Declaring_variables">Declaring variables</h3>
<p>You can declare a variable in two ways:</p>
<ul>
  <li>With the keyword [[/js/statements/var|var]]. For example, <code>var x = 42</code>. This syntax can be used to declare both [[#Variable_Scope|local and global]] variables.</li>
  <li>By simply assigning it a value. For example, <code>x = 42</code>. This always declares a [[#Global_Variables|global variable]] and generates a strict JavaScript warning. You shouldn't use this variant.</li>
</ul>
<h3 id="Evaluating_variables">Evaluating variables</h3>
<p>A variable declared using the <code>var</code> statement with no initial value specified has the value <code>[[/js/objects/undefined|undefined]]</code>.</p>
<p>An attempt to access an undeclared variable will result in a <code>ReferenceError</code> exception being thrown:</p>
<pre class="brush: js">
var a;
console.log("The value of a is " + a); // prints "The value of a is undefined"
console.log("The value of b is " + b); // throws ReferenceError exception
</pre>
<p>You can use <code>undefined</code> to determine whether a variable has a value. In the following code, the variable <code>input</code> is not assigned a value, and the <code>[[/js/statements/if...else|if]]</code> statement evaluates to <code>true</code>.</p>
<pre class="brush: js">
var input;
if(input === undefined){
  doThis();
} else {
  doThat();
}
</pre>
<p><span class="comment">The following is related to "Variables" section as potential values in assignment.</span></p>
<p>The <code>undefined</code> value behaves as <code>false</code> when used in a boolean context. For example, the following code executes the function <code>myFunction</code> because the <code>myArray</code> element is not defined:</p>
<pre class="brush: js">
var myArray = new Array();
if (!myArray[0]) myFunction(); 
</pre>
<p>The <code>undefined</code> value converts to <code>NaN</code> when used in numeric context.</p>
<pre class="brush: js">
var a;
a + 2 = NaN</pre>
<p>When you evaluate a null variable, the null value behaves as 0 in numeric contexts and as false in boolean contexts. For example:</p>
<pre class="brush: js">
var n = null;
console.log(n * 32); // prints 0
</pre>
<h3 id="Variable_scope">Variable scope</h3>
<p>When you declare a variable outside of any function, it is called a <em>global</em> variable, because it is available to any other code in the current document. When you declare a variable within a function, it is called a <em>local</em> variable, because it is available only within that function.</p>
<p>JavaScript does not have [[/js/guide/Statements#Block_Statement|block statement]] scope; rather, it will be local to the code that the block resides within. For example the following code will log <code>5</code>, because the scope of <code>x</code> is the function (or global context) within which <code>x</code> is declared, not the block, which in this case is an <code>if</code> statement.</p>
<pre class="brush: js">
if (true) {
  var x = 5;
}
console.log(x);
</pre>
<p>Another unusual thing about variables in JavaScript is that you can refer to a variable declared later, without getting an exception. This concept is known as hoisting; variables in JavaScript are in a sense "hoisted" or lifted to the top of the function or statement. However, variables that aren't initialized yet will return a value of <code>undefined</code>.</p>
<pre class="brush: js">
/**
 * Example 1
 */
console.log(x === undefined); // logs "true"
var x = 3;


/**
 * Example 2
 */
// will return a value of undefined
var myvar = "my value";

(function() {
  console.log(myvar); // undefined
  var myvar = "local value";
})();
</pre>
<p>Example 2, above, will be interpreted the same as:</p>
<pre class="brush: js">
var myvar = "my value";

(function() {
  var myvar;
  console.log(myvar); // undefined
  myvar = "local value";
})();</pre>
<p>Because of hoisting, all <code>var</code> statements in a function should be placed as near to the top of the function as possible. This best practice increases the clarity of the code.</p>
<h3 id="Global_variables">Global variables</h3>
<p><span class="comment">need links to pages discussing scope chains and the global object</span> Global variables are in fact properties of the <em>global object</em>. In web pages the global object is <code>[[/dom/window|window]]</code>, so you can set and access global variables using the <code>window.<em>variable</em></code> syntax.</p>
<p>Consequently, you can access global variables declared in one window or frame from another window or frame by specifying the window or frame name. For example, if a variable called <code>phoneNumber</code> is declared in a <code>FRAMESET</code> document, you can refer to this variable from a child frame as <code>parent.phoneNumber</code>.</p>
<h2 id="Constants">Constants</h2>
<p>You can create a read-only, named constant with the <code>[[/js/statements/const|const]]</code> keyword. The syntax of a constant identifier is the same as for a variable identifier: it must start with a letter or underscore and can contain alphabetic, numeric, or underscore characters.</p>
<pre class="brush: js">
const prefix = '212';
</pre>
<p>A constant cannot change value through assignment or be re-declared while the script is running.</p>
<p>The scope rules for constants are the same as those for variables, except that the <code>const</code> keyword is always required, even for global constants. If the keyword is omitted, the identifier is assumed to represent a variable.</p>
<p>You cannot declare a constant with the same name as a function or variable in the same scope. For example:</p>
<pre class="brush: js">
// THIS WILL CAUSE AN ERROR
function f() {};
const f = 5;

// THIS WILL CAUSE AN ERROR ALSO
function f() {
  const g = 5;
  var g;

  //statements
}
</pre>
<h2 id="Literals">Literals</h2>
<p>You use literals to represent values in JavaScript. These are fixed values, not variables, that you <em>literally</em> provide in your script. This section describes the following types of literals:</p>

* [[#Array_literals|Array literals]]
* [[#Boolean literals|Boolean literals]]
* [[#Floating-point literals|Floating-point literals]]
* [[#Integers"|Integers]]
* [[#Object literals|Object literals]]
* [[#String literals|String literals]]

<h3 id="Array_literals">Array literals</h3>
<p>An array literal is a list of zero or more expressions, each of which represents an array element, enclosed in square brackets ([]). When you create an array using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified.</p>
<p>The following example creates the <code>coffees</code> array with three elements and a length of three:</p>
<pre class="brush: js">
var coffees = ["French Roast", "Colombian", "Kona"];
</pre>
<p><strong>Note</strong> An array literal is a type of object initializer. See [[/js/guide/About_objects#Using_Object_Initializers|Using Object Initializers]].</p>
<p>If an array is created using a literal in a top-level script, JavaScript interprets the array each time it evaluates the expression containing the array literal. In addition, a literal used in a function is created each time the function is called.</p>
<p>Array literals are also <code>Array</code> objects. See [[/js/guide/About_predefined_core_objects#Array_Object|Array Object]] for details on <code>Array</code> objects.</p>
<h4 id="Extra_commas_in_array_literals">Extra commas in array literals</h4>
<p>You do not have to specify all elements in an array literal. If you put two commas in a row, the array is created with <code>undefined</code> for the unspecified elements. The following example creates the <code>fish</code> array:</p>
<pre class="brush: js">
var fish = ["Lion", , "Angel"];
</pre>
<p>This array has two elements with values and one empty element (<code>fish[0]</code> is "Lion", <code>fish[1]</code> is <code>undefined</code>, and <code>fish[2]</code> is "Angel").</p>
<p>If you include a trailing comma at the end of the list of elements, the comma is ignored. In the following example, the length of the array is three. There is no <code>myList[3]</code>. All other commas in the list indicate a new element. (<strong>Note</strong> trailing commas can create errors in older browser versions and it is a best practice to remove them)</p>
<pre class="brush: js">
var myList = ['home', , 'school', ];
</pre>
<p>In the following example, the length of the array is four, and <code>myList[0]</code> and <code>myList[2]</code> are missing.</p>
<pre class="brush: js">
var myList = [ , 'home', , 'school'];
</pre>
<p>In the following example, the length of the array is four, and <code>myList[1]</code> and <code>myList[3]</code> are missing. Only the last comma is ignored.</p>
<pre class="brush: js">
var myList = ['home', , 'school', , ];
</pre>
<p>Understanding the behavior of extra commas is important to understanding JavaScript as a language, however when writing your own code: explicitly declaring the missing elements as <code>undefined</code> will increase your code's clarity and maintainability.</p>
<h3 id="Boolean_literals">Boolean literals</h3>
<p>The Boolean type has two literal values: <code>true</code> and <code>false</code>.</p>
<p>Do not confuse the primitive Boolean values <code>true</code> and <code>false</code> with the true and false values of the Boolean object. The Boolean object is a wrapper around the primitive Boolean data type. See [[/js/guide/About_predefined_Core_Objects#Boolean_Object|Boolean Object]] for more information.</p>
<h3 id="Integers">Integers</h3>
<p>Integers can be expressed in decimal (base 10), hexadecimal (base 16), and octal (base 8).</p>
<ul>
  <li>Decimal integer literal consists of a sequence of digits without a leading 0 (zero).</li>
  <li>Leading 0 (zero) on an integer literal indicates it is in octal. Octal integers can include only the digits 0-7.</li>
  <li>Leading 0x (or 0X) indicates hexadecimal. Hexadecimal integers can include digits (0-9) and the letters a-f and A-F.</li>
</ul>
<p>Octal integer literals are deprecated and have been removed from the ECMA-262, Edition 3 standard (in <em>strict mode</em>). JavaScript 1.5 still supports them for backward compatibility.</p>
<p>Some examples of integer literals are:</p>
<pre class="eval">
0, 117 and -345 (decimal, base 10)
015, 0001 and -077 (octal, base 8) 
0x1123, 0x00111 and -0xF1A7 (hexadecimal, "hex" or base 16)
</pre>
<h3 id="Floating-point_literals">Floating-point literals</h3>
<p>A floating-point literal can have the following parts:</p>
<ul>
  <li>A decimal integer which can be signed (preceded by "+" or "-"),</li>
  <li>A decimal point ("."),</li>
  <li>A fraction (another decimal number),</li>
  <li>An exponent.</li>
</ul>
<p>The exponent part is an "e" or "E" followed by an integer, which can be signed (preceded by "+" or "-"). A floating-point literal must have at least one digit and either a decimal point or "e" (or "E").</p>
<p>Some examples of floating-point literals are 3.1415, -3.1E12, .1e12, and 2E-12.</p>
<p>More succinctly, the syntax is:</p>
<pre class="eval">
[digits][.digits][(E|e)[(+|-)]digits]
</pre>
<p>For example:</p>
<pre class="eval">
3.14
2345.789
.3333333333333333333
</pre>
<h3 id="Object_literals">Object literals</h3>
<p>An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces ({}). You should not use an object literal at the beginning of a statement. This will lead to an error or not behave as you expect, because the { will be interpreted as the beginning of a block.</p>
<p>The following is an example of an object literal. The first element of the <code>car</code> object defines a property, <code>myCar</code>; the second element, the <code>getCar</code> property, invokes a function <code>(CarTypes("Honda"));</code> the third element, the <code>special</code> property, uses an existing variable (<code>Sales</code>).</p>
<pre class="brush: js">
var Sales = "Toyota";

function CarTypes(name) {
  return (name == "Honda") ?
    name :
    "Sorry, we don't sell " + name + "." ;
}

var car = { myCar: "Saturn", getCar: CarTypes("Honda"), special: Sales };

console.log(car.myCar);   // Saturn
console.log(car.getCar);  // Honda
console.log(car.special); // Toyota 
</pre>
<p>Additionally, you can use a numeric or string literal for the name of a property or nest an object inside another. The following example uses these options.</p>
<pre class="brush: js">
var car = { manyCars: {a: "Saab", "b": "Jeep"}, 7: "Mazda" };

console.log(car.manyCars.b); // Jeep
console.log(car[7]); // Mazda
</pre>
<p>Please note:</p>
<pre class="brush: js">
var foo = {a: "alpha", 2: "two"};
console.log(foo.a);    // alpha
console.log(foo[2]);   // two
//console.log(foo.2);  // Error: missing ) after argument list
//console.log(foo[a]); // Error: a is not defined
console.log(foo["a"]); // alpha
console.log(foo["2"]); // two
</pre>
<h3 id="String_literals">String literals</h3>
<p>A string literal is zero or more characters enclosed in double (<code>"</code>) or single (<code>'</code>) quotation marks. A string must be delimited by quotation marks of the same type; that is, either both single quotation marks or both double quotation marks. The following are examples of string literals:</p>
<ul>
  <li><code>"foo"</code></li>
  <li><code>'bar'</code></li>
  <li><code>"1234"</code></li>
  <li><code>"one line \n another line"</code></li>
  <li><code>"John's cat"</code></li>
</ul>
<p>You can call any of the methods of the String object on a string literal value—JavaScript automatically converts the string literal to a temporary String object, calls the method, then discards the temporary String object. You can also use the <code>String.length</code> property with a string literal:</p>
<pre class="brush: js">
"John's cat".length
</pre>
<p>You should use string literals unless you specifically need to use a String object. See [[/js/guide/About _predefined_Core_Objects#String_Object|String Object]] for details on <code>String</code> objects.</p>
<h4 id="Using_special_characters_in_strings">Using special characters in strings</h4>
<p>In addition to ordinary characters, you can also include special characters in strings, as shown in the following example.</p>
<pre class="brush: js">
"one line \n another line"
</pre>
<p>The following table lists the special characters that you can use in JavaScript strings.</p>
<table class="standard-table">
  <caption style="text-align: left;">
    Table 2.1 JavaScript special characters</caption>
  <thead>
    <tr>
      <th scope="col">Character</th>
      <th scope="col">Meaning</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>\b</code></td>
      <td>Backspace</td>
    </tr>
    <tr>
      <td><code>\f</code></td>
      <td>Form feed</td>
    </tr>
    <tr>
      <td><code>\n</code></td>
      <td>New line</td>
    </tr>
    <tr>
      <td><code>\r</code></td>
      <td>Carriage return</td>
    </tr>
    <tr>
      <td><code>\t</code></td>
      <td>Tab</td>
    </tr>
    <tr>
      <td><code>\v</code></td>
      <td>Vertical tab</td>
    </tr>
    <tr>
      <td><code>\'</code></td>
      <td>Apostrophe or single quote</td>
    </tr>
    <tr>
      <td><code>\"</code></td>
      <td>Double quote</td>
    </tr>
    <tr>
      <td><code>\\</code></td>
      <td>Backslash character (\).</td>
    </tr>
    <tr>
      <td><code>\<em>XXX</em></code></td>
      <td>The character with the Latin-1 encoding specified by up to three octal digits <em>XXX</em> between 0 and 377. For example, \251 is the octal sequence for the copyright symbol.</td>
    </tr>
    <tr>
      <td><code>\x<em>XX</em></code></td>
      <td>The character with the Latin-1 encoding specified by the two hexadecimal digits <em>XX</em> between 00 and FF. For example, \xA9 is the hexadecimal sequence for the copyright symbol.</td>
    </tr>
    <tr>
      <td><code>\u<em>XXXX</em></code></td>
      <td>The Unicode character specified by the four hexadecimal digits <em>XXXX</em>. For example, \u00A9 is the Unicode sequence for the copyright symbol. See [[#Unicode escape sequences|Unicode escape sequences]].</td>
    </tr>
  </tbody>
</table>
<h4 id="Escaping_characters">Escaping characters</h4>
<p>For characters not listed in Table 2.1, a preceding backslash is ignored, but this usage is deprecated and should be avoided.</p>
<p>You can insert a quotation mark inside a string by preceding it with a backslash. This is known as <em>escaping</em> the quotation mark. For example:</p>
<pre class="brush: js">
var quote = "He read \"The Cremation of Sam McGee\" by R.W. Service.";
console.log(quote);
</pre>
<p>The result of this would be:</p>
<pre class="eval">
He read "The Cremation of Sam McGee" by R.W. Service.
</pre>
<p>To include a literal backslash inside a string, you must escape the backslash character. For example, to assign the file path <code>c:\temp</code> to a string, use the following:</p>
<pre class="brush: js">
var home = "c:\\temp";
</pre>
<p>You can also escape line breaks by preceding them with backslash. The backslash and line break are both removed from the value of the string.</p>
<pre class="brush: js">
var str = "this string \
is broken \
across multiple\
lines."
<span class="objectBox objectBox-text ">console.log(str);</span>   // <span class="objectBox objectBox-text ">this string is broken across multiplelines.</span>
</pre>
<p>Although JavaScript does not have "heredoc" syntax, you can get close by adding a linebreak escape and an escaped linebreak at the end of each line:</p>
<pre class="brush: js">
var poem = 
"Roses are red,\n\
Violets are blue.\n\
I'm schizophrenic,\n\
And so am I."
</pre>
<h2 id="Unicode">Unicode</h2>
<p>Unicode is a universal character-coding standard for the interchange and display of principal written languages. It covers the languages of the Americas, Europe, Middle East, Africa, India, Asia, and Pacifica, as well as historic scripts and technical symbols. Unicode allows for the exchange, processing, and display of multilingual texts, as well as the use of common technical and mathematical symbols. It hopes to resolve internationalization problems of multilingual computing, such as different national character standards. Not all modern or archaic scripts, however, are currently supported.</p>
<p>The Unicode character set can be used for all known encoding. Unicode is modeled after the ASCII (American Standard Code for Information Interchange) character set. It uses a numerical value and name for each character. The character encoding specifies the identity of the character and its numeric value (code position), as well as the representation of this value in bits. The 16-bit numeric value (code value) is defined by a hexadecimal number and a prefix U, for example, U+0041 represents A. The unique name for this value is LATIN CAPITAL LETTER A.</p>
<p><strong>Unicode is not supported in versions of JavaScript prior to 1.3.</strong></p>
<h3 id="Unicode_compatibility_with_ASCII_and_ISO">Unicode compatibility with ASCII and ISO</h3>
<p>Unicode is fully compatible with the International Standard ISO/IEC 10646-1; 1993, which is a subset of ISO 10646.</p>
<p>Several encoding standards (including UTF-8, UTF-16 and ISO UCS-2) are used to physically represent Unicode as actual bits.</p>
<p>The UTF-8 encoding of Unicode is compatible with ASCII characters and is supported by many programs. The first 128 Unicode characters correspond to the ASCII characters and have the same byte value. The Unicode characters U+0020 through U+007E are equivalent to the ASCII characters 0x20 through 0x7E. Unlike ASCII, which supports the Latin alphabet and uses a 7-bit character set, UTF-8 uses between one and four octets for each character ("octet" meaning a byte, or 8 bits.) This allows for several million characters. An alternative encoding standard, UTF-16, uses two octets to represent Unicode characters. An escape sequence allows UTF-16 to represent the whole Unicode range by using four octets. The ISO UCS-2 (Universal Character Set) uses two octets.</p>
<p>JavaScript and Navigator support for UTF-8/Unicode means you can use non-Latin, international, and localized characters, plus special technical symbols in JavaScript programs. Unicode provides a standard way to encode multilingual text. Since the UTF-8 encoding of Unicode is compatible with ASCII, programs can use ASCII characters. You can use non-ASCII Unicode characters in the comments, string literals, identifiers, and regular expressions of JavaScript.</p>
<h3 id="Unicode_escape_sequences">Unicode escape sequences</h3>
<p>You can use the Unicode escape sequence in string literals, regular expressions, and identifiers. The escape sequence consists of six ASCII characters: \u and a four-digit hexadecimal number. For example, \u00A9 represents the copyright symbol. Every Unicode escape sequence in JavaScript is interpreted as one character.</p>
<p>The following code returns the copyright symbol and the string "Netscape Communications".</p>
<pre class="brush: js">
var x = "\u00A9 Netscape Communications";</pre>
<p>The following table lists frequently used special characters and their Unicode value.</p>
<table class="standard-table">
  <caption style="text-align: left;">
    Table 2.2 Unicode values for special characters</caption>
  <thead>
    <tr>
      <th scope="col">Category</th>
      <th scope="col">Unicode value</th>
      <th scope="col">Name</th>
      <th scope="col">Format name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">White space values</td>
      <td>\u0009</td>
      <td>Tab</td>
      <td>&lt;TAB&gt;</td>
    </tr>
    <tr>
      <td>\u000B</td>
      <td>Vertical Tab</td>
      <td>&lt;VT&gt;</td>
    </tr>
    <tr>
      <td>\u000C</td>
      <td>Form Feed</td>
      <td>&lt;FF&gt;</td>
    </tr>
    <tr>
      <td>\u0020</td>
      <td>Space</td>
      <td>&lt;SP&gt;</td>
    </tr>
    <tr>
      <td rowspan="2">Line terminator values</td>
      <td>\u000A</td>
      <td>Line Feed</td>
      <td>&lt;LF&gt;</td>
    </tr>
    <tr>
      <td>\u000D</td>
      <td>Carriage Return</td>
      <td>&lt;CR&gt;</td>
    </tr>
    <tr>
      <td rowspan="5">Additional Unicode escape sequence values</td>
      <td>\u0008</td>
      <td>Backspace</td>
      <td>&lt;BS&gt;</td>
    </tr>
    <tr>
      <td>\u0009</td>
      <td>Horizontal Tab</td>
      <td>&lt;HT&gt;</td>
    </tr>
    <tr>
      <td>\u0022</td>
      <td>Double Quote</td>
      <td>"</td>
    </tr>
    <tr>
      <td>\u0027</td>
      <td>Single Quote</td>
      <td>'</td>
    </tr>
    <tr>
      <td>\u005C</td>
      <td>Backslash</td>
      <td>\</td>
    </tr>
  </tbody>
</table>
<p>The JavaScript use of the Unicode escape sequence is different from Java. In JavaScript, the escape sequence is never interpreted as a special character first. For example, a line terminator escape sequence inside a string does not terminate the string before it is interpreted by the function. JavaScript ignores any escape sequence if it is used in comments. In Java, if an escape sequence is used in a single comment line, it is interpreted as an Unicode character. For a string literal, the Java compiler interprets the escape sequences first. For example, if a line terminator escape character (e.g., \u000A) is used in Java, it terminates the string literal. In Java, this leads to an error, because line terminators are not allowed in string literals. You must use \n for a line feed in a string literal. In JavaScript, the escape sequence works the same way as \n.</p>
<h3 id="Unicode_characters_in_JavaScript_files">Unicode characters in JavaScript files</h3>
<p>Earlier versions of Gecko assumed the Latin-1 character encoding for JavaScript files loaded from XUL. Starting with Gecko 1.8, the character encoding is inferred from the XUL file's encoding. Please see [https:/developer.mozilla.org/en-US/docs/International_characters_in_XUL_JavaScript International characters in XUL JavaScript] for more information.</p>
<h3 id="Displaying_characters_with_Unicode">Displaying characters with Unicode</h3>
<p>You can use Unicode to display the characters in different languages or technical symbols. For characters to be displayed properly, a client such as Mozilla Firefox or Netscape needs to support Unicode. Moreover, an appropriate Unicode font must be available to the client, and the client platform must support Unicode. Often, Unicode fonts do not display all the Unicode characters. Some platforms, such as Windows 95, provide partial support for Unicode.</p>
<p>To receive non-ASCII character input, the client needs to send the input as Unicode. Using a standard enhanced keyboard, the client cannot easily input the additional characters supported by Unicode. Sometimes, the only way to input Unicode characters is by using Unicode escape sequences.</p>
<p>For more information on Unicode, see the [http://www.unicode.org/ Unicode Home Page] and The Unicode Standard, Version 2.0, published by Addison-Wesley, 1996.</p>
<h2 id="Resources">Resources</h2>
<ul>
  <li>[http://0xcc.net/jsescape/ Text Escaping and Unescaping in JavaScript] – an utility to convert characters in JavaScript unicode values</li>
</ul>

{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Values,_variables,_and_literals$
|MSDN_link=
|HTML5Rocks_link=
}}