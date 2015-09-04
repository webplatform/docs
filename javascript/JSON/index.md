---
title: JSON
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'An intrinsic object that provides functions to convert JavaScript values to and from the JavaScript Object Notation (JSON) format. The JSON.stringify function serializes a JavaScript value to JSON text. The JSON.parse function deserializes JSON text to produce a JavaScript value.'
uri: javascript/JSON

---
# JSON

## Summary

An intrinsic object that provides functions to convert JavaScript values to and from the JavaScript Object Notation (JSON) format. The JSON.stringify function serializes a JavaScript value to JSON text. The JSON.parse function deserializes JSON text to produce a JavaScript value.

## Syntax

    JSON.[method]

**Method**
:   Required. Name of one of the methods of the JSON object.

## Remarks

You cannot create a JSON object by using the new operator. An error occurs if you try to do this. However, you can override or modify the JSON object.

The scripting engine creates the JSON object when the engine is loaded. Its methods are available to your script at all times.

To use the intrinsic JSON object, make sure that you do not override it with another JSON object that is defined in your script. You may need to modify existing script statements that detect the presence of a JSON object because those statements will evaluate differently. This is demonstrated in the following example.

    if (!this.JSON) {
        // JSON object does not exist.
        }

In the previous example, `!this.JSON` evaluates to false in Internet Explorer 8 standards mode, Internet Explorer 9 standards mode, Internet Explorer 10 standards mode, and win8\_appname\_long apps. Therefore, the code inside the if statement does not execute.

## Functions

[JSON.parse Function](/javascript/JSON/parse)

[JSON.stringify Function](/javascript/JSON/stringify)

## See also

### Other articles

-   [toJSON Method (Date)](/javascript/Date/toJSON)
-   [JavaScript Objects](/javascript/objects)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/cc836458(v=vs.94).aspx)

