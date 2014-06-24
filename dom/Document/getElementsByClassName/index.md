{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a collection of all descendant elements with given classes. Not recommended; see Notes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=classNames
|Data type=String
|Description=A space separated list of classes.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=elements
|Javascript_data_type=Object
|Return_value_description=A live [[dom/HTMLCollection|HTMLCollection]] of elements with the given class names.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example returns the text of the first <code>li</code> whose class is "sublistitem", in this case, "Sub Item 1.1".
|Code=<!doctype html>
<html>
 <head>
  <script>
function printFirstSubLIText(){
  var aReturn = document.getElementsByClassName("sublistitem");
  alert("Length: " + aReturn.length + "\nFirst Item: " + aReturn[0].childNodes[0].nodeValue);
}
  </script>
 </head>
 <body>
  <ul onclick="printFirstSubLIText()">
   <li>Item 1
    <ul>
     <li class="sublistitem">Sub Item 1.1
      <ol>
       <li>Super Sub Item 1.1</li>
       <li>Super Sub Item 1.2</li>
      </ol>
     </li>
     <li class="sublistitem">Sub Item 1.2</li>
     <li class="sublistitem">Sub Item 1.3</li>
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
 </body>
</html>
}}
}}
{{Notes_Section
|Usage=The use of this property is discouraged. See the [[#Notes|Notes]] section for details.
|Notes=The use of this property is discouraged because of performance implications (due to the live DOMCollection where any changes to the document must be reflected on the returned object immediately) and complexity (the removal of an element from the document will result in immediate changes to the collection).

A close alternative is
*[[css/selectors_api/querySelectorAll|querySelectorAll]]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Candidate Recommendation
|Relevant_changes=Section 3.1.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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