{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN import
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
|Examples={{Single Example
|Description=This example uses the '''offsetLeft''' property to determine whether an object is in the user's view.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function isinView(element) {
    var oparent {{=}} element.offsetParent; 
    var osleft {{=}} oID_1.offsetLeft;
    var cleft {{=}} oparent.clientWidth;
    if (osleft &gt; cleft) {
        alert("Expand the window to see the paragraph!");
    }
}
&lt;/script&gt;
...
&lt;button onclick{{=}}"isinView(this)"&gt;Click here&lt;/button&gt;
...
&lt;div id{{=}}"oID_1" style{{=}}"position: absolute; top:200px; left:1200px;"&gt;
...
&lt;/div&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetLeft.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
You can determine the location, width, and height of an object by using a combination of the '''offsetLeft''', [[dom/HTMLElement/offsetTop|'''offsetTop''']], [[dom/HTMLElement/offsetHeight|'''offsetHeight''']], and [[dom/HTMLElement/offsetWidth|'''offsetWidth''']] properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
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