{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This element defines parameters for plugins invoked by object elements. }}
{{Markup_Element
|DOM_interface=dom/HTMLParamElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example displays the Internet Explorer Data Binding component's [[dom/properties/outerdom/outerHTML|'''outerHTML''']] so you can view the properties assigned by the '''PARAM''' elements.  You can perform this check to gather information when debugging an '''OBJECT''' element's properties.  You cannot edit the object's '''outerHTML''' property without reintializing the '''outerHTML''' object.
|Code=// The OBJECT CLASSID below is for the 
// Microsoft Internet Explorer Data Binding component
// Use just the following HTML and press the button
&lt;OBJECT                 
 ID{{=}}tdcContents
 CLASSID{{=}}"clsid:333C7BC4-460F-11D0-BC04-0080C7055A83"&gt;
  &lt;PARAM NAME{{=}}"DataURL" VALUE{{=}}"DataBinding.csv"&gt;								  
&lt;/OBJECT&gt;
&lt;BUTTON onclick{{=}}"oTxt.value{{=}}tdcContents.outerHTML"&gt;
Show Object outerHTML&lt;/BUTTON&gt;&lt;BR/&gt;
&lt;TEXTAREA ID{{=}}"oTxt"  STYLE{{=}}"height:400; width:450;padding:3; overflow{{=}}auto;"&gt; &lt;/TEXTAREA&gt;
//When the button is pressed the complete list of the object's
// PARAM elements display unformatted in the TEXTAREA as follows:
 
&lt;OBJECT id{{=}}tdcContents classid{{=}}clsid:333C7BC4-460F-11D0-BC04-0080C7055A83&gt;
&lt;PARAM NAME{{=}}"RowDelim" VALUE{{=}}"&amp;#10;"&gt;&lt;PARAM NAME{{=}}"FieldDelim" VALUE{{=}}","&gt;
&lt;PARAM NAME{{=}}"TextQualifier" VALUE{{=}}'"'&gt;&lt;PARAM NAME{{=}}"EscapeChar" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"UseHeader" VALUE{{=}}"0"&gt;&lt;PARAM NAME{{=}}"SortAscending" VALUE{{=}}"-1"&gt;
&lt;PARAM NAME{{=}}"SortColumn" VALUE{{=}}""&gt;&lt;PARAM NAME{{=}}"FilterValue" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"FilterCriterion" VALUE{{=}}"??"&gt;&lt;PARAM NAME{{=}}"FilterColumn" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"CharSet" VALUE{{=}}""&gt;&lt;PARAM NAME{{=}}"Language" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"CaseSensitive" VALUE{{=}}"-1"&gt;&lt;PARAM NAME{{=}}"Sort" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"Filter" VALUE{{=}}""&gt;&lt;PARAM NAME{{=}}"AppendData" VALUE{{=}}"0"&gt;
&lt;PARAM NAME{{=}}"DataURL" VALUE{{=}}"DataBinding.csv"&gt;
&lt;PARAM NAME{{=}}"ReadyState" VALUE{{=}}"4"&gt;
&lt;/OBJECT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''PARAM''' element is valid within the '''APPLET''', '''EMBED''', and '''OBJECT''' elements.
'''Note'''  Properties set by a '''PARAM''' element cannot be altered by changing the '''PARAM''' object.
After the '''APPLET''', '''EMBED''', or '''OBJECT''' element is instantiated, the property set by the '''PARAM''' element cannot be changed with the '''param''' object.  To change the object's properties, use the script properties exposed by the object.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 13.3.2


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
The '''param''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''param''' object has these events.
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
The '''param''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
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
|[[dom/methods/removeAttributeNS|'''removeAttributeNS''']]
|Removes the specified attribute from the object.
|-
|[[dom/methods/setAttributeNodeNS|'''setAttributeNodeNS''']]
|Sets an [[dom/attributes|'''attribute''']] object as part of the object.
|-
|[[dom/methods/setAttributeNS|'''setAttributeNS''']]
|Sets the value of the specified attribute within the specified namespace.
|}
 

====Properties====
The '''param''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[html/attributes/dataFld|'''dataFld''']]
|Sets or retrieves a field of a given data source, as specified by the [[html/attributes/dataSrc|'''dataSrc''']] property, to bind to the specified object.
|-
|[[html/attributes/name param element)|'''name''']]
|Sets or retrieves the name of an input parameter for an element.
|-
|[[html/attributes/type  (param element)|'''type''']]
|Sets or retrieves the content type of the resource designated by the [[html/attributes/value (param element)|'''value''']] attribute.
|-
|[[html/attributes/value (param element)|'''value''']]
|Sets or retrieves the value of an input parameter for an element.
|-
|[[html/attributes/valueType|'''valueType''']]
|Sets or retrieves the data type of the [[html/attributes/value (param element)|'''value''']] attribute.
|}
 
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
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}