{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a collection of all descendant elements with a given name.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of an element.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=A DOM collection of elements with the given name.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example uses the '''getElementsByTagName''' method to return the children of a '''ul''' element based on the selected '''li''' element.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function printFirstLIText(e){
  var oWorkItem = event.target;
  var aReturn = oWorkItem.parentElement.getElementsByTagName("LI");
  console.log("Length: " + aReturn.length + "\nFirst Item: " +
   aReturn[0].childNodes[0].nodeValue);
}
function initialize() {
  document.getElementById("ex").addEventListener("click", printFirstLIText, false);
}
window.addEventListener("load", initialize, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;ul id="ex"&gt;
   &lt;li&gt;Item 1
    &lt;ul&gt;
     &lt;li&gt;Sub Item 1.1
      &lt;ol&gt;
       &lt;li&gt;Super Sub Item 1.1&lt;/li&gt;
       &lt;li&gt;Super Sub Item 1.2&lt;/li&gt;
      &lt;/ol&gt;
     &lt;/li&gt;
     &lt;li&gt;Sub Item 1.2&lt;/li&gt;
     &lt;li&gt;Sub Item 1.3&lt;/li&gt;
    &lt;/ul&gt;
   &lt;/li&gt;	
   &lt;li&gt;Item 2
    &lt;ul&gt;
     &lt;li&gt;Sub Item 2.1
     &lt;li&gt;Sub Item 2.3
    &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Item 3&lt;/li&gt;
  &lt;/ul&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getElementsByTagName.htm
}}
}}
{{Notes_Section
|Usage=Use this method to get a collection of all child and nested child elements with the specified tag name.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.6.5
}}
}}
{{Compatibility_Section
|Not_required=Yes
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