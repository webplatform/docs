{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Converts a JavaScript Object Notation (JSON) string into an object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=JSON.parse( text [ , reviver] )
}}
|Values={{JS Syntax Parameter
|Name=text
|Required=Required
|Description=A valid JSON string.
}}{{JS Syntax Parameter
|Name=reviver
|Required=Optional
|Description=A function that transforms the results. This function is called for each member of the object. If a member contains nested objects, the nested objects are transformed before the parent object is. For each member, the following occurs: If reviver returns a valid value, the member value is replaced with the transformed value.If reviver returns the same value it received, the member value is not modified.If reviver returns null or undefined , the member is deleted.
}}
}}
{{JS_Return_Value
|Description=An object or array.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example uses '''JSON.parse''' to convert a JSON string to an object.
|Code=var jsontext = '{"firstname":"Jesper","surname":"Aaberg","phone":["555-0100","555-0120"]}';
 var contact = JSON.parse(jsontext);
 document.write(contact.surname + ", " + contact.firstname);
 
 // Output: Aaberg, Jesper
}}{{Single Example
|Language=JavaScript
|Description=The following example shows how to convert an array to a JSON string by using '''JSON.stringify''' , and then convert the string back to an array by using '''JSON.parse'''.
|Code=var arr = ["a", "b", "c"];
 var str = JSON.stringify(arr);
 document.write(str);
 document.write ("&lt;br/&gt;");
 
 var newArr = JSON.parse(str);
 
 while (newArr.length &gt; 0) {
     document.write(newArr.pop() + "&lt;br/&gt;");
 }
 
 // Output:
 var arr = ["a", "b", "c"];
 var str = JSON.stringify(arr);
 document.write(str);
 document.write ("&lt;br/&gt;");
 
 var newArr = JSON.parse(str);
 
 while (newArr.length &gt; 0) {
     document.write(newArr.pop + "&lt;br/&gt;");
 }
 
 // Output:
 ["a","b","c"]
 c
 b
 a
}}{{Single Example
|Language=JavaScript
|Description=The reviver function is often used to transform JSON representation of International Organization for Standardization (ISO) date strings into Coordinated Universal Time (UTC) format Date objects.

This example uses JSON.parse to deserialize an ISO-formatted date string. The <code>dateReviver</code> function returns <code>Date</code> objects for members that are formatted like ISO date strings.
|Code=var jsontext = '{ "hiredate": "2008-01-01T12:00:00Z", "birthdate": "2008-12-25T12:00:00Z" }';
 var dates = JSON.parse(jsontext, dateReviver);
 document.write(dates.birthdate.toUTCString());
 
 function dateReviver(key, value) {
     var a;
     if (typeof value === 'string') {
         a = /^(\d{4})-(\d{2})-(\d{2})T(\d{2}):(\d{2}):(\d{2}(?:\.\d*)?)Z$/.exec(value);
         if (a) {
             return new Date(Date.UTC(+a[1], +a[2] - 1, +a[3], +a[4],
                             +a[5], +a[6]));
         }
     }
     return value;
 };
 
 // Output:
 // Thu, 25 Dec 2008 12:00:00 UTC
}}
}}
{{Remarks_Section}}
{{Notes_Section}}
{{JS Object Listing}}
==Exceptions==
If this function provokes a JavaScript parser error (such as "SCRIPT1014: Invalid character", the input text does not comply with JSON syntax. To correct the error, do one of the following:

* Modify the text argument to comply with JSON syntax. For more information, see the [http://go.microsoft.com/fwlink/?LinkId=125203 BNF syntax notation] of JSON objects.
* Make sure that the text argument was serialized by a JSON-compliant implementation, such as '''JSON.stringify'''.


{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/JSON/stringify{{!}}JSON.stringify Function]]
* [[javascript/Date/toJSON{{!}}toJSON Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/cc836466(v=vs.94).aspx
|HTML5Rocks_link=
}}