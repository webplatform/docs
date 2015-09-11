---
title: Overview
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/JavaScript/Guide/JavaScript_Overview)'
readiness: 'Not Ready'
summary: 'This chapter introduces JavaScript and discusses some of its fundamental concepts.'
tags:
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/programming/javascript/overview/guides/JavaScript/About the object model'
    - concepts/programming/javascript/overview/js
uri: concepts/programming/javascript/overview

---
## <span>Summary</span>

This chapter introduces JavaScript and discusses some of its fundamental concepts.

# <span>What is JavaScript?</span>

JavaScript is a cross-platform, object-oriented scripting language. JavaScript is a small, lightweight language; it is not useful as a standalone language, but is designed for easy embedding in other products and applications, such as web browsers. Inside a host environment, JavaScript can be connected to the objects of its environment to provide programmatic control over them.

Core JavaScript contains a core set of objects, such as Array, Date, and Math, and a core set of language elements such as operators, control structures, and statements. Core JavaScript can be extended for a variety of purposes by supplementing it with additional objects; for example:

-   *Client-side JavaScript* extends the core language by supplying objects to control a browser (Navigator or another web browser) and its Document Object Model (DOM). For example, client-side extensions allow an application to place elements on an HTML form and respond to user events such as mouse clicks, form input, and page navigation.
-   *Server-side JavaScript* extends the core language by supplying objects relevant to running JavaScript on a server. For example, server-side extensions allow an application to communicate with a relational database, provide continuity of information from one invocation to another of the application, or perform file manipulations on a server.

Through JavaScript's LiveConnect functionality, you can let Java and JavaScript code communicate with each other. From JavaScript, you can instantiate Java objects and access their public methods and fields. From Java, you can access JavaScript objects, properties, and methods.

Netscape invented JavaScript, and JavaScript was first used in Netscape browsers.

# <span>JavaScript and Java</span>

JavaScript and Java are similar in some ways but fundamentally different in some others. The JavaScript language resembles Java but does not have Java's static typing and strong type checking. JavaScript follows most Java expression syntax, naming conventions and basic control-flow constructs which was the reason why it was renamed from LiveScript to JavaScript.

In contrast to Java's compile-time system of classes built by declarations, JavaScript supports a runtime system based on a small number of data types representing numeric, Boolean, and string values. JavaScript has a prototype-based object model instead of the more common class-based object model. The prototype-based model provides dynamic inheritance; that is, what is inherited can vary for individual objects. JavaScript also supports functions without any special declarative requirements. Functions can be properties of objects, executing as loosely typed methods.

JavaScript is a very free-form language compared to Java. You do not have to declare all variables, classes, and methods. You do not have to be concerned with whether methods are public, private, or protected, and you do not have to implement interfaces. Variables, parameters, and function return types are not explicitly typed.

Java is a class-based programming language designed for fast execution and type safety. Type safety means, for instance, that you can't cast a Java integer into an object reference or access private memory by corrupting Java bytecodes. Java's class-based model means that programs consist exclusively of classes and their methods. Java's class inheritance and strong typing generally require tightly coupled object hierarchies. These requirements make Java programming more complex than JavaScript programming.

In contrast, JavaScript descends in spirit from a line of smaller, dynamically typed languages such as HyperTalk and dBASE. These scripting languages offer programming tools to a much wider audience because of their easier syntax, specialized built-in functionality, and minimal requirements for object creation.

**Table 1.1 JavaScript compared to Java**

|JavaScript|Java|
|:---------|:---|
|Object-oriented. No distinction between types of objects. Inheritance is through the prototype mechanism, and properties and methods can be added to any object dynamically.|Class-based. Objects are divided into classes and instances with all inheritance through the class hierarchy. Classes and instances cannot have properties or methods added dynamically.|
|Variable data types are not declared (dynamic typing).|Variable data types must be declared (static typing).|
|Cannot automatically write to hard disk.|Cannot automatically write to hard disk.|

 For more information on the differences between JavaScript and Java, see the chapter [About the object model](/w/index.php?title=concepts/programming/javascript/overview/guides/JavaScript/About_the_object_model&action=edit&redlink=1).

# <span>JavaScript and the ECMAScript Specification</span>

Netscape invented JavaScript, and JavaScript was first used in Netscape browsers. However, Netscape is working with Ecma International — the European association for standardizing information and communication systems (ECMA was formerly an acronym for the European Computer Manufacturers Association) to deliver a standardized, international programming language based on core JavaScript. This standardized version of JavaScript, called ECMAScript, behaves the same way in all applications that support the standard. Companies can use the open standard language to develop their implementation of JavaScript. The ECMAScript standard is documented in the ECMA-262 specification.

The ECMA-262 standard is also approved by the ISO (International Organization for Standardization) as ISO-16262. You can find a PDF version of ECMA-262 (outdated version) at the Mozilla website. You can also find the specification on the Ecma International website. The ECMAScript specification does not describe the Document Object Model (DOM), which is standardized by the World Wide Web Consortium (W3C). The DOM defines the way in which HTML document objects are exposed to your script.

## <span>Relationship between JavaScript Versions and ECMAScript Editions</span>

Netscape worked closely with Ecma International to produce the ECMAScript Specification (ECMA-262). The following table describes the relationship between JavaScript versions and ECMAScript editions.

**Table 1.2 JavaScript versions and ECMAScript editions**

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">JavaScript version</th>
<th align="left">Relationship to ECMAScript edition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">JavaScript 1.1</td>
<td align="left">ECMA-262, Edition 1 is based on JavaScript 1.1.</td>
</tr>
<tr class="even">
<td align="left">JavaScript 1.2</td>
<td align="left">ECMA-262 was not complete when JavaScript 1.2 was released. JavaScript 1.2 is not fully compatible with ECMA-262, Edition 1, for the following reasons: <br />(1) Netscape developed additional features in JavaScript 1.2 that were not considered for ECMA-262.
<p><br />(2) ECMA-262 adds two new features: internationalization using Unicode, and uniform behavior across all platforms. Several features of JavaScript 1.2, such as the Date object, were platform-dependent and used platform-specific behavior.</p></td>
</tr>
<tr class="odd">
<td align="left">JavaScript 1.3</td>
<td align="left">JavaScript 1.3 is fully compatible with ECMA-262, Edition 1. <br />JavaScript 1.3 resolved the inconsistencies that JavaScript 1.2 had with ECMA-262, while keeping all the additional features of JavaScript 1.2 except == and !=, which were changed to conform with ECMA-262.</td>
</tr>
<tr class="even">
<td align="left">JavaScript 1.4</td>
<td align="left">JavaScript 1.4 is fully compatible with ECMA-262, Edition 1.<br />The third version of the ECMAScript specification was not finalized when JavaScript 1.4 was released.</td>
</tr>
<tr class="odd">
<td align="left">JavaScript 1.5</td>
<td align="left">JavaScript 1.5 is fully compatible with ECMA-262, Edition 3.</td>
</tr>
</tbody>
</table>

**Note**: ECMA-262, Edition 2 consisted of minor editorial changes and bug fixes to the Edition 1 specification. The current release by the TC39 working group of Ecma International is ECMAScript Edition 5.1

 The [JavaScript Reference](/w/index.php?title=concepts/programming/javascript/overview/js&action=edit&redlink=1) indicates which features of the language are ECMAScript-compliant.

JavaScript will always include features that are not part of the ECMAScript Specification; JavaScript is compatible with ECMAScript, while providing additional features.

## <span>JavaScript Documentation versus the ECMAScript Specification</span>

The ECMAScript specification is a set of requirements for implementing ECMAScript; it is useful if you want to determine whether a JavaScript feature is supported in other ECMAScript implementations. If you plan to write JavaScript code that uses only features supported by ECMAScript, then you may need to review the ECMAScript specification.

The ECMAScript document is not intended to help script programmers; use the JavaScript documentation for information on writing scripts.

## <span>JavaScript and ECMAScript Terminology</span>

The ECMAScript specification uses terminology and syntax that may be unfamiliar to a JavaScript programmer. Although the description of the language may differ in ECMAScript, the language itself remains the same. JavaScript supports all functionality outlined in the ECMAScript specification.

The JavaScript documentation describes aspects of the language that are appropriate for a JavaScript programmer. For example:

-   The Global Object is not discussed in the JavaScript documentation because you do not use it directly. The methods and properties of the Global Object, which you do use, are discussed in the JavaScript documentation but are called top-level functions and properties.
-   The no parameter (zero-argument) constructor with the `Number` and `String` objects is not discussed in the JavaScript documentation, because what is generated is of little use. A `Number` constructor without an argument returns +0, and a `String` constructor without an argument returns "" (an empty string).
