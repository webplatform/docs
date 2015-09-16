---
title: About LiveConnect
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/LiveConnect_Overview)'
readiness: 'Out of Date'
summary: 'This chapter describes using LiveConnect technology to let Java and JavaScript code communicate with each other. The chapter assumes you are familiar with Java programming.'
tags:
  - Tutorials
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/liveconnect/guides/JavaScript/Statements
    - concepts/programming/javascript/liveconnect/guides/JavaScript/closures
uri: concepts/programming/javascript/liveconnect

---
## Summary

This chapter describes using LiveConnect technology to let Java and JavaScript code communicate with each other. The chapter assumes you are familiar with Java programming.

## Working with Wrappers

In JavaScript, a *wrapper* is an object of the target language data type that encloses an object of the source language. When programming in JavaScript, you can use a wrapper object to access methods and fields of the Java object; calling a method or accessing a property on the wrapper results in a call on the Java object. On the Java side, JavaScript objects are wrapped in an instance of the class `netscape.javascript.JSObject` and passed to Java.

When a JavaScript object is sent to Java, the runtime engine creates a Java wrapper of type `JSObject`; when a `JSObject` is sent from Java to JavaScript, the runtime engine unwraps it to its original JavaScript object type. The `JSObject` class provides an interface for invoking JavaScript methods and examining JavaScript properties.

## JavaScript to Java Communication

When you refer to a Java package or class, or work with a Java object or array, you use one of the special LiveConnect objects. All JavaScript access to Java takes place with these objects, which are summarized in the following table.

|Object|Description|
|:-----|:----------|
|`JavaArray`|A wrapped Java array, accessed from within JavaScript code.|
|`JavaClass`|A JavaScript reference to a Java class.|
|`JavaObject`|A wrapped Java object, accessed from within JavaScript code.|
|`JavaPackage`|A JavaScript reference to a Java package.|

**Note**: Because Java is a strongly typed language and JavaScript is weakly typed, the JavaScript runtime engine converts argument values into the appropriate data types for the other language when you use LiveConnect. See [Data Type Conversion](#Data_Type_Conversion) for complete information.

In some ways, the existence of the LiveConnect objects is transparent, because you interact with Java in a fairly intuitive way. For example, you can create a Java `String` object and assign it to the JavaScript variable `myString` by using the `new` operator with the Java constructor, as follows:

    var myString = new java.lang.String("Hello world");

In the previous example, the variable `myString` is a `JavaObject` because it holds an instance of the Java object `String`. As a `JavaObject`, `myString` has access to the public instance methods of `java.lang.String` and its superclass, `java.lang.Object`. These Java methods are available in JavaScript as methods of the `JavaObject`, and you can call them as follows:

    myString.length(); // returns 11

Static members can be called directly on the JavaClass object.

    alert(java.lang.Integer.MAX_VALUE); //alerts 2147483647

### The Packages Object

If a Java class is not part of the `java`, `sun`, or `netscape` packages, you access it with the `Packages` object. For example, suppose the Redwood corporation uses a Java package called `redwood` to contain various Java classes that it implements. To create an instance of the `HelloWorld` class in `redwood`, you access the constructor of the class as follows:

    var red = new Packages.redwood.HelloWorld();

You can also access classes in the default package (that is, classes that don't explicitly name a package). For example, if the HelloWorld class is directly in the `CLASSPATH` and not in a package, you can access it as follows:

    var red = new Packages.HelloWorld();

The LiveConnect `java`, `sun`, and `netscape` objects provide shortcuts for commonly used Java packages. For example, you can use the following:

    var myString = new java.lang.String("Hello world");

instead of the longer version:

    var myString = new Packages.java.lang.String("Hello world");

### Working with Java Arrays

When any Java method creates an array and you reference that array in JavaScript, you are working with a `JavaArray`. For example, the following code creates the `JavaArray x` with ten elements of type int:

    var x = java.lang.reflect.Array.newInstance(java.lang.Integer, 10);

Like the JavaScript `Array` object, `JavaArray` has a `length` property which returns the number of elements in the array. Unlike `Array.length`, `JavaArray.length` is a read-only property, because the number of elements in a Java array are fixed at the time of creation.

### Package and Class References

Simple references to Java packages and classes from JavaScript create the `JavaPackage` and `JavaClass` objects. In the earlier example about the Redwood corporation, for example, the reference Packages.redwood is a JavaPackage object. Similarly, a reference such as `java.lang.String` is a `JavaClass` object.

Most of the time, you don't have to worry about the `JavaPackage` and `JavaClass` objects—you just work with Java packages and classes, and LiveConnect creates these objects transparently. There are cases where LiveConnect will fail to load a class, and you will need to manually load it like this:

    var Widgetry = java.lang.Thread.currentThread().getContextClassLoader().loadClass("org.mywidgets.Widgetry");

In JavaScript 1.3 and earlier, `JavaClass` objects are not automatically converted to instances of `java.lang.Class` when you pass them as parameters to Java methods—you must create a wrapper around an instance of `java.lang.Class`. In the following example, the `forName` method creates a wrapper object `theClass`, which is then passed to the `newInstance` method to create an array.

    // JavaScript 1.3
    var theClass = java.lang.Class.forName("java.lang.String");
    var theArray = java.lang.reflect.Array.newInstance(theClass, 5);

In JavaScript 1.4 and later, you can pass a `JavaClass` object directly to a method, as shown in the following example:

    // JavaScript 1.4
    var theArray = java.lang.reflect.Array.newInstance(java.lang.String, 5);

### Arguments of Type char

In JavaScript 1.4 and later, you can pass a one-character string to a Java method which requires an argument of type `char`. For example, you can pass the string "H" to the `Character` constructor as follows:

    var c = new java.lang.Character("H");

In JavaScript 1.3 and earlier, you must pass such methods an integer which corresponds to the Unicode value of the character. For example, the following code also assigns the value "H" to the variable `c`:

    var c = new java.lang.Character(72);

### Handling Java Exceptions in JavaScript

When Java code fails at run time, it throws an exception. If your JavaScript code accesses a Java data member or method and fails, the Java exception is passed on to JavaScript for you to handle. Beginning with JavaScript 1.4, you can catch this exception in a `try...catch` statement. (Although this functionality (along with some others) had been broken in Gecko 1.9 (see [bug 391642](https://bugzilla.mozilla.org/show_bug.cgi?id=391642)) as the Mozilla-specific LiveConnect code had not been maintained inside Mozilla, with Java 6 update 11 and 12 building support for reliance on Mozilla's implementation of the generic (and cross-browser) [NPAPI](http://developer.mozilla.org/en-US/docs/Plugins) plugin code, this has again been fixed.)

For example, suppose you are using the Java `forName` method to assign the name of a Java class to a variable called `theClass`. The `forName` method throws an exception if the value you pass it does not evaluate to the name of a Java class. Place the `forName` assignment statement in a `try` block to handle the exception, as follows:

    function getClass(javaClassName) {
       try {
          var theClass = java.lang.Class.forName(javaClassName);
       } catch (e) {
          return ("The Java exception is " + e);
       }
       return theClass;
    }

In this example, if `javaClassName` evaluates to a legal class name, such as "java.lang.String", the assignment succeeds. If `javaClassName` evaluates to an invalid class name, such as "String", the `getClass` function catches the exception and returns something similar to the following:

    The Java exception is java.lang.ClassNotFoundException: String

For specialized handling based on the exception type, use the `instanceof` operator:

    try {
      // ...
    } catch (e) {
      if (e instanceof java.io.FileNotFound) {
         // handling for FileNotFound
      } else {
        throw e;
      }
    }

See [Exception Handling Statements](http://docs.webplatform.org/en-US/docs/JavaScript/Guide/Statements#Exception_Handling_Statements) for more information about JavaScript exceptions.

## Java to JavaScript Communication

If you want to use JavaScript objects in Java, you must import the `netscape.javascript` package into your Java file. This package defines the following classes:

-   `netscape.javascript.JSObject` allows Java code to access JavaScript methods and properties.
-   `netscape.javascript.JSException` allows Java code to handle JavaScript errors.

### Locating the LiveConnect classes

In older versions of the Netscape browser, these classes were distributed along with the browser. Starting with JavaScript 1.2, these classes are delivered in a .jar file; in previous versions of JavaScript, these classes are delivered in a .zip file. For example, with Netscape Navigator 4 for Windows NT, the classes are delivered in the `java40.jar` file in the `Program\Java\Classes` directory beneath the Navigator directory.

More recently, the classes have been distributed with Oracle's Java Runtime; initially in the file "jaws.jar" in the "jre/lib" directory of the runtime distribution (for JRE 1.3), then in "plugin.jar" in the same location (JRE 1.4 and up).

### Using the LiveConnect classes with the JDK

To access the LiveConnect classes, place the .jar or .zip file in the `CLASSPATH` of the JDK compiler in either of the following ways:

-   Create a `CLASSPATH` environment variable to specify the path and name of .jar or .zip file.
-   Specify the location of .jar or .zip file when you compile by using the `-classpath` command line parameter.

You can specify an environment variable in Windows NT by double-clicking the System icon in the Control Panel and creating a user environment variable called `CLASSPATH` with a value similar to the following:

    C:\Program Files\Java\jre1.4.1\lib\plugin.jar

See the Sun JDK documentation for more information about `CLASSPATH`.

**Note**: Because Java is a strongly typed language and JavaScript is weakly typed, the JavaScript runtime engine converts argument values into the appropriate data types for the other language when you use LiveConnect. See [Data Type Conversions](#Data_Type_Conversions) for complete information.

### Using the LiveConnect Classes

All JavaScript objects appear within Java code as instances of `netscape.javascript.JSObject`. When you call a method in your Java code, you can pass it a JavaScript object as one of its argument. To do so, you must define the corresponding formal parameter of the method to be of type `JSObject`.

Also, any time you use JavaScript objects in your Java code, you should put the call to the JavaScript object inside a `try...catch` statement which handles exceptions of type `netscape.javascript.JSException`. This allows your Java code to handle errors in JavaScript code execution which appear in Java as exceptions of type `JSException`.

#### Accessing JavaScript with JSObject

For example, suppose you are working with the Java class called `JavaDog`. As shown in the following code, the `JavaDog` constructor takes the JavaScript object `jsDog`, which is defined as type `JSObject`, as an argument:

    import netscape.javascript.*;

    public class JavaDog{
        public String dogBreed;
        public String dogColor;
        public String dogSex;

        // define the class constructor
        public JavaDog(JSObject jsDog){
            // use try...catch to handle JSExceptions here
            this.dogBreed = (String)jsDog.getMember("breed");
            this.dogColor = (String)jsDog.getMember("color");
            this.dogSex = (String)jsDog.getMember("sex");
        }
    }

Notice that the `getMember` method of `JSObject` is used to access the properties of the JavaScript object. The previous example uses `getMember` to assign the value of the JavaScript property `jsDog.breed` to the Java data member `JavaDog.dogBreed`.

**Note:** A more realistic example would place the call to `getMember` inside a `try...catch` statement to handle errors of type `JSException`. See Handling JavaScript Exceptions in Java for more information.

To get a better sense of how `getMember` works, look at the definition of the custom JavaScript object `Dog`:

    function Dog(breed,color,sex){
       this.breed = breed;
       this.color = color;
       this.sex = sex;
    }

You can create a JavaScript instance of `Dog` called `gabby` as follows:

    var gabby = new Dog("lab", "chocolate", "female");

If you evaluate `gabby.color`, you can see that it has the value "chocolate". Now suppose you create an instance of `JavaDog` in your JavaScript code by passing the `gabby` object to the constructor as follows:

    var javaDog = new Packages.JavaDog(gabby);

If you evaluate `javaDog.dogColor`, you can see that it also has the value "chocolate", because the `getMember` method in the Java constructor assigns `dogColor` the value of `gabby.color`.

#### Handling JavaScript Exceptions in Java

When JavaScript code called from Java fails at run time, it throws an exception. If you are calling the JavaScript code from Java, you can catch this exception in a `try...catch` statement. The JavaScript exception is available to your Java code as an instance of `netscape.javascript.JSException`.

`JSException` is a Java wrapper around any exception type thrown by JavaScript, similar to the way that instances of `JSObject` are wrappers for JavaScript objects. Use `JSException` when you are evaluating JavaScript code in Java.

When you are evaluating JavaScript code in Java, the following situations can cause run-time errors:

-   The JavaScript code is not evaluated, either due to a JavaScript compilation error or to some other error that occurred at run time. The JavaScript interpreter generates an error message that is converted into an instance of `JSException`.
-   Java successfully evaluates the JavaScript code, but the JavaScript code executes an unhandled `throw` statement. JavaScript throws an exception that is wrapped as an instance of `JSException`. Use the `getWrappedException` method of `JSException` to unwrap this exception in Java.

For example, suppose the Java object `eTest` evaluates the string `jsCode` that you pass to it. You can respond to either type of run-time error the evaluation causes by implementing an exception handler such as the following:

    import netscape.javascript.JSObject;
    import netscape.javascript.JSException;

    public class eTest {
        public static Object doit(JSObject obj, String jsCode) {
            try {
                obj.eval(jsCode);
            } catch (JSException e) {
                if (e.getWrappedException() == null)
                    return e;
                return e.getWrappedException();
            }
            return null;
        }
    }

In this example, the code in the `try` block attempts to evaluate the string `jsCode` that you pass to it. Let's say you pass the string "`myFunction()`" as the value of `jsCode`. If `myFunction` is not defined as a JavaScript function, the JavaScript interpreter cannot evaluate `jsCode`. The interpreter generates an error message, the Java handler catches the message, and the `doit` method returns an instance of `netscape.javascript.JSException`.

However, suppose `myFunction` is defined in JavaScript as follows:

    function myFunction() {
       try {
          if (theCondition == true) {
             return "Everything's ok";
          } else {
             throw "JavaScript error occurred";
          }
       } catch (e) {
          if (canHandle == true) {
             handleIt();
          } else {
             throw e;
          }
       }
    }

If `theCondition` is false, the function throws an exception. The exception is caught in the JavaScript code, and if `canHandle` is true, JavaScript handles it. If `canHandle` is false, the exception is rethrown, the Java handler catches it, and the `doit` method returns a Java string:

    JavaScript error occurred

See [Exception Handling Statements](/w/index.php?title=concepts/programming/javascript/liveconnect/guides/JavaScript/Statements&action=edit&redlink=1) for complete information about JavaScript exceptions.

#### Backward Compatibility

In JavaScript 1.3 and earlier versions, the `JSException` class had three public constructors which optionally took a string argument, specifying the detail message or other information for the exception. The `getWrappedException` method was not available.

Use a `try...catch` statement such as the following to handle LiveConnect exceptions in JavaScript 1.3 and earlier versions:

    try {
       global.eval("foo.bar = 999;");
    } catch (Exception e) {
       if (e instanceof JSException) {
          jsCodeFailed();
       } else {
          otherCodeFailed();
       }
    }

In this example, the `eval` statement fails if `foo` is not defined. The `catch` block executes the `jsCodeFailed` method if the `eval` statement in the `try` block throws a `JSException`; the `otherCodeFailed` method executes if the `try` block throws any other error.

## Data Type Conversions

Because Java is a strongly typed language and JavaScript is weakly typed, the JavaScript runtime engine converts argument values into the appropriate data types for the other language when you use LiveConnect. These conversions are described in the following sections:

-   [JavaScript to Java Conversions](#JavaScript_to_Java_Conversions)
-   [Java to JavaScript Conversions](#Java_to_JavaScript_Conversions)

### JavaScript to Java Conversions

When you call a Java method and pass it parameters from JavaScript, the data types of the parameters you pass in are converted according to the rules described in the following sections:

-   [Number Values](#Number_Values)
-   [Boolean Values](#Boolean_Value)
-   [String Values](#String_Values)
-   [Undefined Values](#Undefined_Values)
-   [Null Values](#Null_Values)
-   [JavaArray and JavaObject objects](#JavaArray_and_JavaObject_objects)
-   [JavaClass objects](#JavaClass_objects)
-   [Other JavaScript objects](#Other_JavaScript_objects)

The return values of methods of `netscape.javascript.JSObject` are always converted to instances of `java.lang.Object`. The rules for converting these return values are also described in these sections.

For example, if `JSObject.eval` returns a JavaScript number, you can find the rules for converting this number to an instance of `java.lang.Object` in [Number Values](#Number_Values).

#### Number Values

When you pass JavaScript number types as parameters to Java methods, Java converts the values according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">double</td>
<td align="left"><ul>
<li>The exact value is transferred to Java without rounding and without a loss of magnitude or sign.</li>
<li><code>NaN</code> is converted to NaN.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">java.lang.Double<br /> java.lang.Object</td>
<td align="left">A new instance of <code>java.lang.Double</code> is created, and the exact value is transferred to Java without rounding and without a loss of magnitude or sign.</td>
</tr>
<tr class="odd">
<td align="left">float</td>
<td align="left"><ul>
<li>Values are rounded to float precision.</li>
<li>Values which are too large or small to be represented are rounded to +infinity or -infinity.</li>
<li><code>NaN</code> is converted to <code>NaN</code>.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>byte<br /> char<br /> int<br /> long<br /> short</p></td>
<td align="left"><ul>
<li>Values are rounded using round-to-negative-infinity mode.</li>
<li>Values which are too large or small to be represented result in a run-time error.</li>
<li><code>NaN</code> can not be converted and results in a run-time error.</li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><code>java.lang.String</code></td>
<td align="left"><p>Values are converted to strings. For example:</p>
<ul>
<li>237 becomes &quot;237&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">boolean</td>
<td align="left"><ul>
<li>0 and <code>NaN</code> values are converted to false.</li>
<li>Other values are converted to true.</li>
</ul></td>
</tr>
</tbody>
</table>

When a JavaScript number is passed as a parameter to a Java method which expects an instance of `java.lang.String`, the number is converted to a string. Use the `equals()` method to compare the result of this conversion with other string values.

#### Boolean Values

When you pass JavaScript Boolean types as parameters to Java methods, Java converts the values according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">boolean</td>
<td align="left">All values are converted directly to the Java equivalents.</td>
</tr>
<tr class="even">
<td align="left"><code>java.lang.Boolean</code><br /><code>java.lang.Object</code></td>
<td align="left">A new instance of <code>java.lang.Boolean</code> is created. Each parameter creates a new instance, not one instance with the same primitive value.</td>
</tr>
<tr class="odd">
<td align="left"><code>java.lang.String</code></td>
<td align="left"><p>Values are converted to strings. For example:</p>
<ul>
<li>true becomes &quot;true&quot;</li>
<li>false becomes &quot;false&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>byte<br /> char<br /> double<br /> float<br /> int<br /> long<br /> short</p></td>
<td align="left"><ul>
<li>true becomes 1</li>
<li>false becomes 0</li>
</ul></td>
</tr>
</tbody>
</table>

When a JavaScript Boolean is passed as a parameter to a Java method which expects an instance of `java.lang.String`, the Boolean is converted to a string. Use the == operator to compare the result of this conversion with other string values.

#### String Values

When you pass JavaScript string types as parameters to Java methods, Java converts the values according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>java.lang.String</code><br /><code>java.lang.Object</code></td>
<td align="left"><p>JavaScript 1.4:</p>
<ul>
<li>A JavaScript string is converted to an instance of <code>java.lang.String</code> with a Unicode value.</li>
</ul>
<p>JavaScript 1.3 and earlier:</p>
<ul>
<li>A JavaScript string is converted to an instance of <code>java.lang.String</code> with an ASCII value.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>byte<br /> double<br /> float<br /> int<br /> long<br /> short<br /></p></td>
<td align="left">All values are converted to numbers as described in ECMA-262. The JavaScript string value is converted to a number according to the rules described in ECMA-262.</td>
</tr>
<tr class="odd">
<td align="left">char</td>
<td align="left"><p>JavaScript 1.4:</p>
<ul>
<li>One-character strings are converted to Unicode characters.</li>
<li>All other values are converted to numbers.</li>
</ul>
<p>JavaScript 1.3 and earlier:</p>
<ul>
<li>All values are converted to numbers.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">boolean</td>
<td align="left"><ul>
<li>The empty string becomes false.</li>
<li>All other values become true.</li>
</ul></td>
</tr>
</tbody>
</table>

#### Undefined Values

When you pass undefined JavaScript values as parameters to Java methods, Java converts the values according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>java.lang.String</code><br /><code>java.lang.Object</code></td>
<td align="left">The value is converted to an instance of java.lang.String whose value is the string &quot;undefined&quot;.</td>
</tr>
<tr class="even">
<td align="left">boolean</td>
<td align="left">The value becomes false.</td>
</tr>
<tr class="odd">
<td align="left">double<br /> float</td>
<td align="left">The value becomes <code>NaN</code>.</td>
</tr>
<tr class="even">
<td align="left"><p>byte<br /> char<br /> int<br /> long<br /> short</p></td>
<td align="left">The value becomes 0.</td>
</tr>
</tbody>
</table>

The undefined value conversion is possible in JavaScript 1.3 and later versions only. Earlier versions of JavaScript do not support undefined values.

When a JavaScript undefined value is passed as a parameter to a Java method which expects an instance of `java.lang.String`, the undefined value is converted to a string. Use the == operator to compare the result of this conversion with other string values.

#### Null Values

When you pass null JavaScript values as parameters to Java methods, Java converts the values according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Any class<br /> Any interface type</td>
<td align="left">The value becomes null.</td>
</tr>
<tr class="even">
<td align="left"><p>byte<br /> char<br /> double<br /> float<br /> int<br /> long<br /> short</p></td>
<td align="left">The value becomes 0.</td>
</tr>
<tr class="odd">
<td align="left">boolean</td>
<td align="left">The value becomes false.</td>
</tr>
</tbody>
</table>

#### JavaArray and JavaObject objects

In most situations, when you pass a JavaScript `JavaArray` or `JavaObject` as a parameter to a Java method, Java simply unwraps the object; in a few situations, the object is coerced into another data type according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Any interface or class that is assignment-compatible with the unwrapped object.</td>
<td align="left">The object is unwrapped.</td>
</tr>
<tr class="even">
<td align="left"><code>java.lang.String</code></td>
<td align="left">The object is unwrapped, the <code>toString</code> method of the unwrapped Java object is called, and the result is returned as a new instance of <code>java.lang.String</code>.</td>
</tr>
<tr class="odd">
<td align="left"><p>byte<br /> char<br /> double<br /> float<br /> int<br /> long<br /> short</p></td>
<td align="left"><p>The object is unwrapped, and either of the following situations occur:</p>
<ul>
<li>If the unwrapped Java object has a <code>doubleValue</code> method, the <code>JavaArray</code> or <code>JavaObject</code> is converted to the value returned by this method.</li>
<li>If the unwrapped Java object does not have a <code>doubleValue</code> method, an error occurs.</li>
</ul></td>
</tr>
<tr class="even">
<td align="left">boolean</td>
<td align="left"><p>In JavaScript 1.3 and later versions, the object is unwrapped and either of the following situations occur:</p>
<ul>
<li>If the object is null, it is converted to false.</li>
<li>If the object has any other value, it is converted to true.</li>
</ul>
<p>In JavaScript 1.2 and earlier versions, the object is unwrapped and either of the following situations occur:</p>
<ul>
<li>If the unwrapped object has a booleanValue method, the source object is converted to the return value.</li>
<li>If the object does not have a booleanValue method, the conversion fails.</li>
</ul></td>
</tr>
</tbody>
</table>

An interface or class is assignment-compatible with an unwrapped object if the unwrapped object is an instance of the Java parameter type. That is, the following statement must return true:

    unwrappedObject instanceof parameterType;

#### JavaClass objects

When you pass a JavaScript `JavaClass` object as a parameter to a Java method, Java converts the object according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>java.lang.Class</code></td>
<td align="left">The object is unwrapped.</td>
</tr>
<tr class="even">
<td align="left"><code>netscape.javascript.JSObject</code><br /><code>java.lang.Object</code></td>
<td align="left">The <code>JavaClass</code> object is wrapped in a new instance of <code>netscape.javascript.JSObject</code>.</td>
</tr>
<tr class="odd">
<td align="left"><code>java.lang.String</code></td>
<td align="left">The object is unwrapped, the <code>toString</code> method of the unwrapped Java object is called, and the result is returned as a new instance of <code>java.lang.String</code>.</td>
</tr>
<tr class="even">
<td align="left">boolean</td>
<td align="left"><p>In JavaScript 1.3 and later versions, the object is unwrapped and either of the following situations occur:</p>
<ul>
<li>If the object is null, it is converted to false.</li>
<li>If the object has any other value, it is converted to true.</li>
</ul>
<p>In JavaScript 1.2 and earlier versions, the object is unwrapped and either of the following situations occur:</p>
<ul>
<li>If the unwrapped object has a booleanValue method, the source object is converted to the return value.</li>
<li>If the object does not have a booleanValue method, the conversion fails.</li>
</ul></td>
</tr>
</tbody>
</table>

#### Other JavaScript objects

When you pass any other JavaScript object as a parameter to a Java method, Java converts the object according to the rules described in the following table:

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Java parameter type</th>
<th align="left">Conversion rules</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>netscape.javascript.JSObject</code><br /><code>java.lang.Object</code></td>
<td align="left">The object is wrapped in a new instance of <code>netscape.javascript.JSObject</code>.</td>
</tr>
<tr class="even">
<td align="left"><code>java.lang.String</code></td>
<td align="left">The object is unwrapped, the <code>toString</code> method of the unwrapped object is called, and the result is returned as a new instance of <code>java.lang.String</code>.</td>
</tr>
<tr class="odd">
<td align="left"><p>byte<br /> char<br /> double<br /> float<br /> int<br /> long<br /> short</p></td>
<td align="left">The object is converted to a value using the logic of the <code>ToPrimitive</code> operator described in ECMA-262. The <em>PreferredType</em> hint used with this operator is Number.</td>
</tr>
<tr class="even">
<td align="left">boolean</td>
<td align="left"><p>In JavaScript 1.3 and later versions, the object is unwrapped and either of the following situations occur:</p>
<ul>
<li>If the object is null, it is converted to false.</li>
<li>If the object has any other value, it is converted to true.</li>
</ul>
<p>In JavaScript 1.2 and earlier versions, the object is unwrapped and either of the following situations occur:</p>
<ul>
<li>If the unwrapped object has a booleanValue method, the source object is converted to the return value.</li>
<li>If the object does not have a booleanValue method, the conversion fails.</li>
</ul></td>
</tr>
</tbody>
</table>

### Java to JavaScript Conversions

Values passed from Java to JavaScript are converted as follows:

-   Java byte, char, short, int, long, float, and double are converted to JavaScript numbers.
-   A Java boolean is converted to a JavaScript boolean.
-   An object of class `netscape.javascript.JSObject` is converted to the original JavaScript object.
-   Java arrays are converted to a JavaScript pseudo-Array object; this object behaves just like a JavaScript `Array` object: you can access it with the syntax `arrayName[index]` (where `index` is an integer), and determine its length with `arrayName.length`.
-   A Java object of any other class is converted to a JavaScript wrapper, which can be used to access methods and fields of the Java object:
    -   Converting this wrapper to a string calls the `toString` method on the original object.
    -   Converting to a number calls the `doubleValue` method, if possible, and fails otherwise.
    -   Converting to a boolean in JavaScript 1.3 and later versions returns false if the object is null, and true otherwise.
    -   Converting to a boolean in JavaScript 1.2 and earlier versions calls the `booleanValue` method, if possible, and fails otherwise.

Note that instances of java.lang.Double and java.lang.Integer are converted to JavaScript objects, not to JavaScript numbers. Similarly, instances of java.lang.String are also converted to JavaScript objects, not to JavaScript strings.

Java `String` objects also correspond to JavaScript wrappers. If you call a JavaScript method that requires a JavaScript string and pass it this wrapper, you'll get an error. Instead, convert the wrapper to a JavaScript string by appending the empty string to it, as shown here:

    var JavaString = JavaObj.methodThatReturnsAString();
    var JavaScriptString = JavaString + "";

<span style="float: left">[« Previous](/w/index.php?title=concepts/programming/javascript/liveconnect/guides/JavaScript/closures&action=edit&redlink=1)</span>
