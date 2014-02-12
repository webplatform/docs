{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Covers what the click action is and what happens when it is performed.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example demonstrates how simulating a click using the '''click''' does not, by default, bring the element into focus.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;onfocus Sample&lt;/title&gt;
&lt;link rel{{=}}"stylesheet" type{{=}}"text/css" href{{=}}"samplesSDKIE4.css" /&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;p&gt;DEMO: USING CLICK METHOD DOES NOT SET FOCUS&lt;p&gt;
    &lt;ul&gt;
      &lt;li&gt;Both these buttons apply the click method to the check box. &lt;/li&gt;
      &lt;li&gt;An alert has been set to fire when the check box is put into focus.&lt;/li&gt; 
    &lt;/ul&gt;
  &lt;/p&gt;
  &lt;input type{{=}}"checkbox" id{{=}}"chk1"/&gt;	
    &lt;br&gt;
    &lt;button onclick{{=}}"simclick1()"&gt;This button &lt;strong&gt;applies the focus method&lt;/strong&gt; to 
      check box&lt;/button&gt;
    &lt;br&gt;
    &lt;button onclick{{=}}"simclick2()"&gt;This button &lt;strong&gt;does not apply the focus method&lt;/strong&gt; to check box&lt;/button&gt;
    &lt;br&gt;

  &lt;script&gt;
	// When chk1 gets focus, pop an alert
	document.getElementById("chk1").addEventListener("focus", function(){alert("check box is in focus!");}, false);
    function simclick1() {
      chk1.focus(); //focus is explicitly set
      chk1.click(); 
    }
    function simclick2() {
      chk1.click();
    }
  &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/click.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  Simulating a click using the '''click''' does not bring the element being clicked into focus. (See example below).
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