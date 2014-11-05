{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Item for later cleanup: An automatically generated list of properties and methods (either static, instance or inherited ones) is absent.
|Checked_Out=No
}}
{{Summary_Section|Allows manipulation and formatting of text strings and determination and location of substrings within strings.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=// Declaring a string literal.
var newString = "stringLiteral";

// Or, declaring a String object - discouraged, long, verbose and pretty useless.
var newString = new String([" stringLiteral "]);
}}
|Values={{JS Syntax Parameter
|Name=newString
|Required=Required
|Description=The variable name to which the String object is assigned.
}}{{JS Syntax Parameter
|Name=stringLiteral
|Required=Optional
|Description=Any group of Unicode characters.
}}
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=JavaScript provides escape sequences that you can include in strings to create characters that you cannot type directly. For example, <code>\t</code> specifies a tab character. For more information, see Special Characters (JScript).

A string literal is zero or more characters enclosed in single or double quotation marks. A string literal has a primary (primitive) data type of string. A String object is created by using the [[javascript/operators/new{{!}}new Operator]] , and has a data type of '''Object'''.

The following example shows that the data type of a string literal is not the same as that of a '''String''' object.
|Code=var strLit = "This is a string literal.";
var strObj = new String("This is a string object.");
 
document.write(typeof strLit);
document.write("&lt;br/&gt;");
document.write(typeof strObj);
// Output:
// string
// object
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=When you call a method on a string literal, it is temporarily converted to a string wrapper object. The string literal is treated as though the '''new''' operator were used to create it.

The following example applies the '''toUpperCase''' method to a string literal.
|Code=var strLit = "This is a string literal.";
 
var result1 = strLit.toUpperCase();
 
var result2 = (new String(strLit)).toUpperCase();
 
document.write(result1);
document.write("&lt;br/&gt;");
document.write(result2);
// Output: 
// THIS IS A STRING LITERAL.
// THIS IS A STRING LITERAL.
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=In modern browsers (2011 onwards), you can access an individual character of a string as a read-only array-indexed property. The following example accesses individual string characters.
|Code=var str = "abcd";
var result = str[2];
document.write (result);
// Output: c
 
var result = "the"[0];
document.write(result);
// Output: t
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
==Properties==
The following table lists the properties of the '''String''' object.

{{{!}} class='wikitable'
{{!}}-
! Property
! Description
{{!}}-
{{!}} [[javascript/String/constructor|constructor]]
{{!}} Specifies the function that creates an object.
{{!}}-
{{!}} [[javascript/String/length|length]]
{{!}} Returns the length of a String object.
{{!}}-
{{!}} [[javascript/String/prototype|prototype]]
{{!}} Returns a reference to the prototype for a class of objects.
{{!}}}

==Functions==
The following table lists the functions of the '''String''' object.

{{{!}} class='wikitable'
{{!}}-
! Function
! Description
{{!}}-
{{!}} [[javascript/String/fromCharCode|fromCharCode]]
{{!}} Returns a string from a number of Unicode character values.
{{!}}}

==Methods==
The following table lists the methods of the '''String''' object.

{{{!}} class='wikitable'
{{!}}-
! Method
! Description
{{!}}-
{{!}} [[javascript/String/HTML Tag Methods|HTML Tag Methods]]
{{!}} Places various HTML tags around text.
{{!}}-
{{!}} [[javascript/String/charAt|charAt]]
{{!}} Returns the character at the specified index.
{{!}}-
{{!}} [[javascript/String/charCodeAt|charCodeAt]]
{{!}} Returns the Unicode encoding of the specified character.
{{!}}-
{{!}} [[javascript/String/concat|concat]]
{{!}} Returns a string that contains the concatenation of two supplied strings.
{{!}}-
{{!}} [[javascript/String/indexOf|indexOf]]
{{!}} Returns the character position where the first occurrence of a substring occurs within a string.
{{!}}-
{{!}} [[javascript/String/lastIndexOf|lastIndexOf]]
{{!}} Returns the last occurrence of a substring within a string.
{{!}}-
{{!}} [[javascript/String/localeCompare|localeCompare]]
{{!}} Returns a value that indicates whether two strings are equivalent in the current locale.
{{!}}-
{{!}} [[javascript/String/match|match]]
{{!}} Searches a string by using a supplied '''Regular Expression''' object and returns the results as an array.
{{!}}-
{{!}} [[javascript/String/replace|replace]]
{{!}} Uses a regular expression to replace text in a string and returns the result.
{{!}}-
{{!}} [[javascript/String/search|search]]
{{!}} Returns the position of the first substring match in a regular expression search.
{{!}}-
{{!}} [[javascript/String/slice|slice]]
{{!}} Returns a section of a string.
{{!}}-
{{!}} [[javascript/String/split|split]]
{{!}} Returns the array of strings that results when a string is separated into substrings.
{{!}}-
{{!}} [[javascript/String/substr|substr]]
{{!}} Returns a substring beginning at a specified location and having a specified length.
{{!}}-
{{!}} [[javascript/String/substring|substring]]
{{!}} Returns the substring at a specified location within a String object.
{{!}}-
{{!}} [[javascript/String/toLocaleLowerCase|toLocaleLowerCase]]
{{!}} Returns a string in which all alphabetic characters are converted to lowercase, taking into account the host environment's current locale.
{{!}}-
{{!}} [[javascript/String/toLocaleUpperCase|toLocaleUpperCase]]
{{!}} Returns a string in which all alphabetic characters are converted to uppercase, taking into account the host environment's current locale.
{{!}}-
{{!}} [[javascript/String/toLowerCase|toLowerCase]]
{{!}} Returns a string in which all alphabetic characters are converted to lowercase.
{{!}}-
{{!}} [[javascript/String/toString|toString]]
{{!}} Returns the string.
{{!}}-
{{!}} [[javascript/String/toUpperCase|toUpperCase]]
{{!}} Returns a string in which all alphabetic characters are converted to uppercase.
{{!}}-
{{!}} [[javascript/String/trim|trim]]
{{!}} Returns a string with leading and trailing white space and line terminator characters removed.
{{!}}-
{{!}} [[javascript/String/valueOf|valueOf]]
{{!}} Returns the string.
{{!}}}

{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/new{{!}}new Operator]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ecczf11c(v=vs.94).aspx
|HTML5Rocks_link=
}}