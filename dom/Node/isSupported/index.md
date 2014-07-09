{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Returns a value indicating whether or not the object supports a specific DOM standard.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=feature
|Data type=String
|Description=The name of the standard.
|Optional=No
}}{{Method Parameter
|Name=version
|Data type=String
|Description=The version number of the standard.  Supported values vary according to the standard.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=isSupported
|Javascript_data_type=Boolean
|Return_value_description=Whether the standard is supported.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=&lt;div id="divMain"&gt;
&lt;/div&gt;

&lt;script&gt;
 // check to see if its supports the DOM2 HTML Module.
 var main {{=}} document.getElementById('doc');
 var output {{=}} main.isSupported('HTML', '2.0');
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes=Gecko-specific notes

[1] Starting with Gecko 19.0 (Firefox 19.0 / Thunderbird 19.0 / SeaMonkey 2.16) this method will always return true (bug 801425) and starting with Gecko 22.0 (Firefox 22.0 / Thunderbird 22.0 / SeaMonkey 2.19) this method has been removed.

Deprecated
This feature has been removed from the Web. Though some browsers may still support it, it is in the process of being dropped. Do not use it in old or new projects. Pages or Web apps using it may break at any time.


}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=Living Standard
|URL=http://dom.spec.whatwg.org/#interface-node
|Status=Recommendation
|Relevant_changes=5.4 Interface Node
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=[http://www.w3.org/DOM/Test/ W3C DOM Conformance Tests]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.isSupported Node.isSupported]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975130(v=vs.85).aspx isSupported Method]
|HTML5Rocks_link=
}}