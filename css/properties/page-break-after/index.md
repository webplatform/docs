{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=always |Description=Always insert a page break after the object.}}
{{CSS_Property_Value|Data Type=auto |Description=Default. Neither force nor forbid a page break after the object.}}
{{CSS_Property_Value|Data Type=avoid |Description=Internet Explorer 8. Forbid a page break after the object, if possible.}}
{{CSS_Property_Value|Data Type=empty string |Description=Behaves the same as '''auto'''.}}
{{CSS_Property_Value|Data Type=inherit |Description=Internet Explorer 8. Inherit the value of the same property for the object's parent.}}
{{CSS_Property_Value|Data Type=left |Description=Currently behaves the same as '''always'''.}}
{{CSS_Property_Value|Data Type=right |Description=Currently behaves the same as '''always'''.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''page-break-after''' attribute and the '''page-break-after''' property to start printing on a new page.

This example uses the '''p''' element as a selector in an embedded style sheet to break the page at the end of all paragraphs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/page-break-after.htm
|Code=
&lt;html&gt;
&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
P {
	page-break-after: always;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;
: 
&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
{{Single_Example
|Description=This example uses a button to turn off the page break after the object that has an [[html/attributes/id|'''ID''']] value of '''oPrgrph'''. When the page is printed or previewed, a page break occurs after the first paragraph unless the user clicks the button.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pagebreakAfter.htm
|Code=
&lt;html&gt;
&lt;body&gt;
&lt;p id{{=}}"oPrgrph" style{{=}}"page-break-after: always;"&gt;If you print (or preview) this 
page, there will be a page-break after this paragraph, unless you click the button.&lt;/p&gt;
&lt;!-- CLICKING ON THIS BUTTON TURNS OFF BREAK --&gt;
&lt;button onclick{{=}}"oPrgrph.style.pageBreakAfter{{=}}''"&gt;Turn Off Break&lt;/button&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property applies when printing the document. This property does not apply to the '''br''' or '''hr''' elements.
If there are conflicts between this property and the [[css/properties/page-break-before|'''page-break-before''']] value on the object previously displayed in the browser, the value that results in the largest number of page breaks is used.
Page breaks are not permitted inside positioned objects.
|Import_Notes=
===Syntax===
<code>'''page-break-after: '''auto '''{{!}}''' always '''{{!}}''' avoid '''{{!}}''' left '''{{!}}''' right '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/page-break-inside|page-break-inside]]</code>
*<code>[[css/properties/page-break-before|page-break-before]]</code>
*<code>Conceptual</code>
*<code>CSS How-to - Optimize Pages for Printing Using CSS</code>
|Topic_clusters=Paged Media
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}