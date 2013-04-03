{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The page-break-before property sets the page-breaking behavior before an element.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Insert a page break before the element if necessary.
}}{{CSS Property Value
|Data Type=always
|Description=Insert a page break before the element.
}}{{CSS Property Value
|Data Type=avoid
|Description=Avoid inserting a page break before the element.
}}{{CSS Property Value
|Data Type=empty string
|Description=Behaves the same as '''auto'''.
}}{{CSS Property Value
|Data Type=left
|Description=Insert page breaks before the element until it reaches a blank left page.
}}{{CSS Property Value
|Data Type=right
|Description=Insert page breaks before the element until it reaches a blank right page.
}}{{CSS Property Value
|Data Type=inherit
|Description=Specifies that the value of the page-break-before property should be inherited from the parent element
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''page-break-before''' attribute and the '''page-break-before''' property to start printing on a new page.

This example uses the '''hn''' element as a selector in an embedded style sheet to break the page before all '''hn''' headings.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
h3 {
	page-break-before: always;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;
:
&lt;/p&gt;
&lt;h3&gt;Start New Section on New Page&lt;/h3&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/page-break-before.htm
}}{{Single Example
|Description=This example uses a button to turn off the page break before the object that has an [[html/attributes/id|'''ID''']] value of '''oPrgrph'''. When the page is printed or previewed, a page break occurs before the first paragraph unless the user clicks the button.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function offBreak()
{
    oPrgrph.style.pageBreakBefore{{=}}"";
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;button onclick{{=}}"offBreak()"&gt;Turn Off Break&lt;/button&gt;
&lt;p id{{=}}"oPrgrph" style{{=}}"page-break-before: always"&gt;
: 
&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/pagebreakBefore.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This property applies when printing the document. This property does not apply to the '''br''' or '''hr''' elements.
If there are conflicts between the value of this property and the [[css/properties/page-break-after|'''page-break-after''']] property of the object previously displayed in the browser, the value that results in the largest number of page breaks is used.
Page breaks are not permitted inside positioned objects.
|Import_Notes====Syntax===
<code>'''page-break-before: '''auto '''{{!}}''' always '''{{!}}''' avoid '''{{!}}''' left '''{{!}}''' right '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3.1
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
{{See_Also_Section
|Topic_clusters=Paged Media
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/page-break-inside|page-break-inside]]</code>
*<code>[[css/properties/page-break-after|page-break-after]]</code>
*<code>Conceptual</code>
*<code>CSS How-to - Optimize Pages for Printing Using CSS</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}