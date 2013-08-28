{{Page_Title}}
{{Flags
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete
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
    <dt>[[html/attributes/cite|cite]]</dt>
    <dd>
        The <code>&lt;cite&gt;</code> attribute may be used to specify the address of a document that explains the change. 
        When that document is long, for instance the minutes of a meeting, authors are encouraged to include a fragment 
        identifier pointing to the specific part of that document that discusses the change.
        If present, it must be a [[html/data_types/url|URL]] potentially surrounded by spaces that explains the change.
    </dd>
    <dt>[[html/attributes/datetime|datetime]]</dt>
    <dd>
        The <code>&lt;datetime&gt;</code> attribute may be used to specify the time and date of the change.
        If present, it must be a valid [[html/data_types/datetime|date string with optional time]].
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
|Code=display: inline;
text-decoration: underline;
}}
}}
{{Notes_Section
|Notes=For Internet Explorer 8 and later the value of the [[html/attributes/cite|'''cite''']] attribute depends on the current document compatibility mode.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-ins
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/edits.html#the-ins-element
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/ins Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535842%28v=vs.85%29.aspx Microsoft Developer Network]
* http://www.w3.org/TR/html-markup/ins.html#ins
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}