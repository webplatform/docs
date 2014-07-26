{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the number of characters in a text node.}}
{{API_Object_Property
|Property_applies_to=dom/CharacterData
|Read_only=Yes
|Example_object_name=textualNode
|Return_value_name=textLength
|Javascript_data_type=Number
|Return_value_description=The number of characters in the node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//create text node
var phrase = document.createTextNode ("A flawed plan today is better than a perfect plan tomorrow.");
//report length
alert(phrase.length);
}}{{Single Example
|Language=HTML
|Description=This example uses the '''length''' property to specify where a [[dom/Text|'''Text''']] node is split by using the [[dom/Text/splitText|'''splitText''']] method.
|Code=&lt;script&gt;
function fnChangeValue(){
   var oListItem {{=}} document.createElement("LI");
   var oList = document.getElementById("oList");
   oList.appendChild(oListItem);
   var oNode {{=}} oList.firstChild.childNodes(0);
   var oTextNode {{=}} oList.firstChild.childNodes(0);
   var oSplit {{=}} oTextNode.splitText(oTextNode.length/2);
   oListItem.appendChild(oSplit);
}
&lt;/script&gt;
&lt;ul id{{=}}"oList" onclick{{=}}"fnChangeValue()"&gt;
&lt;li&gt;Start Here&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}