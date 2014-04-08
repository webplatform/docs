{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets or sets the X coordinate position of a dialog window.}}
{{API_Object_Property
|Property_applies_to=dom/WindowModal
|Read_only=No
|Example_object_name=window
|Return_value_name=xCoordinate
|Javascript_data_type=String
|Return_value_description=The X coordinate position and a unit of measure.
|Example_value_name=newYCoordinate
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example creates a dialog window that uses the '''dialogLeft''' property to set the position relative to the left side of the screen.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function someMessage(e) {
    e.target.blur();
    window.showModalDialog("message.htm", "", 
        "dialogWidth:5cm; dialogHeight:10cm; dialogTop:0cm; dialogLeft:0cm")
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;select onchange{{=}}"someMessage(event)"&gt;
   &lt;option&gt;Item 1&lt;/option&gt;
   &lt;option&gt;Item 2&lt;/option&gt;
   &lt;option&gt;Item 3&lt;/option&gt;
  &lt;/select&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/dialogLeft.htm
}}
}}
{{Notes_Section
|Notes=*This property applies only to windows that are created by using the [[dom/HTMLElement/showModalDialog|'''showModalDialog''']] method and the [[dom/HTMLElement/showModelessDialog|'''showModelessDialog''']] method.
*When a script calls the '''showModalDialog''' method, it suspends execution until the modal dialog box is closed.  As a result, the script cannot use the '''dialogLeft''' property to change the appearance of the modal dialog box. To control the appearance of the modal dialog box, use script in the file loaded by the '''sURL''' parameter or use the value of the '''sFeatures''' parameter to specify the desired settings.
*The default unit of measure is <code>px</code>.
*The value can be an integer or floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>), or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For consistent results, specify the <code>dialogLeft</code> in pixels when you design modal dialog boxes.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=4
|Note=The default unit of measure is <code>em</code>.
}}
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