{{Page_Title}}
{{Flags}}
{{Summary_Section|Creates a new object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= new constructor ([ arguments ]) }}
|Values={{JS_Syntax_Parameter
|Name=constructor
|Required=Required
|Description=The constructor of the object. The parentheses can be omitted if the constructor takes no arguments.}}{{JS_Syntax_Parameter
|Name=arguments
|Required=Optional
|Description=Any arguments to be passed to the new object's constructor.}}
}}
{{Remarks_Section
|Remarks=The new operator performs the following tasks:

* It creates an object with no members.
* It calls the constructor for that object, passing a pointer to the newly created object as the this pointer.
* The constructor then initializes the object according to the arguments passed to the constructor.
These are examples of valid uses of the '''new''' operator.

 my_object = new Object;
 my_array = new Array();
 my_date = new Date("Jan 5 1996");
}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ec3z6dcc(v=vs.94).aspx
|HTML5Rocks_link=
}}