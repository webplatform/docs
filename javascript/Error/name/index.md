---
title: 'name'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/96s4ewf9(v=vs.94).aspx)'
compatibility:
  feature: name
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the name of an error.'
tags:
  - JS
  - Basic
uri: javascript/Error/name

---
## Summary

Returns the name of an error.

## Syntax

    errorObj.name

**errorObj**
:   Required. Instance of Error object.

## Examples

The following example causes a TypeError exception to be thrown and displays the name of the error and its message.

``` js
try
 {
     var x = y;
 }
 catch(e)
 {
     document.write ("Error Message: " + e.message);
     document.write ("<br />");
     document.write ("Error Code: ");
     document.write (e.number & 0xFFFF)
     document.write ("<br />");
     document.write ("Error Name: " + e.name);
 }
```

The output of this code is as follows.

``` js
Error Message: 'y' is undefined
 Error Code: 5009
 Error Name: TypeError
```

## Remarks

The **name** property returns the name or exception type of an error. When a runtime error occurs, the name property is set to one of the following native exception types:

|Exception Type|Meaning|
|:-------------|:------|
|ConversionError|This error occurs whenever there is an attempt to convert an object into something to which it cannot be converted.|
|RangeError|This error occurs when a function is supplied with an argument that has exceeded its allowable range. For example, this error occurs if you attempt to construct an **Array** object with a length that is not a valid positive integer.|
|ReferenceError|This error occurs when an invalid reference has been detected. This error will occur, for example, if an expected reference is null.|
|RegExpError|This error occurs when a compilation error occurs with a regular expression. Once the regular expression is compiled, however, this error cannot occur. This example will occur, for example, when a regular expression is declared with a pattern that has an invalid syntax, or flags other than **i** , **g** , or **m** , or if it contains the same flag more than once.|
|SyntaxError|This error occurs when source text is parsed and that source text does not follow correct syntax. This error will occur, for example, if the **eval** function is called with an argument that is not valid program text.|
|TypeError|This error occurs whenever the actual type of an operand does not match the expected type. An example of when this error occurs is a function call made on something that is not an object or does not support the call.|
|URIError|This error occurs when an illegal Uniform Resource Indicator (URI) is detected. For example, this is error occurs when an illegal character is found in a string being encoded or decoded.|

## See also

### Other articles

-   [description Property (Error)](/javascript/Error/description)
-   [message Property (Error)](/javascript/Error/message)
-   [number Property (Error)](/javascript/Error/number)

