---
title: String
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ecczf11c(v=vs.94).aspx)'
notes:
  - 'Item for later cleanup: An automatically generated list of properties and methods (either static, instance or inherited ones) is absent.'
readiness: 'Ready to Use'
summary: 'Allows manipulation and formatting of text strings and determination and location of substrings within strings.'
tags:
  - JS
  - Basic
uri: javascript/String

---
## Summary

Allows manipulation and formatting of text strings and determination and location of substrings within strings.

## Syntax

<span class="language">JavaScript</span>

    // Declaring a string literal.
    var newString = "stringLiteral";

    // Or, declaring a String object - discouraged, long, verbose and pretty useless.
    var newString = new String([" stringLiteral "]);

**newString**
:   Required. The variable name to which the String object is assigned.

**stringLiteral**
:   Optional. Any group of Unicode characters.

## Examples

JavaScript provides escape sequences that you can include in strings to create characters that you cannot type directly. For example, `\t` specifies a tab character. For more information, see Special Characters (JScript).

A string literal is zero or more characters enclosed in single or double quotation marks. A string literal has a primary (primitive) data type of string. A String object is created by using the [new Operator](/javascript/operators/new) , and has a data type of **Object**.

The following example shows that the data type of a string literal is not the same as that of a **String** object.

``` js
var strLit = "This is a string literal.";
var strObj = new String("This is a string object.");

document.write(typeof strLit);
document.write("<br/>");
document.write(typeof strObj);
// Output:
// string
// object
```

When you call a method on a string literal, it is temporarily converted to a string wrapper object. The string literal is treated as though the **new** operator were used to create it.

The following example applies the **toUpperCase** method to a string literal.

``` js
var strLit = "This is a string literal.";

var result1 = strLit.toUpperCase();

var result2 = (new String(strLit)).toUpperCase();

document.write(result1);
document.write("<br/>");
document.write(result2);
// Output:
// THIS IS A STRING LITERAL.
// THIS IS A STRING LITERAL.
```

In modern browsers (2011 onwards), you can access an individual character of a string as a read-only array-indexed property. The following example accesses individual string characters.

``` js
var str = "abcd";
var result = str[2];
document.write (result);
// Output: c

var result = "the"[0];
document.write(result);
// Output: t
```

## Properties

The following table lists the properties of the **String** object.

|Property|Description|
|:-------|:----------|
|[constructor](/javascript/String/constructor)|Specifies the function that creates an object.|
|[length](/javascript/String/length)|Returns the length of a String object.|
|[prototype](/javascript/String/prototype)|Returns a reference to the prototype for a class of objects.|

## Functions

The following table lists the functions of the **String** object.

|Function|Description|
|:-------|:----------|
|[fromCharCode](/javascript/String/fromCharCode)|Returns a string from a number of Unicode character values.|

## Methods

The following table lists the methods of the **String** object.

|Method|Description|
|:-----|:----------|
|[HTML Tag Methods](/javascript/String/HTML_Tag_Methods)|Places various HTML tags around text.|
|[charAt](/javascript/String/charAt)|Returns the character at the specified index.|
|[charCodeAt](/javascript/String/charCodeAt)|Returns the Unicode encoding of the specified character.|
|[concat](/javascript/String/concat)|Returns a string that contains the concatenation of two supplied strings.|
|[indexOf](/javascript/String/indexOf)|Returns the character position where the first occurrence of a substring occurs within a string.|
|[lastIndexOf](/javascript/String/lastIndexOf)|Returns the last occurrence of a substring within a string.|
|[localeCompare](/javascript/String/localeCompare)|Returns a value that indicates whether two strings are equivalent in the current locale.|
|[match](/javascript/String/match)|Searches a string by using a supplied **Regular Expression** object and returns the results as an array.|
|[replace](/javascript/String/replace)|Uses a regular expression to replace text in a string and returns the result.|
|[search](/javascript/String/search)|Returns the position of the first substring match in a regular expression search.|
|[slice](/javascript/String/slice)|Returns a section of a string.|
|[split](/javascript/String/split)|Returns the array of strings that results when a string is separated into substrings.|
|[substr](/javascript/String/substr)|Returns a substring beginning at a specified location and having a specified length.|
|[substring](/javascript/String/substring)|Returns the substring at a specified location within a String object.|
|[toLocaleLowerCase](/javascript/String/toLocaleLowerCase)|Returns a string in which all alphabetic characters are converted to lowercase, taking into account the host environment's current locale.|
|[toLocaleUpperCase](/javascript/String/toLocaleUpperCase)|Returns a string in which all alphabetic characters are converted to uppercase, taking into account the host environment's current locale.|
|[toLowerCase](/javascript/String/toLowerCase)|Returns a string in which all alphabetic characters are converted to lowercase.|
|[toString](/javascript/String/toString)|Returns the string.|
|[toUpperCase](/javascript/String/toUpperCase)|Returns a string in which all alphabetic characters are converted to uppercase.|
|[trim](/javascript/String/trim)|Returns a string with leading and trailing white space and line terminator characters removed.|
|[valueOf](/javascript/String/valueOf)|Returns the string.|

## See also

### Other articles

-   [new Operator](/javascript/operators/new)

