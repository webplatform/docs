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
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example returns a formatted listing of all 'data-' prefixed attributes of an element (el)
|Code=function GetDataAttributes(el) {
            var buf ={{'}}{{'}};
            try {
                for (var i = 0; i < el.attributes.length; i++) {
                	if (el.attributes[i].value !== 'null' && el.attributes[i].value.length > 0 && el.attributes[i].name.indexOf('data-')>-1) {
                        buf += '<b>' + el.attributes[i].name + '<\/b>=\"' + el.attributes[i].value + '\"&nbsp;<br/>';}
                }
            }
            catch (e) {}
            return buf;
        }
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