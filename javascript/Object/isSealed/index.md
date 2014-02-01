{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns true if existing property attributes cannot be modified in an object and new properties cannot be added to the object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Object.isSealed( object )}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=The object to test.}}
}}
{{JS_Return_Value
|Description=true if both of the following are true:

* The object is non-extensible, which indicates that new properties cannot be added to the object.
* The configurable attribute is false for all existing properties.
If the object does not have any properties, the function returns true if the object is non-extensible.}}
==Exceptions==
If the object argument is not an object, a TypeError exception is thrown.
{{Remarks_Section
|Remarks=When the configurable attribute of a property is false , the property attributes cannot be changed and the property cannot be deleted. When writable is false , the data property value cannot be changed. When configurable is false and writable is true , the value and writable attributes can be changed.

The '''Object.isSealed''' function does not use the writable attribute of properties to determine its return value.

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
{{!}} '''Object.isSealed'''
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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example illustrates the use of the '''Object.isSealed''' function.

|Code= // Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };
 
 // Seal the object, and verify that it is sealed.
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
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/preventExtensions{{!}}Object.preventExtensions Function]]
* [[javascript/Object/seal{{!}}Object.seal Function]]
* [[javascript/Object/freeze{{!}}Object.freeze Function]]
* [[javascript/Object/isExtensible{{!}}Object.isExtensible Function]]
* [[javascript/Object/isFrozen{{!}}Object.isFrozen Function]]
* [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]
* [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff806189(v=vs.94).aspx
|HTML5Rocks_link=
}}