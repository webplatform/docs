{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
|High-level issues=Data Not Semantic, Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The HTML <code>&lt;meter&gt;</code> element represents a value within a specified range.  This value can be any real number.}}
{{Markup_Element
|DOM_interface=dom/HTMLMeterElement
|Content=<table class{{=}}"wikitable">
<tr>
<th style{{=}}"vertical-align: top" id="permitted-contents">Permitted&#160;contents</th>
<td style{{=}}"vertical-align: top; padding-top: 10px">[[html/concepts/phrasingContent|Phrasing content]], but may not contain any <code>&lt;meter&gt;</code> elements itself.</td>
</tr>
<tr>
<th id="permitted-parents">Permitted&#160;parents</th>
<td>Any element that can contain [[html/concepts/phrasingContent|phrasing content]].</td>
</tr>
<tr>
<th id="tag-omission">Tag&#160;omission</th>
<td>A <code>&lt;meter&gt;</code> element must have both a start tag and an end tag.</td>
</tr>
</table>


The meter element defines a value between a minimum or maximum.  This can be used for fundraisers, test results, or a number of other things.  It should not be used as a progress bar.  For that, use the [[html/elements/progress|progress element]].  You should give a description of the meter within the tags, such as <code>&lt;meter min&#61;&quot;0&quot; max&#61;&quot;10&quot; value&#61;&quot;5&quot;&gt;5 out of 10 squares occupied&lt;&#47;meter&gt;</code>.  This meter can also have various attributes on it, such as the optimum, high and low values.

The content of the '''meter''' element should represent the set min/max/value attributes in human readable form. This will be picked up by assistive technologies as well as act as a fallback for browsers not supporting the element. 

===Attributes===

This element supports the HTML5 [[html/global_attributes|global attributes]].

<dl>
    <dt id="attribute-value">[[html/attributes/value|value]]</dt>
    <dd>The current value of the meter.  If there is no value specified, or if the value is incorrectly formatted, it defaults to 0.  This value must be between the [[#attribute-min|min]] and [[#attribute-max|max]] values of the element.  If not, it will default to the closest available value within the ranges.</dd>

    <dt id="attribute-optimum">[[html/attributes/optimum|optimum]]</dt>
    <dd>The optimum, or goal value of the meter.  For example, on a test score, this would be 100.  Or, on a fundraiser, this may be a monetary value.  This must be below the [[#attribute-max|max]] value and above the [[#attribute-min|min]] value.</dd>

    <dt id="attribute-min">[[html/attributes/min|min]]</dt>
    <dd>The minimum value of the meter.  This must be less than the [[#attribute-max|max]] attribute value.  If this attribute is not present, it defaults to 0.</dd>

    <dt id="attribute-max">[[html/attributes/max|max]]</dt>
    <dd>The maximum value of the meter.  This must be greater than the [[#attribute-min|min]] attribute value. If this attribute is not present, it defaults to 1.</dd>

    <dt id="attribute-low">[[html/attributes/low|low]]</dt>
    <dd>The low value is what is considered a low range for the meter.  In the example of a fundraiser, it may be near the starting value.  This must be greater than the [[#attribute-min|min]] and less than the [[#attribute-max|max]] and [[#attribute-high|high]] values.  If unspecified, it defaults to 0.</dd>

    <dt id="attribute-high">[[html/attributes/high|high]]</dt>
    <dd>The high value is what is considered a high range for the meter.  In the example of a fundraiser, it may be near the goal value.  This must be less than the [[#attribute-max|max]] and greater than the [[#attribute-min|min]] and [[#attribute-low|low]] values.  If unspecified, it defaults to 1.</dd>
</dl>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A basic example of the meter element
|Code=<meter min="0" max="10" value="5">5 out of 10</meter>
|LiveURL=http://code.webplatform.org/gist/5281236
}}{{Single Example
|Language=HTML
|Description=An example of the meter element using all of its attributes
|Code=<meter min="0" max="1000" value="500" low="200" high="800" optimum="900">&#36;500 raised</meter>
|LiveURL=http://code.webplatform.org/gist/5281393
}}{{Single Example
|Language=CSS
|Description=Styling options for the meter bar
|Code=meter {
  -webkit-appearance: none;
}

meter::-webkit-meter-bar {
  border: 2px solid black;
}

meter::-webkit-meter-bar {
  background: lightblue;
}

meter::-webkit-meter-optimum-value {
  background: green;
}

meter::-webkit-meter-suboptimum-value {
  background: orange;
}

meter::-webkit-meter-even-less-good-value {
  background: red;
}
|LiveURL=http://jsbin.com/ometoTE/4/edit
}}
}}
{{Notes_Section
|Usage=The meter element is intended to have descriptive text inside of it, similar to the alt tag of the [http://docs.webplatform.org/wiki/html/elements/img image element].
The title attribute may be used to specify a unit.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/forms.html#the-meter-element
|Status=Editor's Draft
|Relevant_changes=
}}{{Related Specification
|Name=WHATWG
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/the-button-element.html#the-meter-element
|Status=Living Standard
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=* [[html/elements/progress|HTML5 progress element]]
|External_links=
|Manual_sections=
}}
{{Topics|DOM, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/meter
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=6.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
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
|Feature=Basic Support
|Android_supported=No
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
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
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