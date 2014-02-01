{{Page_Title}}
{{Flags}}
{{Summary_Section|An intrinsic object that provides functions to convert JavaScript values to and from the JavaScript Object Notation (JSON) format. The JSON.stringify function serializes a JavaScript value to JSON text. The JSON.parse function deserializes JSON text to produce a JavaScript value.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= JSON.[method]}}
|Values={{JS_Syntax_Parameter
|Name=Method
|Required=Required
|Description=Name of one of the methods of the JSON object.}}
}}
{{Remarks_Section
|Remarks=You cannot create a JSON object by using the new operator. An error occurs if you try to do this. However, you can override or modify the JSON object.

The scripting engine creates the JSON object when the engine is loaded. Its methods are available to your script at all times.

To use the intrinsic JSON object, make sure that you do not override it with another JSON object that is defined in your script. You may need to modify existing script statements that detect the presence of a JSON object because those statements will evaluate differently. This is demonstrated in the following example.

 if (!this.JSON) {
     // JSON object does not exist.
     }
In the previous example, <code>!this.JSON</code> evaluates to false in Internet Explorer 8 standards mode, Internet Explorer 9 standards mode, Internet Explorer 10 standards mode, and win8_appname_long apps. Therefore, the code inside the if statement does not execute.
}}
==Functions==
[[javascript/JSON/parse|JSON.parse Function]]

[[javascript/JSON/stringify|JSON.stringify Function]]
{{See_Also_Section
|Manual_links=* [[javascript/Date/toJSON{{!}}toJSON Method (Date)]]
* [[javascript/objects{{!}}JavaScript Objects]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/cc836458(v=vs.94).aspx
|HTML5Rocks_link=
}}