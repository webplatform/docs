{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>&lt;ins&gt;</code> element represents a range of text that has been inserted (added) to a document.}}
{{Markup_Element
|DOM_interface=dom/HTMLModElement
|Content==== Attributes ===

<p>Besides the [[html/global_attributes|universal attributes]] the following attributes are supported:</p>

<dl>
    <dt>cite</dt>
    <dd>
        The <code>&lt;cite&gt;</code> attribute may be used to specify the address of a document that explains the change. 
        When that document is long, for instance the minutes of a meeting, authors are encouraged to include a fragment 
        identifier pointing to the specific part of that document that discusses the change.
        If present, it must be a [http://www.w3.org/html/wg/drafts/html/master/infrastructure.html#valid-url-potentially-surrounded-by-spaces valid URL] potentially surrounded by spaces that explains the change.
    </dd>
    <dt>datetime</dt>
    <dd>
        The <code>&lt;datetime&gt;</code> attribute may be used to specify the time and date of the change.
        If present, it must be a valid [http://www.w3.org/html/wg/drafts/html/master/infrastructure.html#valid-date-string-with-optional-time date string with optional time].
    </dd>
</dl>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the <code>&lt;ins&gt;</code> element to specify text inserted into a document.
|Code=&lt;ins datetime{{=}}"1997-10-01T12:15:30-05:00"&gt;This text has been inserted.&lt;/ins&gt;
}}{{Single Example
|Language=HTML
|Description=This example uses <code>&lt;ins&gt;</code> and <code>&lt;del&gt;</code> elements to explain changes in a document
|Code=&lt;p&gt;I &lt;del&gt;am&lt;/del&gt;&lt;ins&gt;was&lt;/ins&gt; on vacation in &lt;del&gt;France&lt;/del&gt;&lt;ins&gt;Italy&lt;/ins&gt;.&lt;/p&gt;
&lt;p&gt;
  &lt;del&gt;It is supposed to be sunny and hot.&lt;/del&gt;
  &lt;ins&gt;It rained in France so we decided to go to Italy instead.&lt;/ins&gt;
&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/6365735
}}{{Single Example
|Language=CSS
|Description=Typical browser default CSS properties for the <code>&lt;dl&gt;</code> element.
|Code=text-decoration: underline;
}}
}}
{{Notes_Section
|Notes=For Internet Explorer 8 and later the value of the [[html/attributes/cite|'''cite''']] attribute depends on the current document compatibility mode.
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
|External_links=http://www.w3.org/TR/html-markup/ins.html#ins
|Manual_sections====Related pages (MSDN)===
*<code>del</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}