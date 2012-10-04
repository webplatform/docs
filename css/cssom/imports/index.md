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
|Description=This example shows how to display the URL paths of the imported style sheets in the document.
|LiveURL=
|Code=
for ( i {{=}} 0; i &lt; document.styleSheets.length; i++ )
{
    if ( document.styleSheets(i).owningElement.tagName {{=}}{{=}} "STYLE" )
    {
        for ( j {{=}} 0; j &lt; document.styleSheets(i).imports.length; j++ )
            alert("Imported style sheet " + j + " is at " +
                   document.styleSheets(i).imports(j).href);
    }
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
An imported style sheet is one that is brought into the document using the cascading style sheets (CSS) [[css/atrules/@import|'''@import''']] rule.
|Import_Notes=
===Members===
The '''imports''' collection has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''imports''' collection has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[css/cssom/properties/item|'''item''']]
|Retrieves an object from a collection.
|}
 

====Properties====
The '''imports''' collection has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[css/cssom/properties/length|'''length''']]
|Retrieves  the number of properties that  are  explicitly set on the parent object.
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