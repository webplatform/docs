{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example uses the '''specified''' property to determine the attributes that are set for an object. The function checks each attribute and lists all of the attributes of the object and their values.
|LiveURL=
|Code=
&lt;script&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
An attribute value is specified if it is assigned through HTML or script.
Windows Internet Explorer 9. When webpages are displayed in IE9 Standards mode, the [[dom/properties/attribute|'''attributes''']] collection does not contain attributes that are not specifically created (unlike previous Windows Internet Explorer versions). As a result, the '''specified''' property returns <code>true</code> for every [[dom/methods/item|'''item''']] in the '''attributes''' collection.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/attributes|attribute]]</code>
*<code>About the W3C Document Object Model</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}