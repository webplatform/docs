{{Page_Title}}
{{Flags}}
{{Summary_Section|Provides functionality common to all JavaScript objects.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= obj ''' = new Object(''' [ value ] ''')''' }}
|Values={{JS_Syntax_Parameter
|Name=obj
|Required=Required
|Description=The variable name to which the Object object is assigned.}}{{JS_Syntax_Parameter
|Name=value
|Required=Optional
|Description=Any one of the JavaScript primitive data types (Number, Boolean, or String). If value is an object, the object is returned unmodified. If value is null , '''undefined''' , or not supplied, an object with no content is created.}}
}}
{{Remarks_Section
|Remarks=The Object object is contained in all other JavaScript objects; all of its methods and properties are available in all other objects. The methods can be redefined in user-defined objects, and are called by JavaScript at appropriate times. The '''toString''' method is an example of a frequently redefined Object method.

In this language reference, the description of each Object method includes both default and object-specific implementation information for the intrinsic JavaScript objects.
}}
==Properties==
The following table lists properties of the '''Object Object'''.

{| class='wikitable'
|-
! Property
! Description
|-
| [[javascript/Object/constructor|constructor Property]]
| Specifies the function that creates an object.
|-
| [[javascript/Object/prototype|prototype Property]]
| Returns a reference to the prototype for a class of objects.
|}
==Functions==
The following table lists functions of the '''Object Object'''.

{| class='wikitable'
|-
! Function
! Description
|-
| [[javascript/Object/create|Object.create Function]]
| Creates an object that has a specified prototype, and that optionally contains specified properties.
|-
| [[javascript/Object/defineProperties|Object.defineProperties Function]]
| Adds one or more properties to an object, and/or modifies attributes of existing properties.
|-
| [[javascript/Object/defineProperty|Object.defineProperty Function]]
| Adds a property to an object, or modifies attributes of an existing property.
|-
| [[javascript/Object/freeze|Object.freeze Function]]
| Prevents the modification of existing property attributes and values, and prevents the addition of new properties.
|-
| [[javascript/Object/getOwnPropertyDescriptor|Object.getOwnPropertyDescriptor Function]]
| Returns the definition of a data property or an accessor property.
|-
| [[javascript/Object/getOwnPropertyNames|Object.getOwnPropertyNames Function]]
| Returns the names of the properties and methods of an object.
|-
| [[javascript/Object/getPrototypeOf|Object.getPrototypeOf Function]]
| Returns the prototype of an object.
|-
| [[javascript/Object/isExtensible|Object.isExtensible Function]]
| Returns a value that indicates whether new properties can be added to an object.
|-
| [[javascript/Object/isFrozen|Object.isFrozen Function]]
| Returns true if existing property attributes and values cannot be modified in an object and new properties cannot be added to the object.
|-
| [[javascript/Object/isSealed|Object.isSealed Function]]
| Returns true if existing property attributes cannot be modified in an object and new properties cannot be added to the object.
|-
| [[javascript/Object/keys|Object.keys Function]]
| Returns the names of the enumerable properties and methods of an object.
|-
| [[javascript/Object/preventExtensions|Object.preventExtensions Function]]
| Prevents the addition of new properties to an object.
|-
| [[javascript/Object/seal|Object.seal Function]]
| Prevents the modification of attributes of existing properties, and prevents the addition of new properties.
|}
==Methods==
The following table lists methods of the '''Object Object'''.

{| class='wikitable'
|-
! Method
! Description
|-
| [[javascript/Object/hasOwnProperty|hasOwnProperty method]]
| Returns a Boolean value that indicates whether an object has a property with the specified name.
|-
| [[javascript/Object/isPrototypeOf|isPrototypeOf method]]
| Returns a Boolean value that indicates whether an object exists in another object's prototype hierarchy.
|-
| [[javascript/Object/propertyIsEnumerable|propertyIsEnumerable method]]
| Returns a Boolean value that indicates whether a specified property is part of an object and whether it is enumerable.
|-
| [[javascript/Object/toLocaleString|toLocaleString method]]
| Returns an object converted to a string based on the current locale.
|-
| [[javascript/Object/toString|toString method]]
| Returns a string representation of an object.
|-
| [[javascript/Object/valueOf|valueOf method]]
| Returns the primitive value of the specified object.
|}
{{See_Also_Section
|Manual_links=* [[javascript/objects{{!}}JavaScript Objects]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/kb6te8d3(v=vs.94).aspx
|HTML5Rocks_link=
}}