{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Adds an attribute to an element by using an attributes collection.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=ppNode
|Data type=any
|Description='''attribute'''
|Optional=No
}}
|Method_applies_to=dom/NamedNodeMap
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMAttribute'''

'''attribute'''

attribute
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to add an attribute to an element using the '''setNamedItem''' method.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;title&gt;setNamedItem example&lt;/title&gt;
&lt;script&gt;
function fnSetNamedItem(){
var nnm {{=}} myDIV.attributes;
var namedItem {{=}} document.createAttribute("title");
namedItem.value {{=}} "This is a ToolTip";
nnm.setNamedItem(namedItem);
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"fnSetNamedItem();"&gt;
&lt;div id{{=}}"myDIV"&gt;This DIV now has a ToolTip.&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setNamedItemEx1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
An [[dom/HTMLElement|'''attribute''']] that is set with this method does not have to apply to the element.
If an '''attribute''' with the same name is already present, it is replaced by the new '''attribute'''.
'''setNamedItem''' was introduced in Microsoft Internet Explorer 6.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap NamedNodeMap]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536751(v=vs.85).aspx setNamedItem Method]
|HTML5Rocks_link=
}}