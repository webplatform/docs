{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=needs example
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the namespace prefix associated with a URI, if any.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=namespaceURI
|Data type=String
|Description=The namespace URI.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=prefix
|Javascript_data_type=String
|Return_value_description=The namespace prefix associated with the URI, or null if none is found.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=&lt;html xmlns{{=}}"http://www.w3.org/1999/xhtml"  xmlns:svg{{=}}"http://www.w3.org/2000/svg"&gt;
   &lt;script type{{=}}"text/javascript">//<![CDATA[
    var nsxml {{=}} 'http://www.w3.org/1999/xhtml';
    var nssvg {{=}} 'http://www.w3.org/2000/svg';
    alert('root element nsprefix is ' + document.documentElement.lookupPrefix(nssvg));
   //]]>&lt;/script&gt;





}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.lookupPrefix Node.lookupPrefix]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975159(v=vs.85).aspx lookupPrefix Method]
|HTML5Rocks_link=
}}