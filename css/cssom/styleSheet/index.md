{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''styleSheet''' object to change the cascading style sheets (CSS) values of inline and imported styles.
|LiveURL=
|Code=
&lt;STYLE&gt;
BODY {background-color: #CFCFCF;}
@import url("otherStyleSheet.css");
&lt;/STYLE&gt;
&lt;SCRIPT&gt;
window.onload{{=}}fnInit;
function fnInit(){
   // Access a rule in the styleSheet, change backgroundColor to blue.
   var oStyleSheet{{=}}document.styleSheets[0];
   var oRule{{=}}oStyleSheet.rules[0];
   oRule.style.backgroundColor{{=}}"#0000FF";
   // Add a rule for P elements to have yellow backgrounds.
   oStyleSheet.addRule("P","background-color: #FFFF00;");
   // Change and imported rule:
   oStyleSheet.imports[0].color{{=}}"#000000";
}
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can use this object to retrieve style sheet information, such as the URL of the source file for the style sheet and the element in the document that owns (defines) the style sheet. You can also use it to modify style sheets.
You can retrieve a '''styleSheet''' object from the [[css/cssom/styleSheets|'''styleSheets''']] collection or from the [[css/cssom/imports|'''imports''']] collection. Each item in these collections is a style sheet. A '''styleSheet''' object is available for a style sheet only if it is included in a document with a '''style''' or '''link''' element, or with an [[css/atrules/@import|'''@import''']] statement in a '''style''' element.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''styleSheet''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''styleSheet''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[css/cssom/styleSheet/addImport|'''addImport''']]
|Adds a style sheet to the [[css/cssom/imports|'''imports''']] collection for the specified style sheet.
|-
|[[css/cssom/methods/addPageRule|'''addPageRule''']]
|Not implemented. Creates a new [[css/cssom/page|'''page''']] object for a style sheet.
|-
|[[css/cssom/methods/addRule|'''addRule''']]
|Creates a new rule for a style sheet.
|-
|[[css/cssom/styleSheet/deleteRule|'''deleteRule''']]
|Deletes a rule from the style sheet.
|-
|[[dom/methods/fireEvent|'''fireEvent''']]
|Fires a specified event on the object.
|-
|[[css/cssom/styleSheet/insertRule|'''insertRule''']]
|Inserts a new rule into the style sheet.
|-
|[[css/cssom/methods/removeImport|'''removeImport''']]
|Removes the imported style sheet from the [[css/cssom/imports|'''imports''']] collection based on ordinal position.
|-
|[[css/cssom/methods/removeRule|'''removeRule''']]
|Deletes an existing style rule for the '''styleSheet''' object, and adjusts the index of the [[css/cssom/rules|'''rules''']] collection accordingly.
|}
 

====Properties====
The '''styleSheet''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[css/cssom/styleSheet/cssRules|'''cssRules''']]
|Retrieves  a list of all CSS rules contained within the parent object.
|-
|[[css/cssom/styleSheet/cssText|'''cssText''']]
|Sets or retrieves the persisted representation of the style rule.
|-
|[[html/attributes/disabled|'''disabled''']]
|Sets or retrieves a value that indicates whether the user can interact with the object.
|-
|[[css/cssom/properties/href|'''href''']]
|Sets or retrieves the URL of the linked style sheet.
|-
|[[html/attributes/id|'''id''']]
|Sets or retrieves the string identifying the object.
|-
|[[css/cssom/properties/isAlternate|'''isAlternate''']]
|Retrieves a value that indicates whether the '''IHTMLStyleSheet3''' object is an alternative  style sheet.
|-
|[[css/cssom/properties/isPrefAlternate|'''isPrefAlternate''']]
|Retrieves a value that indicates whether the '''IHTMLStyleSheet3''' object is the preferred style sheet.
|-
|[[css/cssom/properties/media|'''media''']]
|Sets or retrieves the media type.
|-
|[[css/cssom/styleSheet/ownerNode|'''ownerNode''']]
|Retrieves  the node that associates this style sheet with the document.
|-
|[[css/cssom/styleSheet/ownerRule|'''ownerRule''']]
|Retrieves  a value that indicates whether this style sheet comes from an [[css/atrules/@import|'''@import''']] rule or a link (an element or processing instruction).
|-
|[[css/cssom/styleSheet/owningElement|'''owningElement''']]
|Retrieves the next object in the HTML hierarchy.
|-
|[[css/cssom/styleSheet/parentStyleSheet|'''parentStyleSheet''']]
|Retrieves the style sheet that imported the current style sheets.
|-
|[[css/cssom/styleSheet/readOnly|'''readOnly''']]
|Retrieves whether the rule or style sheet is defined on the document or is imported.
|-
|[[css/properties/text-autospace|'''textAutospace''']]
|Sets or retrieves  the autospacing and narrow space width adjustment of text.
|-
|[[css/cssom/styleSheet/title|'''title''']]
|Sets or retrieves the title of the style sheet.
|-
|[[css/cssom/styleSheet/type|'''type''']]
|Retrieves the CSS language in which the style sheet is written.
|}
 

}}
{{See_Also_Section
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}