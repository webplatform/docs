{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Lets you specify the dimensions of an absolutely positioned element that should be visible, and the element is clipped into this shape, and displayed.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. Clip to expose entire object.
}}{{CSS Property Value
|Data Type=rect(top, right, bottom, left)
|Description=Top, right, bottom, and left specify length values, any of which can be replaced by '''auto''', leaving that side not clipped. The value of top specifies that everything above this value on the Y axis (with 0 at the top) is clipped. The value of right specifies that everything above this value on the X axis (with 0 at the left) is clipped. The value of bottom specifies that everything below this value on the Y axis (with 0 at the top) is clipped. The value of left specifies that everything to the left of this value on the X axis (with 0 at the left) is clipped.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use an inline style to clip the image.
|Code=&lt;HTML&gt;
&lt;BODY&gt;
&lt;DIV STYLE{{=}}"position:absolute;top:0;left:100;
    clip:rect(15px, auto, auto, auto)"&gt;
&lt;IMG SRC{{=}}"sphere.jpg"/&gt;
&lt;/DIV&gt;
&lt;DIV STYLE{{=}}"position:absolute;top:0;left:200;
    clip:rect(auto, 15px, auto, auto)"&gt;
&lt;IMG SRC{{=}}"sphere.jpg"/&gt;
&lt;/DIV&gt;
&lt;DIV STYLE{{=}}"position:absolute;top:0;left:300;
    clip:rect(auto, auto, 15px, auto)"&gt;
&lt;IMG SRC{{=}}"sphere.jpg"/&gt;
&lt;/DIV&gt;
&lt;DIV STYLE{{=}}"position:absolute;top:0;left:400;
    clip:rect(auto, auto, auto, 15px)"&gt;
&lt;IMG SRC{{=}}"sphere.jpg"/&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clip_h.htm
}}{{Single Example
|Description=The following example shows how to use inline scripting to clip the image.
|Code=&lt;IMG ID{{=}}"sphere" SRC{{=}}"sphere.jpg" 
    STYLE{{=}}"position:absolute;top:0cm;left:0cm;"&gt;
&lt;BUTTON 
    onclick{{=}}"sphere.style.clip{{=}}'rect(0.2cm, 0.6cm, 1cm, 0.1cm)'"&gt;
    Clip Image&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clip_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Windows Internet Explorer 8, the required syntax of the '''clip''' attribute is identical to that specified in the Cascading Style Sheets, Level 2 Revision 1 (CSS2.1) specification; that is, commas are now required between the parameters of the <code>rect()</code> value. This behavior requires Windows Internet Explorer to be in IE8 Standards mode (or EmulateIE8 mode with an Internet Explorer 8 [[html/elements/!DOCTYPE|!DOCTYPE]] directive). For more information on document compatibility modes, see Defining Document Compatibility.
In Windows Internet Explorer 7 and earlier (and in Internet Explorer 8 or later in IE7 Standards mode, EmulateIE7 mode, or IE5 (Quirks) mode), the commas should be omitted. For example: '''clip''':<code>rect(0 50 50 0)</code>
The required syntax of the '''clip''' attribute is identical to that specified in the CSS2.1 specification; that is, commas are now required between the parameters of the <code>rect()</code> value.
This property defines the shape and size of the positioned object that is visible. The [[css/properties/position|'''position''']] must be set to '''absolute'''. Any part of the object that is outside the clipping region is transparent. Any coordinate can be replaced by the value '''auto''', which exposes the respective side (that is, the side is not clipped).
The order of the values '''clip''':<code>rect(0, 0, 50, 50)</code> renders the object invisible because it sets the top and right positions of the clipping region to 0. To achieve a 50-by-50 view port, use '''clip''':<code>rect(0, 50, 50, 0)</code>.
The '''clip''' attribute and the '''clip''' property are available on the Macintosh platform, as of Microsoft Internet Explorer 5.
|Import_Notes====Syntax===
<code>'''clip: '''auto '''{{!}}''' rect(top, right, bottom, left)</code>
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
|Topic_clusters=Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/properties/clipBottom|clipBottom]]</code>
*<code>[[css/cssom/properties/clipLeft|clipLeft]]</code>
*<code>[[css/cssom/properties/clipRight|clipRight]]</code>
*<code>[[css/cssom/properties/clipTop|clipTop]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}