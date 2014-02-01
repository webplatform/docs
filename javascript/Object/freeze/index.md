{{Page_Title}}
{{Flags}}
{{Summary_Section|Prevents the modification of existing property attributes and values, and prevents the addition of new properties.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= Object.freeze( object )}}
|Values={{JS_Syntax_Parameter
|Name=object
|Required=Required
|Description=The object on which to lock the attributes.}}
}}
{{JS_Return_Value
|Description=The object that is passed to the function.}}
==Exceptions==
If the object argument is not an object, a TypeError exception is thrown.
{{Remarks_Section
|Remarks=The Object.freeze function does the following:

* Makes the object non-extensible, so that new properties cannot be added to it.
* Sets the configurable attribute to false for all properties of the object. When configurable is false , the property attributes cannot be changed and the property cannot be deleted.
* Sets the writable attribute to false for all data properties of the object. When writable is false, the data property value cannot be changed.
For more information about how to set property attributes, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]. To obtain the attributes of a property, you can use the [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]].

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
{{!}} '''Object.freeze'''
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
{{!}} Yes
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
|Description=The following example illustrates the use of the '''Object.freeze''' function.

|Code= // Create an object that has two properties.
 var obj = { pasta: "spaghetti", length: 10 };
 
 // Freeze the object.
 Object.freeze(obj);
 
 // Try to add a new property, and then verify that it is not added. 
     obj.newProp = 50;
     document.write(obj.newProp);
     document.write("&lt;br/&gt;");
 
 // Try to delete a property, and then verify that it is still present. 
 delete obj.length;
 document.write(obj.length);
 document.write("&lt;br/&gt;");
 
 // Try to change a property value, and then verify that it is not changed. 
 obj.pasta = "linguini";
 document.write(obj.pasta);
 
 // Output:
 // undefined
 // 10
 // spaghetti
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/preventExtensions{{!}}Object.preventExtensions Function]]
* [[javascript/Object/seal{{!}}Object.seal Function]]
* [[javascript/Object/isExtensible{{!}}Object.isExtensible Function]]
* [[javascript/Object/isSealed{{!}}Object.isSealed Function]]
* [[javascript/Object/isFrozen{{!}}Object.isFrozen Function]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff806186(v=vs.94).aspx
|HTML5Rocks_link=
}}