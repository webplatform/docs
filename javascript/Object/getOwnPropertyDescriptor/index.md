{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Gets the own property descriptor of the specified object. An own property descriptor is one that is defined directly on the object and is not inherited from the object's prototype.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=Object.getOwnPropertyDescriptor( object , propertyname )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object that contains the property.
}}{{JS Syntax Parameter
|Name=propertyname
|Required=Required
|Description=The name of the property.
}}
}}
{{JS_Return_Value
|Description=The descriptor of the property.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example gets a data property descriptor and uses it to make the property read-only.
|Code=// Create a user-defined object.
var obj = {};
 
// Add a data property.
obj.newDataProperty = "abc";
 
// Get the property descriptor.
var descriptor = Object.getOwnPropertyDescriptor(obj, "newDataProperty");
 
// Change a property attribute.
descriptor.writable = false;
Object.defineProperty(obj, "newDataProperty", descriptor);
}}{{Single Example
|Language=JavaScript
|Description=To list the property attributes, you can add the following code to this example.

|Code=// Get the descriptor from the object.
var desc2 = Object.getOwnPropertyDescriptor(obj, "newDataProperty");
 
// List the descriptor attributes.
for (var prop in desc2) {
    document.write(prop + ': ' + desc2[prop]);
    document.write("&lt;br /&gt;");
}
 
// Output:
// value: abc
// writable: false
// enumerable: true
// configurable: true
}}
}}
{{Remarks_Section
|Remarks=You can use the '''Object.getOwnPropertyDescriptor''' function to obtain a descriptor object that describes attributes of the property.

The [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]] is used to add or modify properties.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/dd548686(v=vs.94).aspx
|HTML5Rocks_link=
}}