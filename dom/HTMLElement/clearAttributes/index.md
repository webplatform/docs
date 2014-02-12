{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''clearAttributes''' method to remove user-defined attributes from an element.
|Code=&lt;SCRIPT&gt;
function fnClear(){
   oSource.children[0].clearAttributes();
}
&lt;/SCRIPT&gt;
&lt;SPAN ID{{=}}oSource&gt;
&lt;DIV
   ID{{=}}"oDiv"
   ATTRIBUTE1{{=}}"true"
   ATTRIBUTE2{{=}}"true"
   onclick{{=}}"alert('click');"
   onmouseover{{=}}"this.style.color{{=}}'#0000FF';"
   onmouseout{{=}}"this.style.color{{=}}'#000000';"
&gt;
This is a sample &lt;b&gt;DIV&lt;/b&gt; element.
&lt;/DIV&gt;
&lt;/SPAN&gt;
&lt;INPUT
   TYPE{{=}}"button"
   VALUE{{=}}"Clear Attributes"
   onclick{{=}}"fnClear()"
&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clearAttributes.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''clearAttributes''' method clears only persistent HTML attributes. The ID attribute, styles, and script-only properties are not affected.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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