{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''caption''' (&lt;caption&gt;) element represents the title of the table that is its parent.}}
{{Markup_Element
|DOM_interface=dom/HTMLTableCaptionElement
|Content=The '''caption''' element (&lt;caption&gt;) specifies a brief description for a table.
The &lt;caption&gt; element must be inserted immediately after the (&lt;table&gt;) element.
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
The '''caption''' element should be a child of the <nowiki><table> element.
The <table> object and its associated elements have a separate table object model, which uses different methods than the general object model.  For more information about the table object model, see Building Tables Dynamically.</nowiki>

The '''caption-side''' property is the preferred way to position a table caption.

===HTML information===
{| class="wikitable"
|-
!Closing Tag
|required
|-
!CSS Display
|inline
|-
!Element Type
|$disp element
|-}
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
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}