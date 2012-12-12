{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Progress is a number in the range zero to a maximum, giving the fraction of work that has so far been completed. The progress element is not the correct element to use for something that is just a gauge, as opposed to task progress. For instance, indicating disk space usage using progress would be inappropriate. Instead, the meter element is available for such use cases.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
When the '''value''' attribute is omitted, the '''progress''' element becomes indeterminate, that is, it shows activity but not how much progress has actually been made. If the '''value''' attribute is used without a maximum value, the range is from 0 to 1. To change the appearance from a ring to a bar, use the [[css/properties/animation-name|'''animation-name''']] property  to style   the '''progress''' element's '''ms-fill''' pseudo-element. The progress element can be styled using CSS.
'''Note'''  For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_htmlref\ie]:%20Progress element {{!}} Progress object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


===Members===
The '''Progress''' object has these types of members:
*[#properties Properties]


====Properties====
The '''Progress''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/form|'''form''']]
|Retrieves a reference to the form that the object is embedded in.
|-
|[[html/attributes/max(HTMLProgressElement)|'''max''']]
|Defines the maximum, or "done" value for a progress element.
|-
|[[css/selectors/-ms-progress-appearance|'''msProgressAppearance''']]
|This property is obsolete. Use [[css/properties/animation-name|'''animation-name''']] instead.
|-
|[[dom/properties/position|'''position''']]
|Returns the quotient of [[html/attributes/value (HTMLProgressElement)|'''value''']]/[[html/attributes/max(HTMLProgressElement)|'''max''']] when the '''value''' attribute is set (determinate progress bar), or -1 when the '''value''' attribute is missing (indeterminate progress bar).
|-
|[[html/attributes/value (HTMLProgressElement)|'''value''']]
|Sets or gets the current value of a progress element. The value must be a non-negative number between 0 and the [[html/attributes/max(HTMLProgressElement)|'''max''']] value.
|}
 
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
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}