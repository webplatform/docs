{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Returns the window itself, which is an array-like object, listing the direct sub-frames of the current window.}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=Yes
|Example_object_name=window
|Return_value_name=frames
|Javascript_data_type=DOM Node
|Return_value_description=Collection of HTMLWindow objects that are children of the window Node.
|Example_value_name=frames
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.frames frames]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms535873(v=vs.85).aspx window Object]
|HTML5Rocks_link=
}}