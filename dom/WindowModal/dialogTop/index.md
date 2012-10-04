{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example creates a dialog window using the '''dialogTop''' property to set the position relative to the top of the screen. Do not break the script code into two lines as in the fourth line of the example. This was done for readability only.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogTop.htm
|Code=
&lt;SCRIPT&gt;
function someMessage()
{
    event.srcElement.blur();
    window.showModalDialog("message.htm", "",
        "dialogWidth:5cm; dialogHeight:10cm; 
        dialogTop:0cm; dialogLeft:0cm")
}
&lt;/SCRIPT&gt; 
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;SELECT onchange{{=}}"someMessage()"&gt;
    &lt;OPTION&gt;Item 1&lt;/OPTION&gt;
    &lt;OPTION&gt;Item 2&lt;/OPTION&gt;
    &lt;OPTION&gt;Item 3&lt;/OPTION&gt;
&lt;/SELECT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''dialogTop''' property applies only to windows that are created by using the [[dom/methods/showModalDialog|'''showModalDialog''']] method and the [[dom/methods/showModelessDialog|'''showModelessDialog''']] method.
When a script calls the [[dom/methods/showModalDialog|'''showModalDialog''']] method, it suspends execution until the modal dialog box is closed.  As a result, the script cannot use the '''dialogTop''' property to change the appearance of the modal dialog box. To control the appearance of the modal dialog box, use script in the file loaded by the '''sURL''' parameter or use the value of the '''sFeatures''' parameter to specify the desired settings.
The default unit of measure for <code>dialogTop</code> in Microsoft Internet Explorer 4.0 is the em; in Microsoft Internet Explorer 5 it is the pixel. The value can be an integer or floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>), or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For consistent results, specify the <code>dialogTop</code> in pixels when you design modal dialog boxes.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}