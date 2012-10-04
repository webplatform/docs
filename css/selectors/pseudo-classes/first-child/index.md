{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=In the following example, the selector matches any '''p''' element that is the first child of its parent. The style rule below applies indentation to the '''p''' of the First fragment only.
|LiveURL=
|Code=
&lt;style&gt;
    p:first-child { text-indent: 5px; }
&lt;/style&gt; 
}}
{{Single_Example
|Description=The preceding selector would match the '''p''' inside the '''div''' of the first fragment that follows, but would not match the '''p''' in the second fragment.
|LiveURL=
|Code=
&lt;!-- First fragment --&gt;
&lt;div class{{=}}"note"&gt;
   &lt;p&gt; The first P inside the note. &lt;/p&gt;
&lt;/div&gt;
&lt;!-- Second fragment --&gt;
&lt;div class{{=}}"note"&gt;
   &lt;h2&gt;Note&lt;/h2&gt;
   &lt;p&gt; The first P inside the note. &lt;/p&gt;
&lt;/div&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The ''':first-child''' pseudo-class matches an element that is the first child element of some other element.
'''Note'''   Requires Windows Internet Explorer 7 or later.
'''Note'''   Pseudo-class enabled only in standards-compliant mode (strict [[html/elements/!DOCTYPE|!DOCTYPE]]).
Inline text is not considered to be part of the document tree, and is not counted when calculating the first child. For example, the '''EM''' element is the first child of the '''p''' element in the following HTML.
 <code>&lt;p&gt;abc &lt;em&gt;default&lt;/em&gt; def&lt;/p&gt;</code>
|Import_Notes=
===Syntax===

selector
:first-child
===Parameters===
;''selector'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.11.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>[[css/selectors/pseudo-elements/::first-letter|::first-letter]]</code>
*<code>[[css/selectors/pseudo-elements/::first-line|::first-line]]</code>
|Topic_clusters=Selectors, Pseudo-Classes
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}