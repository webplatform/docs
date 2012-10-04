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
|Description=This example uses the '''EVENT''' attribute and the '''event''' property to handle the [[dom/events/click|'''onclick''']] event.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/event.htm
|Code=
&lt;SCRIPT ID{{=}}oButtonScript FOR{{=}}"oButton" EVENT{{=}}"onclick()"&gt;
    var sMessage1 {{=}} "Flip"
    var sMessage2 {{=}} "Flop"
    if (oButton.innerText {{=}}{{=}} sMessage1) {
        oButton.innerText {{=}} sMessage2;
        }
    else {
    if (oButton.innerText {{=}}{{=}} sMessage2) {
        oButton.innerText {{=}} sMessage1;
        }
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
:
&lt;BUTTON ID{{=}}"oButton" onmouseout{{=}}"console.log(oButtonScript.event)"&gt;Flip&lt;/BUTTON&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>script</code>
*<code>event</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}