{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The background-position property sets the starting position of a background image.}}
{{API_Object_Property
|Property_applies_to=css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
|Read_only=No
|Example_object_name=declaration
|Javascript_data_type=String
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''background''' property and the '''background''' attribute to set the background values.

This example uses inline event handlers to modify the [[css/properties/background-color|'''background-color''']] and [[css/properties/background-position|'''background-position''']] attributes of an image. These attributes are specified in an embedded style sheet using the '''background''' attribute.
|Code=&lt;STYLE&gt;
.style1{background:beige url(sphere.jpg) no-repeat top center}
.style2{background:ivory url(sphere.jpeg) no-repeat bottom right}
&lt;/STYLE&gt;
&lt;/HEAD&gt; 
&lt;BODY&gt;
&lt;SPAN onmouseover{{=}}"this.className{{=}}'style1'"
    onmouseout{{=}}"this.className{{=}}'style2'"&gt;
. . .  &lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background_h.htm
}}{{Single Example
|Description=This example uses inline scripting to modify the [[css/properties/background-color|'''background-color''']] and [[css/properties/background-position|'''background-position''']] properties of an image.
|Code=&lt;SPAN onclick{{=}}"this.style.background{{=}}'beige url(sphere.jpeg) 
  no-repeat top center'"&gt;
. . . &lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''background''' property is a composite property. Separate properties can be used to specify each property, but in many cases it is more convenient to set them in one place using this composite property.
Individual background properties not set by the composite background property are set to their default values. For example, the default value for 
'''image''' is '''none'''. Setting '''background''': 
'''white''' is equivalent to setting '''background''': '''white''' '''none''' '''repeat''' '''scroll''' '''0%''' '''0%'''. So, in addition to setting the background color to white, setting 
'''background''': '''white''' clears any 
'''image''', '''repeat''', '''attachment''', or '''position''' values previously set.
The background properties render in the object's content and padding; however, borders are set using the [[css/properties/border|'''border''']] properties.
In Microsoft Internet Explorer 3.0, elements that expose the '''background''' property only support the '''color''' and '''image''' values; the '''attachment''' value is only supported by the '''body''', [[html/elements/table|'''table''']], and '''td''' elements. In block elements, such as '''p''' and '''div''', background images and colors appear only behind text in Internet Explorer 3.0; in Microsoft Internet Explorer 4.0 and later, backgrounds stretch from margin to margin when used with block elements.
Although objects do not inherit the '''background''' property, the background image or color of an object's parent appears behind an object if a background is not specified.
For more information about supported colors, see the Color Table.
|Import_Notes====Syntax===
<code>'''background: ''''''[''' ''
&lt;color&gt;
'' '''{{!}}{{!}}''' image '''{{!}}{{!}}''' repeat '''{{!}}{{!}}''' attachment '''{{!}}{{!}}''' position ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.7
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
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
|Topic_clusters=Background
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}