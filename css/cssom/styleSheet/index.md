{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A style sheet in the document.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''styleSheet''' object to change the cascading style sheets (CSS) values of inline and imported styles.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;&lt;/title&gt;
  &lt;style&gt;
BODY {background-color: #CFCFCF;}
@import url("otherStyleSheet.css");
  &lt;/style&gt;
  &lt;script&gt;
window.onload{{=}}fnInit;
function fnInit() {
   // Access a rule in the styleSheet, change backgroundColor to blue.
   var stylesheet {{=}} document.styleSheets[0];
   var rule {{=}} stylesheet.rules[0];
   rule.style.backgroundColor {{=}} "#0000FF";
   // Add a rule for P elements to have yellow backgrounds.
   stylesheet.addRule("P", "background-color: #FFFF00;");
   // Change and imported rule:
   stylesheet.imports[0].color {{=}} "#000000";
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=You can use this object to retrieve style sheet information, such as the URL of the source file for the style sheet and the element in the document that owns (defines) the style sheet. You can also use it to modify style sheets.
You can retrieve a '''styleSheet''' object from the [[css/cssom/styleSheets|'''styleSheets''']] collection or from the [[css/cssom/imports|'''imports''']] collection. Each item in these collections is a style sheet. A '''styleSheet''' object is available for a style sheet only if it is included in a document with a '''style''' or '''link''' element, or with an [[css/atrules/@import|'''@import''']] statement in a '''style''' element.
|Import_Notes=====Non Standard Methods====
The '''styleSheet''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[css/cssom/methods/addRule|'''addRule''']]
{{!}}Non standard. Creates a new rule for a style sheet.
{{!}}-
{{!}}[[dom/methods/fireEvent|'''fireEvent''']]
{{!}}Fires a specified event on the object.
{{!}}}
 

====Non Standard Properties====
The '''styleSheet''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[html/attributes/disabled|'''disabled''']]
{{!}}Sets or retrieves a value that indicates whether the user can interact with the object.
{{!}}-
{{!}}[[css/cssom/properties/href|'''href''']]
{{!}}Sets or retrieves the URL of the linked style sheet.
{{!}}-
{{!}}[[html/attributes/id|'''id''']]
{{!}}Sets or retrieves the string identifying the object.
{{!}}-
{{!}}[[css/cssom/properties/isAlternate|'''isAlternate''']]
{{!}}Retrieves a value that indicates whether the styleSheet object is an alternative  style sheet.
{{!}}-
{{!}}[[css/cssom/properties/isPrefAlternate|'''isPrefAlternate''']]
{{!}}Retrieves a value that indicates whether the style sheet is the preferred style sheet.
{{!}}-
{{!}}[[css/cssom/properties/media|'''media''']]
{{!}}Sets or retrieves the media type.
{{!}}-
{{!}}[[css/cssom/styleSheet/ownerNode|'''ownerNode''']]
{{!}}Retrieves the node that associates this style sheet with the document.
{{!}}-
{{!}}[[css/cssom/styleSheet/parentStyleSheet|'''parentStyleSheet''']]
{{!}}Retrieves the style sheet that imported the current style sheets.
{{!}}-
{{!}}[[css/properties/text-autospace|'''textAutospace''']]
{{!}}Sets or retrieves  the autospacing and narrow space width adjustment of text.
{{!}}-
{{!}}[[css/cssom/styleSheet/title|'''title''']]
{{!}}Sets or retrieves the title of the style sheet.
{{!}}-
{{!}}[[css/cssom/styleSheet/type|'''type''']]
{{!}}Retrieves the CSS language in which the style sheet is written.
{{!}}}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}