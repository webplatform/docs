{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
|High-level issues=Stub
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Just like [[dom/Document/getElementsByTagNameNS|document.getElementsByTagNameNS]] except that it only works within the scope of this ShadowRoot's shadow tree.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=pvarNS
|Data type=VARIANT
|Description=The namespace URI that defines the desired elements or an asterisk (*) to match all namespaces with the document.
|Optional=No
}}{{Method Parameter
|Name=bstrLocalName
|Data type=BSTR
|Description=The name of the desired element or an asterisk (*) to match all elements with the specified namespace.
|Optional=No
}}
|Method_applies_to=dom/shadowdom/ShadowRoot
|Javascript_data_type=DOM Node
|Return_value_description=An IHTMLElementCollection of elements within the namespace.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
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
{{Topics|DOM, Shadow DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}