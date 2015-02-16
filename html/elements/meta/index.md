{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add example, compatibility, and the description/notes section is not enough.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Conveys hidden information about the document to the server and the client.}}
{{Markup_Element
|DOM_interface=dom/HTMLMetaElement
|Content=Internationalization topics related to the <code>meta</code> element:
* [http://www.w3.org/International/techniques/authoring-html#indoc Declaring the character encoding for HTML]
* [http://www.w3.org/International/techniques/authoring-html#choosing Choosing and applying a character encoding]
* [http://www.w3.org/International/techniques/authoring-html#changing Changing to UTF-8]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example disables theming support for the document.
|Code=&lt;META HTTP-EQUIV{{=}}"MSTHEMECOMPATIBLE" CONTENT{{=}}"no"&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''META''' element also embeds document information that some search engines use to index and categorize documents on the World Wide Web.
This element can be used only within the '''HEAD''' element.
Windows Internet Explorer 8 or later. The behavior of the [[dom/methods/setAttribute|'''setAttribute''']] method depends on the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 7.4.4
*[http://www.w3.org/TR/html5/document-metadata.html#the-meta-element HTML5 Specification]


===HTML information===
{| class="wikitable"
|-
!Closing Tag
|forbidden
|-
!CSS Display
|
|}

===Members===
The '''meta''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''meta''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[dom/events/abort|'''onabort''']]
|Fires when the user aborts the download.
|-
|[[dom/events/change|'''onchange''']]
|Fires when the contents of the object or selection have changed.
|-
|[[dom/events/error|'''onerror''']]
|Fires when an error occurs during object loading.
|-
|[[dom/events/input|'''oninput''']]
|Occurs when the text content of an element is changed through the user interface.
|-
|[[dom/events/load|'''onload''']]
|Fires immediately after the client loads the object.
|-
|[[dom/events/reset|'''onreset''']]
|Fires when the user resets a form.
|-
|[[dom/events/selectstart|'''onselect''']]
|Fires when the current selection changes.
|}
 

====Methods====
The '''meta''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/dragDrop|'''dragDrop''']]
|Initiates a drag event.
|-
|[[dom/methods/getAttribute|'''getAttribute''']]
|Retrieves the value of the specified attribute.
|-
|[[dom/methods/getAttributeNodeNS|'''getAttributeNodeNS''']]
|Gets an [[dom/attributes|'''attribute''']] object that matches the specified namespace and name.
|-
|[[dom/methods/getAttributeNS|'''getAttributeNS''']]
|Gets the value of the specified attribute within the specified namespace.
|-
|[[dom/methods/getElementsByClassName|'''getElementsByClassName''']]
|Gets a collection of objects that are based on the value of the [[dom/properties/className|'''CLASS''']] attribute.
|-
|[[dom/methods/getElementsByTagNameNS|'''getElementsByTagNameNS''']]
|Gets a collection of objects that are based on the specified element names within a specified namespace.
|-
|[[dom/methods/hasAttributeNS|'''hasAttributeNS''']]
|Determines whether an attribute that has the specified namespace and name exists.
|-
|[[dom/methods/matchesSelector|'''msMatchesSelector''']]
|Determines whether an object matches the specified selector.
|-
|[[dom/methods/removeAttribute|'''removeAttribute''']]
|Removes an attribute from an object.
|-
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|[[dom/methods/setAttribute|'''setAttribute''']]
|Sets the value of the specified attribute.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|}
 

====Properties====
The '''meta''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/charset|'''charset''']]
|Sets or retrieves the character set used to encode the object.
|-
|[[dom/properties/clientHeight|'''clientHeight''']]
|Retrieves the height of the object including padding, but not including margin, border, or scroll bar.
|-
|[[dom/properties/clientLeft|'''clientLeft''']]
|Retrieves the distance between the [[dom/properties/offsetLeft|'''offsetLeft''']] property and the true left side of the client area.
|-
|[[dom/properties/clientTop|'''clientTop''']]
|Retrieves the distance between the [[dom/properties/offsetTop|'''offsetTop''']] property and the true top of the client area.
|-
|[[dom/properties/clientWidth|'''clientWidth''']]
|Retrieves the width of the object including padding, but not including margin, border, or scroll bar.
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|'''content'''
|Gets or sets meta-information to associate with [[html/attributes/httpEquiv|'''httpEquiv''']] or [[html/attributes/name (meta object)|'''name''']].
|-
|[[html/attributes/httpEquiv|'''httpEquiv''']]
|Gets or sets information used to bind the value of a '''content''' attribute of a '''meta''' element to an HTTP response header.
|-
|[[html/attributes/name (meta object)|'''name''']]
|Sets or retrieves the value specified in the '''CONTENT''' attribute of the '''meta''' object.
|-
|[[html/attributes/scheme|'''scheme''']]
|Sets or retrieves  a scheme to be used in interpreting the value of a property specified for the object.
|-
|[[dom/properties/scrollHeight|'''scrollHeight''']]
|Retrieves the scrolling height of the object.
|-
|[[dom/properties/scrollLeft|'''scrollLeft''']]
|Sets or retrieves the distance between the left edge of the object and the leftmost portion of the content currently visible in the window.
|-
|[[dom/properties/scrollTop|'''scrollTop''']]
|Sets or retrieves the distance between the top of the object and the topmost portion of the content currently visible in the window.
|-
|[[dom/properties/scrollWidth|'''scrollWidth''']]
|Retrieves the scrolling width of the object.
|-
|[[html/attributes/url|'''url''']]
|Sets or retrieves the [[dom/properties/URL|'''URL''']] property that will be loaded after the specified time has elapsed.
|}
 
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/document-metadata.html#the-meta-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/document-metadata.html#the-meta-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-META
|Status=W3C Recommendation
|Relevant_changes=
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
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>content</code>
*<code>[[html/attributes/httpEquiv|httpEquiv]]</code>
*<code>Conceptual</code>
*<code>Defining Document Compatibility</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}