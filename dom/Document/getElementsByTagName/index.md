{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns an HTMLCollection of all descendant elements with a given tag name.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of an element tag.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=A DOM collection of elements with the given tag name.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example returns the number of <code>li</code> elements (10) and the text of the first one ("Item 1").
|Code=<!doctype html>
<html>
 <head>
  <script>
function printFirstLIText(){
  var aReturn = document.getElementsByTagName("LI");
  alert("Length: " + aReturn.length + "\nFirst Item: " + aReturn[0].childNodes[0].nodeValue);
}
  </script>
 </head>
 <body>
<nowiki>
  <ul onclick="printFirstLIText()">
   <li>Item 1
    <ul>
     <li>Sub Item 1.1
      <ol>
       <li>Super Sub Item 1.1</li>
       <li>Super Sub Item 1.2</li>
      </ol>
     </li>
     <li>Sub Item 1.2</li>
     <li>Sub Item 1.3</li>
    </ul>
   </li>	
   <li>Item 2
    <ul>
     <li>Sub Item 2.1
     <li>Sub Item 2.3
    </ul>
   </li>
   <li>Item 3</li>
  </ul>
</nowiki>
 </body>
</html>
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