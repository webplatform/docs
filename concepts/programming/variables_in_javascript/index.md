---
title: Variables in JavaScript
readiness: 'Almost Ready'
summary: 'JavaScript recognizes values such as integers and strings, which are represented with symbolic names by which they are referenced in the source code. Each variable is associated with a data type and has a scope, or area in which it is valid.'
tags:
  - Concept
  - Pages
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - js/data-types/number
    - js/data-types/boolean
    - js/data-types/string
    - js/objects/undefined
    - js/objects/date
    - js/objects
    - js/functions
    - javascript/functions/parseInt
    - javascript/functions/parseFloat
    - js/statements/var
uri: 'concepts/programming/variables in javascript'

---
## <span>Summary</span>

JavaScript recognizes values such as integers and strings, which are represented with symbolic names by which they are referenced in the source code. Each variable is associated with a data type and has a scope, or area in which it is valid.

 This chapter discusses values that JavaScript recognizes and describes the fundamental building blocks of JavaScript expressions: variables, constants, and literals.

## <span>Values</span>

JavaScript recognizes the following types of values:

-   [Numbers](/w/index.php?title=js/data-types/number&action=edit&redlink=1), such as 42 or 3.14159
-   [Logical (Boolean)](/w/index.php?title=js/data-types/boolean&action=edit&redlink=1) values, either `true` or `false`
-   [Strings](/w/index.php?title=js/data-types/string&action=edit&redlink=1), such as "Howdy!"
-   `null`, a special keyword denoting a null value; `null` is also a primitive value. Because JavaScript is case-sensitive, `null` is not the same as `Null`, `NULL`, or any other variant
-   `undefined`, a top-level property whose value is undefined; `undefined` is also a primitive value.

This relatively small set of types of values, or *data types*, enables you to perform useful functions with your applications. There is no explicit distinction between integer and real-valued numbers. Nor is there an explicit date data type in JavaScript. However, you can use the `Date` object and its methods to handle dates.

[Objects](/w/index.php?title=js/objects&action=edit&redlink=1) and [functions](/w/index.php?title=js/functions&action=edit&redlink=1) are the other fundamental elements in the language. You can think of objects as named containers for values, and functions as procedures that your application can perform.

### <span>Data type conversion</span>

JavaScript is a dynamically typed language. That means you do not have to specify the data type of a variable when you declare it, and data types are converted automatically as needed during script execution. So, for example, you could define a variable as follows:

    var answer = 42;

And later, you could assign the same variable a string value, for example:

    answer = "Thanks for all the fish...";

Because JavaScript is dynamically typed, this assignment does not cause an error message. But abusing dynamic typing may cause a performance problem.

In expressions involving numeric and string values with the + operator, JavaScript converts numeric values to strings. For example, consider the following statements:

    x = "The answer is " + 42 // returns "The answer is 42"
    y = 42 + " is the answer" // returns "42 is the answer"

In statements involving other operators, JavaScript does not convert numeric values to strings. For example:

    "37" - 7 // returns 30
    "37" + 7 // returns "377"

### <span>Converting strings to numbers</span>

In the case that a value representing a number is in memory as a string, there are methods for conversion.

#### <span>`parseInt()` and `parseFloat()`</span>

See: `parseInt()` and `parseFloat()` pages.

`parseInt()` will only return whole numbers. Use `parseFloat()` if you need floating-point numbers. Additionally, a best practice for `parseInt()` is to always include the radix parameter.

#### <span>Plus operator</span>

An alternative method of retrieving a number from a string is with the `+` operator.

    "1.1" + "1.1" = "1.11.1"
    (+"1.1") + (+"1.1") = 2.2   // Note: the parentheses are added for clarity, not required.

## <span>Variables</span>

You use variables as symbolic names for values in your application. The names of variables, called *identifiers*, conform to certain rules.

A JavaScript identifier must start with a letter, underscore (\_), or dollar sign (\$); subsequent characters can also be digits (0-9). Because JavaScript is case sensitive, letters include the characters "A" through "Z" (uppercase) and the characters "a" through "z" (lowercase).

Starting with JavaScript 1.5, you can use ISO 8859-1 or Unicode letters such as å and ü in identifiers. You can also use the \\uXXXX {{anch("Unicode escape sequences")}} as characters in identifiers.

Some examples of legal names are `Number_hits`, `temp99`, and `_name`.

### <span>Declaring variables</span>

You can declare a variable in two ways:

-   With the keyword [var](/w/index.php?title=js/statements/var&action=edit&redlink=1). For example, `var x = 42`. This syntax can be used to declare both [local and global](#Variable_scope) variables.
-   By simply assigning it a value. For example, `x = 42`. This always declares a [global variable](#Global_variables) and generates a strict JavaScript warning. You shouldn't use this variant.

### <span>Evaluating variables</span>

A variable declared using the `var` statement with no initial value specified has the value `undefined`.

An attempt to access an undeclared variable will result in a `ReferenceError` exception being thrown:

    var a;
    console.log("The value of a is " + a); // prints "The value of a is undefined"
    console.log("The value of b is " + b); // throws ReferenceError exception

You can use `undefined` to determine whether a variable has a value. In the following code, the variable `input` is not assigned a value, and the `if` statement evaluates to `true`.

    var input;
    if(input === undefined) {
      doThis();
    } else {
      doThat();
    }

<span class="comment">The following is related to "Variables" section as potential values in assignment.</span>

The `undefined` value behaves as `false` when used in a boolean context. For example, the following code executes the function `myFunction` because the `myArray` element is not defined:

    var myArray = new Array();
    if (!myArray[0]) myFunction();

The `undefined` value converts to `NaN` when used in numeric context.

    var a;
    a + 2 = NaN

When you evaluate a null variable, the null value behaves as 0 in numeric contexts and as false in boolean contexts. For example:

    var n = null;
    console.log(n * 32); // prints 0

### <span>Variable scope</span>

When you declare a variable outside of any function, it is called a *global* variable, because it is available to any other code in the current document. When you declare a variable within a function, it is called a *local* variable, because it is available only within that function.

JavaScript does not have block statement scope; rather, it will be local to the code that the block resides within. For example the following code will log `5`, because the scope of `x` is the function (or global context) within which `x` is declared, not the block, which in this case is an `if` statement.

    if (true) {
      var x = 5;
    }
    console.log(x);

Another unusual thing about variables in JavaScript is that you can refer to a variable declared later, without getting an exception. This concept is known as hoisting; variables in JavaScript are in a sense "hoisted" or lifted to the top of the function or statement. However, variables that aren't initialized yet will return a value of `undefined`.

    /**
     * Example 1
     */
    console.log(x === undefined); // logs "true"
    var x = 3;

    /**
     * Example 2
     */
    // will return a value of undefined
    var myvar = "my value";

    (function() {
      console.log(myvar); // undefined
      var myvar = "local value";
    })();

Example 2, above, will be interpreted the same as:

    var myvar = "my value";

    (function() {
      var myvar;
      console.log(myvar); // undefined
      myvar = "local value";
    })();

Because of hoisting, all `var` statements in a function should be placed as near to the top of the function as possible. This best practice increases the clarity of the code.

### <span>Global variables</span>

<span class="comment">need links to pages discussing scope chains and the global object</span> Global variables are in fact properties of the *global object*. In web pages the global object is `window`, so you can set and access global variables using the `window.variable` syntax.

Consequently, you can access global variables declared in one window or frame from another window or frame by specifying the window or frame name. For example, if a variable called `phoneNumber` is declared in a `FRAMESET` document, you can refer to this variable from a child frame as `parent.phoneNumber`.

## <span>Constants</span>

You can create a read-only, named constant with the `const` keyword. The syntax of a constant identifier is the same as for a variable identifier: it must start with a letter or underscore and can contain alphabetic, numeric, or underscore characters.

    const prefix = '212';

A constant cannot change value through assignment or be re-declared while the script is running.

The scope rules for constants are the same as those for variables, except that the `const` keyword is always required, even for global constants. If the keyword is omitted, the identifier is assumed to represent a variable.

You cannot declare a constant with the same name as a function or variable in the same scope. For example:

    // THIS WILL CAUSE AN ERROR
    function f() {};
    const f = 5;

    // THIS WILL CAUSE AN ERROR ALSO
    function f() {
      const g = 5;
      var g;

      //statements
    }

## <span>Literals</span>

You use literals to represent values in JavaScript. These are fixed values, not variables, that you *literally* provide in your script. This section describes the following types of literals:

-   [Array literals](#Array_literals)
-   [Boolean literals](#Boolean_literals)
-   [Floating-point literals](#Floating-point_literals)
-   [Integers](#Integers)
-   [Object literals](#Object_literals)
-   [String literals](#String_literals)

### <span>Array literals</span>

An array literal is a list of zero or more expressions, each of which represents an array element, enclosed in square brackets ([]). When you create an array using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified.

The following example creates the `coffees` array with three elements and a length of three:

    var coffees = ["French Roast", "Colombian", "Kona"];

**Note** An array literal is a type of object initializer.

If an array is created using a literal in a top-level script, JavaScript interprets the array each time it evaluates the expression containing the array literal. In addition, a literal used in a function is created each time the function is called.

Array literals are also `Array` objects.

#### <span>Extra commas in array literals</span>

You do not have to specify all elements in an array literal. If you put two commas in a row, the array is created with `undefined` for the unspecified elements. The following example creates the `fish` array:

    var fish = ["Lion", , "Angel"];

This array has two elements with values and one empty element (`fish[0]` is "Lion", `fish[1]` is `undefined`, and `fish[2]` is "Angel").

If you include a trailing comma at the end of the list of elements, the comma is ignored. In the following example, the length of the array is three. There is no `myList[3]`. All other commas in the list indicate a new element. (**Note** trailing commas can create errors in older browser versions and it is a best practice to remove them)

    var myList = ['home', , 'school', ];

In the following example, the length of the array is four, and `myList[0]` and `myList[2]` are missing.

    var myList = [ , 'home', , 'school'];

In the following example, the length of the array is four, and `myList[1]` and `myList[3]` are missing. Only the last comma is ignored.

    var myList = ['home', , 'school', , ];

Understanding the behavior of extra commas is important to understanding JavaScript as a language, however when writing your own code: explicitly declaring the missing elements as `undefined` will increase your code's clarity and maintainability.

### <span>Boolean literals</span>

The Boolean type has two literal values: `true` and `false`.

Do not confuse the primitive Boolean values `true` and `false` with the true and false values of the Boolean object. The Boolean object is a wrapper around the primitive Boolean data type.

### <span>Integers</span>

Integers can be expressed in decimal (base 10), hexadecimal (base 16), and octal (base 8).

-   Decimal integer literal consists of a sequence of digits without a leading 0 (zero).
-   Leading 0 (zero) on an integer literal indicates it is in octal. Octal integers can include only the digits 0-7.
-   Leading 0x (or 0X) indicates hexadecimal. Hexadecimal integers can include digits (0-9) and the letters a-f and A-F.

Octal integer literals are deprecated and have been removed from the ECMA-262, Edition 3 standard (in *strict mode*). JavaScript 1.5 still supports them for backward compatibility.

Some examples of integer literals are:

    0, 117 and -345 (decimal, base 10)
    015, 0001 and -077 (octal, base 8)
    0x1123, 0x00111 and -0xF1A7 (hexadecimal, "hex" or base 16)

### <span>Floating-point literals</span>

A floating-point literal can have the following parts:

-   A decimal integer which can be signed (preceded by "+" or "-"),
-   A decimal point ("."),
-   A fraction (another decimal number),
-   An exponent.

The exponent part is an "e" or "E" followed by an integer, which can be signed (preceded by "+" or "-"). A floating-point literal must have at least one digit and either a decimal point or "e" (or "E").

Some examples of floating-point literals are 3.1415, -3.1E12, .1e12, and 2E-12.

More succinctly, the syntax is:

    [digits][.digits][(E|e)[(+|-)]digits]

For example:

    3.14
    2345.789
    .3333333333333333333

### <span>Object literals</span>

An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces ({}). You should not use an object literal at the beginning of a statement. This will lead to an error or not behave as you expect, because the { will be interpreted as the beginning of a block.

The following is an example of an object literal. The first element of the `car` object defines a property, `myCar`; the second element, the `getCar` property, invokes a function `(CarTypes("Honda"));` the third element, the `special` property, uses an existing variable (`Sales`).

    var Sales = "Toyota";

    function CarTypes(name) {
      return (name == "Honda") ?
        name :
        "Sorry, we don't sell " + name + "." ;
    }

    var car = { myCar: "Saturn", getCar: CarTypes("Honda"), special: Sales };

    console.log(car.myCar);   // Saturn
    console.log(car.getCar);  // Honda
    console.log(car.special); // Toyota

Additionally, you can use a numeric or string literal for the name of a property or nest an object inside another. The following example uses these options.

    var car = { manyCars: {a: "Saab", "b": "Jeep"}, 7: "Mazda" };

    console.log(car.manyCars.b); // Jeep
    console.log(car[7]); // Mazda

Please note:

    var foo = {a: "alpha", 2: "two"};
    console.log(foo.a);    // alpha
    console.log(foo[2]);   // two
    //console.log(foo.2);  // Error: missing ) after argument list
    //console.log(foo[a]); // Error: a is not defined
    console.log(foo["a"]); // alpha
    console.log(foo["2"]); // two

### <span>String literals</span>

A string literal is zero or more characters enclosed in double (`"`) or single (`'`) quotation marks. A string must be delimited by quotation marks of the same type; that is, either both single quotation marks or both double quotation marks. The following are examples of string literals:

-   `"foo"`
-   `'bar'`
-   `"1234"`
-   `"one line \n another line"`
-   `"John's cat"`

You can call any of the methods of the String object on a string literal value—JavaScript automatically converts the string literal to a temporary String object, calls the method, then discards the temporary String object. You can also use the `String.length` property with a string literal:

    "John's cat".length

You should use string literals unless you specifically need to use a String object.

#### <span>Using special characters in strings</span>

In addition to ordinary characters, you can also include special characters in strings, as shown in the following example.

    "one line \n another line"

The following table lists the special characters that you can use in JavaScript strings.

|Character|Meaning|
|:--------|:------|
|`\b`|Backspace|
|`\f`|Form feed|
|`\n`|New line|
|`\r`|Carriage return|
|`\t`|Tab|
|`\v`|Vertical tab|
|`\'`|Apostrophe or single quote|
|`\"`|Double quote|
|`\\`|Backslash character (\\).|
|`\XXX`|The character with the Latin-1 encoding specified by up to three octal digits *XXX* between 0 and 377. For example, \\251 is the octal sequence for the copyright symbol.|
|`\xXX`|The character with the Latin-1 encoding specified by the two hexadecimal digits *XX* between 00 and FF. For example, \\xA9 is the hexadecimal sequence for the copyright symbol.|
|`\uXXXX`|The Unicode character specified by the four hexadecimal digits *XXXX*. For example, \\u00A9 is the Unicode sequence for the copyright symbol. See {{anch("Unicode escape sequences")}}.|

#### <span>Escaping characters</span>

For characters not listed in Table 2.1, a preceding backslash is ignored, but this usage is deprecated and should be avoided.

You can insert a quotation mark inside a string by preceding it with a backslash. This is known as *escaping* the quotation mark. For example:

    var quote = "He read \"The Cremation of Sam McGee\" by R.W. Service.";
    console.log(quote);

The result of this would be:

    He read "The Cremation of Sam McGee" by R.W. Service.

To include a literal backslash inside a string, you must escape the backslash character. For example, to assign the file path `c:\temp` to a string, use the following:

    var home = "c:\\temp";

You can also escape line breaks by preceding them with backslash. The backslash and line break are both removed from the value of the string.

    var str = "this string \
    is broken \
    across multiple\
    lines."
    console.log(str);   // this string is broken across multiplelines.

Although JavaScript does not have "heredoc" syntax, you can get close by adding a linebreak escape and an escaped linebreak at the end of each line:

    var poem =
    "Roses are red,\n\
    Violets are blue.\n\
    I'm schizophrenic,\n\
    And so am I."

## <span>Unicode</span>

Unicode is a universal character-coding standard for the interchange and display of principal written languages. It covers the languages of the Americas, Europe, Middle East, Africa, India, Asia, and Pacifica, as well as historic scripts and technical symbols. Unicode allows for the exchange, processing, and display of multilingual texts, as well as the use of common technical and mathematical symbols. It hopes to resolve internationalization problems of multilingual computing, such as different national character standards. Not all modern or archaic scripts, however, are currently supported.

The Unicode character set can be used for all known encoding. Unicode is modeled after the ASCII (American Standard Code for Information Interchange) character set. It uses a numerical value and name for each character. The character encoding specifies the identity of the character and its numeric value (code position), as well as the representation of this value in bits. The 16-bit numeric value (code value) is defined by a hexadecimal number and a prefix U, for example, U+0041 represents A. The unique name for this value is LATIN CAPITAL LETTER A.

**Unicode is not supported in versions of JavaScript prior to 1.3.**

### <span>Unicode compatibility with ASCII and ISO</span>

Unicode is fully compatible with the International Standard ISO/IEC 10646-1; 1993, which is a subset of ISO 10646.

Several encoding standards (including UTF-8, UTF-16 and ISO UCS-2) are used to physically represent Unicode as actual bits.

The UTF-8 encoding of Unicode is compatible with ASCII characters and is supported by many programs. The first 128 Unicode characters correspond to the ASCII characters and have the same byte value. The Unicode characters U+0020 through U+007E are equivalent to the ASCII characters 0x20 through 0x7E. Unlike ASCII, which supports the Latin alphabet and uses a 7-bit character set, UTF-8 uses between one and four octets for each character ("octet" meaning a byte, or 8 bits.) This allows for several million characters. An alternative encoding standard, UTF-16, uses two octets to represent Unicode characters. An escape sequence allows UTF-16 to represent the whole Unicode range by using four octets. The ISO UCS-2 (Universal Character Set) uses two octets.

JavaScript and Navigator support for UTF-8/Unicode means you can use non-Latin, international, and localized characters, plus special technical symbols in JavaScript programs. Unicode provides a standard way to encode multilingual text. Since the UTF-8 encoding of Unicode is compatible with ASCII, programs can use ASCII characters. You can use non-ASCII Unicode characters in the comments, string literals, identifiers, and regular expressions of JavaScript.

### <span>Unicode escape sequences</span>

You can use the Unicode escape sequence in string literals, regular expressions, and identifiers. The escape sequence consists of six ASCII characters: \\u and a four-digit hexadecimal number. For example, \\u00A9 represents the copyright symbol. Every Unicode escape sequence in JavaScript is interpreted as one character.

The following code returns the copyright symbol and the string "Netscape Communications".

    var x = "\u00A9 Netscape Communications";

The following table lists frequently used special characters and their Unicode value.

<table class="standard-table">
<caption style="text-align: left">
Table 2.2 Unicode values for special characters

</caption>
<tr>
<th scope="col">
Category

</th>
<th scope="col">
Unicode value

</th>
<th scope="col">
Name

</th>
<th scope="col">
Format name

</th>
</tr>
<tr>
<td rowspan="4">
White space values

</td>
<td>
\\u0009

</td>
<td>
Tab

</td>
<td>
\<TAB\>

</td>
</tr>
<tr>
<td>
\\u000B

</td>
<td>
Vertical Tab

</td>
<td>
\<VT\>

</td>
</tr>
<tr>
<td>
\\u000C

</td>
<td>
Form Feed

</td>
<td>
\<FF\>

</td>
</tr>
<tr>
<td>
\\u0020

</td>
<td>
Space

</td>
<td>
\<SP\>

</td>
</tr>
<tr>
<td rowspan="2">
Line terminator values

</td>
<td>
\\u000A

</td>
<td>
Line Feed

</td>
<td>
\<LF\>

</td>
</tr>
<tr>
<td>
\\u000D

</td>
<td>
Carriage Return

</td>
<td>
\<CR\>

</td>
</tr>
<tr>
<td rowspan="5">
Additional Unicode escape sequence values

</td>
<td>
\\u0008

</td>
<td>
Backspace

</td>
<td>
\<BS\>

</td>
</tr>
<tr>
<td>
\\u0009

</td>
<td>
Horizontal Tab

</td>
<td>
\<HT\>

</td>
</tr>
<tr>
<td>
\\u0022

</td>
<td>
Double Quote

</td>
<td>
"

</td>
</tr>
<tr>
<td>
\\u0027

</td>
<td>
Single Quote

</td>
<td>
'

</td>
</tr>
<tr>
<td>
\\u005C

</td>
<td>
Backslash

</td>
<td>
\\

</td>
</tr>
</table>
The JavaScript use of the Unicode escape sequence is different from Java. In JavaScript, the escape sequence is never interpreted as a special character first. For example, a line terminator escape sequence inside a string does not terminate the string before it is interpreted by the function. JavaScript ignores any escape sequence if it is used in comments. In Java, if an escape sequence is used in a single comment line, it is interpreted as an Unicode character. For a string literal, the Java compiler interprets the escape sequences first. For example, if a line terminator escape character (e.g., \\u000A) is used in Java, it terminates the string literal. In Java, this leads to an error, because line terminators are not allowed in string literals. You must use \\n for a line feed in a string literal. In JavaScript, the escape sequence works the same way as \\n.

### <span>Unicode characters in JavaScript files</span>

Earlier versions of Gecko assumed the Latin-1 character encoding for JavaScript files loaded from XUL. Starting with Gecko 1.8, the character encoding is inferred from the XUL file's encoding.

### <span>Displaying characters with Unicode</span>

You can use Unicode to display the characters in different languages or technical symbols. For characters to be displayed properly, a client such as Mozilla Firefox or Netscape needs to support Unicode. Moreover, an appropriate Unicode font must be available to the client, and the client platform must support Unicode. Often, Unicode fonts do not display all the Unicode characters. Some platforms, such as Windows 95, provide partial support for Unicode.

To receive non-ASCII character input, the client needs to send the input as Unicode. Using a standard enhanced keyboard, the client cannot easily input the additional characters supported by Unicode. Sometimes, the only way to input Unicode characters is by using Unicode escape sequences.

For more information on Unicode, see the [<http://www.unicode.org/>

**Needs Examples**: This section should include examples.

