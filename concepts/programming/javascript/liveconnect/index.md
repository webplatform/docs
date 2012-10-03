{{Page_Title|About LiveConnect}}
{{Flags
|Content=Not Neutral
|Editorial notes=Add info about other browser support for LiveConnect.
}}
{{Summary_Section|This chapter describes using LiveConnect technology to let Java and JavaScript code communicate with each other. The chapter assumes you are familiar with Java programming.

}}
{{Tutorial
|Content===Working with Wrappers==

In JavaScript, a ''wrapper'' is an object of the target language data type that encloses an object of the source language. When programming in JavaScript, you can use a wrapper object to access methods and fields of the Java object; calling a method or accessing a property on the wrapper results in a call on the Java object. On the Java side, JavaScript objects are wrapped in an instance of the class <code>netscape.javascript.JSObject</code> and passed to Java.

When a JavaScript object is sent to Java, the runtime engine creates a Java wrapper of type <code>JSObject</code><nowiki>; when a </nowiki><code>JSObject</code> is sent from Java to JavaScript, the runtime engine unwraps it to its original JavaScript object type. The <code>JSObject</code> class provides an interface for invoking JavaScript methods and examining JavaScript properties.

==JavaScript to Java Communication==

When you refer to a Java package or class, or work with a Java object or array, you use one of the special LiveConnect objects. All JavaScript access to Java takes place with these objects, which are summarized in the following table.

{{{!}} class="standard-table"
{{!}}+  Table 9.1 The LiveConnect Objects
{{!}}-
! scope="col" {{!}} Object
! scope="col" {{!}} Description
{{!}}-
{{!}} <code>JavaArray</code>
{{!}} A wrapped Java array, accessed from within JavaScript code.
{{!}}-
{{!}} <code>JavaClass</code>
{{!}} A JavaScript reference to a Java class.
{{!}}-
{{!}} <code>JavaObject</code>
{{!}} A wrapped Java object, accessed from within JavaScript code.
{{!}}-
{{!}} <code>JavaPackage</code>
{{!}} A JavaScript reference to a Java package.
{{!}}}

{{Note|Because Java is a strongly typed language and JavaScript is weakly typed, the JavaScript runtime engine converts argument values into the appropriate data types for the other language when you use LiveConnect. See [[#Data_Type_Conversion|Data Type Conversion]] for complete information.}}


In some ways, the existence of the LiveConnect objects is transparent, because you interact with Java in a fairly intuitive way. For example, you can create a Java <code>String</code> object and assign it to the JavaScript variable <code>myString</code> by using the <code>new</code> operator with the Java constructor, as follows:

 var myString = new java.lang.String("Hello world");

In the previous example, the variable <code>myString</code> is a <code>JavaObject</code> because it holds an instance of the Java object <code>String</code>. As a <code>JavaObject</code>, <code>myString</code> has access to the public instance methods of <code>java.lang.String</code> and its superclass, <code>java.lang.Object</code>. These Java methods are available in JavaScript as methods of the <code>JavaObject</code>, and you can call them as follows:

 myString.length(); // returns 11

Static members can be called directly on the JavaClass object.

 alert(java.lang.Integer.MAX_VALUE); //alerts 2147483647

===The Packages Object===

If a Java class is not part of the <code>java</code>, <code>sun</code>, or <code>netscape</code> packages, you access it with the <code>Packages</code> object. For example, suppose the Redwood corporation uses a Java package called <code>redwood</code> to contain various Java classes that it implements. To create an instance of the <code>HelloWorld</code> class in <code>redwood</code>, you access the constructor of the class as follows:

 var red = new Packages.redwood.HelloWorld();

You can also access classes in the default package (that is, classes that don't explicitly name a package). For example, if the HelloWorld class is directly in the <code>CLASSPATH</code> and not in a package, you can access it as follows:

 var red = new Packages.HelloWorld();

The LiveConnect <code>java</code>, <code>sun</code>, and <code>netscape</code> objects provide shortcuts for commonly used Java packages. For example, you can use the following:

 var myString = new java.lang.String("Hello world");

instead of the longer version:

 var myString = new Packages.java.lang.String("Hello world");

===Working with Java Arrays===

When any Java method creates an array and you reference that array in JavaScript, you are working with a <code>JavaArray</code>. For example, the following code creates the <code>JavaArray x</code> with ten elements of type int:

 var x = java.lang.reflect.Array.newInstance(java.lang.Integer, 10);

Like the JavaScript <code>Array</code> object, <code>JavaArray</code> has a <code>length</code> property which returns the number of elements in the array. Unlike <code>Array.length</code>, <code>JavaArray.length</code> is a read-only property, because the number of elements in a Java array are fixed at the time of creation.

===Package and Class References===

Simple references to Java packages and classes from JavaScript create the <code>JavaPackage</code> and <code>JavaClass</code> objects. In the earlier example about the Redwood corporation, for example, the reference Packages.redwood is a JavaPackage object. Similarly, a reference such as <code>java.lang.String</code> is a <code>JavaClass</code> object.

Most of the time, you don't have to worry about the <code>JavaPackage</code> and <code>JavaClass</code> objects—you just work with Java packages and classes, and LiveConnect creates these objects transparently. There are cases where LiveConnect will fail to load a class, and you will need to manually load it like this:

 var Widgetry = java.lang.Thread.currentThread().getContextClassLoader().loadClass("org.mywidgets.Widgetry");

In JavaScript 1.3 and earlier, <code>JavaClass</code> objects are not automatically converted to instances of <code>java.lang.Class</code> when you pass them as parameters to Java methods—you must create a wrapper around an instance of <code>java.lang.Class</code>. In the following example, the <code>forName</code> method creates a wrapper object <code>theClass</code>, which is then passed to the <code>newInstance</code> method to create an array.

 // JavaScript 1.3
 var theClass = java.lang.Class.forName("java.lang.String");
 var theArray = java.lang.reflect.Array.newInstance(theClass, 5);

In JavaScript 1.4 and later, you can pass a <code>JavaClass</code> object directly to a method, as shown in the following example:

 // JavaScript 1.4
 var theArray = java.lang.reflect.Array.newInstance(java.lang.String, 5);

===Arguments of Type char===

In JavaScript 1.4 and later, you can pass a one-character string to a Java method which requires an argument of type <code>char</code>. For example, you can pass the string "H" to the <code>Character</code> constructor as follows:

 var c = new java.lang.Character("H");

In JavaScript 1.3 and earlier, you must pass such methods an integer which corresponds to the Unicode value of the character. For example, the following code also assigns the value "H" to the variable <code>c</code><nowiki>:</nowiki>

 var c = new java.lang.Character(72);

===Handling Java Exceptions in JavaScript===

When Java code fails at run time, it throws an exception. If your JavaScript code accesses a Java data member or method and fails, the Java exception is passed on to JavaScript for you to handle. Beginning with JavaScript 1.4, you can catch this exception in a <code>try...catch</code> statement. (Although this functionality (along with some others) had been broken in Gecko 1.9 (see [https://bugzilla.mozilla.org/show_bug.cgi?id=391642 bug 391642]) as the Mozilla-specific LiveConnect code had not been maintained inside Mozilla, with Java 6 update 11 and 12 building support for reliance on Mozilla's implementation of the generic (and cross-browser) [http://developer.mozilla.org/en-US/docs/Plugins NPAPI] plugin code, this has again been fixed.)

For example, suppose you are using the Java <code>forName</code> method to assign the name of a Java class to a variable called <code>theClass</code>. The <code>forName</code> method throws an exception if the value you pass it does not evaluate to the name of a Java class. Place the <code>forName</code> assignment statement in a <code>try</code> block to handle the exception, as follows:

 function getClass(javaClassName) {
    try {
       var theClass = java.lang.Class.forName(javaClassName);
    } catch (e) {
       return ("The Java exception is " + e);
    }
    return theClass;
 }

In this example, if <code>javaClassName</code> evaluates to a legal class name, such as "java.lang.String", the assignment succeeds. If <code>javaClassName</code> evaluates to an invalid class name, such as "String", the <code>getClass</code> function catches the exception and returns something similar to the following:

 The Java exception is java.lang.ClassNotFoundException: String

For specialized handling based on the exception type, use the <code>instanceof</code> operator:

 try {
   // ...
 } catch (e) {
   if (e instanceof java.io.FileNotFound) {
      // handling for FileNotFound
   } else {
     throw e;
   }
 }

See [http://docs.webplatform.org/en-US/docs/JavaScript/Guide/Statements#Exception_Handling_Statements Exception Handling Statements] for more information about JavaScript exceptions.

==Java to JavaScript Communication==

If you want to use JavaScript objects in Java, you must import the <code>netscape.javascript</code> package into your Java file. This package defines the following classes:

* <code>[https://developer.mozilla.org/docs/JavaScript/Reference/LiveConnect/JSObject netscape.javascript.JSObject]</code> allows Java code to access JavaScript methods and properties.
* <code>[https://developer.mozilla.org/docs/JavaScript/Reference/LiveConnect/JSException netscape.javascript.JSException]</code> allows Java code to handle JavaScript errors.


===Locating the LiveConnect classes===

In older versions of the Netscape browser, these classes were distributed along with the browser. Starting with JavaScript 1.2, these classes are delivered in a .jar file; in previous versions of JavaScript, these classes are delivered in a .zip file. For example, with Netscape Navigator 4 for Windows NT, the classes are delivered in the <code>java40.jar</code> file in the <code>Program\Java\Classes</code> directory beneath the Navigator directory.

More recently, the classes have been distributed with Oracle's Java Runtime; initially in the file "jaws.jar" in the "jre/lib" directory of the runtime distribution (for JRE 1.3), then in "plugin.jar" in the same location (JRE 1.4 and up).

===Using the LiveConnect classes with the JDK===

To access the LiveConnect classes, place the .jar or .zip file in the <code>CLASSPATH</code> of the JDK compiler in either of the following ways:

* Create a <code>CLASSPATH</code> environment variable to specify the path and name of .jar or .zip file.
* Specify the location of .jar or .zip file when you compile by using the <code>-classpath</code> command line parameter.

You can specify an environment variable in Windows NT by double-clicking the System icon in the Control Panel and creating a user environment variable called <code>CLASSPATH</code> with a value similar to the following:

 C:\Program Files\Java\jre1.4.1\lib\plugin.jar

See the Sun JDK documentation for more information about <code>CLASSPATH</code>.

{{Note| Because Java is a strongly typed language and JavaScript is weakly typed, the JavaScript runtime engine converts argument values into the appropriate data types for the other language when you use LiveConnect. See [[#Data_Type_Conversions| Data Type Conversions]] for complete information.}}

===Using the LiveConnect Classes===

All JavaScript objects appear within Java code as instances of <code>netscape.javascript.JSObject</code>. When you call a method in your Java code, you can pass it a JavaScript object as one of its argument. To do so, you must define the corresponding formal parameter of the method to be of type <code>JSObject</code>.

Also, any time you use JavaScript objects in your Java code, you should put the call to the JavaScript object inside a <code>try...catch</code> statement which handles exceptions of type <code>netscape.javascript.JSException</code>. This allows your Java code to handle errors in JavaScript code execution which appear in Java as exceptions of type <code>JSException</code>.

====Accessing JavaScript with JSObject====

For example, suppose you are working with the Java class called <code>JavaDog</code>. As shown in the following code, the <code>JavaDog</code> constructor takes the JavaScript object <code>jsDog</code>, which is defined as type <code>JSObject</code>, as an argument:

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

Notice that the <code>getMember</code> method of <code>JSObject</code> is used to access the properties of the JavaScript object. The previous example uses <code>getMember</code> to assign the value of the JavaScript property <code>jsDog.breed</code> to the Java data member <code>JavaDog.dogBreed</code>.

'''Note:''' A more realistic example would place the call to <code>getMember</code> inside a <code>try...catch</code> statement to handle errors of type <code>JSException</code>. See Handling JavaScript Exceptions in Java for more information.

To get a better sense of how <code>getMember</code> works, look at the definition of the custom JavaScript object <code>Dog</code><nowiki>:</nowiki>

 function Dog(breed,color,sex){
    this.breed = breed;
    this.color = color;
    this.sex = sex;
 }

You can create a JavaScript instance of <code>Dog</code> called <code>gabby</code> as follows:

 var gabby = new Dog("lab", "chocolate", "female");

If you evaluate <code>gabby.color</code>, you can see that it has the value "chocolate". Now suppose you create an instance of <code>JavaDog</code> in your JavaScript code by passing the <code>gabby</code> object to the constructor as follows:

 var javaDog = new Packages.JavaDog(gabby);

If you evaluate <code>javaDog.dogColor</code>, you can see that it also has the value "chocolate", because the <code>getMember</code> method in the Java constructor assigns <code>dogColor</code> the value of <code>gabby.color</code>.

====Handling JavaScript Exceptions in Java====

When JavaScript code called from Java fails at run time, it throws an exception. If you are calling the JavaScript code from Java, you can catch this exception in a <code>try...catch</code> statement. The JavaScript exception is available to your Java code as an instance of <code>netscape.javascript.JSException</code>.

<code>JSException</code> is a Java wrapper around any exception type thrown by JavaScript, similar to the way that instances of <code>JSObject</code> are wrappers for JavaScript objects. Use <code>JSException</code> when you are evaluating JavaScript code in Java.

When you are evaluating JavaScript code in Java, the following situations can cause run-time errors:

* The JavaScript code is not evaluated, either due to a JavaScript compilation error or to some other error that occurred at run time. The JavaScript interpreter generates an error message that is converted into an instance of <code>JSException</code>.
* Java successfully evaluates the JavaScript code, but the JavaScript code executes an unhandled <code>throw</code> statement. JavaScript throws an exception that is wrapped as an instance of <code>JSException</code>. Use the <code>getWrappedException</code> method of <code>JSException</code> to unwrap this exception in Java.

For example, suppose the Java object <code>eTest</code> evaluates the string <code>jsCode</code> that you pass to it. You can respond to either type of run-time error the evaluation causes by implementing an exception handler such as the following:

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

In this example, the code in the <code>try</code> block attempts to evaluate the string <code>jsCode</code> that you pass to it. Let's say you pass the string "<code>myFunction()</code>" as the value of <code>jsCode</code>. If <code>myFunction</code> is not defined as a JavaScript function, the JavaScript interpreter cannot evaluate <code>jsCode</code>. The interpreter generates an error message, the Java handler catches the message, and the <code>doit</code> method returns an instance of <code>netscape.javascript.JSException</code>.

However, suppose <code>myFunction</code> is defined in JavaScript as follows:

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

If <code>theCondition</code> is false, the function throws an exception. The exception is caught in the JavaScript code, and if <code>canHandle</code> is true, JavaScript handles it. If <code>canHandle</code> is false, the exception is rethrown, the Java handler catches it, and the <code>doit</code> method returns a Java string:

 JavaScript error occurred

See [[/guides/JavaScript/Statements#Exception_Handling_Statements|Exception Handling Statements]] for complete information about JavaScript exceptions.

====Backward Compatibility====

In JavaScript 1.3 and earlier versions, the <code>JSException</code> class had three public constructors which optionally took a string argument, specifying the detail message or other information for the exception. The <code>getWrappedException</code> method was not available.

Use a <code>try...catch</code> statement such as the following to handle LiveConnect exceptions in JavaScript 1.3 and earlier versions:

 try {
    global.eval("foo.bar = 999;");
 } catch (Exception e) {
    if (e instanceof JSException) {
       jsCodeFailed();
    } else {
       otherCodeFailed();
    }
 }

In this example, the <code>eval</code> statement fails if <code>foo</code> is not defined. The <code>catch</code> block executes the <code>jsCodeFailed</code> method if the <code>eval</code> statement in the <code>try</code> block throws a <code>JSException</code><nowiki>; the </nowiki><code>otherCodeFailed</code> method executes if the <code>try</code> block throws any other error.

==Data Type Conversions==

Because Java is a strongly typed language and JavaScript is weakly typed, the JavaScript runtime engine converts argument values into the appropriate data types for the other language when you use LiveConnect. These conversions are described in the following sections:

* [[#JavaScript_to_Java_Conversions|JavaScript to Java Conversions]]
* [[#Java_to_JavaScript_Conversions|Java to JavaScript Conversions]]

===JavaScript to Java Conversions===

When you call a Java method and pass it parameters from JavaScript, the data types of the parameters you pass in are converted according to the rules described in the following sections:

* [[#Number_Values|Number Values]]
* [[#Boolean_Value|Boolean Values]]
* [[#String_Values|String Values]]
* [[#Undefined_Values|Undefined Values]]
* [[#Null_Values|Null Values]]
* [[#JavaArray_and_JavaObject_objects|JavaArray and JavaObject objects]]
* [[#JavaClass_objects|JavaClass objects]]
* [[#Other_JavaScript_objects|Other JavaScript objects]]

The return values of methods of <code>netscape.javascript.JSObject</code> are always converted to instances of <code>java.lang.Object</code>. The rules for converting these return values are also described in these sections.

For example, if <code>JSObject.eval</code> returns a JavaScript number, you can find the rules for converting this number to an instance of <code>java.lang.Object</code> in [[#Number_Values|Number Values]].

====Number Values====

When you pass JavaScript number types as parameters to Java methods, Java converts the values according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} double
{{!}}
* The exact value is transferred to Java without rounding and without a loss of magnitude or sign.
* <code>NaN</code> is converted to NaN.
{{!}}-
{{!}} java.lang.Double<br /> java.lang.Object
{{!}} A new instance of <code>java.lang.Double</code> is created, and the exact value is transferred to Java without rounding and without a loss of magnitude or sign.
{{!}}-
{{!}} float
{{!}}
* Values are rounded to float precision.
* Values which are too large or small to be represented are rounded to +infinity or -infinity.
* <code>NaN</code> is converted to <code>NaN</code>.
{{!}}-
{{!}}
byte<br />
char<br /> 
int<br />
long<br />
short
{{!}}
* Values are rounded using round-to-negative-infinity mode.
* Values which are too large or small to be represented result in a run-time error.
* <code>NaN</code> can not be converted and results in a run-time error.
{{!}}-
{{!}} <code>java.lang.String</code>
{{!}}
Values are converted to strings. For example:

* 237 becomes "237"
{{!}}-
{{!}} boolean
{{!}}
* 0 and <code>NaN</code> values are converted to false.
* Other values are converted to true.
{{!}}}

When a JavaScript number is passed as a parameter to a Java method which expects an instance of <code>java.lang.String</code>, the number is converted to a string. Use the <code>equals()</code> method to compare the result of this conversion with other string values.

====Boolean Values====

When you pass JavaScript Boolean types as parameters to Java methods, Java converts the values according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} boolean
{{!}} All values are converted directly to the Java equivalents.
{{!}}-
{{!}} <code>java.lang.Boolean</code><br /><code>java.lang.Object</code>
{{!}} A new instance of <code>java.lang.Boolean</code> is created. Each parameter creates a new instance, not one instance with the same primitive value.
{{!}}-
{{!}} <code>java.lang.String</code>
{{!}}
Values are converted to strings. For example:

* true becomes "true"
* false becomes "false"
{{!}}-
{{!}}
byte<br />
char<br />
double<br />
float<br /> 
int<br /> 
long<br />
short
{{!}}
* true becomes 1
* false becomes 0
{{!}}}

When a JavaScript Boolean is passed as a parameter to a Java method which expects an instance of <code>java.lang.String</code>, the Boolean is converted to a string. Use the == operator to compare the result of this conversion with other string values.

====String Values====

When you pass JavaScript string types as parameters to Java methods, Java converts the values according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} <code>java.lang.String</code><br /><code>java.lang.Object</code>
{{!}}
JavaScript 1.4:

* A JavaScript string is converted to an instance of <code>java.lang.String</code> with a Unicode value.

JavaScript 1.3 and earlier:

* A JavaScript string is converted to an instance of <code>java.lang.String</code> with an ASCII value.
{{!}}-
{{!}}
byte<br />
double<br /> 
float<br />
int<br /> 
long<br /> 
short<br />
{{!}} All values are converted to numbers as described in ECMA-262. The JavaScript string value is converted to a number according to the rules described in ECMA-262.
{{!}}-
{{!}} char
{{!}}
JavaScript 1.4:

* One-character strings are converted to Unicode characters.
* All other values are converted to numbers.

JavaScript 1.3 and earlier:

* All values are converted to numbers.
{{!}}-
{{!}} boolean
{{!}}
* The empty string becomes false.
* All other values become true.
{{!}}}

====Undefined Values====

When you pass undefined JavaScript values as parameters to Java methods, Java converts the values according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} <code>java.lang.String</code><br /><code>java.lang.Object</code>
{{!}} The value is converted to an instance of java.lang.String whose value is the string "undefined".
{{!}}-
{{!}} boolean
{{!}} The value becomes false.
{{!}}-
{{!}} double<br /> float
{{!}} The value becomes <code>NaN</code>.
{{!}}-
{{!}}
byte<br />
char<br /> 
int<br /> 
long<br />
short
{{!}} The value becomes 0.
{{!}}}

The undefined value conversion is possible in JavaScript 1.3 and later versions only. Earlier versions of JavaScript do not support undefined values.

When a JavaScript undefined value is passed as a parameter to a Java method which expects an instance of <code>java.lang.String</code>, the undefined value is converted to a string. Use the == operator to compare the result of this conversion with other string values.

====Null Values====

When you pass null JavaScript values as parameters to Java methods, Java converts the values according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} Any class<br /> Any interface type
{{!}} The value becomes null.
{{!}}-
{{!}}
byte<br />
char<br /> 
double<br /> 
float<br /> 
int<br /> 
long<br />
short
{{!}} The value becomes 0.
{{!}}-
{{!}} boolean
{{!}} The value becomes false.
{{!}}}

====JavaArray and JavaObject objects====

In most situations, when you pass a JavaScript <code>JavaArray</code> or <code>JavaObject</code> as a parameter to a Java method, Java simply unwraps the object; in a few situations, the object is coerced into another data type according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} Any interface or class that is assignment-compatible with the unwrapped object.
{{!}} The object is unwrapped.
{{!}}-
{{!}} <code>java.lang.String</code>
{{!}} The object is unwrapped, the <code>toString</code> method of the unwrapped Java object is called, and the result is returned as a new instance of <code>java.lang.String</code>.
{{!}}-
{{!}}
byte<br />
char<br /> 
double<br /> 
float<br /> 
int<br /> 
long<br />
short
{{!}}
The object is unwrapped, and either of the following situations occur:

* If the unwrapped Java object has a <code>doubleValue</code> method, the <code>JavaArray</code> or <code>JavaObject</code> is converted to the value returned by this method.
* If the unwrapped Java object does not have a <code>doubleValue</code> method, an error occurs.
{{!}}-
{{!}} boolean
{{!}}
In JavaScript 1.3 and later versions, the object is unwrapped and either of the following situations occur:

* If the object is null, it is converted to false.
* If the object has any other value, it is converted to true.

In JavaScript 1.2 and earlier versions, the object is unwrapped and either of the following situations occur:

* If the unwrapped object has a booleanValue method, the source object is converted to the return value.
* If the object does not have a booleanValue method, the conversion fails.
{{!}}}

An interface or class is assignment-compatible with an unwrapped object if the unwrapped object is an instance of the Java parameter type. That is, the following statement must return true:

 unwrappedObject instanceof parameterType;

====JavaClass objects====

When you pass a JavaScript <code>JavaClass</code> object as a parameter to a Java method, Java converts the object according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} <code>java.lang.Class</code>
{{!}} The object is unwrapped.
{{!}}-
{{!}} <code>netscape.javascript.JSObject</code><br /><code>java.lang.Object</code>
{{!}} The <code>JavaClass</code> object is wrapped in a new instance of <code>netscape.javascript.JSObject</code>.
{{!}}-
{{!}} <code>java.lang.String</code>
{{!}} The object is unwrapped, the <code>toString</code> method of the unwrapped Java object is called, and the result is returned as a new instance of <code>java.lang.String</code>.
{{!}}-
{{!}} boolean
{{!}}
In JavaScript 1.3 and later versions, the object is unwrapped and either of the following situations occur:

* If the object is null, it is converted to false.
* If the object has any other value, it is converted to true.

In JavaScript 1.2 and earlier versions, the object is unwrapped and either of the following situations occur:

* If the unwrapped object has a booleanValue method, the source object is converted to the return value.
* If the object does not have a booleanValue method, the conversion fails.
{{!}}}

====Other JavaScript objects====

When you pass any other JavaScript object as a parameter to a Java method, Java converts the object according to the rules described in the following table:

{{{!}} class="standard-table"
! scope="col" {{!}} Java parameter type
! scope="col" {{!}} Conversion rules
{{!}}-
{{!}} <code>netscape.javascript.JSObject</code><br /><code>java.lang.Object</code>
{{!}} The object is wrapped in a new instance of <code>netscape.javascript.JSObject</code>.
{{!}}-
{{!}} <code>java.lang.String</code>
{{!}} The object is unwrapped, the <code>toString</code> method of the unwrapped object is called, and the result is returned as a new instance of <code>java.lang.String</code>.
{{!}}-
{{!}}
byte<br />
char<br /> 
double<br /> 
float<br /> 
int<br /> 
long<br />
short
{{!}} The object is converted to a value using the logic of the <code>ToPrimitive</code> operator described in ECMA-262. The ''PreferredType'' hint used with this operator is Number.
{{!}}-
{{!}} boolean
{{!}}
In JavaScript 1.3 and later versions, the object is unwrapped and either of the following situations occur:

* If the object is null, it is converted to false.
* If the object has any other value, it is converted to true.

In JavaScript 1.2 and earlier versions, the object is unwrapped and either of the following situations occur:

* If the unwrapped object has a booleanValue method, the source object is converted to the return value.
* If the object does not have a booleanValue method, the conversion fails.
{{!}}}

===Java to JavaScript Conversions===

Values passed from Java to JavaScript are converted as follows:

* Java byte, char, short, int, long, float, and double are converted to JavaScript numbers.
* A Java boolean is converted to a JavaScript boolean.
* An object of class <code>netscape.javascript.JSObject</code> is converted to the original JavaScript object.
* Java arrays are converted to a JavaScript pseudo-Array object; this object behaves just like a JavaScript <code>Array</code> object: you can access it with the syntax <code>arrayName[index]</code> (where <code>index</code> is an integer), and determine its length with <code>arrayName.length</code>.
* A Java object of any other class is converted to a JavaScript wrapper, which can be used to access methods and fields of the Java object:
** Converting this wrapper to a string calls the <code>toString</code> method on the original object.
** Converting to a number calls the <code>doubleValue</code> method, if possible, and fails otherwise.
** Converting to a boolean in JavaScript 1.3 and later versions returns false if the object is null, and true otherwise.
** Converting to a boolean in JavaScript 1.2 and earlier versions calls the <code>booleanValue</code> method, if possible, and fails otherwise.

Note that instances of java.lang.Double and java.lang.Integer are converted to JavaScript objects, not to JavaScript numbers. Similarly, instances of java.lang.String are also converted to JavaScript objects, not to JavaScript strings.

Java <code>String</code> objects also correspond to JavaScript wrappers. If you call a JavaScript method that requires a JavaScript string and pass it this wrapper, you'll get an error. Instead, convert the wrapper to a JavaScript string by appending the empty string to it, as shown here:

 var JavaString = JavaObj.methodThatReturnsAString();
 var JavaScriptString = JavaString + "";


<span style="float: left">[[/guides/JavaScript/closures|&laquo; Previous]]</span>

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
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/LiveConnect_Overview
|MSDN_link=
|HTML5Rocks_link=
}}