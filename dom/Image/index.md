{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|An image element within a web document, normally defined by an <img> tag.}}
{{API_Object
|Subclass_of=dom/DOMCollection
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script creates a new image and appends it to the '''body''' object..
|Code=var img {{=}} new Image(50, 50);
img.src {{=}} "image.png";
document.body.appendChild( img );
}}
}}
{{Notes_Section
|Notes=Use this object to instantiate new '''img''' elements before adding them to the document. You can specify up to two optional arguments:
{| class="wikitable"
|-
|nWidth
|Optional. '''Integer''' that specifies the '''img''' width.
|-
|nHeight
|Optional. '''Integer''' that specifies the '''img''' height.
|}
 
String values are coerced into their numeric equivalents, if possible.
|Import_Notes====Additional Members (MSDN)===
The '''Image''' object has these types of members:
[[#Additional_Methods|Additional Methods]]


====Additional Methods====
The '''Image''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[dom/methods/create (image)|'''create''']]
{{!}}Creates a new '''img''' element of the specified width and height. This method cannot be called directly. See '''Image''' object.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}