{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''XMLDocument''' property to access the object model of an '''xml''' data island.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnCheck(){
   var oNode {{=}} oMetaData.XMLDocument.selectSingleNode
       ("METADATA/ABSTRACT");
   alert(oNode.text);
}
&lt;/SCRIPT&gt;

&lt;XML ID{{=}}"oMetaData"&gt;
  &lt;METADATA&gt;
     &lt;AUTHOR&gt;John Smith&lt;/AUTHOR&gt;
     &lt;GENERATOR&gt;Visual Notepad&lt;/GENERATOR&gt;
     &lt;PAGETYPE&gt;Reference&lt;/PAGETYPE&gt;
     &lt;ABSTRACT&gt;Specifies a data island&lt;/ABSTRACT&gt;
  &lt;/METADATA&gt;
&lt;/XML&gt;

&lt;INPUT TYPE{{=}}button VALUE{{=}}"Test" onclick{{=}}"fnCheck()"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''XMLDocument''' is the default property; specifying the property is optional.  The '''XMLDocument''' property is useful when an entire XML document is passed to a method that requires an '''html''' element, instead of an '''xml''' element.  The '''XMLDocument''' property provides access to the root of the XML tree in the data island.
For a complete description of the XML DOM exposed by the '''XMLDocument''' property, see the XML DOM overview.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>xml</code>
*<code>Reference</code>
*<code>[[apis/xhr/properties/XSLDocument|XSLDocument]]</code>
*<code>Conceptual</code>
*<code>Introduction to Persistence</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}