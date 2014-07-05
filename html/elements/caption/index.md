{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''caption''' (&lt;caption&gt;) element represents the title of the table that is its parent.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableCaptionElement
|Content=The '''caption''' element (&lt;caption&gt;) specifies a brief description for a table.
The &lt;caption&gt; element must be inserted immediately after the &lt;table&gt; element.

===HTML information===
Closing tags are required. CSS display is inline.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''caption''' element to provide a brief description for a table.
|Code=<nowiki>
<table>
 <caption>Characteristics with positive and negative sides</caption>
 <thead>
  <tr>
   <th> Characteristic
   <th> Negative
   <th> Positive
 <tbody>
  <tr>
   <th> Mood
   <td> Sad
   <td> Happy
  <tr>
   <th> Grade
   <td> Failing
   <td> Passing
</table>
</nowiki>
|LiveURL=http://code.webplatform.org/gist/7282268
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''caption''' element should be a child of the <nowiki><table> element.</nowiki>

A caption can introduce context for a table, making it significantly easier to understand.

When a table element is the only content in a figure element other than the '''figcaption''', the caption element should be omitted in favor of the [http://docs.webplatform.org/wiki/html/elements/figcaption figcaption].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5 - 4.9 Tabular Data
|URL=http://www.w3.org/TR/html5/tabular-data.html#the-caption-element
|Status=W3C Candidate Recommendation
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
|Topic_clusters=HTML, Text
|External_links=http://www.w3.org/wiki/HTML/Elements/caption
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}