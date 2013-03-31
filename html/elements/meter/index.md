{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The HTML <code>&lt;meter&gt;</code> element represents a value within a specified range.  This value can be a fraction, percentage, or any other real number.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=The meter element defines a value between a minimum or maximum.
<b>Attributes:</b>
<br>
<small>This element supports the HTML5 [http://docs.webplatform.org/wiki/html/global_attributes global attributes]</small>
<ul>
<li id="attribute-value"><b>value</b>
<ul>
<li>The current value of the meter.  If there is no value specified, or if the value is incorrectly formatted, it defaults to 0.  This value must be between the [[#attribute-min|min]] and [[#attribute-max|max]] values of the element.  If not, it will default to the closest available value within the ranges.
</li>
</ul>
</li>
<li id="attribute-optimum"><b>optimum</b>
<ul>
<li>The optimum, or goal value of the meter.  For example, on a test score, this would be 100.  Or, on a fundraiser, this may be a monetary value.  This must be below the [[#attribute-max|max]] value and above the [[#attribute-min|min]] value.
</li>
</ul>
</li>
<li id="attribute-form"><b>form</b>
<ul>
<li>This attribute associates the meter with a form.
</li>
</ul>
</li>
<li id="attribute-min"><b>min</b>
<ul>
<li>The minimum value of the meter.  This must be less than the [[#attribute-max|max]] attribute value.  If this attribute is not present, it defaults to 0.
</li>
</ul>
</li>
<li id="attribute-max"><b>max</b>
<ul>
<li>The maximum value of the meter.  This must be greater than the [[#attribute-min|min]] attribute value.  If this attribute is not present, it defaults to 1.
</li>
</ul>
</li>
<li id="attribute-low"><b>low</b>
<ul>
<li>The low value is what is considered a low range for the meter.  In the example of a fundraiser, it may be near the starting value.  This must be greater than the [[#attribute-min|min]] and less than the [[#attribute-max|max]] and [[#attribute-high|high]] values.  If unspecified, it defaults to 0.
</li>
</ul>
</li>
<li id="attribute-high"><b>high</b>
<ul>
<li>The high value is what is considered a high range for the meter.  In the example of a fundraiser, it may be near the goal value.  This must be less than the [[#attribute-max|max]] and greater than the [[#attribute-min|min]] and [[#attribute-low|low]] values.  If unspecified, it defaults to 1.
</li>
</ul>
</li>
</ul>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A basic example of the meter element
|Code=<meter min="0" max="10" value="5">5 out of 10</meter>
|LiveURL=http://code.webplatform.org/gist/5281236
}}
}}
{{Notes_Section}}
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
{{Topics|DOM, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}