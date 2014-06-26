{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, specs, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=Range
|Data type=any
|Description=[[dom/TextRange|'''TextRange''']] object that might be contained.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Boolean

'''Boolean''' that returns one of the following possible values.

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}Range is contained within or is equal to the TextRange object on which the method is called.
{{!}}-
{{!}}false
{{!}}Range is not contained within the TextRange object on which the method is called.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''inRange''' method to show that two [[dom/TextRange|'''TextRange''']] objects are equal.
|Code=&lt;html&gt;
&lt;script type{{=}}"text/javascript"&gt;
window.onload{{=}}fnCheck;
function fnCheck(){
    var oRng1 {{=}} document.body.createTextRange();
    var oRng2 {{=}} oRng1.duplicate();
    var bInside {{=}} oRng1.inRange(oRng2); // returns true;
}
&lt;/script&gt;
   
&lt;body&gt;
    &lt;div id{{=}}div1&gt;
    Content for division 1.
    &lt;/div&gt;
    &lt;div id{{=}}div2&gt;
    Content for division 2.
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Description=The following example shows how to use the '''inRange''' method to show that two contained ranges are not equal.
|Code=&lt;html&gt;
&lt;script type{{=}}"text/javascript"&gt;
window.onload{{=}}fnCheck;
function fnCheck(){
  	 var oRng1 {{=}} document.body.createTextRange(); // create a text range
	   var oRng2 {{=}} oRng1.duplicate();		// create a duplicate range base on oRng1

    oRng1.moveToElementText(document.getElementById("div1"));
    oRng2.moveToElementText(document.getElementById("div2"));
    var bInside {{=}} oRng1.inRange(oRng2); // returns false;
}
&lt;/script&gt;
   
&lt;body&gt;
    &lt;div id{{=}}"div1"&gt;
    Content for division 1.
    &lt;/div&gt;
    &lt;div ID{{=}}"div2"&gt;
    Content for division 2.
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Description=The following example shows how to use the '''inRange''' method to show that a text range exists within another text range.
|Code=&lt;html&gt;
&lt;script type{{=}}"text/javascript"&gt;
window.onload{{=}}fnCheck;
function fnCheck(){
    var oRng1 {{=}} document.body.createTextRange();
    var oRng3 {{=}} oRng1.duplicate();
    oRng3.findText('division 1');
    var bInside {{=}} oRng1.inRange(oRng3); // returns true; 
}
&lt;/script&gt;
&lt;body&gt;
    &lt;div id{{=}}"div1"&gt;
    Content for division 1.
    &lt;/div&gt;
    &lt;div ID{{=}}"div2"&gt;
    Content for division 2.
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/inrange.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This feature might not be available on platforms other than Microsoft Win32.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/TextRange|TextRange]]</code>
*<code>[[dom/Element/isEqual|isEqual]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}