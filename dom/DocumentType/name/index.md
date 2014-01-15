{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/DocumentType
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows the '''name''' property with respect to a [[html/elements/!DOCTYPE|!DOCTYPE]] directive.
|Code=&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
  "http://www.w3.org/TR/html4/strict.dtd"&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;IE9 Doctype Sample: Name&lt;/title&gt;
  &lt;meta name{{=}}"x-ua-compatible" content{{=}}"ie{{=}}9"&gt;
  &lt;script type{{=}}"text/javascript"&gt;
  function showInfo() {
    var s {{=}} document.doctype.name;
    // Displays "HTML"
    alert( s );
  }
  &lt;/script&gt;
  &lt;/head&gt;
  &lt;body&gt;
  &lt;button onclick{{=}}"showInfo();"&gt;Click Me!&lt;/button&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The value of the '''name''' property corresponds to the ''TopElement'' attribute of a [[html/elements/!DOCTYPE|!DOCTYPE]] directive.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.5
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
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/DocumentType|DocumentType]]</code>
*<code>[[dom/DocumentType/publicId|publicId]]</code>
*<code>[[dom/DocumentType/systemId|systemId]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}