{{Page_Title}}
{{Flags}}
{{Summary_Section|Converts a JavaScript value to a JavaScript Object Notation (JSON) string.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= '''JSON.stringify(''' value [ , replacer] [ , space] ''')'''}}
|Values={{JS_Syntax_Parameter
|Name=value
|Required=Required
|Description=A JavaScript value, usually an object or array, to be converted.}}{{JS_Syntax_Parameter
|Name=replacer
|Required=Optional
|Description=A function or array that transforms the results.If replacer is a function, JSON.stringify calls the function, passing in the key and value of each member. The return value is used instead of the original value. If the function returns undefined , the member is excluded. The key for the root object is an empty string: "".If replacer is an array, only members with key values in the array will be converted. The order in which the members are converted is the same as the order of the keys in the array. The replacer array is ignored when the value argument is also an array.}}{{JS_Syntax_Parameter
|Name=space
|Required=Optional
|Description=Adds indentation, white space, and line break characters to the return-value JSON text to make it easier to read.If space is omitted, the return-value text is generated without any extra white space.If space is a number, the return-value text is indented with the specified number of white spaces at each level. If space is greater than 10, text is indented 10 spaces.If space is a non-empty string, such as '\t', the return-value text is indented with the characters in the string at each level.If space is a string that is longer than 10 characters, the first 10 characters are used.}}
}}
{{JS_Return_Value
|Description=A string that contains the JSON text.}}
==Exceptions==
{| class='wikitable'
|-
! Exception
! Condition
|-
| Invalid replacer argument
| The replacer argument is not a function or an array.
|-
| Circular reference in value argument not supported
| The value argument contains a circular reference.
|}
{{Remarks_Section
|Remarks=If value has a toJSON method, the JSON.stringify function uses the return value of that method. If the return value of the toJSON method is undefined , the member is not converted. This enables an object to determine its own JSON representation.

Values that do not have JSON representations, such as undefined , will not be converted. In objects, they will be dropped. In arrays, they will be replaced with null.

String values begin and end with a quotation mark. All Unicode characters may be enclosed in the quotation marks except for the characters that must be escaped by using a backslash. The following characters must be preceded by a backslash:

* Quotation mark (")
* Backslash (\)
* Backspace (b)
* Formfeed (f)
* Newline (n)
* Carriage return (r)
* Horizontal tab (t)
* Four-hexadecimal-digits (uhhhh)
During the serialization process, if a toJSON method exists for the value argument, JSON.stringify first calls the toJSON method. If it does not exist, the original value is used. Next, if a replacer argument is provided, the value (original value or toJSON return-value) is replaced with the return-value of the replacer argument. Finally, white spaces are added to the value based on the optional space argument to generate the final JSON text.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=This example uses JSON.stringify to convert the <code>contact</code> object to JSON text. The <code>memberfilter</code> array is defined so that only the <code>surname</code> and <code>phone</code> members are converted. The <code>firstname</code> member is omitted.

|Code= var contact = new Object();
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
}}{{Single_Example
|Language=JavaScript
|Description=This example uses JSON.stringify with an array. The <code>replaceToUpper</code> function converts every string in the array to uppercase.

|Code= var continents = new Array();
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
}}{{Single_Example
|Language=JavaScript
|Description=This example uses the toJSON method to convert string values to uppercase.

|Code= var contact = new Object(); 
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
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/JSON/parse{{!}}JSON.parse Function]]
* [[javascript/Date/toJSON{{!}}toJSON Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}