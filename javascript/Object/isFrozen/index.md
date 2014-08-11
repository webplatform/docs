{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns true if existing property attributes and values cannot be modified in an object, and new properties cannot be added to the object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Object.isFrozen( object )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object to test.
}}
}}
{{JS_Return_Value
|Description=true if all of the following are true:

* The object is non-extensible, which indicates that new properties cannot be added to the object.
* The configurable attribute is false for all existing properties.
* The writable attribute is false for all existing data properties.
If the object has no existing properties, the function returns true if the object is non-extensible.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Object.isFrozen''' function.
|Code=// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };
 
 // Freeze the object, and verify that it is frozen.
 Object.freeze(obj);
 document.write(obj.isFrozen());
 
 // Try to add a new property, and then verify that it is not added. 
 obj.newProp = 50;
 document.write (obj.newProp);
 document.write ("&lt;br/&gt;");
 
 // Try to delete a property, and then verify that it is still present.
 delete obj.length;
 document.write (obj.length);
 document.write ("&lt;br/&gt; ");
 
 // Try to change a property value, and then verify that it is not changed.
 obj.pasta = "linguini";
 document.write (obj.pasta);
 
 // Output:
 // true
 // undefined
 // 10
 // spaghetti
}}
}}
{{Remarks_Section
|Remarks=When the configurable attribute of a property is false , the property attributes cannot be changed and the property cannot be deleted. When writable is false , the data property value cannot be changed. When configurable is false and writable is true , the value and writable attributes can be changed.

For information about how to set property attributes, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]. To obtain the attributes of a property, you can use the [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]].

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
{{!}} [[javascript/Object/isExtensible{{!}}Object.isExtensible]]
{{!}} Yes
{{!}} No
{{!}} No
{{!}}-
{{!}} [[javascript/Object/isSealed{{!}}Object.isSealed]]
{{!}} No
{{!}} Yes
{{!}} No
{{!}}-
{{!}} '''Object.isFrozen'''
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
* [[javascript/Object/isExtensible{{!}}Object.isExtensible Function]]
* [[javascript/Object/isSealed{{!}}Object.isSealed Function]]
* [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]
* [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]]
* [[javascript/Object/getOwnPropertyNames{{!}}Object.getOwnPropertyNames Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff806185(v=vs.94).aspx
|HTML5Rocks_link=
}}