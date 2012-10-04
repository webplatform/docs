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
|Description=This example shows how to display the titles of the style sheets in the document.
|LiveURL=
|Code=
for ( i {{=}} 0; i &lt; document.styleSheets.length; i++ )
{
    alert("Style sheet " + i + " is titled " + document.styleSheets(i).title);
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
Style sheets that are imported using the [[css/atrules/@import|'''@import''']] rule and are contained within the '''style''' object are available through the [[css/cssom/imports|'''imports''']] collection.
|Import_Notes=
===Members===
The '''styleSheets''' collection has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''styleSheets''' collection has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[css/cssom/properties/item|'''item''']]
|Retrieves an object from a collection.
|-
|'''urns'''
|Retrieves a collection of all objects to which a specified behavior is attached.
|}
 

====Properties====
The '''styleSheets''' collection has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/length|'''length''']]
|Sets or retrieves the number of objects in a collection.
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