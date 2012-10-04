{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example in JScript (compatible with ECMA 262 language specification) shows how to display the URLs of the HTML documents contained in windows created by the '''iframe''' objects in the document.
|LiveURL=
|Code=
var frm {{=}} document.frames;
for (i{{=}}0; i &lt; frm.length; i++)
    alert(frm(i).location);
}}
{{Single_Example
|Description=This example in JScript shows how to display the name of each window defined by '''frame''' tags in the parent window of the current document.
|LiveURL=
|Code=
var frm {{=}} window.parent.frames;
for (i{{=}}0; i &lt; frm.length; i++) 
    alert(frm(i).name);
}}}}
{{Notes_Section
|Notes=
===Remarks===
If the HTML source document contains a '''body''' tag, the collection contains one window for each '''iframe''' object in the document. If the source document contains '''frameSet''' tags, the collection contains one window for each '''frame''' tag in the document. In both cases, the order is determined by the HTML source.
This collection contains only '''window''' objects and does not provide access to the corresponding '''frame''' and '''iframe''' objects. To access these objects, use the [[dom/properties/all|'''all''']] collection for the document containing the objects.
Although you can use names with the [[dom/methods/item|'''item''']] method on this collection, the method never returns a collection. Instead, it always returns the first window having the given name. To ensure that all windows are accessible, make sure that no two windows in a document have the same name.
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