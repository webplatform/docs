{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Associatve array containing the attributes of node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Return_value_description=NamedNodeMap that allows to access attributes through their names.
}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Language=JavaScript
|Description=This example enumerates the attributes of the body element.
|Code=var el=document.body;
var buf='';
for(var i=0;i<el.attributes.length;i++)
{
buf+=el.attributes[i].name + '\n';
}
alert(buf);
}}
}}
{{Notes_Section
|Usage=Retrieve a listing of ALL Nodes of an element, including developer defined attributes and data- prefixed attributes.

The depreciated presentational attributes are
datafld, datasrc, marginwidth, marginheight, allowtransparency, vspace, hspace, height, width, align, valign, alink, link, vlink, background, bgcolor, color, fgcolor, border, cellpadding, cellspacing, clear, frameborder, nowrap, scrolling
|Notes=For backwards compatibility first test if an attribute Node is null.
Binary attributes may or may not have a value
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 3 Core Specification
|URL=http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-84CF096
|Status=W3C Recommendation
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.attributes Node.attributes]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms537438(v=vs.85).aspx attributes Collection]
|HTML5Rocks_link=
}}