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
|Description=This example retrieves the '''checked''' property to fire an event.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/checked.htm
|Code=
&lt;head&gt;
    &lt;script&gt;
    function checkthis()
    {
        if (oCheckbox.checked {{=}}{{=}} true)
        {
            window.open("http://www.microsoft.com");
        }
    }
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;Check here if you wish to go to Microsoft:
    &lt;input id{{=}}"oCheckbox" type{{=}}"checkbox" onclick{{=}}"checkthis()"&gt;&lt;/p&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Check boxes that are not selected do not return their values when the '''form''' is submitted.
A user can select a radio button only if the button has a [[html/attributes/name|'''name''']]. To clear a selected radio button, a user must select another button in the set.
Windows Internet Explorer 8 and later. In IE8 Standards mode, parsing operations on the '''checked''' content attribute always affect both the '''checked''' content attribute and [[dom/properties/defaultChecked|'''defaultChecked''']] Document Object Model (DOM) attribute. For example, [[dom/methods/removeAttribute|'''removeAttribute('checked')''']] sets both '''checked''' and '''defaultChecked''' to false. Similarly, [[dom/methods/setAttribute|'''setAttribute('checked', 'checked')''']] sets both DOM attributes to true (as if the element was being re-parsed)  For more information on IE8 mode, see Defining Document Compatibility.
Internet Explorer 8 and later. In IE8 mode, the [[dom/properties/defaultChecked|'''defaultChecked''']] DOM attribute reflects the value of the '''checked''' content attribute.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}radio</code>
*<code>input</code>
*<code>Reference</code>
*<code>[[dom/properties/defaultChecked|defaultChecked]]</code>
*<code>Conceptual</code>
*<code>Introduction to Forms</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1]</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}