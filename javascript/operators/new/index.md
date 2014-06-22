{{Page_Title}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Summary_Section|Creates a new object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=new constructor ([ arguments ])
}}
|Values={{JS Syntax Parameter
|Name=constructor
|Required=Required
|Description=The constructor of the object. The parentheses can be omitted if the constructor takes no arguments.
}}{{JS Syntax Parameter
|Name=arguments
|Required=Optional
|Description=Any arguments to be passed to the new object's constructor.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
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
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/statements/function{{!}}function Statement]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ec3z6dcc(v=vs.94).aspx
|HTML5Rocks_link=
}}