{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script creates a new image and appends it to the '''body''' object..
|LiveURL=
|Code=
&lt;script type{{=}}"text/javascript"&gt;
var img {{=}} new Image(50, 50);
img.src {{=}} "image.png";
document.body.appendChild( img );
&lt;/script&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use this object to instantiate new '''img''' elements before adding them to the document. You can specify up to two optional arguments:
{| class="wikitable"
|-
|nWidth
|Optional. '''Integer''' that specifies the '''img''' width.
|-
|nHeight
|Optional. '''Integer''' that specifies the '''img''' height.
|}
 
String values are coerced into their numeric equivalents, if possible.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''Image''' object has these types of members:
*[#methods Methods]


====Methods====
The '''Image''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/create (image)|'''create''']]
|Creates a new '''img''' element of the specified width and height. This method cannot be called directly. See '''Image''' object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/attributes/src (input, img)|src]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}