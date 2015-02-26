{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add summary, notes, compatibility.
Add information about alternatives for producing word breaks, including Unicode zero-width spaces.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The Word Break Opportunity (<code>wbr</code>) element represents a position within text where the browser may optionally break a line, though its line-breaking rules would not otherwise create a break at that location.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=none
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''WBR''' element to create line breaks. In contrast, the '''NOBR''' element does not break lines.
|Code=&lt;NOBR&gt;This line of text will not break, no matter how narrow the window gets.&lt;/NOBR&gt;
&lt;NOBR&gt;This one, however,&lt;WBR&gt; will break after the word "however," 
if the window gets small enough.&lt;/NOBR&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
A soft line break is a point inside a '''NOBR''' section at which a line break is permitted but not required.

On UTF-8 encoded pages, <code><wbr></code> behaves like the U+200B ZERO-WIDTH SPACE code point. In particular, it behaves like a Unicode bidi BN code point, meaning it has no effect on bidi-ordering: <div dir=rtl>123,<wbr>456</div> displays, when not broken on two lines, 123,456 and not 456,123.

For the same reason, the <﻿wbr﻿> element does not introduce a hyphen at the line break point. To make a hyphen appear only at the end of a line, use the soft hyphen character entity (&﻿shy;) instead.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-wbr-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-wbr-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>br</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/wbr
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