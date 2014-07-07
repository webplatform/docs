{{Page Title}}
{{Flags
|State=In Progress
|Editorial notes=needs summary, clean-up of MSDN import
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to display the text and values of all '''option''' objects in the first '''select''' object in the document.
|LiveURL=
|Code=
var coll {{=}} document.all.tags("SELECT");
if (coll.length&gt;0) {
    for (i{{=}}0; i&lt; coll(0).options.length; i++)
        alert("Element " + i + " is " + coll(0).options(i).text +
		    " and has the value " + coll(0).options(i).value);
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
To delete an '''option''' object from a '''select''' object, assign the '''option''' object a null value. This compresses the array.
If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position.
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