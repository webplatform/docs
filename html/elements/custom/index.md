{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Ancient text from MSDN?
Deletion Candidate
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Represents a user-defined HTML tag (nonstandard)}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=
|CSS_display=
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''custom''' element to create custom RED, GREEN, and BLUE elements. These elements change the color of the text to red, green, or blue, depending on whether it is surrounded by RED, GREEN, or BLUE tags. In this example, the RED, GREEN, and BLUE tags are defined within a namespace called CUSTOMTAG.
|Code=&lt;HTML XMLNS:CUSTOMTAG&gt;
&lt;HEAD&gt;
&lt;STYLE&gt;
@media all {
    CUSTOMTAG\:RED { color: red; }
    CUSTOMTAG\:GREEN { color: green; }
    CUSTOMTAG\:BLUE { color: blue; }
}
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;CUSTOMTAG:RED&gt;
This text is red because it is enclosed within opening
and closing CUSTOMTAG:RED tags.
&lt;/CUSTOMTAG:RED&gt;
&lt;CUSTOMTAG:GREEN&gt;
This text is green because it is enclosed within opening
and closing CUSTOMTAG:GREEN tags.
&lt;/CUSTOMTAG:GREEN&gt;
&lt;CUSTOMTAG:BLUE&gt;
This text is blue because it is enclosed within opening
and closing CUSTOMTAG:BLUE tags.
&lt;/CUSTOMTAG:BLUE&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/custom.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
To declare a namespace, use the [[apis/xhr/properties/XMLNS attribute|'''XMLNS''']] attribute of the HTML element.
When defining custom tags, you must enclose custom tag definitions within an [[css/atrules/@media|'''@media''']] wrapper.
Custom tags become much more interesting when applied with a Dynamic HTML (DHTML) behavior. Dynamic HTML (DHTML) behaviors (or behaviors) and styles are applied to elements on a page the same way—using Cascading Style Sheets (CSS) attributes. More specifically, the proposed CSS [[css/media queries/behavior|'''behavior''']] attribute enables a document author to specify the location of the behavior and apply that behavior to an element.
The Windows Internet Explorer support for custom tags on an HTML page requires that a namespace be defined for the tag. Otherwise, the custom tag is treated as an unknown tag when the document is parsed. Although navigating to a page with an unknown tag in Internet Explorer does not result in an error, unknown tags have the disadvantage of not being able to contain other tags, nor can they have behaviors applied to them.
This element is available in HTML and script as of Microsoft Internet Explorer 5.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>Using Custom Tags in Internet Explorer</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}