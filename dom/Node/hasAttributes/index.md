{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Incorrect MSDN link removed.
Neither MSDN nor MDN document hasAttributes
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns whether this node (if it is an element) has any attributes}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Node
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=Boolean
|Return_value_description=true if this node has any attributes, false otherwise.
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example will display an alert message that "the root element has attributes'
|Code=&lt;!DOCTYPE html&gt;
&lt;html id{{=}}"root" class{{=}}"desktop"&gt;

&lt;head&gt;
&lt;meta content{{=}}"text/html; charset=utf-8" http-equiv{{=}}"Content-Type"&gt;
&lt;title&gt;hasAttributesExample&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;script type{{=}}"text/javascript"&gt;
var re{{=}}document.getElementById('root');
if(re.hasAttributes()){alert('the root element has attributes');}
var be{{=}}document.body;
if(be.hasAttributes()){alert('the body element has attributes');}
&lt;/script&gt;
&lt;/body&gt;

</html>

}}
}}
{{Notes_Section
|Notes====Remarks===
The '''hasAttributes''' method determines whether the object has any attributes at all. The [[dom/Element/hasAttribute|'''hasAttribute''']] method tests for the existence of a specified attribute.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Core
|URL=http://www.w3.org/TR/DOM-Level-2-Core/core.html
|Status=Recommendation
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}