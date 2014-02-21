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
|Description=This example uses the '''offsetTop''' property to determine whether an object is in the user's view.
|Code=&lt;html&gt;

&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function isinView(oObject)
{
    var oParent {{=}} oObject.offsetParent; 
    var iOffsetTop {{=}} oObject.offsetTop;
    var iClientHeight {{=}} oParent.clientHeight;
    if (iOffsetTop &gt; iClientHeight) {
        alert("Special Text not in view. Expand Window to put Text in View.");
    }
    else{
         alert("Special Text in View!");
    }
}
&lt;/script&gt;
&lt;/head&gt;

&lt;body onload{{=}}"window.resizeTo(430,250)" onclick{{=}}"isinView(oID_1)" scroll{{=}}"NO"&gt;

&lt;div style{{=}}"position: absolute; left: 20px"&gt;
    Click anywhere in window to see if special text is in view.&lt;/div&gt;
&lt;div id{{=}}"oID_1" style{{=}}"position: absolute; 
    left: 50px; 
    top: 300px; 
    width: 280px; 
    color: silver; 
    font-size: large; 
    font-weight: bold; 
    background-color: aqua; 
    font-family: Arial"&gt;
    Here&amp;#39;s some special text &lt;/div&gt;

&lt;/body&gt;

&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetTop.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
You can determine the location, width, and height of an object by using a combination of the [[dom/HTMLElement/offsetLeft|'''offsetLeft''']], '''offsetTop''', [[dom/HTMLElement/offsetHeight|'''offsetHeight''']], and [[dom/HTMLElement/offsetWidth|'''offsetWidth''']] properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent.
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