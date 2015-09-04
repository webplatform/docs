---
title: json
tags:
  - Concept
  - Pages
  - JavaScript
  - Web
  - Services
readiness: 'In Progress'
summary: 'Lightweight data interchange format that is useful for serializing data into a string.'
uri: concepts/programming/javascript/json

---
# json

## Summary

Lightweight data interchange format that is useful for serializing data into a string.

**JSON (JavaScript Object Notation)** is designed to be a lightweight data interchange format. As its name implies, its syntax is based on a subset of the JavaScript programming language. However, it also shares some conventions with other languages, and is generally language-independent. JSON is useful for serializing data into a string, though it only can hold certain data types. All types are either data structures or values, and JSON inherits JavaScript's weak typing by allowing the use of different types in those structures.

## Syntax

JSON supports a number of data types common to many programming languages, but are inherited from JavaScript:

-   Objects are unordered sets of name/value pairs. Names are strings, and are separated from their corresponding values with a colon (`:`). Each name/value pair is separated by a comma (`,`). Objects are enclosed by curly braces: `{` and `}`.
-   Arrays are ordered sets of any values, separated with commas. Arrays are enclosed by square brackets: `[` and `]`.
-   Strings store arbitrary text data. They are enclosed with double-quotes (`"`) and can hold most Unicode characters. Some characters, however, must be escaped with a backslash (`\`).
-   Numbers are double-precision floating-point, like those in JavaScript, excluding the octal and hexadecimal formats.
-   Booleans are either `true` or `false`.
-   Null is `null` and represents an empty value.

Arbitrary whitespace is also allowed outside of values for formatting purposes.

### Example Object

     {name: "Robert", prefix: "Mr", age: 23, programmer: true}

## Using JSON

### JavaScript

Being a subset of JavaScript itself, JSON is widely used by JS developers. Modern implementations of JavaScript include the global `JSON` object. It contains two methods: `parse` for parsing JSON strings, and `stringify` for converting a JS object into JSON. This object can also be polyfilled for older browsers that don't support it.

However, you should never parse JSON by calling the `eval` function. This works because JSON is almost always valid JavaScript, but using `eval` opens up several security risks by possibly allowing arbitrary code execution. If you do use it, make sure to properly sanitize its input first.

### Example Usage

      //This is a JavaScript object with 4 key.value pairs
      var obj = {name: "John Doe", prefix: "Mr", age: 23, programmer: true};

      //We serialize the object like so.
      var objSerialized = JSON.stringify(obj);

      //objSerialized now looks like: '{"name":"Robert","prefix":"Mr","age":23,"programmer":true}'
      //We can now de-serialize the string using the JSON.parse method.

      var objDeserialized = JSON.parse(objSerialized);

      //We can now use this object to access the values.
      alert(objDeserialized.prefix + " " + objDeserialized.name); //Mr John Doe


### Other languages

JSON parsers also exist for other languages. However, because not all of them share the same data types as JavaScript, some extra conversion may be required. [JSON.org](http://www.json.org/) has a listing of parsers in other languages.

## See also

### External resources

-   [JSON.org](http://www.json.org/)
-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/JSON)
-   [Wikipedia](http://en.wikipedia.org/wiki/JSON)

