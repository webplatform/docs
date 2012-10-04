{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code  example demonstrates how  you can include metadata  in an SVG document. This example uses the Dublin Core version 1.1 schema. (You can also use other XML-compatible metadata languages, including ones that are not based on RDF.)
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"yes"?&gt;
&lt;svg width{{=}}"4in" height{{=}}"3in" version{{=}}"1.1"
    xmlns {{=}} 'http://www.w3.org/2000/svg'&gt;
    &lt;desc xmlns:myfoo{{=}}"http://example.org/myfoo"&gt;
      &lt;myfoo:title&gt;This is a financial report&lt;/myfoo:title&gt;
      &lt;myfoo:descr&gt;The global description uses markup from the
        &lt;myfoo:emph&gt;myfoo&lt;/myfoo:emph&gt; namespace.&lt;/myfoo:descr&gt;
      &lt;myfoo:scene&gt;&lt;myfoo:what&gt;widget $growth&lt;/myfoo:what&gt;
      &lt;myfoo:contains&gt;$three $graph-bar&lt;/myfoo:contains&gt;
        &lt;myfoo:when&gt;1998 $through 2000&lt;/myfoo:when&gt; &lt;/myfoo:scene&gt;
   &lt;/desc&gt;
    &lt;metadata&gt;
      &lt;rdf:RDF
           xmlns:rdf {{=}} "http://www.w3.org/1999/02/22-rdf-syntax-ns#"
           xmlns:rdfs {{=}} "http://www.w3.org/2000/01/rdf-schema#"
           xmlns:dc {{=}} "http://purl.org/dc/elements/1.1/" &gt;
        &lt;rdf:Description about{{=}}"http://example.org/myfoo"
             dc:title{{=}}"MyFoo Financial Report"
             dc:description{{=}}"$three $bar $thousands $dollars $from 1998 $through 2000"
             dc:publisher{{=}}"Example Organization"
             dc:date{{=}}"2000-04-11"
             dc:format{{=}}"image/svg+xml"
             dc:language{{=}}"en" &gt;
          &lt;dc:creator&gt;
            &lt;rdf:Bag&gt;
              &lt;rdf:li&gt;Irving Bird&lt;/rdf:li&gt;
              &lt;rdf:li&gt;Mary Lambert&lt;/rdf:li&gt;
            &lt;/rdf:Bag&gt;
          &lt;/dc:creator&gt;
        &lt;/rdf:Description&gt;
      &lt;/rdf:RDF&gt;
    &lt;/metadata&gt;
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
You should specify metadata, which  you can  include with SVG content, within '''metadata''' elements. The contents of a '''metadata''' element should be children elements from other XML namespaces that are  expressed in a manner that conforms with the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203781 Namespaces in XML Recommendation].
You should provide a '''metadata''' child element  to the outermost [[svg/elements/svg|'''svg''']] element within a stand-alone SVG document. The '''metadata''' child element to an '''svg''' element  identifies  document-level metadata.
'''Note'''  We  recommend  that  you add at most one '''metadata''' element  as a child of any particular element, and that this element appear before any other child elements (except possibly [[svg/elements/desc|'''desc''']] or [[svg/elements/title|'''title''']] elements) or character data content.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204750 Scalable Vector Graphics: Metadata], Section 21.4.1


===Members===
The '''SVGMetadataElement''' object has these types of members:
*[#events Events]
*[#properties Properties]


====Events====
The '''SVGMetadataElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Properties====
The '''SVGMetadataElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/properties/viewportElement|'''viewportElement''']]
|Gets the element that established the current viewport.
|-
|[[svg/properties/xmlbase|'''xmlbase''']]
|Gets or sets the <code>base</code> attribute on the element.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}