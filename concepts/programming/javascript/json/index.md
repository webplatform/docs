{{Flags
|High-level issues=Stub
}}
'''JSON (JavaScript Object Notation)''' is designed to be a lightweight data interchange format. As its name implies, its syntax is based on a subset of the JavaScript programming language. However, it also shares some conventions with other languages, and is generally language-independent. JSON is useful for serializing data into a string, though it only can hold certain data types. All types are either data structures or values, and JSON inherits JavaScript's weak typing by allowing the use of different types in those structures.

==Syntax==
JSON supports a number of data types common to many programming languages, but are inherited from JavaScript:
* Objects are unordered sets of name/value pairs. Names are strings, and are separated from their corresponding values with a colon (<code>:</code>). Each name/value pair is separated by a comma (<code>,</code>). Objects are enclosed by curly braces: <code>{</code> and <code>}</code>.
* Arrays are ordered sets of any values, separated with commas. Arrays are enclosed by square brackets: <code>[</code> and <code>]</code>.
* Strings store arbitrary text data. They are enclosed with double-quotes  (<code>"</code>) and can hold most Unicode characters. Some characters, however, must be escaped with a backslash (<code>/</code>).
* Numbers are double-precision floating-point, like those in JavaScript, excluding the octal and hexadecimal formats.
* Booleans are either <code>true</code> or <code>false</code>.
* Null is <code>null</code> and represents an empty value.

Arbitrary whitespace is also allowed outside of values for formatting purposes.

==Using JSON==
===JavaScript===
Being a subset of JavaScript itself, JSON is widely used by JS developers. Modern implementations of JavaScript include the global <code>JSON</code> object. It contains two methods: <code>parse</code> for parsing JSON strings, and <code>stringify</code> for converting a JS object into JSON. This object can also be polyfilled for older browsers that don't support it.

However, you should never parse JSON by calling the <code>eval</code> function. This works because JSON is almost always valid JavaScript, but using <code>eval</code> opens up several security risks by possibly allowing arbitrary code execution. If you do use it, make sure to properly sanitize its input first.
===Other languages===
JSON parsers also exist for other languages. However, because not all of them share the same data types as JavaScript, some extra conversion may be required. [http://www.json.org/ JSON.org] has a listing of parsers in other languages.

[[Category:Concept Pages]]