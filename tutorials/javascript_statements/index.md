{{Flags}}
{{Summary_Section|JavaScript supports a compact set of statements that you can use to incorporate a great deal of interactivity in Web pages. This chapter provides an overview of these statements.}}
{{Guide
|Content=<p>Any expression is also a statement. See [[/guides/js/Expressions|Expressions and Operators]] for complete information about statements.</p>
<p>Use the semicolon (<code>;</code>) character to separate statements in JavaScript code.</p>
<p>See the [[/js/statements|JavaScript Reference]] for details about the statements in this chapter.</p>
<h2 id="Block_Statement">Block Statement</h2>
<p>A block statement is used to group statements. The block is delimited by a pair of curly brackets:</p>
  <pre >
{
   statement_1;
   statement_2;
   .
   .
   .
   statement_n;
}
</pre>

<p><strong>Example</strong><br />
  Block statements are commonly used with control flow statements (e.g. <code>if</code>, <code>for</code>, <code>while</code>).</p>
  <pre >
while (x &lt; 10){
  x++;
}
</pre>


<p>Here, <code>{ x++; }</code> is the block statement.</p>
<p><strong>Important</strong>: JavaScript does <strong>not</strong> have block scope. Variables introduced with a block are scoped to the containing function or script, and the effects of setting them persist beyond the block itself. In other words, block statements do not introduce a scope. Although "standalone" blocks are valid syntax, you do not want to use standalone blocks in JavaScript, because they don't do what you think they do, if you think they do anything like such blocks in C or Java. For example:</p>
<pre >
var x = 1;
{
  var x = 2;
}
alert(x); // outputs 2
</pre>
<p>This outputs 2 because the <code>var x</code> statement within the block is in the same scope as the <code>var x</code> statement before the block. In C or Java, the equivalent code would have outputted 1.</p>
<h2 id="Conditional_Statements">Conditional Statements</h2>
<p>A conditional statement is a set of commands that executes if a specified condition is true. JavaScript supports two conditional statements: <code>if...else</code> and <code>switch</code>.</p>
<h3 id="if...else_Statement">if...else Statement</h3>
<p>Use the <code>if</code> statement to execute a statement if a logical condition is true. Use the optional <code>else</code> clause to execute a statement if the condition is false. An <code>if</code> statement looks as follows:</p>
<pre >
if (condition)
  statement_1
[else
  statement_2]
</pre>
<p><code>condition</code> can be any expression that evaluates to true or false. If <code>condition</code> evaluates to true, <code>statement_1</code> is executed; otherwise, <code>statement_2</code> is executed. <code>statement_1</code> and <code>statement_2</code> can be any statement, including further nested <code>if</code> statements.</p>
<p>You may also compound the statements using <code>else if</code> to have multiple conditions tested in sequence, as follows:</p>
<pre >
if (condition)
  statement_1
[else if (condition_2)
  statement_2]
...
[else if (condition_n_1)
  statement_n_1]
[else
  statement_n]
</pre>
<p>To execute multiple statements, use a block statement (<code>{ ... }</code>) to group those statements. In general, it is a good practice to always use block statements, especially in code involving nested <code>if</code> statements:</p>
<pre >
if (condition) {
  statements_1
} else {
  statements_2
}
</pre>
<p>It is advisable to not use simple assignments in a conditional expression, because the assignment can be confused with equality when glancing over the code. For example, do not use the following code:</p>
<pre >
if (x = y) {
  /* do the right thing */
}
</pre>
<p>If you need to use an assignment in a conditional expression, a common practice is to put additional parentheses around the assignment. For example:</p>
<pre >
if ((x = y)) {
  /* do the right thing */
}
</pre>
<p>The following values will evaluate to false:</p>
<ul>
  <li><code>false</code></li>
  <li><code>undefined</code></li>
  <li><code>null</code></li>
  <li><code>0</code></li>
  <li><code>NaN</code></li>
  <li>the empty string (<code>""</code>)</li>
</ul>
<p>All other values, including all objects evaluate to true when passes to a conditional statement.</p>
<p>Do not confuse the primitive boolean values <code>true</code> and <code>false</code> with the true and false values of the Boolean object. For example:</p>
<pre >
var b = new Boolean(false);
if (b) // this condition evaluates to true
</pre>
<p><strong>Example</strong><br />
  In the following example, the function <code>checkData</code> returns true if the number of characters in a <code>Text</code> object is three; otherwise, it displays an alert and returns false.</p>
<pre >
function checkData() {
  if (document.form1.threeChar.value.length == 3) {
    return true;
  } else {
    alert("Enter exactly three characters. " +
      document.form1.threeChar.value + " is not valid.");
    return false;
  }
}
</pre>
<h3 id="switch_Statement">switch Statement</h3>
<p>A <code>switch</code> statement allows a program to evaluate an expression and attempt to match the expression's value to a case label. If a match is found, the program executes the associated statement. A <code>switch</code> statement looks as follows:</p>
<pre >
switch (expression) {
   case label_1:
      statements_1
      [break;]
   case label_2:
      statements_2
      [break;]
   ...
   default:
      statements_def
      [break;]
}
</pre>
<p>The program first looks for a <code>case</code> clause with a label matching the value of expression and then transfers control to that clause, executing the associated statements. If no matching label is found, the program looks for the optional <code>default</code> clause, and if found, transfers control to that clause, executing the associated statements. If no <code>default</code> clause is found, the program continues execution at the statement following the end of <code>switch</code>. By convention, the <code>default</code> clause is the last clause, but it does not need to be so.</p>
<p>The optional <code>break</code> statement associated with each <code>case</code> clause ensures that the program breaks out of <code>switch</code> once the matched statement is executed and continues execution at the statement following switch. If <code>break</code> is omitted, the program continues execution at the next statement in the <code>switch</code> statement.</p>
<p><strong>Example</strong><br />
  In the following example, if <code>fruittype</code> evaluates to "Bananas", the program matches the value with case "Bananas" and executes the associated statement. When <code>break</code> is encountered, the program terminates <code>switch</code> and executes the statement following <code>switch</code>. If <code>break</code> were omitted, the statement for case "Cherries" would also be executed.</p>
<pre >
switch (fruittype) {
   case "Oranges":
      document.write("Oranges are $0.59 a pound.&lt;br&gt;");
      break;
   case "Apples":
      document.write("Apples are $0.32 a pound.&lt;br&gt;");
      break;
   case "Bananas":
      document.write("Bananas are $0.48 a pound.&lt;br&gt;");
      break;
   case "Cherries":
      document.write("Cherries are $3.00 a pound.&lt;br&gt;");
      break;
   case "Mangoes":
   case "Papayas":
      document.write("Mangoes and papayas are $2.79 a pound.&lt;br&gt;");
      break;
   default:
      document.write("Sorry, we are out of " + fruittype + ".&lt;br&gt;");
}
document.write("Is there anything else you'd like?&lt;br&gt;");</pre>
<h2 id="Loop_Statements">Loop Statements</h2>
<p>A loop is a set of commands that executes repeatedly until a specified condition is met. JavaScript supports the <code>for</code>, <code>do while</code>, and <code>while</code> loop statements, as well as label (label is not itself a looping statement, but is frequently used with these statements). In addition, you can use the <code>break</code> and <code>continue</code> statements within loop statements.</p>
<p>Another statement, <code>for...in</code>, executes statements repeatedly but is used for object manipulation. See {{ linkToFragment("Object Manipulation Statements") }}.</p>
<p>The loop statements are:</p>
<ul>
  <li>[[#for_Statement|for Statement]]</li>
  <li>[[#do...while_Statement|do...while Statement]]</li>
  <li>[[#while_Statement|while Statement]]</li>
  <li>[[#label_Statement|label Statement]]</li>
  <li>[[#break_Statement|break Statement]]</li>
  <li>[[#continue_Statement|continue Statement]]</li>
</ul>
<h3 id="for_Statement">for Statement</h3>
<p>A <code>for</code> loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C <code>for</code> loop. A <code>for</code> statement looks as follows:</p>
<pre >
for ([initialExpression]; [condition]; [incrementExpression])
   statement
</pre>
<p>When a <code>for</code> loop executes, the following occurs:</p>
<ol>
  <li>The initializing expression <code>initialExpression</code>, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.</li>
  <li>The <code>condition</code> expression is evaluated. If the value of <code>condition</code> is true, the loop statements execute. If the value of <code>condition</code> is false, the <code>for</code> loop terminates. If the <code>condition</code> expression is omitted entirely, the condition is assumed to be true.</li>
  <li>The <code>statement</code> executes. To execute multiple statements, use a block statement (<code>{ ... }</code>) to group those statements.</li>
  <li>The update expression <code>incrementExpression</code>, if there is one, executes, and control returns to step 2.</li>
</ol>
<p><strong>Example</strong><br />
  The following function contains a <code>for</code> statement that counts the number of selected options in a scrolling list (a <code>Select</code> object that allows multiple selections). The <code>for</code> statement declares the variable <code>i</code> and initializes it to zero. It checks that <code>i</code> is less than the number of options in the <code>Select</code> object, performs the succeeding <code>if</code> statement, and increments <code>i</code> by one after each pass through the loop.</p>
<pre >
&lt;script type="text/javascript"&gt;

function howMany(selectObject) {
   var numberSelected = 0;
   for (var i = 0; i &lt; selectObject.options.length; i++) {
      if (selectObject.options[i].selected)
         numberSelected++;
   }
   return numberSelected;
}

&lt;/script&gt;
&lt;form name="selectForm"&gt;
   &lt;p&gt;
      &lt;strong&gt;Choose some music types, then click the button below:&lt;/strong&gt;
      &lt;br/&gt;
      &lt;select name="musicTypes" multiple="multiple"&gt;
         &lt;option selected="selected"&gt;R&amp;B&lt;/option&gt;
         &lt;option&gt;Jazz&lt;/option&gt;
         &lt;option&gt;Blues&lt;/option&gt;
         &lt;option&gt;New Age&lt;/option&gt;
         &lt;option&gt;Classical&lt;/option&gt;
         &lt;option&gt;Opera&lt;/option&gt;
      &lt;/select&gt;
   &lt;/p&gt;
   &lt;p&gt;
      &lt;input type="button" value="How many are selected?"
         onclick="alert ('Number of options selected: ' + howMany(document.selectForm.musicTypes))"/&gt;
   &lt;/p&gt;
&lt;/form&gt;</pre>
<h3 id="do...while_Statement">do...while Statement</h3>
<p>The <code>do...while</code> statement repeats until a specified condition evaluates to false. A <code>do...while</code> statement looks as follows:</p>
<pre >
do
   statement
while (condition);
</pre>
<p><code>statement</code> executes once before the condition is checked. To execute multiple statements, use a block statement (<code>{ ... }</code>) to group those statements. If <code>condition</code> is true, the statement executes again. At the end of every execution, the condition is checked. When the condition is false, execution stops and control passes to the statement following <code>do...while</code>.</p>
<p><strong>Example</strong><br />
  In the following example, the <code>do</code> loop iterates at least once and reiterates until i is no longer less than 5.</p>
<pre class="brush: js">
do {
   i += 1;
   document.write(i);
} while (i &lt; 5);</pre>
<h3 id="while_Statement">while Statement</h3>
<p>A <code>while</code> statement executes its statements as long as a specified condition evaluates to true. A <code>while</code> statement looks as follows:</p>
<pre class="brush: js">
while (condition)
   statement
</pre>
<p>If the condition becomes false, <code>statement</code> within the loop stops executing and control passes to the statement following the loop.</p>
<p>The condition test occurs before <code>statement</code> in the loop are executed. If the condition returns true, <code>statement</code> is executed and the condition is tested again. If the condition returns false, execution stops and control is passed to the statement following <code>while</code>.</p>
<p>To execute multiple statements, use a block statement ({ ... }) to group those statements.</p>
<p><strong>Example 1</strong><br />
  The following <code>while</code> loop iterates as long as <code>n</code> is less than three:</p>
<pre class="brush: js">
n = 0;
x = 0;
while (n &lt; 3) {
   n++;
   x += n;
}
</pre>
<p>With each iteration, the loop increments <code>n</code> and adds that value to <code>x</code>. Therefore, <code>x</code> and <code>n</code> take on the following values:</p>
<ul>
  <li>After the first pass: <code>n</code> = 1 and <code>x</code> = 1</li>
  <li>After the second pass: <code>n</code> = 2 and <code>x</code> = 3</li>
  <li>After the third pass: <code>n</code> = 3 and <code>x</code> = 6</li>
</ul>
<p>After completing the third pass, the condition <code>n &lt; 3</code> is no longer true, so the loop terminates.</p>
<p><strong>Example 2</strong><br />
  Avoid infinite loops. Make sure the condition in a loop eventually becomes false; otherwise, the loop will never terminate. The statements in the following <code>while</code> loop execute forever because the condition never becomes false:</p>
<pre class="brush: js">
while (true) {
   alert("Hello, world");
}</pre>
<h3 id="label_Statement">label Statement</h3>
<p>A label provides a statement with an identifier that lets you refer to it elsewhere in your program. For example, you can use a label to identify a loop, and then use the <code>break</code> or <code>continue</code> statements to indicate whether a program should interrupt the loop or continue its execution.</p>
<p>The syntax of the label statement looks like the following:</p>
<pre class="brush: js">
label :
   statement
</pre>
<p>The value of <code><em>label</em></code> may be any JavaScript identifier that is not a reserved word. The <code><em>statement</em></code> that you identify with a label may be any statement.</p>
<p><strong>Example</strong><br />
  In this example, the label <code>markLoop</code> identifies a <code>while</code> loop.</p>
<pre class="brush: js">
markLoop:
while (theMark == true) {
   doSomething();
}</pre>
<h3 id="break_Statement">break Statement</h3>
<p>Use the <code>break</code> statement to terminate a loop, <code>switch</code>, or in conjunction with a label statement.</p>
<ul>
  <li>When you use <code>break</code> without a label, it terminates the innermost enclosing <code>while</code>, <code>do-while</code>, <code>for</code>, or <code>switch</code> immediately and transfers control to the following statement.</li>
  <li>When you use <code>break</code> with a label, it terminates the specified labeled statement.</li>
</ul>
<p>The syntax of the <code>break</code> statement looks like this:</p>
<ol>
  <li><code>break;</code></li>
  <li><code>break <em>label</em>;</code></li>
</ol>
<p>The first form of the syntax terminates the innermost enclosing loop or <code>switch</code>; the second form of the syntax terminates the specified enclosing label statement.</p>
<p><strong>Example</strong> <strong>1:</strong><br />
  The following example iterates through the elements in an array until it finds the index of an element whose value is <code>theValue</code>:</p>
<pre class="brush: js">
for (i = 0; i &lt; a.length; i++) {
   if (a[i] == theValue)
      break;
}</pre>
<p><strong>Example 2: </strong>Breaking to a Label</p>
<pre class="brush: js">
var x = 0;
var z = 0
labelCancelLoops: while (true) {
    console.log("Outer loops: " + x);
    x += 1;
    z = 1;
    while (true) {
        console.log("Inner loops: " + z);
        z += 1;
        if (z === 10 &amp;&amp; x === 10) {
            break labelCancelLoops;
        } else if (z === 10) {
            break;
        }
    }
}
</pre>
<h3 id="continue_Statement">continue Statement</h3>
<p>The <code>continue</code> statement can be used to restart a <code>while</code>, <code>do-while</code>, <code>for</code>, or <code>label</code> statement.</p>
<ul>
  <li>When you use <code>continue</code> without a label, it terminates the current iteration of the innermost enclosing <code>while</code>, <code>do-while</code> or <code>for</code> statement and continues execution of the loop with the next iteration. In contrast to the <code>break</code> statement, <code>continue</code> does not terminate the execution of the loop entirely. In a <code>while</code> loop, it jumps back to the condition. In a <code>for</code> loop, it jumps to the <code>increment-expression</code>.</li>
  <li>When you use <code>continue</code> with a label, it applies to the looping statement identified with that label.</li>
</ul>
<p>The syntax of the <code>continue</code> statement looks like the following:</p>
<ol>
  <li><code>continue</code></li>
  <li><code>continue </code><em><code>label</code></em></li>
</ol>
<p><strong>Example 1</strong><br />
  The following example shows a <code>while</code> loop with a <code>continue</code> statement that executes when the value of <code>i</code> is three. Thus, <code>n</code> takes on the values one, three, seven, and twelve.</p>
<pre class="brush: js">
i = 0;
n = 0;
while (i &lt; 5) {
   i++;
   if (i == 3)
      continue;
   n += i;
}
</pre>
<p><strong>Example 2</strong><br />
  A statement labeled <code>checkiandj</code> contains a statement labeled <code>checkj</code>. If <code>continue</code> is encountered, the program terminates the current iteration of <code>checkj</code> and begins the next iteration. Each time <code>continue</code> is encountered, <code>checkj</code> reiterates until its condition returns <code>false</code>. When <code>false</code> is returned, the remainder of the <code>checkiandj</code> statement is completed, and <code>checkiandj</code> reiterates until its condition returns <code>false</code>. When <code>false</code> is returned, the program continues at the statement following <code>checkiandj</code>.</p>
<p>If <code>continue</code> had a label of <code>checkiandj</code>, the program would continue at the top of the <code>checkiandj</code> statement.</p>
<pre class="brush: js">
checkiandj :
   while (i &lt; 4) {
      document.write(i + "&lt;br/&gt;");
      i += 1;
      checkj :
         while (j &gt; 4) {
            document.write(j + "&lt;br/&gt;");
            j -= 1;
            if ((j % 2) == 0)
               continue checkj;
            document.write(j + " is odd.&lt;br/&gt;");
         }
      document.write("i = " + i + "&lt;br/&gt;");
      document.write("j = " + j + "&lt;br/&gt;");
   }</pre>
<h2 id="Object_Manipulation_Statements">Object Manipulation Statements</h2>
<p>JavaScript uses the <code>for...in</code>, <code>for each...in</code>, and <code>with</code> statements to manipulate objects.</p>
<h3 id="for...in_Statement">for...in Statement</h3>
<p>The <a href="/en-US/docs/JavaScript/Reference/Statements/for...in" title="en-US/docs/JavaScript/Reference/Statements/for...in"><code>for...in</code></a> statement iterates a specified variable over all the properties of an object. For each distinct property, JavaScript executes the specified statements. A <code>for...in</code> statement looks as follows:</p>
<pre class="brush: js">
for (variable in object) {
   statements
}
</pre>
<p><strong>Example</strong><br />
  The following function takes as its argument an object and the object's name. It then iterates over all the object's properties and returns a string that lists the property names and their values.</p>
<pre class="brush: js">
function dump_props(obj, obj_name) {
   var result = "";
   for (var i in obj) {
      result += obj_name + "." + i + " = " + obj[i] + "&lt;br&gt;";
   }
   result += "&lt;hr&gt;";
   return result;
}
</pre>
<p>For an object <code>car</code> with properties <code>make</code> and <code>model</code>, <code>result</code> would be:</p>
<pre class="brush: js">
car.make = Ford
car.model = Mustang
</pre>
<p><strong>Arrays</strong><br />
  Although it may be tempting to use this as a way to iterate over <a href="/en-US/docs/JavaScript/Reference/Global_Objects/Array" title="en-US/docs/JavaScript/Reference/Global Objects/Array">Array</a> elements, because the <strong>for...in</strong> statement iterates over user-defined properties in addition to the array elements, if you modify the Array object, such as adding custom properties or methods, the <strong>for...in</strong> statement will return the name of your user-defined properties in addition to the numeric indexes. Thus it is better to use a traditional <a href="/en-US/docs/JavaScript/Reference/Statements/for" title="en-US/docs/JavaScript/Reference/Statements/for">for</a> loop with a numeric index when iterating over arrays.</p>
<h3 id="for_each...in_Statement">for each...in Statement</h3>
<p><a href="/en-US/docs/JavaScript/Reference/Statements/for_each...in" title="en-US/docs/JavaScript/Reference/Statements/for each...in"><code>for each...in</code></a> is a loop statement introduced in <a href="/en-US/docs/JavaScript/New_in_JavaScript/1.6" title="en-US/docs/JavaScript/New in JavaScript/1.6">JavaScript 1.6</a>. <!--{12722816747680}-->It is similar to <code>for...in</code>, but iterates over the values of object's properties, not their names.</p>
<pre class="brush: js">
var sum = 0;
var obj = {prop1: 5, prop2: 13, prop3: 8};
for each (var item in obj) {
  sum += item;
}
print(sum); // prints "26", which is 5+13+8</pre>
<h2 id="Comments">Comments</h2>
<p>Comments are author notations that explain what a script does. Comments are ignored by the interpreter. JavaScript supports Java and C++-style comments:</p>
<ul>
  <li>Comments on a single line are preceded by a double-slash (//).</li>
  <li>Comments that span multiple lines are preceded by /* and followed by */:</li>
</ul>
<p><strong>Example</strong><br />
  The following example shows two comments:</p>
<pre class="brush: js">
// This is a single-line comment.

/* This is a multiple-line comment. It can be of any length, and
you can put whatever you want here. */</pre>
<h2 id="Exception_Handling_Statements">Exception Handling Statements</h2>
<p>You can throw exceptions using the <code>throw</code> statement and handle them using the <code>try...catch</code> statements.</p>
<p>You can also use the <code>try...catch</code> statement to handle Java exceptions (though there is a {{ bug("391642") }} with this). See <a href="/en-US/docs/JavaScript/Guide/LiveConnect_Overview#Handling_Java_Exceptions_in_JavaScript" title="en-US/docs/JavaScript/Guide/LiveConnect Overview#Handling Java Exceptions in JavaScript">Handling Java Exceptions in JavaScript</a> and <a href="/en-US/docs/JavaScript/Guide/LiveConnect_Overview#JavaScript_to_Java_Communication" title="en-US/docs/JavaScript/Guide/LiveConnect Overview#JavaScript to Java Communication">JavaScript to Java Communication</a> for information.</p>
<ul>
  <li>[[#throw_Statement|throw Statement]]</li>
  <li>[[#try...catch_Statement|try...catch Statement]]</li>
</ul>
<h3 id="Exception_Types">Exception Types</h3>
<p>Just about any object can be thrown in JavaScript. Nevertheless, not all thrown objects are created equal. While it is fairly common to throw numbers or strings as errors it is frequently more effective to use one of the exception types specifically created for this purpose:</p>
<ul>
  <li><a href="/en-US/docs/JavaScript/Reference/Global_Objects#Error_constructors">ECMAScript exceptions</a></li>
  <li><a href="/en-US/docs/DOM/DOMException" title="en-US/docs/DOM/DOMException">DOMException</a></li>
  <li><a href="/en-US/docs/XPCOM_Interface_Reference/nsIXPCException" title="en-US/docs/nsIXPCException">nsIXPCException</a> (<a href="/en-US/docs/XPConnect" title="en-US/docs/XPConnect">XPConnect</a>)</li>
</ul>
<h3 id="throw_Statement">throw Statement</h3>
<p>Use the <code>throw</code> statement to throw an exception. When you throw an exception, you specify the expression containing the value to be thrown:</p>
<pre class="brush: js">
throw expression;
</pre>
<p>You may throw any expression, not just expressions of a specific type. The following code throws several exceptions of varying types:</p>
<pre class="brush: js">
throw "Error2";
throw 42;
throw true;
throw {toString: function() { return "I'm an object!"; } };
</pre>
<div class="note">
  <strong>Note:</strong> You can specify an object when you throw an exception. You can then reference the object's properties in the <code>catch</code> block. The following example creates an object <code>myUserException</code> of type <code>UserException</code> and uses it in a throw statement.</div>
<pre class="brush: js">
// Create an object type UserException
function UserException (message){
  this.message=message;
  this.name="UserException";
}

// Make the exception convert to a pretty string when used as
// a string (e.g. by the error console)
UserException.prototype.toString = function (){
  return this.name + ': "' + this.message + '"';
}

// Create an instance of the object type and throw it
throw new UserException("Value too high");</pre>
<h3 id="try...catch_Statement">try...catch Statement</h3>
<p>The <code>try...catch</code> statement marks a block of statements to try, and specifies one or more responses should an exception be thrown. If an exception is thrown, the <code>try...catch</code> statement catches it.</p>
<p>The <code>try...catch</code> statement consists of a <code>try</code> block, which contains one or more statements, and zero or more <code>catch</code> blocks, containing statements that specify what to do if an exception is thrown in the <code>try</code> block. That is, you want the <code>try</code> block to succeed, and if it does not succeed, you want control to pass to the <code>catch</code> block. If any statement within the <code>try</code> block (or in a function called from within the <code>try</code> block) throws an exception, control immediately shifts to the <code>catch</code> block. If no exception is thrown in the <code>try</code> block, the <code>catch</code> block is skipped. The <code>finally</code> block executes after the <code>try</code> and <code>catch</code> blocks execute but before the statements following the <code>try...catch</code> statement.</p>
<p>The following example uses a <code>try...catch</code> statement. The example calls a function that retrieves a month name from an array based on the value passed to the function. If the value does not correspond to a month number (1-12), an exception is thrown with the value <code>"InvalidMonthNo"</code> and the statements in the <code>catch</code> block set the <code>monthName</code> variable to <code>unknown</code>.</p>
<pre class="brush: js">
function getMonthName (mo) {
    mo=mo-1; // Adjust month number for array index (1=Jan, 12=Dec)
    var months=new Array("Jan","Feb","Mar","Apr","May","Jun","Jul",
          "Aug","Sep","Oct","Nov","Dec");
    if (months[mo] != null) {
       return months[mo]
    } else {
       throw "InvalidMonthNo"
    }
}

try {
// statements to try
    monthName=getMonthName(myMonth) // function could throw exception
}
catch (e) {
    monthName="unknown"
    logMyErrors(e) // pass exception object to error handler
}
</pre>
<h4 id="The_catch_Block" name="The_catch_Block">The catch Block</h4>
<p>You can use a <code>catch</code> block to handle all exceptions that may be generated in the <code>try</code> block.</p>
<pre class="brush: js">
catch (catchID) {
  statements
}
</pre>
<p>The <code>catch</code> block specifies an identifier (<code>catchID</code> in the preceding syntax) that holds the value specified by the <code>throw</code> statement; you can use this identifier to get information about the exception that was thrown. JavaScript creates this identifier when the <code>catch</code> block is entered; the identifier lasts only for the duration of the <code>catch</code> block; after the <code>catch</code> block finishes executing, the identifier is no longer available.</p>
<p>For example, the following code throws an exception. When the exception occurs, control transfers to the <code>catch</code> block.</p>
<pre class="brush: js">
try {
   throw "myException" // generates an exception
}
catch (e) {
// statements to handle any exceptions
   logMyErrors(e) // pass exception object to error handler
}
</pre>
<h4 id="The_finally_Block">The finally Block</h4>
<p>The <code>finally</code> block contains statements to execute after the <code>try</code> and <code>catch</code> blocks execute but before the statements following the <code>try...catch</code> statement. The <code>finally</code> block executes whether or not an exception is thrown. If an exception is thrown, the statements in the <code>finally</code> block execute even if no <code>catch</code> block handles the exception.</p>
<p>You can use the <code>finally</code> block to make your script fail gracefully when an exception occurs; for example, you may need to release a resource that your script has tied up. The following example opens a file and then executes statements that use the file (server-side JavaScript allows you to access files). If an exception is thrown while the file is open, the <code>finally</code> block closes the file before the script fails.</p>
<pre class="brush: js">
openMyFile();
try {
    writeMyFile(theData); //This may throw a error
}catch(e){
    handleError(e); // If we got a error we handle it
}finally {
    closeMyFile(); // always close the resource
}
</pre>
<p>If the <code>finally</code> block returns a value, this value becomes the return value of the entire <code>try-catch-finally</code> production, regardless of any <code>return</code> statements in the <code>try</code> and <code>catch</code> blocks:</p>
<pre class="brush: js">
function f() {
    try {
        alert(0);
        throw "bogus";
    } catch(e) {
        alert(1);
        return true; // this return statement is suspended until finally block has completed
        alert(2); // not reachable
    } finally {
        alert(3);
        return false; // overwrites the previous "return"
        alert(4); // not reachable
    }
    // "return false" is executed now
    
    alert(5); // not reachable
}
f(); // alerts 0, 1, 3; returns false
</pre>
<h4 id="Nesting_try...catch_Statements" name="Nesting_try...catch_Statements">Nesting try...catch Statements</h4>
<p>You can nest one or more <code>try...catch</code> statements. If an inner <code>try...catch</code> statement does not have a <code>catch</code> block, the enclosing <code>try...catch</code> statement's <code>catch</code> block is checked for a match.</p>
<h3 id="Utilizing_Error_objects">Utilizing Error objects</h3>
<p>Depending on the type of error, you may be able to use the 'name' and 'message' properties to get a more refined message. 'name' provides the general class of Error (e.g., 'DOMException' or 'Error'), while 'message' generally provides a more succinct message than one would get by converting the error object to a string.</p>
<p>If you are throwing your own exceptions, in order to take advantage of these properties (such as if your catch block doesn't discriminate between your own exceptions and system ones), you can use the Error constructor. For example:</p>
<pre class="brush: js">
function doSomethingErrorProne () {
   if (ourCodeMakesAMistake()) {
      throw (new Error('The message'));
   }
   else {
      doSomethingToGetAJavascriptError();
   }
}
....
try {
   doSomethingErrorProne();
}
catch (e) {
   alert(e.name);// alerts 'Error'
   alert(e.message); // alerts 'The message' or a JavaScript error message)
}</pre>
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Statements
|MSDN_link=
|HTML5Rocks_link=
}}