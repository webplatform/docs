{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, examples, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''window'''.'''length''' property returns the number of frames contained in a window.
The '''comment'''.'''length''' property returns the number of characters in the object.
Although this property is read-only for most objects, it is read/write for the [[dom/HTMLMapElement/areas|'''areas''']] collection (image maps), the [[dom/HTMLElement/options|'''options''']] collection (select boxes), and the '''select''' object. In all other cases, this property has read-only permission, which means you can retrieve, but cannot change, its current value.
The '''length''' property does not count '''input type{{=}}image''' elements. To access all elements contained in a form use the [[dom/Element/children|'''children''']] property of the '''HTMLElement'''.
This property is read-write on the areas collection for image maps and the options collection for select boxes. This allows a developer to shrink the collection.
For Windows CE only, this collection will always be empty.
As of Windows Internet Explorer 8, this property is read-only in the [[dom/HTMLMapElement/areas|'''areas''']] collection.
In Microsoft Internet Explorer 6 and later, this property applies to the '''comment''' object.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
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