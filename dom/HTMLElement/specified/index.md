{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example uses the '''specified''' property to determine the attributes that are set for an object. The function checks each attribute and lists all of the attributes of the object and their values.
|Code=&lt;script&gt;
function fnFindSpecified(){
   var oAttributes{{=}}oList.attributes;
   alert(oAttributes(0).nodeName);
   for(var i{{=}}0;i&lt;oAttributes.length;i++){
      var oNode{{=}}document.createElement("LI");
      var oNodeValue{{=}}document.createTextNode(i + " "
                     + oAttributes(i).nodeName + " {{=}} "
                     + oAttributes(i).nodeValue);
      oList.appendChild(oNode);
      oNode.appendChild(oNodeValue);
      if(oAttributes(i).nodeValue!{{=}}null){
         alert(oAttributes(i).nodeName
         + " specified: " + oAttributes(i).specified);
      }
   }
}
&lt;/script&gt;
&lt;ul id{{=}}"oList" onclick{{=}} "fnFindSpecified()"&gt;
&lt;li&gt;Click to Find Specified Attributes&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
An attribute value is specified if it is assigned through HTML or script.
Windows Internet Explorer 9. When webpages are displayed in IE9 Standards mode, the [[dom/Node/attributes|'''attributes''']] collection does not contain attributes that are not specifically created (unlike previous Windows Internet Explorer versions). As a result, the '''specified''' property returns <code>true</code> for every item in the '''attributes''' collection.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 1.2
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}