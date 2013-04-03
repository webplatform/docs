{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Review
|Content=Compatibility Incomplete, Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The text-align CSS property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements itself, only their inline content.}}
{{CSS Property
|Initial value=start, or a nameless value that acts as left if direction is ltr, right if direction is rtl if start is not supported by the browser.
|Applies to=block containers
|Inherited=Yes
|Media=visual
|Computed value=as specified, except for the match-parent value which is calculated against its parent's direction value and results in a computed value of either left or right
|Animatable=No
|CSS object model property=textAlign
|Values={{CSS Property Value
|Data Type=start
|Description=The same as ''<code>left</code>'' if direction is left-to-right and ''<code>right</code>'' if direction is right-to-left. '''''Experimental'''
}}{{CSS Property Value
|Data Type=end
|Description=The same as ''<code>right</code>'' if direction is left-to-right and ''<code>left</code>'' if direction is right-to-left. '''''Experimental'''
}}{{CSS Property Value
|Data Type=left
|Description=The inline contents are aligned to the left edge of the line box.
}}{{CSS Property Value
|Data Type=right
|Description=The inline contents are aligned to the right edge of the line box.
}}{{CSS Property Value
|Data Type=center
|Description=The inline contents are centered within the line box.
}}{{CSS Property Value
|Data Type=<string>
|Description=The first occurrence of the one-char string is the element used for alignment. the keyword that follows or precedes it indicates how it is aligned. This allows to align numeric values on the decimal point, for instance. '''''Experimental'''
}}{{CSS Property Value
|Data Type=justify
|Description=The text is justified. Text should line up their left and right edges to the left and right content edges of the paragraph.
}}{{CSS Property Value
|Data Type=match-parent
|Description=Similar to inherit with the difference that the value ''<code>start</code>'' and ''<code>end</code>'' are calculated according the parent's direction and are replaced by the adequate ''<code>left</code>'' or ''<code>right</code>'' value. '''''Experimental'''
}}{{CSS Property Value
|Data Type=start end
|Description=Specifies ''<code>start</code>'' alignment of the first line and any line immediately after a forced line break; and ''<code>end</code>'' alignment of any remaining lines not affected by [[css/properties/text-align-last|'''text-align-last''']].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This just shows the four possible types of text-alignment.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
    &lt;head&gt;
        &lt;title&gt; Alignment examples &lt;/title&gt;

        &lt;style&gt;
            body{
                padding : 10px;
            }
            .example{
                border-bottom: 1px solid gray;
            }
            .justified{
                width: 200px; /* We limit the width in order to show the justified text */
            }

        &lt;/style&gt;
        &lt;style&gt;
            .left { text-align: left;}
            .cenetered{ text-align: center;}
            .right { text-align: right;}
            .justified { text-align: justify;}
        &lt;/style&gt;
    &lt;/head&gt;

    &lt;body&gt;
        &lt;p class=&quot;left-aligned example&quot;&gt; This paragraph is aligned to the left. &lt;/p&gt;

        &lt;p class=&quot;cenetered example&quot;&gt; This paragraph is ceneterd. &lt;/p&gt;

        &lt;p class=&quot;right example&quot;&gt; This paragraph is aligned to the right. &lt;/p&gt;

        &lt;p class=&quot;justified example&quot;&gt;
            This paragraph needs to be really long in order to show how to justify text.
            It only works because we set a width for this paragraph though.
        &lt;/p&gt;
    &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://dabblet.com/gist/4739662
}}{{Single Example
|Description=This example uses inline scripting to change the alignment of the text when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;P STYLE{{=}}"font-size:14" 
    onmouseover{{=}}"this.style.textAlign{{=}}'center'"&gt;
. . . &lt;/P&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textAlign.htm
}}{{Single Example
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
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Level 3
|URL=http://dev.w3.org/csswg/css3-text/#text-align
|Status=Working Draft
|Relevant_changes=Added the <code>start</code> and <code>end</code> keyword. Changed the unnamed initial value to <code>start</code> (which it was). Added the <code><string></code> value, the <code>match-parent</code> value and the <code>start end</code> double value.
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/text.html#alignment-prop
|Status=Recommendation
|Relevant_changes=No Changes
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#text-align
|Status=Recommendation
|Relevant_changes=Initial definition.
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