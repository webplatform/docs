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
|Description=This example uses a '''rule''' object consisting of the selector '''H1''' to define a single rule that changes the H1 headings in a document to red.
|LiveURL=
|Code=
&lt;STYLE&gt;
    H1 { color: red }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=If the style sheet containing the preceding rule is the first style sheet in the document, the following code returns the '''rule''' object associated with the rule.
|LiveURL=
|Code=
oRule{{=}}document.styleSheets(0).rules(0)
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''rule''' object defines a set of Cascading Style Sheets (CSS) attributes applied to a set of HTML elements. For example, a rule consisting of the selector '''H1''' and the declaration [[css/properties/font-family|'''font-family''']]:Arial defines all '''H1''' elements to render in the Arial font.
This object is available in script as of Microsoft Internet Explorer 5.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''rule''' object has these types of members:
*[#properties Properties]


====Properties====
The '''rule''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/constructor|'''constructor''']]
|Returns a reference to the constructor of an object.
|-
|[[css/cssom/styleSheet/cssText|'''cssText''']]
|Sets or retrieves the persisted representation of the style rule.
|-
|[[css/cssom/CSSRule/parentRule|'''parentRule''']]
|Retrieves the containing rule, if the current rule is contained inside another rule.
|-
|[[css/cssom/CSSRule/parentStyleSheet|'''parentStyleSheet''']]
|Retrieves the style sheet that contains the current rule.
|-
|[[css/cssom/styleSheet/readOnly|'''readOnly''']]
|Retrieves whether the rule or style sheet is defined on the document or is imported.
|-
|[[css/cssom/rule/selectorText|'''selectorText''']]
|Retrieves a string that identifies which elements the corresponding style sheet rule applies to.
|-
|[[css/cssom/CSSRule/type|'''type''']]
|Retrieves the type of the rule.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/rules|rules]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}