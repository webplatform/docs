{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A collection of nodes that can be accessed by name. Objects contained in a '''NamedNodeMap''' may also be accessed by an ordinal index, but this is simply to allow convenient enumeration of the contents of a '''NamedNodeMap''', and does not imply that the DOM specifies an order to these nodes.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''attribute''' object to create a list of attributes that are [[dom/HTMLElement/specified|'''specified''']].
|Code=&lt;script type{{=}}"text/javascript"&gt;
function fnFind(){
   for(var i{{=}}0;i&lt;oList.attributes.length;i++){
      if(oList.attributes[i].specified){
         alert(oList.attributes[i].nodeName + ' {{=}} '
          + oList.attributes[i].nodeValue);
      }
   }
}
&lt;/script&gt;
&lt;ul onclick{{=}}"fnFind()"&gt;
&lt;li ID {{=}} "oList" ACCESSKEY {{=}} "L"&gt;List Item 1&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''attribute''' object is accessible through the [[dom/Node/attributes|'''attributes''']] collection.
A valid attribute or property can be any Dynamic HTML (DHTML) property or event that applies to the object.
When displaying a Web page in IE8 Standards mode, Windows Internet Explorer distinguishes between attribute values specified by the original page author and the representation of those values in the DOM. For more information, see Attribute Differences in Internet Explorer 8.
This object is available in script as of Microsoft Internet Explorer 5.
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}