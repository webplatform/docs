{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example shows the relationship between the '''target''' and [[dom/properties/data|'''data''']] properties of a processing instruction object.
|LiveURL=
|Code=
&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
  "http://www.w3.org/TR/html4/strict.dtd"&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;IE9 DOMProcessingInstruction Sample&lt;/title&gt;
  &lt;meta name{{=}}"x-ua-compatible" content{{=}}"ie{{=}}9"&gt;
  &lt;script type{{=}}"text/javascript"&gt;
  function showInfo() {
    try {
      var oImp {{=}} document.implementation;
      var oDoc {{=}} oImp.createDocument( "", "", null );  // works
      var sTarget {{=}} "xml-stylesheet";
      var sData {{=}} "type{{=}}'text/css' href{{=}}'style.css'";
      var oPI {{=}} oDoc.createProcessingInstruction( sTarget, sData );
      alert( oPI );
    } catch( oErr ) {
        var sError {{=}} "Error " + oErr.code + ": " + oErr.message;
        alert( sError );
    };
  }
  &lt;/script&gt;
  &lt;/head&gt;
  &lt;body&gt;
  &lt;button onclick{{=}}"showInfo();"&gt;Click Me!&lt;/button&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Processing instructions are  supported only  by XML documents.
A processing instruction provides direction to an XML parser. The following  code example shows a processing instruction  that is specified in markup.
 <code>&lt;?xml-stylesheet type{{=}}"text/css" href{{=}}"style.css"?&gt;</code>
For  this example, the '''target''' property would return <code>xml-stylesheet</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182703 Document Object Model (DOM) Level 2 Core Specification], Section 1.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/processingInstruction|ProcessingInstruction]]</code>
*<code>Reference</code>
*<code>[[dom/methods/createProcessingInstruction|createProcessingInstruction]]</code>
*<code>[[dom/properties/data|data]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}