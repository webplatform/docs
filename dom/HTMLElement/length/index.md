{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''window'''.'''length''' property returns the number of frames contained in a window.
The '''comment'''.'''length''' property returns the number of characters in the object.
Although this property is read-only for most of the objects listed in the Applies To section,

it is read/write for the [[dom/properties/areas|'''areas''']] collection (image maps), the [[dom/properties/options|'''options''']] collection (select boxes), and the '''select''' object. In all other cases, this property has read-only permission, which means you can retrieve, but cannot change, its current value.
The '''length''' property does not count '''input type{{=}}image''' elements. To access all elements contained in a form, call '''IHTMLFormElement''' and request an '''IHTMLElement''' interface. Use the [[dom/properties/children (document)+B416|'''children''']] property of the '''IHTMLElement''' interface to retrieve a collection of all elements in the form.
The '''form'''.'''length''' property does not count '''input type{{=}}image''' elements. To access all elements contained in a form, use the [[dom/properties/children (document)+B416|'''children''']] collection.
This property is read-write on the areas collection for image maps and the options collection for select boxes. This allows a developer to shrink the collection.
For Windows CE only, this collection will always be empty.
As of Windows Internet Explorer 8, this property is read-only in the [[dom/properties/areas|'''areas''']] collection.
In Microsoft Internet Explorer 6 and later, this property applies to the '''comment''' object.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/all|all]]</code>
*<code>[[dom/properties/anchors|anchors]]</code>
*<code>[[dom/properties/applet|applets]]</code>
*<code>[[dom/properties/areas|areas]]</code>
*<code>[[dom/properties/attribute|attributes]]</code>
*<code>behaviorUrns</code>
*<code>bookmarks</code>
*<code>[[dom/properties/boundElements|boundElements]]</code>
*<code>[[dom/properties/cellSpacing|cells]]</code>
*<code>[[dom/properties/childNodes|childNodes]]</code>
*<code>[[dom/properties/children (document)+B416|children]]</code>
*<code>comment</code>
*<code>[[dom/properties/controlRange|controlRange]]</code>
*<code>[[dom/properties/elements|elements]]</code>
*<code>[[dom/properties/embeds|embeds]]</code>
*<code>filters</code>
*<code>[[dom/properties/forms|forms]]</code>
*<code>[[dom/properties/frames|frames]]</code>
*<code>[[dom/properties/image|images]]</code>
*<code>[[css/cssom/imports|imports]]</code>
*<code>[[dom/properties/links|links]]</code>
*<code>namespaces</code>
*<code>[[dom/properties/options|options]]</code>
*<code>[[css/cssom/pages|pages]]</code>
*<code>plugins</code>
*<code>[[dom/properties/rows (table)|rows]]</code>
*<code>[[css/cssom/rules|rules]]</code>
*<code>[[dom/properties/scripts|scripts]]</code>
*<code>select</code>
*<code>[[css/cssom/styleSheets|styleSheets]]</code>
*<code>[[dom/properties/tBodies|tBodies]]</code>
*<code>[[dom/TextRectangle|TextRectangle]]</code>
*<code>[[dom/traversal/properties/TextRange|TextRange]]</code>
*<code>window</code>
*<code>form</code>
*<code>[[dom/documentCompatibleInfoCollection|documentCompatibleInfoCollection]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}