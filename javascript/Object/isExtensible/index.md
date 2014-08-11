{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns a value that indicates whether new properties can be added to an object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Object.isExtensible( object )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object to test.
}}
}}
{{JS_Return_Value
|Description=true if the object is extensible, which indicates that new properties can be added to the object; otherwise, false.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Object.isExtensible''' function.
|Code=// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };
 
 // Make the object non-extensible.
 Object.preventExtensions(obj);
 
 // Try to add a new property, and then verify that it is not added.
 obj.newProp = 50;
 document.write(obj.newProp);
 
 // Output:
 undefined
}}
}}
{{Remarks_Section
|Remarks=For information about how to set property attributes, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]. To obtain the attributes of a property, you can use the [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]].

The following related functions prevent the modification of object attributes.

{{{!}} class='wikitable'
{{!}}-
! Function
! Object is made non-extensible
! configurable is set to false for each property
! writable is set to false for each property
{{!}}-
{{!}} [[javascript/Object/preventExtensions{{!}}Object.preventExtensions]]
{{!}} Yes
{{!}} No
{{!}} No
{{!}}-
{{!}} [[javascript/Object/seal{{!}}Object.seal]]
{{!}} Yes
{{!}} Yes
{{!}} No
{{!}}-
{{!}} [[javascript/Object/freeze{{!}}Object.freeze]]
{{!}} Yes
{{!}} Yes
{{!}} Yes
{{!}}} 
The following functions return true if all of the conditions marked in the following table are true.

{{{!}} class='wikitable'
{{!}}-
! Function
! Object is extensible?
! configurable is false for all properties?
! writable is false for all data properties?
{{!}}-
{{!}} '''Object.isExtensible'''
{{!}} Yes
{{!}} No
{{!}} No
{{!}}-
{{!}} [[javascript/Object/isSealed{{!}}Object.isSealed]]
{{!}} No
{{!}} Yes
{{!}} No
{{!}}-
{{!}} [[javascript/Object/isFrozen{{!}}Object.isFrozen]]
{{!}} No
{{!}} Yes
{{!}} Yes
{{!}}}
}}
{{Notes_Section}}
{{JS Object Listing}}
==Exceptions==
If the object argument is not an object, a TypeError exception is thrown.



{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/preventExtensions{{!}}Object.preventExtensions Function]]
* [[javascript/Object/seal{{!}}Object.seal Function]]
* [[javascript/Object/freeze{{!}}Object.freeze Function]]
* [[javascript/Object/isSealed{{!}}Object.isSealed Function]]
* [[javascript/Object/isFrozen{{!}}Object.isFrozen Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff806188(v=vs.94).aspx
|HTML5Rocks_link=
}}