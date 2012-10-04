{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLFormElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example demonstrates how to use the '''reset''' method for a '''form''' object. When the button is pressed, the '''form''' is reset, resulting in the [[dom/events/reset|'''onreset''']] event call on the '''form''' object. The '''onreset''' event calls an event handler which in turn adds the text <code>Resetting form.</code> to the text area below.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/reset.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function doReset(){
    oTextArea1.value +{{=}} "Resetting form.  ";
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;DIV id{{=}}"oDiv1" 
    style{{=}}"border:1px solid black; background:#EEEEEE; padding:10px;"&gt;
    &lt;B&gt;Form&lt;/B&gt;
    &lt;FORM name{{=}}"form1" onreset{{=}}"doReset();"&gt;
        &lt;b&gt;Enter some text:&lt;/b&gt; &lt;INPUT type{{=}}"text" name{{=}}"oText1" value{{=}}""&gt;&lt;BR&gt;&lt;BR&gt;
        &lt;BUTTON onclick{{=}}"form.reset();"&gt;form.reset()&lt;/BUTTON&gt;
    &lt;/FORM&gt;
&lt;/DIV&gt;
&lt;B&gt;Text area&lt;/B&gt;&lt;BR&gt;
&lt;TEXTAREA id{{=}}"oTextArea1" value{{=}}"" rows{{=}}"5" cols{{=}}"75"&gt;&lt;/TEXTAREA&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''reset''' method raises the '''onreset''' event on the form.
The '''reset''' method fires the [[dom/events/reset|'''onreset''']] event on the form.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>form</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}