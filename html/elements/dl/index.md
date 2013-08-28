{{Page_Title|dl – description list}}
{{Flags
|High-level issues=Needs Flags
|Checked_Out=Yes
|Editorial notes=The <code>&lt;dl&gt;</code> element is a wrapper for an HTML definition list. It defines the start and end of a definition list, and as such can contain other table elements, such as <code>&lt;dt&gt;</code> and <code>&lt;dd&gt;</code>.
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|dl}}
{{Summary_Section|article summary content}}
{{Markup_Element
|DOM_interface=dom/HTMLDListElement
|Content=<p>The <code>&lt;dl&gt;</code> element is a container for HTML definition lists, which are used to markup name-value-group data.</p>

<p>Definition lists are often used for glossaries.</p>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example shows a simple definition list with two item/description pairs.
|Code=<dl>
  <dt>Coffee</dt>
  <dd>A popular hot drink.</dd>
  <dt>Coca Cola</dt>
  <dd>One of the leading brands of a popular cold fizzy drink.</dd>
</dl>
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=HTML
|Description=The example shows a definition list with a single item but multiple descriptions for that item.
|Code=<dl>
  <dt>Coffee</dt>
  <dd>A popular hot drink.</dd>
  <dd>A mid brown colour</dd>
  <dd>A common social invitation</dd>
</dl>
|LiveURL=http://code.webplatform.org/gist/5821157
}}{{Single Example
|Language=HTML
|Description=The example shows a definition list with a single description and multiple items fitting that description.
|Code=<dl>
  <dt>Coffee</dt>
  <dt>Tea</dt>
  <dt>Vimto (in the North of England)</dt>
  <dd>A popular hot drink.</dd>
</dl>
|LiveURL=http://code.webplatform.org/gist/5821157
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML4
|URL=http://www.w3.org/TR/html4/struct/lists.html#h-10.3
|Status=Recommendation
}}{{Related Specification
|Name=HTML5.1
|URL=http://www.w3.org/html/wg/drafts/html/master/grouping-content.html#the-dl-element
|Status=Editor's Draft
|Relevant_changes=In HTML5, definition list has been changed to description list 
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
|Topic_clusters=HTML
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/dl Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535241%28v=vs.85%29.aspx Microsoft Developer Network]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}