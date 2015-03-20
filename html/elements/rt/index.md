{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=HTML information section must be modified. Add compatibility and more example.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The rt element marks the ruby text component of a ruby annotation.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag omissible in certain cases
|CSS_display=ruby-text
|Content=Internationalization topics related to the <code>rt</code> element:
* [http://localhost/International/techniques/authoring-html#ruby Using ruby markup]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''RT''' element to specify a string of text as an annotation or pronunciation guide to the base text.
|Code=&lt;ruby&gt;
   Base Text
   &lt;rt&gt;Ruby Text
&lt;/ruby&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rt.htm
}}{{Single Example
|Language=HTML
|Code=<nowiki>
<p lang="ja">...<ruby>漢<rt>かん</rt>字<rt>じ</rt></ruby>...</p>
</nowiki>
}}
}}
{{Notes_Section
|Notes====Remarks===
A ruby is an annotation or pronunciation guide for a string of text. The string of text annotated with a ruby is referred to as the base.
The ruby text specified by the '''RT''' element is positioned '''above''' or '''inline''' with the [[css/properties/ruby-position|'''rubyPosition''']] property. Browsers that do not support the '''RT''' element render the ruby text inline with the base text.
This element is available in HTML and script as of Microsoft Internet Explorer 5.
The ruby text specified by the '''RT''' element is positioned '''above''' or '''inline''' with the [[css/properties/ruby-position|'''rubyPosition''']] property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-rt-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-rt-element
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>ruby</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}