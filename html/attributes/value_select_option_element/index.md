{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example sets the value for each '''option''' element to a supply stock number.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
&lt;script&gt;
function fnShowText(){
   /* Use the selectedIndex property of the SELECT control
   to retrieve the text from the options collection. */
   
   var sText {{=}} "Stock Number {{=}} " + oSel.options(oSel.selectedIndex).value;
   alert(sText);
}
&lt;/script&gt;
&lt;SELECT ID{{=}}"oSel" onchange {{=}} "fnShowText()"&gt;
&lt;OPTION VALUE{{=}}"STK#45"&gt;Item One - Basketball&lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}"STK#347"&gt;Item Two - Baseball&lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}"STK#67"&gt;Item Three - Hockey Puck&lt;/OPTION&gt;
&lt;/SELECT&gt;
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Individual control objects return a value to the server only 
if they have been selected by the user.
You may pass server-friendly data directly to the server without confusing the user.  
The user sees only the innerText displayed, and not the 
'''value'''.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.6.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>option</code>
*<code>select</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}