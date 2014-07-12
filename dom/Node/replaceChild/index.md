{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Replaces an existing child node with a new child node.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=newChild
|Data type=DOM Node
|Description=The new node to be inserted into the document.
|Optional=No
}}{{Method Parameter
|Name=oldChild
|Data type=DOM Node
|Description=The existing node to be replaced.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=replacedNode
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMNode'''

Returns a reference to the object that is replaced.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''replaceChild''' method to replace a bold element from a '''div''' with an italic element.
|Code=&lt;!doctype html&gt;
&lt;head&gt;
&lt;script&gt;
function replaceElement()
{
var Div1 = document.getElementById("Div1");
        //The first child of the div is the bold element.   
    var oChild{{=}}Div1.children(0);	
    var sInnerHTML {{=}} oChild.innerHTML;
    if (oChild.tagName{{=}}{{=}}"B")
    {
        oNewChild{{=}}document.createElement("I");
        Div1.replaceChild(oNewChild, oChild);
        oNewChild.innerHTML{{=}}sInnerHTML
    }
    else
    {
        oNewChild{{=}}document.createElement("B");
        Div1.replaceChild(oNewChild, oChild);
        oNewChild.innerHTML{{=}}sInnerHTML		
    }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div id{{=}}"Div1" onclick{{=}}"replaceElement()"&gt;
Click anywhere in this sentence to toggle this &lt;strong&gt;word&lt;/strong&gt;
between bold and italic.&lt;/div&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section
|Notes=The node to be replaced must be an immediate child of the parent object. The new node must be created using the [[dom/Document/createElement|'''createElement''']] method.
This property is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.
}}
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=Exceptions are supported.
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.replaceChild Node.replaceChild]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536716(v=vs.85).aspx replaceChild Method]
|HTML5Rocks_link=
}}