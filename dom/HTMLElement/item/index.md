{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=VARIANT
|Description='''Variant''' of type '''Integer''' or '''String''' that specifies the object or collection to retrieve. If this parameter is an integer, it is the zero-based index of the object. If this parameter is a string, all objects with matching [[html/attributes/name|'''name''']] or [[html/attributes/id|'''id''']] properties are retrieved, and a collection is returned if more than one match is made.
|Optional=No
}}{{Method Parameter
|Name=index
|Data type=VARIANT
|Description='''Variant''' of type '''Integer''' that specifies the zero-based index of the object to retrieve when a collection is returned.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example uses the '''item''' method to retrieve each object from the document. In this case, the method parameter is a number, so the objects are retrieved in the order they appear in the document.
|Code=&lt;script language{{=}}"JScript"&gt;
var coll {{=}} document.all;
if (coll!{{=}}null) {
    for (i{{=}}0; i&lt;coll.length; i++) 
        console.log(coll.item(i).tagName);
}
&lt;/script&gt;
}}{{Single Example
|Description=The next example uses the '''item''' method to retrieve a collection of all objects in the document that have "Sample" as an [[html/attributes/id|'''ID''']]. The example then uses '''item''' again to retrieve each object from the "Sample" collection.
|Code=&lt;script language{{=}}"JScript"&gt;
var coll {{=}} document.all.item("Sample");
If (coll !{{=}} null) {
    for (i{{=}}0; i&lt;coll.length; i++) {
        console.log(coll.item(i).tagName);
    }
}
&lt;/script&gt;
}}{{Single Example
|Description=The last example is similar to the previous example, but uses the optional ''index'' parameter of '''item''' to retrieve individual objects.
|Code=&lt;script language{{=}}"JScript"&gt;
var coll {{=}} document.all.item("Sample")
if (coll!{{=}}null) {
    for (i{{=}}0; i&lt;coll.length; i++)
        console.log(document.all.item("Sample",i).tagName);
}
&lt;/script&gt;
}}{{Single Example
|Description=This example uses the '''item''' method to get a collection of the children of the document body.
|Code=&lt;script language{{=}}"JScript"&gt;
var oItem {{=}} document.body.children;
if (oItem!{{=}}null) {
    for (i{{=}}0; i&lt;oItem.length; i++) 
        console.log(oItem.item(i).tagName);
}
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''item''' method cannot retrieve '''input type{{=}}image''' elements from a '''form'''. To access all elements contained in a form, use the [[dom/Element/children|'''children''']] collection.
Windows Internet Explorer 8 and later. In IE8 Standards mode, the ''index'' parameter is not used.  For more information, see Defining Document Compatibility.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
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