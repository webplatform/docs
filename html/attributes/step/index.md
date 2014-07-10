{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specify the increment for <code>input</code> with types <code>number</code>, <code>time</code>, or <code>range</code>}}
{{Markup_Attribute
|Applies_to=[[html/elements/input|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=When <code>input type="range"</code>, <code>input type="date"</code>, or <code>input type="number"</code> is specified, the default increment from <code>min</code> to <code>max</code> is 1.  Override this default with a value in <code>step</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A slider with a  range from 1-12 that increments by 3.
|Code=<input type="range" min="1" max="24" step="3" />
}}{{Single Example
|Language=HTML
|Description=A form input for a number between 0 and 15 that increments by 3.
|Code=<input type="number" min="0" max="15" step="3" />​​​​​​​​​​​​​​​​​​​​
|LiveURL=http://jsfiddle.net/mejarc/YkGZY/2/
}}{{Single Example
|Language=HTML
|Description=Restricting time input to half-hours.
|Code=<input type="time"  step="1800" />
|LiveURL=http://jsfiddle.net/mejarc/YkGZY/6/
}}
}}
{{Notes_Section
|Usage=* when used for <code>input type="time"</code>, value must be in seconds
|Notes====Remarks===
The following example shows the use of the [[html/attributes/min|'''min''']], [[html/attributes/max (HTMLInputElement)|'''max''']], and '''step''' attributes.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.7.3.11
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=16
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML
|External_links=* http://dev.opera.com/articles/view/new-form-features-in-html5/#input-datetime
* http://www.quirksmode.org/html5/inputs.html
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[html/elements/input/type/number|input type{{=}}number]]</code>
*<code>[[html/elements/input/type/range|input type{{=}}range]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN, DevOpera
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/Input#Attributes
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}