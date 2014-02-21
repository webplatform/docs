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
|Description=This example adjusts the size of a clock's readout to fit the current width and height of the document body.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;A Simple Clock&lt;/TITLE&gt;
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
function startClock()
{
    window.setInterval("Clock_Tick()", 1000);
    Clock_Tick();
}

var iRatio {{=}} 4;
function Clock_Tick()
{
    var dToday {{=}} Date();
    var sTime {{=}} dToday.substring(11,19);
    var iDocHeight {{=}} document.body.offsetHeight;
    var iDocWidth {{=}} document.body.offsetWidth;

    if ((iDocHeight*iRatio)&gt;iDocWidth)
        iDocHeight {{=}} iDocWidth / iRatio;
    document.all.MyTime.innerText {{=}} sTime;
    document.all.MyTime.style.fontSize {{=}} iDocHeight;
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"startClock()"&gt;
&lt;P ID{{=}}"MyTime"&gt;&amp;nbsp;&lt;/P&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}{{Single Example
|Description=This example uses the '''offsetHeight''' property and the [[dom/HTMLElement/clientHeight|'''clientHeight''']] property to show different ways of measuring the object size.
|Code=&lt;DIV ID{{=}}oDiv STYLE{{=}}"overflow:scroll; width:200; height:100"&gt; . . . &lt;/DIV&gt;
&lt;BUTTON onclick{{=}}"alert(oDiv.clientHeight)"&gt;client height&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"alert(oDiv.offsetHeight)"&gt;offset height&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/offsetHeight.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
You can determine the location, width, and height of an object by using a combination of the [[dom/HTMLElement/offsetLeft|'''offsetLeft''']], [[dom/HTMLElement/offsetTop|'''offsetTop''']], '''offsetHeight''', and [[dom/HTMLElement/offsetWidth|'''offsetWidth''']] properties. These numeric properties specify the physical coordinates and dimensions of the object relative to the object's offset parent.
For more information about how to access the dimension and location of elements on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
To comply with the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203774 Cascading Style Sheets, Level 1 (CSS1)] box model, Microsoft Internet Explorer 6 and later calculate the height of objects differently when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration in your document to switch on standards-compliant mode.  This difference may affect the value of the '''offsetHeight''' property. When standards-compliant mode is switched on, the [[css/properties/height|'''height''']] property specifies the distance between the top and bottom edges of the bounding box that surrounds the object's content. When standards-compliant mode is not switched on, and with earlier versions of Windows Internet Explorer, the '''height''' property also includes the [[css/properties/border|'''border''']] and [[css/properties/padding|'''padding''']] belts that surround the object's bounding box. For more information, see CSS Enhancements in Internet Explorer 6.
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