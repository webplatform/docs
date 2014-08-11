{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Prevents the modification of attributes of existing properties, and prevents the addition of new properties.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Object.seal( object )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object on which to lock the attributes.
}}
}}
{{JS_Return_Value
|Description=The object that is passed to the function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Object.seal''' function.
|Code=// Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };
 // Seal the object.
 Object.seal(obj);
 document.write(Object.isSealed(obj));
 document.write("&lt;br/&gt;");
 
 // Try to add a new property, and then verify that it is not added. 
 obj.newProp = 50;
 document.write(obj.newProp);
 document.write("&lt;br/&gt;");
 
 // Try to delete a property, and then verify that it is still present. 
 delete obj.length;
 document.write(obj.length);
 
 // Output:
 // true
 // undefined
 // 10
}}
}}
{{Remarks_Section
|Remarks=The '''Object.seal''' function does both of the following:

* Makes the object non-extensible, so that new properties cannot be added to it.
* Sets the configurable attribute to false for all properties of the object.
When the configurable attribute is false , property attributes cannot be changed and the property cannot be deleted. When configurable is false and writable is true , the value and writable attributes can be changed.

The '''Object.seal''' function does not change the writable attribute.

For more information about how to set property attributes, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]. To get the attributes of a property, you can use the [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]].

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
{{!}} Object.seal
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
* [[javascript/Object/freeze{{!}}Object.freeze Function]]
* [[javascript/Object/isExtensible{{!}}Object.isExtensible Function]]
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
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff806192(v=vs.94).aspx
|HTML5Rocks_link=
}}