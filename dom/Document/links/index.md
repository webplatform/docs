{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to display the [[html/attributes/href|'''href''']] of the third link (Microsoft.com) defined in the document.
|LiveURL=
|Code=
&lt;a href{{=}}"http://yahoo.com"&gt;Yahoo.com&lt;/a&gt;
&lt;a href{{=}}"http://msn.com"&gt;MSN.com&lt;/a&gt;
&lt;a href{{=}}"http://microsoft.com"&gt;Microsoft.com&lt;/a&gt;
&lt;script&gt;
alert(document.links[2].href);
&lt;/script&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
For [[html/elements/a|'''a''']] objects to appear in the collection, they must have an [[html/attributes/href|'''href''']] attribute.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}