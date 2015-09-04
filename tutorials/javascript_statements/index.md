---
title: javascript statements
tags:
  - Tutorials
  - JavaScript
readiness: 'Almost Ready'
notes:
  - 'Fix broken links'
summary: 'JavaScript supports a compact set of statements that you can use to incorporate a great deal of interactivity in Web pages. This chapter provides an overview of these statements.'
uri: 'tutorials/javascript statements'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'Template:linkToFragment("Object Manipulation Statements")'
    - 'Template:bug("391642")'

---
# JavaScript statements

## Summary

JavaScript supports a compact set of statements that you can use to incorporate a great deal of interactivity in Web pages. This chapter provides an overview of these statements.

Any expression is also a statement. See [Expressions and Operators](/concepts/programming/javascript/expressions) for complete information about statements.

Use the semicolon (`;`) character to separate statements in JavaScript code.

See the [JavaScript Reference](/javascript/statements) for details about the statements in this chapter.

## Block Statement

A block statement is used to group statements. The block is delimited by a pair of curly brackets:

    {
       statement_1;
       statement_2;
       .
       .
       .
       statement_n;
    }

**Example**
 Block statements are commonly used with control flow statements (e.g. `if`, `for`, `while`).

    while (x < 10){
      x++;
    }

Here, `{ x++; }` is the block statement.

**Important**: JavaScript does **not** have block scope. Variables introduced with a block are scoped to the containing function or script, and the effects of setting them persist beyond the block itself. In other words, block statements do not introduce a scope. Although "standalone" blocks are valid syntax, you do not want to use standalone blocks in JavaScript, because they don't do what you think they do, if you think they do anything like such blocks in C or Java. For example:

    var x = 1;
    {
      var x = 2;
    }
    alert(x); // outputs 2

This outputs 2 because the `var x` statement within the block is in the same scope as the `var x` statement before the block. In C or Java, the equivalent code would have outputted 1.

## Conditional Statements

A conditional statement is a set of commands that executes if a specified condition is true. JavaScript supports two conditional statements: `if...else` and `switch`.

### if...else Statement

Use the `if` statement to execute a statement if a logical condition is true. Use the optional `else` clause to execute a statement if the condition is false. An `if` statement looks as follows:

    if (condition)
      statement_1
    [else
      statement_2]

`condition` can be any expression that evaluates to true or false. If `condition` evaluates to true, `statement_1` is executed; otherwise, `statement_2` is executed. `statement_1` and `statement_2` can be any statement, including further nested `if` statements.

You may also compound the statements using `else if` to have multiple conditions tested in sequence, as follows:

    if (condition)
      statement_1
    [else if (condition_2)
      statement_2]
    ...
    [else if (condition_n_1)
      statement_n_1]
    [else
      statement_n]

To execute multiple statements, use a block statement (`{ ... }`) to group those statements. In general, it is a good practice to always use block statements, especially in code involving nested `if` statements:

    if (condition) {
      statements_1
    } else {
      statements_2
    }

It is advisable to not use simple assignments in a conditional expression, because the assignment can be confused with equality when glancing over the code. For example, do not use the following code:

    if (x = y) {
      /* do the right thing */
    }

If you need to use an assignment in a conditional expression, a common practice is to put additional parentheses around the assignment. For example:

    if ((x = y)) {
      /* do the right thing */
    }

The following values will evaluate to false:

-   `false`
-   `undefined`
-   `null`
-   `0`
-   `NaN`
-   the empty string (`""`)

All other values, including all objects evaluate to true when passes to a conditional statement.

Do not confuse the primitive boolean values `true` and `false` with the true and false values of the Boolean object. For example:

    var b = new Boolean(false);
    if (b) // this condition evaluates to true

**Example**
 In the following example, the function `checkData` returns true if the number of characters in a `Text` object is three; otherwise, it displays an alert and returns false.

    function checkData() {
      if (document.form1.threeChar.value.length == 3) {
        return true;
      } else {
        alert("Enter exactly three characters. " +
          document.form1.threeChar.value + " is not valid.");
        return false;
      }
    }

### switch Statement

A `switch` statement allows a program to evaluate an expression and attempt to match the expression's value to a case label. If a match is found, the program executes the associated statement. A `switch` statement looks as follows:

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

The program first looks for a `case` clause with a label matching the value of expression and then transfers control to that clause, executing the associated statements. If no matching label is found, the program looks for the optional `default` clause, and if found, transfers control to that clause, executing the associated statements. If no `default` clause is found, the program continues execution at the statement following the end of `switch`. By convention, the `default` clause is the last clause, but it does not need to be so.

The optional `break` statement associated with each `case` clause ensures that the program breaks out of `switch` once the matched statement is executed and continues execution at the statement following switch. If `break` is omitted, the program continues execution at the next statement in the `switch` statement.

**Example**
 In the following example, if `fruittype` evaluates to "Bananas", the program matches the value with case "Bananas" and executes the associated statement. When `break` is encountered, the program terminates `switch` and executes the statement following `switch`. If `break` were omitted, the statement for case "Cherries" would also be executed.

    switch (fruittype) {
       case "Oranges":
          document.write("Oranges are $0.59 a pound.<br>");
          break;
       case "Apples":
          document.write("Apples are $0.32 a pound.<br>");
          break;
       case "Bananas":
          document.write("Bananas are $0.48 a pound.<br>");
          break;
       case "Cherries":
          document.write("Cherries are $3.00 a pound.<br>");
          break;
       case "Mangoes":
       case "Papayas":
          document.write("Mangoes and papayas are $2.79 a pound.<br>");
          break;
       default:
          document.write("Sorry, we are out of " + fruittype + ".<br>");
    }
    document.write("Is there anything else you'd like?<br>");

## Loop Statements

A loop is a set of commands that executes repeatedly until a specified condition is met. JavaScript supports the `for`, `do while`, and `while` loop statements, as well as label (label is not itself a looping statement, but is frequently used with these statements). In addition, you can use the `break` and `continue` statements within loop statements.

Another statement, `for...in`, executes statements repeatedly but is used for object manipulation. See [Template:linkToFragment("Object Manipulation Statements")](/w/index.php?title=Template:linkToFragment(%22Object_Manipulation_Statements%22)&action=edit&redlink=1).

The loop statements are:

-   [for Statement](#for_Statement)
-   [do...while Statement](#do...while_Statement)
-   [while Statement](#while_Statement)
-   [label Statement](#label_Statement)
-   [break Statement](#break_Statement)
-   [continue Statement](#continue_Statement)

### for Statement

A `for` loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C `for` loop. A `for` statement looks as follows:

    for ([initialExpression]; [condition]; [incrementExpression])
       statement

When a `for` loop executes, the following occurs:

1.  The initializing expression `initialExpression`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
2.  The `condition` expression is evaluated. If the value of `condition` is true, the loop statements execute. If the value of `condition` is false, the `for` loop terminates. If the `condition` expression is omitted entirely, the condition is assumed to be true.
3.  The `statement` executes. To execute multiple statements, use a block statement (`{ ... }`) to group those statements.
4.  The update expression `incrementExpression`, if there is one, executes, and control returns to step 2.

**Example**
 The following function contains a `for` statement that counts the number of selected options in a scrolling list (a `Select` object that allows multiple selections). The `for` statement declares the variable `i` and initializes it to zero. It checks that `i` is less than the number of options in the `Select` object, performs the succeeding `if` statement, and increments `i` by one after each pass through the loop.

    <script type="text/javascript">

    function howMany(selectObject) {
       var numberSelected = 0;
       for (var i = 0; i < selectObject.options.length; i++) {
          if (selectObject.options[i].selected)
             numberSelected++;
       }
       return numberSelected;
    }

    </script>
    <form name="selectForm">
       <p>
          <strong>Choose some music types, then click the button below:</strong>
          <br/>
          <select name="musicTypes" multiple="multiple">
             <option selected="selected">R&B</option>
             <option>Jazz</option>
             <option>Blues</option>
             <option>New Age</option>
             <option>Classical</option>
             <option>Opera</option>
          </select>
       </p>
       <p>
          <input type="button" value="How many are selected?"
             onclick="alert ('Number of options selected: ' + howMany(document.selectForm.musicTypes))"/>
       </p>
    </form>

### do...while Statement

The `do...while` statement repeats until a specified condition evaluates to false. A `do...while` statement looks as follows:

    do
       statement
    while (condition);

`statement` executes once before the condition is checked. To execute multiple statements, use a block statement (`{ ... }`) to group those statements. If `condition` is true, the statement executes again. At the end of every execution, the condition is checked. When the condition is false, execution stops and control passes to the statement following `do...while`.

**Example**
 In the following example, the `do` loop iterates at least once and reiterates until i is no longer less than 5.

``` {.brush: .js}
do {
   i += 1;
   document.write(i);
} while (i < 5);
```

### while Statement

A `while` statement executes its statements as long as a specified condition evaluates to true. A `while` statement looks as follows:

``` {.brush: .js}
while (condition)
   statement
```

If the condition becomes false, `statement` within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before `statement` in the loop are executed. If the condition returns true, `statement` is executed and the condition is tested again. If the condition returns false, execution stops and control is passed to the statement following `while`.

To execute multiple statements, use a block statement ({ ... }) to group those statements.

**Example 1**
 The following `while` loop iterates as long as `n` is less than three:

``` {.brush: .js}
n = 0;
x = 0;
while (n < 3) {
   n++;
   x += n;
}
```

With each iteration, the loop increments `n` and adds that value to `x`. Therefore, `x` and `n` take on the following values:

-   After the first pass: `n` = 1 and `x` = 1
-   After the second pass: `n` = 2 and `x` = 3
-   After the third pass: `n` = 3 and `x` = 6

After completing the third pass, the condition `n < 3` is no longer true, so the loop terminates.

**Example 2**
 Avoid infinite loops. Make sure the condition in a loop eventually becomes false; otherwise, the loop will never terminate. The statements in the following `while` loop execute forever because the condition never becomes false:

``` {.brush: .js}
while (true) {
   alert("Hello, world");
}
```

### label Statement

A label provides a statement with an identifier that lets you refer to it elsewhere in your program. For example, you can use a label to identify a loop, and then use the `break` or `continue` statements to indicate whether a program should interrupt the loop or continue its execution.

The syntax of the label statement looks like the following:

``` {.brush: .js}
label :
   statement
```

The value of `label` may be any JavaScript identifier that is not a reserved word. The `statement` that you identify with a label may be any statement.

**Example**
 In this example, the label `markLoop` identifies a `while` loop.

``` {.brush: .js}
markLoop:
while (theMark == true) {
   doSomething();
}
```

### break Statement

Use the `break` statement to terminate a loop, `switch`, or in conjunction with a label statement.

-   When you use `break` without a label, it terminates the innermost enclosing `while`, `do-while`, `for`, or `switch` immediately and transfers control to the following statement.
-   When you use `break` with a label, it terminates the specified labeled statement.

The syntax of the `break` statement looks like this:

1.  `break;`
2.  `break label;`

The first form of the syntax terminates the innermost enclosing loop or `switch`; the second form of the syntax terminates the specified enclosing label statement.

**Example** **1:**
 The following example iterates through the elements in an array until it finds the index of an element whose value is `theValue`:

``` {.brush: .js}
for (i = 0; i < a.length; i++) {
   if (a[i] == theValue)
      break;
}
```

**Example 2:**Breaking to a Label

``` {.brush: .js}
var x = 0;
var z = 0
labelCancelLoops: while (true) {
    console.log("Outer loops: " + x);
    x += 1;
    z = 1;
    while (true) {
        console.log("Inner loops: " + z);
        z += 1;
        if (z === 10 && x === 10) {
            break labelCancelLoops;
        } else if (z === 10) {
            break;
        }
    }
}
```

### continue Statement

The `continue` statement can be used to restart a `while`, `do-while`, `for`, or `label` statement.

-   When you use `continue` without a label, it terminates the current iteration of the innermost enclosing `while`, `do-while` or `for` statement and continues execution of the loop with the next iteration. In contrast to the `break` statement, `continue` does not terminate the execution of the loop entirely. In a `while` loop, it jumps back to the condition. In a `for` loop, it jumps to the `increment-expression`.
-   When you use `continue` with a label, it applies to the looping statement identified with that label.

The syntax of the `continue` statement looks like the following:

1.  `continue`
2.  `continue `*`label`*

**Example 1**
 The following example shows a `while` loop with a `continue` statement that executes when the value of `i` is three. Thus, `n` takes on the values one, three, seven, and twelve.

``` {.brush: .js}
i = 0;
n = 0;
while (i < 5) {
   i++;
   if (i == 3)
      continue;
   n += i;
}
```

**Example 2**
 A statement labeled `checkiandj` contains a statement labeled `checkj`. If `continue` is encountered, the program terminates the current iteration of `checkj` and begins the next iteration. Each time `continue` is encountered, `checkj` reiterates until its condition returns `false`. When `false` is returned, the remainder of the `checkiandj` statement is completed, and `checkiandj` reiterates until its condition returns `false`. When `false` is returned, the program continues at the statement following `checkiandj`.

If `continue` had a label of `checkiandj`, the program would continue at the top of the `checkiandj` statement.

``` {.brush: .js}
checkiandj :
   while (i < 4) {
      document.write(i + "<br/>");
      i += 1;
      checkj :
         while (j > 4) {
            document.write(j + "<br/>");
            j -= 1;
            if ((j % 2) == 0)
               continue checkj;
            document.write(j + " is odd.<br/>");
         }
      document.write("i = " + i + "<br/>");
      document.write("j = " + j + "<br/>");
   }
```

## Object Manipulation Statements

JavaScript uses the `for...in`, `for each...in`, and `with` statements to manipulate objects.

### for...in Statement

The \<a href="/en-US/docs/JavaScript/Reference/Statements/for...in" title="en-US/docs/JavaScript/Reference/Statements/for...in"\>`for...in`\</a\> statement iterates a specified variable over all the properties of an object. For each distinct property, JavaScript executes the specified statements. A `for...in` statement looks as follows:

``` {.brush: .js}
for (variable in object) {
   statements
}
```

**Example**
 The following function takes as its argument an object and the object's name. It then iterates over all the object's properties and returns a string that lists the property names and their values.

``` {.brush: .js}
function dump_props(obj, obj_name) {
   var result = "";
   for (var i in obj) {
      result += obj_name + "." + i + " = " + obj[i] + "<br>";
   }
   result += "<hr>";
   return result;
}
```

For an object `car` with properties `make` and `model`, `result` would be:

``` {.brush: .js}
car.make = Ford
car.model = Mustang
```

**Arrays**
 Although it may be tempting to use this as a way to iterate over \<a href="/en-US/docs/JavaScript/Reference/Global\_Objects/Array" title="en-US/docs/JavaScript/Reference/Global Objects/Array"\>Array\</a\> elements, because the **for...in** statement iterates over user-defined properties in addition to the array elements, if you modify the Array object, such as adding custom properties or methods, the **for...in** statement will return the name of your user-defined properties in addition to the numeric indexes. Thus it is better to use a traditional \<a href="/en-US/docs/JavaScript/Reference/Statements/for" title="en-US/docs/JavaScript/Reference/Statements/for"\>for\</a\> loop with a numeric index when iterating over arrays.

### for each...in Statement

\<a href="/en-US/docs/JavaScript/Reference/Statements/for\_each...in" title="en-US/docs/JavaScript/Reference/Statements/for each...in"\>`for each...in`\</a\> is a loop statement introduced in \<a href="/en-US/docs/JavaScript/New\_in\_JavaScript/1.6" title="en-US/docs/JavaScript/New in JavaScript/1.6"\>JavaScript 1.6\</a\>. It is similar to `for...in`, but iterates over the values of object's properties, not their names.

``` {.brush: .js}
var sum = 0;
var obj = {prop1: 5, prop2: 13, prop3: 8};
for each (var item in obj) {
  sum += item;
}
print(sum); // prints "26", which is 5+13+8
```

## Comments

Comments are author notations that explain what a script does. Comments are ignored by the interpreter. JavaScript supports Java and C++-style comments:

-   Comments on a single line are preceded by a double-slash (//).
-   Comments that span multiple lines are preceded by /\* and followed by \*/:

**Example**
 The following example shows two comments:

``` {.brush: .js}
// This is a single-line comment.

/* This is a multiple-line comment. It can be of any length, and
you can put whatever you want here. */
```

## Exception Handling Statements

You can throw exceptions using the `throw` statement and handle them using the `try...catch` statements.

You can also use the `try...catch` statement to handle Java exceptions (though there is a [Template:bug("391642")](/w/index.php?title=Template:bug(%22391642%22)&action=edit&redlink=1) with this). See \<a href="/en-US/docs/JavaScript/Guide/LiveConnect\_Overview\#Handling\_Java\_Exceptions\_in\_JavaScript" title="en-US/docs/JavaScript/Guide/LiveConnect Overview\#Handling Java Exceptions in JavaScript"\>Handling Java Exceptions in JavaScript\</a\> and \<a href="/en-US/docs/JavaScript/Guide/LiveConnect\_Overview\#JavaScript\_to\_Java\_Communication" title="en-US/docs/JavaScript/Guide/LiveConnect Overview\#JavaScript to Java Communication"\>JavaScript to Java Communication\</a\> for information.

-   [throw Statement](#throw_Statement)
-   [try...catch Statement](#try...catch_Statement)

### Exception Types

Just about any object can be thrown in JavaScript. Nevertheless, not all thrown objects are created equal. While it is fairly common to throw numbers or strings as errors it is frequently more effective to use one of the exception types specifically created for this purpose:

-   \<a href="/en-US/docs/JavaScript/Reference/Global\_Objects\#Error\_constructors"\>ECMAScript exceptions\</a\>
-   \<a href="/en-US/docs/DOM/DOMException" title="en-US/docs/DOM/DOMException"\>DOMException\</a\>
-   \<a href="/en-US/docs/XPCOM\_Interface\_Reference/nsIXPCException" title="en-US/docs/nsIXPCException"\>nsIXPCException\</a\> (\<a href="/en-US/docs/XPConnect" title="en-US/docs/XPConnect"\>XPConnect\</a\>)

### throw Statement

Use the `throw` statement to throw an exception. When you throw an exception, you specify the expression containing the value to be thrown:

``` {.brush: .js}
throw expression;
```

You may throw any expression, not just expressions of a specific type. The following code throws several exceptions of varying types:

``` {.brush: .js}
throw "Error2";
throw 42;
throw true;
throw {toString: function() { return "I'm an object!"; } };
```

**Note:** You can specify an object when you throw an exception. You can then reference the object's properties in the `catch` block. The following example creates an object `myUserException` of type `UserException` and uses it in a throw statement.

``` {.brush: .js}
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
throw new UserException("Value too high");
```

### try...catch Statement

The `try...catch` statement marks a block of statements to try, and specifies one or more responses should an exception be thrown. If an exception is thrown, the `try...catch` statement catches it.

The `try...catch` statement consists of a `try` block, which contains one or more statements, and zero or more `catch` blocks, containing statements that specify what to do if an exception is thrown in the `try` block. That is, you want the `try` block to succeed, and if it does not succeed, you want control to pass to the `catch` block. If any statement within the `try` block (or in a function called from within the `try` block) throws an exception, control immediately shifts to the `catch` block. If no exception is thrown in the `try` block, the `catch` block is skipped. The `finally` block executes after the `try` and `catch` blocks execute but before the statements following the `try...catch` statement.

The following example uses a `try...catch` statement. The example calls a function that retrieves a month name from an array based on the value passed to the function. If the value does not correspond to a month number (1-12), an exception is thrown with the value `"InvalidMonthNo"` and the statements in the `catch` block set the `monthName` variable to `unknown`.

``` {.brush: .js}
function getMonthName (mo) {
    mo=mo-1; // Adjust month number for array index (1=Jan, 12=Dec)
    var months=new Array("Jan","Feb","Mar","Apr","May","Jun","Jul",
          "Aug","Sep","Oct","Nov","Dec");
    if (months[mo] != null) {
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
```

#### The catch Block

You can use a `catch` block to handle all exceptions that may be generated in the `try` block.

``` {.brush: .js}
catch (catchID) {
  statements
}
```

The `catch` block specifies an identifier (`catchID` in the preceding syntax) that holds the value specified by the `throw` statement; you can use this identifier to get information about the exception that was thrown. JavaScript creates this identifier when the `catch` block is entered; the identifier lasts only for the duration of the `catch` block; after the `catch` block finishes executing, the identifier is no longer available.

For example, the following code throws an exception. When the exception occurs, control transfers to the `catch` block.

``` {.brush: .js}
try {
   throw "myException" // generates an exception
}
catch (e) {
// statements to handle any exceptions
   logMyErrors(e) // pass exception object to error handler
}
```

#### The finally Block

The `finally` block contains statements to execute after the `try` and `catch` blocks execute but before the statements following the `try...catch` statement. The `finally` block executes whether or not an exception is thrown. If an exception is thrown, the statements in the `finally` block execute even if no `catch` block handles the exception.

You can use the `finally` block to make your script fail gracefully when an exception occurs; for example, you may need to release a resource that your script has tied up. The following example opens a file and then executes statements that use the file (server-side JavaScript allows you to access files). If an exception is thrown while the file is open, the `finally` block closes the file before the script fails.

``` {.brush: .js}
openMyFile();
try {
    writeMyFile(theData); //This may throw a error
}catch(e){
    handleError(e); // If we got a error we handle it
}finally {
    closeMyFile(); // always close the resource
}
```

If the `finally` block returns a value, this value becomes the return value of the entire `try-catch-finally` production, regardless of any `return` statements in the `try` and `catch` blocks:

``` {.brush: .js}
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
```

#### Nesting try...catch Statements

You can nest one or more `try...catch` statements. If an inner `try...catch` statement does not have a `catch` block, the enclosing `try...catch` statement's `catch` block is checked for a match.

### Utilizing Error objects

Depending on the type of error, you may be able to use the 'name' and 'message' properties to get a more refined message. 'name' provides the general class of Error (e.g., 'DOMException' or 'Error'), while 'message' generally provides a more succinct message than one would get by converting the error object to a string.

If you are throwing your own exceptions, in order to take advantage of these properties (such as if your catch block doesn't discriminate between your own exceptions and system ones), you can use the Error constructor. For example:

``` {.brush: .js}
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
}
```

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/Statements)

