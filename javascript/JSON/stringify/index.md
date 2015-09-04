---
title: stringify
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Converts a JavaScript value to a JavaScript Object Notation (JSON) string.'
uri: javascript/JSON/stringify

---
# stringify

## Summary

Converts a JavaScript value to a JavaScript Object Notation (JSON) string.

## Syntax

    JSON.stringify( value [ , replacer] [ , space] )

**value**
:   Required. A JavaScript value, usually an object or array, to be converted.

**replacer**
:   Optional. A function or array that transforms the results.If replacer is a function, JSON.stringify calls the function, passing in the key and value of each member. The return value is used instead of the original value. If the function returns undefined , the member is excluded. The key for the root object is an empty string: "".If replacer is an array, only members with key values in the array will be converted. The order in which the members are converted is the same as the order of the keys in the array. The replacer array is ignored when the value argument is also an array.

**space**
:   Optional. Adds indentation, white space, and line break characters to the return-value JSON text to make it easier to read.If space is omitted, the return-value text is generated without any extra white space.If space is a number, the return-value text is indented with the specified number of white spaces at each level. If space is greater than 10, text is indented 10 spaces.If space is a non-empty string, such as '\\t', the return-value text is indented with the characters in the string at each level.If space is a string that is longer than 10 characters, the first 10 characters are used.

## Return Value

A string that contains the JSON text.

## Examples

This example uses JSON.stringify to convert the `contact` object to JSON text. The `memberfilter` array is defined so that only the `surname` and `phone` members are converted. The `firstname` member is omitted.

``` {.js}
var contact = new Object();
 contact.firstname = "Jesper";
 contact.surname = "Aaberg";
 contact.phone = ["555-0100", "555-0120"];

 var memberfilter = new Array();
 memberfilter[0] = "surname";
 memberfilter[1] = "phone";
 var jsonText = JSON.stringify(contact, memberfilter, "\t");
 document.write(jsonText);
 // Output:
 // { "surname": "Aaberg", "phone": [ "555-0100", "555-0120" ] }
```

This example uses JSON.stringify with an array. The `replaceToUpper` function converts every string in the array to uppercase.

``` {.js}
var continents = new Array();
 continents[0] = "Europe";
 continents[1] = "Asia";
 continents[2] = "Australia";
 continents[3] = "Antarctica";
 continents[4] = "North America";
 continents[5] = "South America";
 continents[6] = "Africa";

 var jsonText = JSON.stringify(continents, replaceToUpper);

 function replaceToUpper(key, value) {
     return value.toString().toUpperCase();
 }

 //Output:
 // "EUROPE,ASIA,AUSTRALIA,ANTARCTICA,NORTH AMERICA,SOUTH AMERICA,AFRICA"
```

This example uses the toJSON method to convert string values to uppercase.

``` {.js}
var contact = new Object();
 contact.firstname = "Jesper";
 contact.surname = "Aaberg";
 contact.phone = ["555-0100", "555-0120"];

 contact.toJSON = function(key)
  {
     var replacement = new Object();
     for (var val in this)
     {
         if (typeof (this[val]) === 'string')
             replacement[val] = this[val].toUpperCase();
         else
             replacement[val] = this[val]
     }
     return replacement;
 };

 var jsonText = JSON.stringify(contact);
 document.write(jsonText);

 // Output:
 {"firstname":"JESPER","surname":"AABERG","phone":["555-0100","555-0120"]}



 '{"firstname":"JESPER","surname":"AABERG","phone":["555-0100","555-0120"]}'
 */
```

## Remarks

If value has a toJSON method, the JSON.stringify function uses the return value of that method. If the return value of the toJSON method is undefined , the member is not converted. This enables an object to determine its own JSON representation.

Values that do not have JSON representations, such as undefined , will not be converted. In objects, they will be dropped. In arrays, they will be replaced with null.

String values begin and end with a quotation mark. All Unicode characters may be enclosed in the quotation marks except for the characters that must be escaped by using a backslash. The following characters must be preceded by a backslash:

-   Quotation mark (")
-   Backslash (\\)
-   Backspace (b)
-   Formfeed (f)
-   Newline (n)
-   Carriage return (r)
-   Horizontal tab (t)
-   Four-hexadecimal-digits (uhhhh)

During the serialization process, if a toJSON method exists for the value argument, JSON.stringify first calls the toJSON method. If it does not exist, the original value is used. Next, if a replacer argument is provided, the value (original value or toJSON return-value) is replaced with the return-value of the replacer argument. Finally, white spaces are added to the value based on the optional space argument to generate the final JSON text.

## Exceptions

Exception
:   Condition
Invalid replacer argument
:   The replacer argument is not a function or an array.
Circular reference in value argument not supported
:   The value argument contains a circular reference.

## See also

### Other articles

-   [JSON.parse Function](/javascript/JSON/parse)
-   [toJSON Method (Date)](/javascript/Date/toJSON)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/cc836459(v=vs.94).aspx)

