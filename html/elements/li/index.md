{{Page_Title|li – list item}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The li element represents one list item.}}
{{Markup_Element
|DOM_interface=dom/HTMLLIElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the &lt;li&gt; element to create individual items in an unordered list.
|Code=
<ul>
     <li>Art</li>
     <li>History</li>
     <li>Literature</li>
     <li>Sports</li>
     <li>Entertainment</li>
     <li>Science</li>
</ul>

}}{{Single Example
|Language=HTML
|Description=This example uses the &lt;li&gt; element to create individual items in an ordered list.
|Code=<ol>
     <li>First</li>
     <li>Second</li>
     <li>Third</li>
</ol>

}}
}}
{{Notes_Section
|Notes====Remarks===
The [[html/attributes/type (ul,li,ol elements)|'''TYPE''']] attribute values '''disc''', '''circle''', and '''square''' apply to unordered lists; the values '''1''', '''a''', '''A''', '''i''', and '''I''' apply to ordered lists.
When the '''LI''' element is absolutely positioned with CSS, the list item marker is not rendered.
As of Microsoft Internet Explorer 6, the default value of the [[css/properties/display|'''display''']] property for this element is '''list-item'''.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 10.2
*[http://www.w3.org/TR/html5/grouping-content.html#the-li-element{{=}}HTML5 Specification]
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
|Manual_links=* [[html/elements/dir|<code>dir</code>]]
* [[html/elements/menu|<code>menu</code>]]
* [[html/elements/ol|<code>ol</code>]]
* [[html/elements/ul|<code>ul</code>]]
* [[html/elements/dd|<code>dd</code>]]
* [[html/elements/dt|<code>dt</code>]]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}