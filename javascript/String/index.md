{{Page_Title}}
{{Flags}}
{{Summary_Section|Allows manipulation and formatting of text strings and determination and location of substrings within strings.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= newString = new String([" stringLiteral "])}}
|Values={{JS_Syntax_Parameter
|Name=newString
|Required=Required
|Description=The variable name to which the String object is assigned.}}{{JS_Syntax_Parameter
|Name=stringLiteral
|Required=Optional
|Description=Any group of Unicode characters.}}
}}
{{Remarks_Section
|Remarks=JavaScript provides escape sequences that you can include in strings to create characters that you cannot type directly. For example, <code>\t</code> specifies a tab character. For more information, see Special Characters (JScript).

A string literal is zero or more characters enclosed in single or double quotation marks. A string literal has a primary (primitive) data type of string. A String object is created by using the [[javascript/operators/new{{!}}new Operator]] , and has a data type of '''Object'''.

The following example shows that the data type of a string literal is not the same as that of a '''String''' object.

 var strLit = "This is a string literal.";
 var strObj = new String("This is a string object.");
 
 document.write(typeof strLit);
 document.write("&lt;br/&gt;");
 document.write(typeof strObj);
 // Output:
 // string
 // object
When you call a method on a string literal, it is temporarily converted to a string wrapper object. The string literal is treated as though the '''new''' operator were used to create it.

The following example applies the '''toUpperCase''' method to a string literal.

 var strLit = "This is a string literal.";
 
 var result1 = strLit.toUpperCase();
 
 var result2 = (new String(strLit)).toUpperCase();
 
 document.write(result1);
 document.write("&lt;br/&gt;");
 document.write(result2);
 // Output: 
 // THIS IS A STRING LITERAL.
 // THIS IS A STRING LITERAL.
You can access an individual character of a string as a read-only array-indexed property. This feature was introduced in Internet Explorer 9 standards mode, Internet Explorer 10 standards mode, and win8_appname_long apps. The following example accesses individual string characters.

 var str = "abcd";
 var result = str[2];
 document.write (result);
 // Output: c
 
 var result = "the"[0];
 document.write(result);
 // Output: t
}}
==Properties==
The following table lists the properties of the '''String''' object.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/String/constructor|constructor Property]]
| Specifies the function that creates an object.
|-
| [[javascript/String/length|length Property (String)]]
| Returns the length of a String object.
|-
| [[javascript/String/prototype|prototype Property]]
| Returns a reference to the prototype for a class of objects.
|}
==Functions==
The following table lists the functions of the '''String''' object.

{| class='wikitable'
|-
! Function
! Description
|-
| [[javascript/String/fromCharCode|String.fromCharCode Function]]
| Returns a string from a number of Unicode character values.
|}
==Methods==
The following table lists the methods of the '''String''' object.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/String/HTML Tag Methods|anchor Method]]
| Places an HTML anchor that has a NAME attribute around text.
|-
| [[javascript/String/HTML Tag Methods|big Method]]
| Places HTML &lt;BIG&gt; tags around text.
|-
| [[javascript/String/HTML Tag Methods|blink Method]]
| Places HTML &lt;BLINK&gt; tags around text.
|-
| [[javascript/String/HTML Tag Methods|bold Method]]
| Places HTML &lt;B&gt; tags around text.
|-
| [[javascript/String/charAt|charAt Method]]
| Returns the character at the specified index.
|-
| [[javascript/String/charCodeAt|charCodeAt Method]]
| Returns the Unicode encoding of the specified character.
|-
| [[javascript/String/concat|concat Method (String)]]
| Returns a string that contains the concatenation of two supplied strings.
|-
| [[javascript/String/HTML Tag Methods|fixed Method]]
| Places HTML &lt;TT&gt; tags around text.
|-
| [[javascript/String/HTML Tag Methods|fontcolor Method]]
| Places HTML &lt;FONT&gt; tags with a COLOR attribute around text.
|-
| [[javascript/String/HTML Tag Methods|fontsize Method]]
| Places HTML &lt;FONT&gt; tags with a SIZE attribute around text.
|-
| [[javascript/Object/hasOwnProperty|hasOwnProperty Method]]
| Returns a Boolean value that indicates whether an object has a property with the specified name.
|-
| [[javascript/String/indexOf|indexOf Method (String)]]
| Returns the character position where the first occurrence of a substring occurs within a string.
|-
| [[javascript/Object/isPrototypeOf|isPrototypeOf Method]]
| Returns a Boolean value that indicates whether an object exists in another object's prototype chain.
|-
| [[javascript/String/HTML Tag Methods|italics Method]]
| Places HTML &lt;I&gt; tags around text.
|-
| [[javascript/String/lastIndexOf|lastIndexOf Method (String)]]
| Returns the last occurrence of a substring within a string.
|-
| [[javascript/String/HTML Tag Methods|link Method]]
| Places an HTML anchor that has an HREF attribute around text.
|-
| [[javascript/String/localeCompare|localeCompare Method]]
| Returns a value that indicates whether two strings are equivalent in the current locale.
|-
| [[javascript/String/match|match Method]]
| Searches a string by using a supplied '''Regular Expression''' object and returns the results as an array.
|-
| [[javascript/Object/propertyIsEnumerable|propertyIsEnumerable Method]]
| Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.
|-
| [[javascript/String/replace|replace Method]]
| Uses a regular expression to replace text in a string and returns the result.
|-
| [[javascript/String/search|search Method]]
| Returns the position of the first substring match in a regular expression search.
|-
| [[javascript/String/slice|slice Method (String)]]
| Returns a section of a string.
|-
| [[javascript/String/HTML Tag Methods|small Method]]
| Places HTML &lt;SMALL&gt; tags around text.
|-
| [[javascript/String/split|split Method]]
| Returns the array of strings that results when a string is separated into substrings.
|-
| [[javascript/String/HTML Tag Methods|strike Method]]
| Places HTML &lt;STRIKE&gt; tags around text.
|-
| [[javascript/String/HTML Tag Methods|sub Method]]
| Places HTML &lt;SUB&gt; tags around text.
|-
| [[javascript/String/substr|substr Method]]
| Returns a substring beginning at a specified location and having a specified length.
|-
| [[javascript/String/substring|substring Method]]
| Returns the substring at a specified location within a String object.
|-
| [[javascript/String/HTML Tag Methods|sup Method]]
| Places HTML &lt;SUP&gt; tags around text.
|-
| [[javascript/String/toLocaleLowerCase|toLocaleLowerCase Method]]
| Returns a string in which all alphabetic characters are converted to lowercase, taking into account the host environment's current locale.
|-
| [[javascript/Object/toLocaleString|toLocaleString Method]]
| Returns an object converted to a string, using the current locale.
|-
| [[javascript/String/toLocaleUpperCase|toLocaleUpperCase Method]]
| Returns a string in which all alphabetic characters are converted to uppercase, taking into account the host environment's current locale.
|-
| [[javascript/String/toLowerCase|toLowerCase Method]]
| Returns a string in which all alphabetic characters are converted to lowercase.
|-
| [[javascript/String/toString|toString Method]]
| Returns the string.
|-
| [[javascript/String/toUpperCase|toUpperCase Method]]
| Returns a string in which all alphabetic characters are converted to uppercase.
|-
| [[javascript/String/trim|trim Method]]
| Returns a string with leading and trailing white space and line terminator characters removed.
|-
| [[javascript/String/valueOf|valueOf Method]]
| Returns the string.
|}
{{See_Also_Section
|Manual_links=* [[javascript/operators/new{{!}}new Operator]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ecczf11c(v=vs.94).aspx
|HTML5Rocks_link=
}}