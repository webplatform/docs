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
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''scrollHeight''' property to retrieve the height of the viewable content.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnCheckScroll(){
    var iNewHeight {{=}} oDiv.scrollHeight;
    alert("The value of the scrollHeight property is: " 
        + iNewHeight + "px"); 
}
&lt;/script&gt;
...
&lt;div id{{=}}"oDiv" style{{=}}"overflow: scroll; height{{=}} 100px; width{{=}} 250px; text-align: left"&gt;
	... 
&lt;/div&gt;
&lt;button onclick{{=}}"fnCheckScroll()"&gt;Check scrollHeight&lt;/button&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollHeight.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The height is the distance between the top and bottom edges of the object's content.
This property is read-only on HTML documents, and read-write on fixed regions.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
|Import_Notes====Syntax===
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