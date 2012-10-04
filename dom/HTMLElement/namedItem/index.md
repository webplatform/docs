{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=name|Data type=BSTR|Description=A '''String''' that specifies the [[html/attributes/name|'''name''']] or [[html/attributes/id|'''id''']] property of the object to retrieve.  A collection is returned if more than one match is made.|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''namedItem''' method to retrieve a '''div''' and change its [[dom/properties/innerText|'''innerText''']] property.
|LiveURL=
|Code=
&lt;div id{{=}}"oDIV1"&gt;This text will not change.&lt;/div&gt;
&lt;div id{{=}}"oDIV2"&gt;This text will change.&lt;/div&gt;
&lt;button onclick{{=}}"document.all.namedItem('oDIV2').innerHTML{{=}}'Changed!';"&gt;
   Change Option
&lt;/button&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 and later. In IE8 Standards mode, the '''namedItem''' method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched Defining Document Compatibility.
The '''namedItem''' method was introduced in Microsoft Internet Explorer 6.
The '''namedItem''' method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched '''element'''.
This method first searches for an object with a matching [[html/attributes/id|'''id''']] attribute. If a match is not found, the method searches for an object with a matching [[html/attributes/name|'''name''']] attribute, but only on those elements that are allowed a name attribute.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/all|all]]</code>
*<code>[[dom/properties/anchors|anchors]]</code>
*<code>[[dom/properties/applet|applets]]</code>
*<code>[[dom/properties/boundElements|boundElements]]</code>
*<code>[[dom/properties/cellSpacing|cells]]</code>
*<code>[[dom/properties/embeds|embeds]]</code>
*<code>filters</code>
*<code>[[dom/properties/forms|forms]]</code>
*<code>[[dom/properties/frames|frames]]</code>
*<code>[[dom/properties/image|images]]</code>
*<code>[[dom/properties/links|links]]</code>
*<code>mimeTypes</code>
*<code>[[dom/properties/rows (table)|rows]]</code>
*<code>[[dom/properties/scripts|scripts]]</code>
*<code>[[dom/properties/tBodies|tBodies]]</code>
*<code>[[dom/traversal/properties/TextRange|TextRange]]</code>
*<code>[[dom/TextRectangle|TextRectangle]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}