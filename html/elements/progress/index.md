{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The HTML <code>&lt;progress&gt;</code> element represents the completion progress of a task.}}
{{Markup_Element
|DOM_interface=dom/HTMLProgressElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">[[html/concepts/phrasingContent|Phrasing content]], but may not contain any <code>&lt;progress&gt;</code> elements itself.</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>Any element that can contain [[html/concepts/phrasingContent|phrasing content]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A <code>&lt;progress&gt;</code> element must have both a start tag and an end tag.</td>
</tr>
</table>

<p>The HTML <code>&lt;progress&gt;</code> element is a number in the range zero to a maximum, giving the fraction of work that has so far been completed. The progress element is not the correct element to use for something that is just a gauge, as opposed to task progress. For instance, indicating disk space usage using progress would be inappropriate. Instead, the [[meter|meter]] element is available for such use cases.</p>

===Attributes===
This element supports the HTML5 [[html/global_attributes|global attributes]].
<ul>
<li id="attribute-value"><b>value</b>
<ul>
<li>How much of the task has been completed. If [[#attribute-max|max]] is not set, this should be a value between 0 and 1, if [[#attribute-max|max]] is set, this should be a value between 0 and [[#attribute-max|max]].</li>
</ul>
</li>
<li id="attribute-max"><b>max</b>
<ul>
<li>How much work the task requires in total. This is optional, if it's not set then [[#attribute-value|value]] is a percentage.</li>
</ul>
</li>
</ul>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Example of a basic progress element
|Code=<progress value="165" max="200">165 of 200 finished</progress>
|LiveURL=http://code.webplatform.org/gist/6365491
}}{{Single Example
|Language=HTML
|Description=Example of progress without a maximum
|Code=<progress value="0.72">72% done</progress>
|LiveURL=http://code.webplatform.org/gist/6365520
}}{{Single Example
|Language=CSS
|Description=Styling options for the progress bar
|Code=progress {
  -webkit-appearance: none;
}

progress::-webkit-progress-bar {
  background-color: lightgray;
}

progress::-webkit-progress-value {
  background-color: lightgreen;
}
|LiveURL=http://code.webplatform.org/gist/6365564
}}{{Single Example
|Language=HTML
|Description=Progress element without value
|Code=<progress></progress>
|LiveURL=http://code.webplatform.org/gist/6365909
}}
}}
{{Notes_Section
|Usage=When the [[#attribute-value|value attribute]] is omitted, the <code>&lt;progress&gt;</code> element becomes indeterminate, that is, it shows activity but not how much progress has actually been made.
|Notes====Remarks===
When the '''value''' attribute is omitted, the '''progress''' element becomes indeterminate, that is, it shows activity but not how much progress has actually been made. If the '''value''' attribute is used without a maximum value, the range is from 0 to 1. To change the appearance from a ring to a bar, use the [[css/properties/animation-name|'''animation-name''']] property  to style   the '''progress''' element's '''ms-fill''' pseudo-element. The progress element can be styled using CSS.
|Import_Notes====Syntax===

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
|Specifications={{Related Specification
|Name=HTML5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/forms.html#the-progress-element
|Status=Editor's Draft
}}{{Related Specification
|Name=WhatWG HTML Living Standard
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/the-button-element.html#the-progress-element
|Status=Living Standard
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=6.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=6.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=* [[html/elements/meter|&lt;meter%gt;]]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}