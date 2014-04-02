{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example in JScript (compatible with ECMA 262 language specification) shows how to display the URLs of the HTML documents contained in windows created by the '''iframe''' objects in the document.
|Code=var frm {{=}} document.frames;
for (i{{=}}0; i &lt; frm.length; i++)
    alert(frm(i).location);
}}{{Single Example
|Description=This example in JScript shows how to display the name of each window defined by '''frame''' tags in the parent window of the current document.
|Code=var frm {{=}} window.parent.frames;
for (i{{=}}0; i &lt; frm.length; i++) 
    alert(frm(i).name);
}}
}}
{{Notes_Section
|Notes====Remarks===
If the HTML source document contains a '''body''' tag, the collection contains one window for each '''iframe''' object in the document. If the source document contains '''frameSet''' tags, the collection contains one window for each '''frame''' tag in the document. In both cases, the order is determined by the HTML source.
This collection contains only '''window''' objects and does not provide access to the corresponding '''frame''' and '''iframe''' objects.
Although you can use names with the [[dom/Element/item|'''item''']] method on this collection, the method never returns a collection. Instead, it always returns the first window having the given name. To ensure that all windows are accessible, make sure that no two windows in a document have the same name.
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