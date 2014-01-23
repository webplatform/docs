{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a new document fragment (DocumentFragment) object.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=documentFragment
|Javascript_data_type=DOM Node
|Return_value_description=The created DocumentFragment instance.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=<nowiki>
var div, docFrag = document.createDocumentFragment(),  i = 0, thismany = 1000;

while ( i < thismany) {
    // Creates a new <div> element if one doesn't exist. Clones it if one does.
    (div === undefined) ? document.createElement('div') : div.cloneNode(false);

    // Appends div to the document fragment.
    docFrag.appendChild(div); 

    i++;
}

// Appends the fragment and child nodes to the document body.  Makes one DOM update instead of 1000
document.body.appendChild(docFrag);
</nowiki>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}