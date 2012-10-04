{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''input type{{=}}tel''' element to create an empty telephone control. The telephone control does not validate or enforce a specific format, so the '''pattern''' attribute is used to require the correct format. The '''title''' attribute gives users a guide when they hover over the field.
|LiveURL=
|Code=
&lt;input type{{=}}"tel" name{{=}}"teleNumber" pattern{{=}}"\(\d\d\d\) ?\d\d\d-\d\d\d\d" title{{=}}"(###) ###-####"
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.7.1.3


===Members===
The '''input type{{=}}tel''' object has these types of members:
*[#properties Properties]


====Properties====
The '''input type{{=}}tel''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/type|'''type''']]
|Retrieves or initially sets  the type of '''input''' control represented by the object.
|-
|[[html/attributes/value (input elements)|'''value''']]
|Sets or retrieves the displayed value for the control object.  This value is returned to the server when the control object is submitted.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>input</code>
*<code>[[html/attributes/pattern|pattern]]</code>
*<code>[[html/attributes/placeholder|placeholder]]</code>
|Topic_clusters=html, form
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}