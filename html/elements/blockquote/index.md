{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''blockquote''' element indicates an extended quotation.}}
{{Markup_Element
|DOM_interface=dom/HTMLQuoteElement
|Content====Introduction===
The '''blockquote''' element represents content that is quoted from another source, optionally with a citation which must be within a [[html/elements/footer|'''footer''']] or [[html/elements/cite|'''cite''']] element, and optionally with in-line changes such as annotations and abbreviations.

Content inside a '''blockquote''' other than citations and in-line changes must be quoted from another source, whose address, if it has one, may be cited in the [[html/attributes/cite|'''cite''' attribute]].

: Note: In cases where a page contains contributions from multiple people, such as comments on a blog post, 'another source' can include text from the same page, written by another person.

If the cite attribute is present, it must be a valid URL potentially surrounded by spaces. To obtain the corresponding citation link, the value of the attribute must be resolved relative to the element. User agents may allow users to follow such citation links, but they are primarily intended for private use (e.g. by server-side scripts collecting statistics about a site's use of quotations), not for readers.

The cite IDL attribute must reflect the element's cite content attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- This example uses the blockquote element to set off a quotation that renders as indented text: --&gt;
&lt;p&gt;He said,
&lt;blockquote cite="http://www.example.com"&gt;"Hi there!"&lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Description=The '''blockquote''' element represents content that is quoted from another source, optionally with a citation which must be within a '''footer''' or '''cite''' element, and optionally with in-line changes such as annotations and abbreviations. For example, in English, abbreviations are traditionally identified using square brackets. Consider a page with the sentence "Fred ate the cracker. He then said he liked apples and fish."; it could be quoted as follows:
|Code=&lt;blockquote&gt;
 &lt;p&gt;[Fred] then said he liked [...] fish.&lt;/p&gt;
&lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Description=Quotation marks may be used to delineate between quoted text and annotations within a '''blockquote'''.
|Code=&lt;!-- For example, an in-line note provided by the author: --&gt;
&lt;figure&gt;
 &lt;blockquote&gt;
 "That monster custom, who all sense doth eat
 Of habit's devil," &lt;abbr title="et cetera"&gt;&c.&lt;/abbr&gt; not in Folio 
 "What a falling off was there !
 From me, whose love was of that dignity
 That it went hand in hand even with the vow
 I made to her in marriage, and to decline
 Upon a wretch."
 &lt;/blockquote&gt;
 &lt;footer&gt;
 — &lt;cite class="title"&gt;Shakespeare manual&lt;/cite&gt; by &lt;cite class="author"&gt;Frederick Gard Fleay&lt;/cite&gt;, 
 p19 (in Google Books)
 &lt;/footer&gt;
 &lt;/figure&gt;
&lt;!-- Note: In the example above, the citation is contained within the footer of a figure element, this groups and associates the information about the quote with the quote. The figcaption element was not used in this case as a container for the citation, as it is not a caption. --&gt;
}}{{Single Example
|Language=HTML
|Description=Attribution for the quotation may be be placed inside the '''blockquote''' element, but must be within a '''cite''' element for in-text attributions or within a '''footer''' element.
|Code=&lt;!-- For example, here the attribution is given in a footer after the quoted text, to clearly relate the quote to its attribution: --&gt;
&lt;blockquote&gt;
 &lt;p&gt;I contend that we are both atheists. I just believe in one fewer
 god than you do. When you understand why you dismiss all the other
 possible gods, you will understand why I dismiss yours.&lt;/p&gt;
 &lt;footer&gt;— &lt;cite&gt;Stephen Roberts&lt;/cite&gt;&lt;/footer&gt;
 &lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- Here the attribution is given in a cite element on the last line of the quoted text. Note that a link to the author is also included. --&gt;
&lt;blockquote&gt;
 The people recognize themselves in their commodities; they find their 
 soul in their automobile, hi-fi set, split-level home, kitchen equipment. 
 — &lt;cite&gt;&lt;a href="http://en.wikipedia.org/wiki/Herbert_Marcuse"&gt;Herbert Marcuse&lt;/a&gt;&lt;/cite&gt;
 &lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- Here the attribution is given in a footer after the quoted text, and metadata about the reference has been added using the Microdata syntax (note it could have equally been marked up using RDFA Lite). --&gt;
&lt;blockquote&gt;
  &lt;p&gt;... she said she would not sign any deposition containing the word "amorous" instead of "advances". For her the difference was of crucial significance, and one of the reasons she had separated from her husband was that he had never been amorous but had consistently made advances.&lt;/p&gt;
  &lt;footer itemscope itemtype="http://schema.org/Book"&gt;
    &lt;span itemprop="author"&gt;Heinrich Böll&lt;/span&gt;,
    &lt;span itemprop="name"&gt;The Lost Honor of Katharina Blum&lt;/span&gt;, 
    &lt;span itemprop="datePublished"&gt;January 1, 1974&lt;/span&gt;
  &lt;/footer&gt;
&lt;/blockquote&gt;
&lt;!-- Note: There is no formal method for indicating the markup in a blockquote is from a quoted source. It is suggested that if the footer or cite elements are included and these elements are also being used within a '''blockquote''' to identify citations, the elements from the quoted source could be annotated with metadata to identify their origin, for example by using the class attribute (a defined extensibility mechanism). --&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- In this example the source of a quote includes a cite element, which is annotated using the class attribute: --&gt;
&lt;blockquote&gt;
  &lt;p&gt;My favorite book is &lt;cite class="from-source"&gt;At Swim-Two-Birds&lt;/cite&gt;&lt;/p&gt;
  &lt;footer&gt;- &lt;cite&gt;Mike[tm]Smith&lt;/cite&gt;&lt;/footer&gt;
&lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Description=The other examples below show other ways of showing attribution.
|Code=&lt;!-- Here a blockquote element is used in conjunction with a figure element and its figcaption: --&gt;
&lt;figure&gt;
 &lt;blockquote&gt;
  &lt;p&gt;The truth may be puzzling. It may take some work to grapple with. It may be counterintuitive. It may contradict deeply held prejudices. It may not be consonant with what we desperately want to be true. But our preferences do not determine what's true. We have a method, and that method helps us to reach not absolute truth, only asymptotic approaches to the truth &mdash; never there, just closer and closer, always finding vast new oceans of undiscovered possibilities. Cleverly designed experiments are the key.&lt;/p&gt;
 &lt;/blockquote&gt;
 &lt;figcaption&gt;&lt;cite&gt;Carl Sagan&lt;/cite&gt;, in "&lt;cite&gt;Wonder and Skepticism&lt;/cite&gt;", from the &lt;cite&gt;Skeptical Enquirer&lt;/cite&gt; Volume 19, Issue 1 (January-February 1995)&lt;/figcaption&gt;
&lt;/figure&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- This next example shows the use of cite alongside blockquote: --&gt;
&lt;p&gt;His next piece was the aptly named &lt;cite&gt;Sonnet 130&lt;/cite&gt;:&lt;/p&gt;
&lt;blockquote cite="http://quotes.example.org/s/sonnet130.html"&gt;
  &lt;p&gt;My mistress' eyes are nothing like the sun,&lt;br&gt;
  Coral is far more red, than her lips red,&lt;br&gt;
  ...
}}{{Single Example
|Language=HTML
|Code=&lt;!-- This example shows how a forum post could use blockquote to show what post a user is replying to. The article element is used for each post, to mark up the threading. --&gt;
&lt;article&gt;
 &lt;h1&gt;&lt;a href="http://bacon.example.com/?blog=109431"&gt;Bacon on a crowbar&lt;/a&gt;&lt;/h1&gt;
 &lt;article&gt;
  &lt;header&gt;&lt;strong&gt;t3yw&lt;/strong&gt; 12 points 1 hour ago&lt;/header&gt;
  &lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;
  &lt;footer&gt;&lt;a href="?pid=29578"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
  &lt;article&gt;
   &lt;header&gt;&lt;strong&gt;greg&lt;/strong&gt; 8 points 1 hour ago&lt;/header&gt;
   &lt;blockquote&gt;&lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;&lt;/blockquote&gt;
   &lt;p&gt;Dude narwhals don't eat bacon.&lt;/p&gt;
   &lt;footer&gt;&lt;a href="?pid=29579"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
   &lt;article&gt;
    &lt;header&gt;&lt;strong&gt;t3yw&lt;/strong&gt; 15 points 1 hour ago&lt;/header&gt;
    &lt;blockquote&gt;
     &lt;blockquote&gt;&lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;&lt;/blockquote&gt;
     &lt;p&gt;Dude narwhals don't eat bacon.&lt;/p&gt;
    &lt;/blockquote&gt;
    &lt;p&gt;Next thing you'll be saying they don't get capes and wizard
    hats either!&lt;/p&gt;
    &lt;footer&gt;&lt;a href="?pid=29580"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
    &lt;article&gt;
     &lt;article&gt;
      &lt;header&gt;&lt;strong&gt;boing&lt;/strong&gt; -5 points 1 hour ago&lt;/header&gt;
      &lt;p&gt;narwhals are worse than ceiling cat&lt;/p&gt;
      &lt;footer&gt;&lt;a href="?pid=29581"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
     &lt;/article&gt;
    &lt;/article&gt;
   &lt;/article&gt;
  &lt;/article&gt;
  &lt;article&gt;
   &lt;header&gt;&lt;strong&gt;fred&lt;/strong&gt; 1 points 23 minutes ago&lt;/header&gt;
   &lt;blockquote&gt;&lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;&lt;/blockquote&gt;
   &lt;p&gt;I bet they'd love to peel a banana too.&lt;/p&gt;
   &lt;footer&gt;&lt;a href="?pid=29582"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
  &lt;/article&gt;
 &lt;/article&gt;
&lt;/article&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- This example shows the use of a blockquote for short snippets, demonstrating that one does not have to use p elements inside blockquote elements: --&gt;
&lt;p&gt;He began his list of "lessons" with the following:&lt;/p&gt;
&lt;blockquote&gt;One should never assume that his side of 
the issue will be recognized, let alone that it will 
be conceded to have merits.&lt;/blockquote&gt;
&lt;p&gt;He continued with a number of similar points, ending with:&lt;/p&gt;
&lt;blockquote&gt;Finally, one should be prepared for the threat 
of breakdown in negotiations at any given moment and not 
be cowed by the possibility.&lt;/blockquote&gt;
&lt;p&gt;We shall now discuss these points...
}}
}}
{{Notes_Section
|Notes====Remarks===
*Examples of how to represent a conversation are shown in a later section; it is not appropriate to use the '''cite''' and '''blockquote''' elements for this purpose.
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-blockquote-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (internal)===
*<code>[[html/elements/q|q]]</code>
*<code>[[html/elements/cite|cite]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/blockquote
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
|HTML5Rocks_link=
}}