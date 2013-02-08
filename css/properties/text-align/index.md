{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The text-align property controls the horizontal alignment of text within an element.}}
{{CSS Property
|Initial value=depends on direction
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=left
|Description=Default. Text is aligned to the left.
}}{{CSS Property Value
|Data Type=right
|Description=Text is aligned to the right.
}}{{CSS Property Value
|Data Type=center
|Description=Text is centered.
}}{{CSS Property Value
|Data Type=justify
|Description=Text is justified.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''text-align''' attribute and the '''text-align''' property to align text within the object.

This example uses '''p''' as a selector and two classes to call an embedded style sheet that aligns the text according to the respective rule.
|Code=&lt;STYLE&gt;
    P { text-align:center }
    .align1 { text-align:right }
    .align2 { text-align:justify }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P onclick{{=}} "this.className{{=}}'align1'" 
    ondblclick{{=}}"this.className{{=}}'align2'"&gt;
. . . &lt;/P&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/text-align.htm
}}{{Single Example
|Description=This example uses inline scripting to change the alignment of the text when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;P STYLE{{=}}"font-size:14" 
    onmouseover{{=}}"this.style.textAlign{{=}}'center'"&gt;
. . . &lt;/P&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textAlign.htm
}}{{Single Example
|Language=HTML
|Description=This just shows the four possible types of text-alignment.
|Code=<!doctype html>
<html>
    <head>
        <title> Alignment examples </title>

        <style>
            body{
                padding : 10px;
            }
            .example{
                border-bottom: 1px solid gray;
            }
            .justified{
                width: 200px; /* We limit the width in order to show the justified text */
            }

        </style>
        <style>
            .left { text-align: left;}
            .cenetered{ text-align: center;}
            .right { text-align: right;}
            .justified { text-align: justify;}
        </style>
    </head>

    <body>
        <p class="left-aligned example"> This paragraph is aligned to the left. </p>

        <p class="cenetered example"> This paragraph is ceneterd. </p>

        <p class="right example"> This paragraph is aligned to the right. </p>

        <p class="justified example">
            This paragraph needs to be really long in order to show how to justify text.
            It only works because we set a width for this paragraph though.
        </p>
    </body>
</html>
}}
}}
{{Notes_Section
|Notes====Remarks===
The property applies to block elements. The property is inherited by all block-level objects inside a '''div''' object. This parameter receives null if the attribute is not set.
The '''justify''' possible value is available as of Microsoft Internet Explorer 4.0.
|Import_Notes====Syntax===
<code>'''text-align: '''left '''{{!}}''' right '''{{!}}''' center '''{{!}}''' justify</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.6
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS2
|URL=http://www.w3.org/TR/CSS2/
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Yes
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}