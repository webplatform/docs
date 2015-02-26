{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=HTML information section must be modified. Add compatibility.
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The ruby element allows one or more spans of phrasing content to be marked with ruby annotations. Ruby annotations are short runs of text presented alongside base text, primarily used in East Asian typography as a guide for pronunciation or to include other annotations.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=ruby
|Content=Ruby annotations are short runs of text presented alongside base text, primarily used in East Asian typography as a guide for pronunciation or to include other annotations.<br />In Japanese, this form of typography is also known as <i>furigana</i>.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''RUBY''' element to specify the first string of text as the base, and the '''RT''' element to specify the second string of text as the ruby.
|Code=&lt;RUBY&gt;
   Base Text
   &lt;RT&gt;Ruby Text
&lt;/RUBY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/ruby.htm
}}{{Single Example
|Language=HTML
|Description=In this example, each ideograph in the Japanese text <i>漢字</i> is annotated with its reading in <i>hiragana</i>.
|Code=<nowiki>
<pre lang="ja">
<p>...<ruby>漢<rt>かん</rt>字<rt>じ</rt></ruby>...</p>
</pre>
</nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
A ruby is an annotation or pronunciation guide for a string of text. The string of text annotated with a ruby is referred to as the base.
The only valid object within the '''RUBY''' element is the '''RT''' element. Text not contained within the ruby text object, '''RT''', is assumed to be a part of the base.
This element is available in HTML and script as of Microsoft Internet Explorer 5.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-ruby-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-ruby-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Ruby
|Manual_links=
|External_links=* [http://www.w3.org/International/techniques/authoring-html#ruby Using ruby markup]
|Manual_sections====Related pages (MSDN)===
*<code>rt</code>
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