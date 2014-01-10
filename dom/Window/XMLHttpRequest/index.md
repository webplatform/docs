{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=Yes
|Example_object_name=window
|Return_value_name=xhr
|Javascript_data_type=DOM Node
|Return_value_description=An XMLHttpRequest instance object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script demonstrates how to create and use the '''XMLHttpRequest''' object:
|Code=if (window.XMLHttpRequest)
{
  var xhr {{=}} new XMLHttpRequest();
  xhr.open("GET", "http://localhost/test.xml", true);
  xhr.onreadystatechange =
    function () {
      if (xhr.readyState === 4) {
        console.log(xhr.statusText);
     }
    };
   xhr.send();
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=XMLHttpRequest
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=Working Draft
|Relevant_changes=Section 3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=8
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5.5 - 6
|Note=Using the XMLHttp ActiveX object, you could emulate the XMLHttpRequest.
}}
}}
{{See_Also_Section
|Topic_clusters=XHR
|Manual_sections====Related pages (MSDN)===
*[[dom/window]]
*<code>create</code>
}}
{{Topics|DOM, XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}