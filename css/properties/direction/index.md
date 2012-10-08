{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=ltr
|Description=Default. Content flows left to right.
}}{{CSS Property Value
|Data Type=rtl
|Description=Content flows right to left.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example demonstrates how to set and retrieve the value of the '''direction''' property.  When the user sets the value of the '''direction''' property of a '''div''' element, the value of the property is retrieved in a '''span''' element.
|Code=&lt;HTML&gt;
  &lt;HEAD&gt;
    &lt;SCRIPT&gt;
    function fnSwitch()
    {
      oDiv.style.direction {{=}} event.srcElement.innerText;
      DirSpan.innerText {{=}} oDiv.style.direction;
    }
    &lt;/SCRIPT&gt;
  &lt;/HEAD&gt;
  &lt;BODY&gt;
    &lt;H1&gt;direction Property Sample&lt;/H1&gt;
    &lt;H2&gt;direction: 
      &lt;SPAN id{{=}}"DirSpan" style{{=}}"color:red"&gt;&lt;/SPAN&gt;
    &lt;/H2&gt;
  [ &lt;A href{{=}}"#" onclick{{=}}fnSwitch()&gt;ltr&lt;/A&gt; {{!}} &lt;A href{{=}}"#" 
  onclick{{=}}fnSwitch()&gt;rtl&lt;/A&gt; {{!}} &lt;A href{{=}}"#" onclick{{=}}fnSwitch()&gt;inherit&lt;/A&gt; ]&lt;/P&gt;
  
  &lt;DIV id{{=}}"oDiv"&gt;The quick brown fox jumps over the lazy yellow dog. The quick brown fox 
  jumps over the lazy yellow dog. The quick brown fox jumps over the lazy yellow 
  dog. The quick brown fox jumps over the lazy yellow dog. The quick brown fox 
  jumps over the lazy yellow dog.&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/direction.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The property does not affect alphanumeric characters in Latin documents. These characters always render '''ltr'''.  However, the property does affect punctuation characters in Latin documents.
The property pertains only to the directional flow of an element's content. It has no effect on properties such as [[css/properties/left|'''left''']] or [[css/properties/right|'''right''']], [[css/properties/margin-left|'''margin-left''']] or [[css/properties/margin-right|'''margin-right''']].  The '''margin-left''' property, for example, sets or retrieves the width of the margin on the left side of the document regardless of the value of the '''direction''' property.
|Import_Notes====Syntax===
<code>'''direction: '''ltr '''{{!}}''' rtl</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.10
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[html/attributes/dir|dir]]</code>
*<code>Conceptual</code>
*<code>HTML Character Sets</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}