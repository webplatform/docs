{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Represents a run of text that is contextually-important for some reason, such as text that has been marked or highlighted.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows the difference between denoting the importance of a span of text ('''strong''') as opposed to denoting the relevance of a span of text ('''mark'''). It is an extract from a textbook, where the extract has had the parts relevant to the exam highlighted. The safety warnings, important though they may be, are not relevant to the exam.
|Code=&lt;h3&gt;Wormhole Physics Introduction&lt;/h3&gt;
&lt;p&gt;&lt;mark&gt;A wormhole in normal conditions can be held open for a
maximum of just under 39 minutes.&lt;/mark&gt; Conditions that can increase
the time include a powerful energy source coupled to one or both of
the gates connecting the wormhole, and a large gravity well (such as a
black hole).&lt;/p&gt;
&lt;p&gt;&lt;mark&gt;Momentum is preserved across the wormhole. Electromagnetic
radiation can travel in both directions through a wormhole,
but matter cannot.&lt;/mark&gt;&lt;/p&gt;
&lt;p&gt;When a wormhole is created, a vortex normally forms.
&lt;strong&gt;Warning: The vortex caused by the wormhole opening will
annihilate anything in its path.&lt;/strong&gt; Vortexes can be avoided when
using sufficiently advanced dialing technology.&lt;/p&gt;
&lt;p&gt;&lt;mark&gt;An obstruction in a gate will prevent it from accepting a
wormhole connection.&lt;/mark&gt;&lt;/p&gt;
}}{{Single Example
|Language=HTML
|Description=This example uses mark to indicate the "current" link.
|Code=&lt;nav>
  &lt;ul>
    &lt;li><a href="/one">One&lt;/a>&lt;/li>
    &lt;li>&lt;mark><a href="/two">Two&lt;/a>&lt;/mark>&lt;/li>
    &lt;li><a href="/three">Three&lt;/a>&lt;/li>
    &lt;li><a href="/four">Four&lt;/a>&lt;/li>
  &lt;/ul>
&lt;nav>
}}
}}
{{Notes_Section
|Usage=The '''mark''' element is a phrasing-level element. It must not contain block-level elements, but it can contain other phrasing-level elements.
|Notes=The '''mark''' element denotes the relevance of a span of text. By default, most browsers render it in black text on a yellow background, but you can change that with CSS.

To indicate importance, use [[html/elements/em|'''strong''']]; for emphasis, use [[html/elements/em|'''em''']].

When used in the main prose of a document, the '''mark''' element indicates a part of the document that has been highlighted. When used in a quotation or other block of text (such as an [[html/elements/aside|'''aside''']]), it indicates a highlight that was not originally present but which has been added to bring the reader's attention to a part of the text. For example, the following are valid uses for the '''mark''' element:

* Bring attention to a particular string of text.
* Highlight parts of document that match a search string.
* Enable body text to refer to a specific part of a quotation or code fragment.

Windows Internet Explorer 9.  The '''mark''' element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.
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
|Topic_clusters=HTML, Text
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}