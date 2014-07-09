{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Indicates whether or not a namespace is the default namespace for a document.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=namespace
|Data type=String
|Description=The namespace to be compared to the default namespace.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=isDefault
|Javascript_data_type=Boolean
|Return_value_description=Whether the namespace specified in the ''namespace'' parameter is the default namespace for the document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example compares the default Namespace of the body element to the SVG namespace and then to the xHTML namespace. 
false then true is displayed.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;

&lt;head&gt;
&lt;meta content{{=}}"text/html; charset=utf-8" http-equiv{{=}}"Content-Type"&gt;
&lt;title&gt;isDefaultNamespace example&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;


   &lt;script type{{=}}"text/javascript"&gt;//&lt;![CDATA[
   	var nsSVG{{=}}'http://www.w3.org/2000/svg';
	alert(document.body.isDefaultNamespace(nsSVG));
	var nsxHTML{{=}}'http://www.w3.org/1999/xhtml';
	alert(document.body.isDefaultNamespace(nsxHTML));
   //]]&gt;&lt;/script&gt;
&lt;/body&gt;

&lt;/html&gt;

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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.isDefaultNamespace Node.isDefaultNamespace]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975127(v=vs.85).aspx isDefaultNamespace Method]
|HTML5Rocks_link=
}}