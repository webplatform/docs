{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Adds one or more properties to an object, and/or modifies attributes of existing properties.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=object.defineProperties( object , descriptors )
}}
|Values={{JS Syntax Parameter
|Name=object
|Required=Required
|Description=The object on which to add or modify the properties. This can be a native JavaScript object or a DOM object.
}}{{JS Syntax Parameter
|Name=descriptors
|Required=Required
|Description=A JavaScript object that contains one or more descriptor objects. Each descriptor object describes a data property or an accessor property.
}}
}}
{{JS_Return_Value
|Description=The object that was passed to the function.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description='''Adding Properties'''

In the following example, the '''Object.defineProperties''' function adds a data property and an accessor property to a user-defined object.

The example uses an object literal to create the descriptors object with the <code>newDataProperty</code> and <code>newAccessorProperty</code> descriptor objects.

|Code=var newLine = "&lt;br /&gt;";
 
var obj = {};
Object.defineProperties(obj, {
    newDataProperty: {
        value: 101,
        writable: true,
        enumerable: true,
        configurable: true
    },
    newAccessorProperty: {
        set: function (x) {
            document.write("in property set accessor" + newLine);
            this.newaccpropvalue = x;
        },
        get: function () {
            document.write("in property get accessor" + newLine);
            return this.newaccpropvalue;
        },
        enumerable: true,
        configurable: true
    }});

// Set the accessor property value.
obj.newAccessorProperty = 10;
document.write ("newAccessorProperty value: " + obj.newAccessorProperty + newLine);

// Output:
// in property set accessor
// in property get accessor
// newAccessorProperty value: 10

}}{{Single Example
|Language=JavaScript
|Description=Like the previous example, the following example adds properties dynamically instead of with an object literal.
|Code=var newLine = "&lt;br /&gt;";
 
// Create the descriptors object.
var descriptors = new Object();
 
// Add a data property descriptor to the descriptors object.
descriptors.newDataProperty = new Object();
descriptors.newDataProperty.value = 101;
descriptors.newDataProperty.writable = true;
descriptors.newDataProperty.enumerable = true;
descriptors.newDataProperty.configurable = true;
 
// Add an accessor property descriptor to the descriptors object.
descriptors.newAccessorProperty = new Object();
descriptors.newAccessorProperty.set = function (x) {
    document.write("in property set accessor" + newLine);
    this.newaccpropvalue = x;
};
descriptors.newAccessorProperty.get = function () {
    document.write("in property get accessor" + newLine);
    return this.newaccpropvalue;
};
descriptors.newAccessorProperty.enumerable = true;
descriptors.newAccessorProperty.configurable = true;
 
// Call the Object.defineProperties function.
var obj = new Object();
Object.defineProperties(obj, descriptors);
 
// Set the accessor property value.
obj.newAccessorProperty = 10;
document.write ("newAccessorProperty value: " + obj.newAccessorProperty + newLine);
 
// Output:
// in property set accessor
// in property get accessor
// newAccessorProperty value: 10

}}{{Single Example
|Language=JavaScript
|Description='''Modifying Properties'''

To modify property attributes for the object, add the following code. The '''Object.defineProperties''' function modifies the writable attribute of <code>newDataProperty</code> , and modifies the enumerable attribute of <code>newAccessorProperty</code>. It adds <code>anotherDataProperty</code> to the object because that property name does not already exist.

|Code=Object.defineProperties(obj, {
        newDataProperty: { writable: false },
        newAccessorProperty: { enumerable: false },
        anotherDataProperty: { value: "abc" }
    });

}}
}}
{{Remarks_Section
|Remarks=The descriptors argument is an object that contains one or more descriptor objects.

A data property is a property that can store and retrieve a value. A data property descriptor contains a value attribute, a writable attribute, or both. For more information, see Data Properties and Accessor Properties.

An accessor property calls a user-provided function every time the property value is set or retrieved. An accessor property descriptor contains a set attribute, a get attribute, or both.

If the object already has a property that has the specified name, the property attributes are modified. For more information, see [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]].

To create an object and add properties to the new object, you can use the [[javascript/Object/create{{!}}Object.create Function]].
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Object/getOwnPropertyDescriptor{{!}}Object.getOwnPropertyDescriptor Function]]
* [[javascript/Object/getOwnPropertyNames{{!}}Object.getOwnPropertyNames Function]]
* [[javascript/Object/defineProperty{{!}}Object.defineProperty Function]]
* [[javascript/Object/create{{!}}Object.create Function]]
* [[javascript/Object{{!}}Object Object]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff800817(v=vs.94).aspx
|HTML5Rocks_link=
}}