{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''className''' attribute to apply one or more styles to an HTML element.
|Code=&lt;HEAD&gt;
    &lt;STYLE TYPE{{=}}"text/css"&gt;
        P {font-size: 24pt;}
        .redText {color: red;}
        .blueText {color: blue;}
        .italicText {font-style: italic;}
    &lt;/STYLE&gt;
&lt;/HEAD&gt;

&lt;BODY&gt;
    &lt;P&gt;
        Large text, no class specified, one implied.
    &lt;/P&gt;
    &lt;P CLASS{{=}}"redText"&gt;
        Large text, .redText class specified.
    &lt;/P&gt;
    &lt;P CLASS{{=}}"blueText italicText"&gt;
        Large text, .blueText and .italicText classes specified.
    &lt;/P&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/className.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The class is typically used to associate a particular style rule in a style sheet with the element.
You can apply multiple styles to an element by specifying more than one style for the '''CLASS''' attribute. To apply multiple styles to a single element, use the following syntax:
 <code>&lt;ELEMENT CLASS {{=}} "sClass [ sClass2 [ sClass3 ... ] ]" ... &gt;</code>
By default, the property is equal to the string assigned to the '''className''' property of the given object, or null if the attribute is not explicitly assigned.
When multiple styles are specified for an element, a conflict could develop if two or more styles define the same attribute differently. In this case, you can resolve the conflict by applying styles to the element in the following order, according to the Cascading Style Sheets (CSS) selector used to define the style:
#Element
#'''CLASS'''
#[[html/attributes/id|'''ID''']]
#Inline styles

When two or more selectors pertain to an element, a style defined later takes precedence over a style defined earlier. For more information, see [http://msdn.microsoft.com/en-us/library/240ww6sz(VS.71).aspx Introduction to Cascading Style Sheets].
Multiple styles are supported as of Microsoft Internet Explorer 5.
In Windows Internet Explorer 8, class names, such as <code>hslice</code> and <code>entry-title</code>, are used to identify portions of a webpage that can be monitored for updates (Web Slices). For more information, see Subscribing to Content with Web Slices.
|Import_Notes====Syntax===
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}