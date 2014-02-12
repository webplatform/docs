{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to iterate through the collection of attributes of the specified object, displaying the name and value of the attributes as well as the language of the attribute (HTML or script).
|Code=&lt;SCRIPT&gt;
function ShowAttribs(oElem)
{
    txtAttribs.innerHTML {{=}} '';
    // Retrieve the collection of attributes for the specified object.
    var oAttribs {{=}} oElem.attributes;
    // Iterate through the collection.
    for (var i {{=}} 0; i &lt; oAttribs.length; i++)
    {
        var oAttrib {{=}} oAttribs[i];
        // Print the name and value of the attribute. 
        // Additionally print whether or not the attribute was specified
        // in HTML or script.
        txtAttribs.innerHTML +{{=}} oAttrib.nodeName + '{{=}}' + 
            oAttrib.nodeValue + ' (' + oAttrib.specified + ')&lt;BR&gt;'; 
    }
}
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''attributes''' collection does not expose the [[css/cssom/style|'''style''']] object. Use the [[css/cssom/styleSheet/cssText|'''cssText''']] property of the object's '''style''' property to retrieve the persistent representation of the cascading styles associated with an object.
Unlike other DHTML collections, such as [[dom/Element/children|'''children''']], the '''attributes''' collection is static. Modifications to the properties of an object are not automatically reflected by an existing reference to the '''attributes''' collection of that object.

|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}