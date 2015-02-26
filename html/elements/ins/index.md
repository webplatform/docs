{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Compatibility
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''ins''' element represents a range of text that has been inserted (added) into a document.}}
{{Markup_Element
|DOM_interface=dom/HTMLModElement
|Tag_omissions=
|CSS_display=
|Content==== Attributes ===

<p>Besides the [[html/global_attributes|global attributes]] the following attributes are supported:</p>

<dl>
    <dt>[[html/attributes/cite|'''cite''']]</dt>
    <dd>
        The '''cite''' attribute may be used to specify the address of a document that explains the change. When that document is long (e.g. the minutes of a meeting) authors are encouraged to include a fragment identifier pointing to the specific part of that document that discusses the change.
    </dd>
    <dt>[[html/attributes/datetime|'''datetime''']]</dt>
    <dd>
        The '''datetime''' attribute may be used to specify the time and date of the change. If present, it must be a valid [http://www.w3.org/html/wg/drafts/html/master/infrastructure.html#valid-date-string-with-optional-time date string with optional time].
    </dd>
</dl>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''ins''' element to specify text inserted into a document.
|Code=&lt;p>This text existed in the document when it 
was written. &lt;ins datetime{{=}}"1997-10-01T12:15:30-05:00"&gt;This 
text was inserted on 1 October 1997 at 12:15pm in
the Eastern time zone.&lt;/ins>&lt;/p>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses '''ins''' and '''del''' elements to explain changes in a document
|Code=&lt;p&gt;I &lt;del&gt;am&lt;/del&gt;&lt;ins&gt;was&lt;/ins&gt; on vacation in &lt;del&gt;France&lt;/del&gt;&lt;ins&gt;Italy&lt;/ins&gt;.&lt;/p&gt;
&lt;p&gt;
  &lt;del&gt;It is supposed to be sunny and hot.&lt;/del&gt;
  &lt;ins&gt;It rained in France so we decided to go to Italy instead.&lt;/ins&gt;
&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/6365735
}}
}}
{{Notes_Section
|Usage=The default behavior of the '''ins''' element is as a phrasing-level element, but it can be wrapped around any element within the '''body'''.
|Notes=The default browser display of '''ins''' is underlined.

If you want to underline text, but it is not an insertion, you should use the CSS rule '''text-decoration: underline''' on the appropriate element enclosing the text.

If you are looking to emphasize a word or phrase, the [[html/elements/em|'''em''' element]] would be a better choice.

For Internet Explorer 8 and later the value of the [[html/attributes/cite|'''cite''']] attribute depends on the current document compatibility mode.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/edits.html#the-ins-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/edits.html#the-ins-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-ins
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
|Manual_links=* [[html/elements/ins|ins]]
* [[html/elements/del|del]]
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/ins Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535842%28v=vs.85%29.aspx Microsoft Developer Network]
* http://www.w3.org/TR/html-markup/ins.html#ins
|Manual_sections=
}}
{{Topics|HTML, XHTML}}
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