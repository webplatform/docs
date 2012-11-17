{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|children}}
{{Summary_Section|Retrieves a live collection of child elements of an element.}}
{{API_Object_Property
|Property_applies_to=dom/Element
|Read_only=Yes
|Example_object_name=element
|Return_value_name=childElementList
|Javascript_data_type=DOM Node
|Return_value_description=A live [[dom/HTMLCollection|HTMLCollection]] of child elements of the element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows how to retrieve a collection of '''input type{{=}}text''', [[html/elements/div|'''div''']] and [[html/elements/button|'''button''']]. The '''children''' collection for <code>oChildDIV</code> includes '''p'''.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;style&gt;
   
  &lt;/style&gt;
  &lt;script&gt;
/*jslint white: true, sloppy: true, plusplus: true, maxlen: 100*/
var oColl, //Collection for children.
    oRow, oCell, //Use for row and cell.
    oParentDIV, oChildDIV, oTable;
/*****************************************************************************
In:
 oColl - Collection of children.
 oCollection - Parent object.
Out: 
 Output to screen.
******************************************************************************/
function getChildren(oColl, oCollection) {
  var x, length = oColl.length;
  for (x = 0; x &lt; length; x++) {
    // Create new row.
    oRow = oTable.insertRow();
        
    // Create cell with the array index of current child.
    oCell = oRow.insertCell();
    oCell.align = 'center';
    oCell.style.color = '#0000FF';
    oCell.textContent = x;
 
    // Create cell with the tagName of current child.     
    oCell = oRow.insertCell();
    oCell.align = 'center';
    oCell.textContent = oCollection.children[x].tagName;

    // Create cell with ID / name of current child.       
    oCell = oRow.insertCell();
    oCell.align = 'center';

    if (oCollection.children[x].name) {
      oCell.textContent = oCollection.children[x].name;
    } else {
      oCell.textContent = oCollection.children[x].id;
    }
  
    // Create cell with applicable Parent object to the child.
    oCell = oRow.insertCell();
    oCell.align = 'center';
    oCell.textContent = oCollection.id;
  }
}
function collect() {
  oColl = oParentDIV.children;
  // Call function to create cells for the top parent object.
  getChildren(oColl, oParentDIV);
  /* Call function to create cells for the child within the parent object
     containing its own child.*/
  oColl = oChildDIV.children;
  getChildren(oColl, oChildDIV);
}
function b1Click() {
  collect();
  this.disabled = true;
}
function initialize() {
  oParentDIV = document.getElementById("oParentDIV");
  oChildDIV = document.getElementById("oChildDIV");
  oTable = document.getElementById("oTable");
  document.getElementById("b1").addEventListener("click", b1Click, false);
  document.getElementById("b0").addEventListener(
    "click",
    function () {
      console.log('Something.');
    },
    false);
}
window.addEventListener("load", initialize, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;center&gt;
   &lt;span class="oTitle"&gt;DIV Object (ID: oParentDIV)&lt;/span&gt;
   &lt;div id="oParentDIV" class="oDIV"&gt;
    Some Input (non-editable):
    &lt;input type="text" name="SomeInputTextBox"
      value="" size="5" contenteditable="false"/&gt;
    &lt;div id="oChildDIV"&gt;
     &lt;p id="oParagraph1"&gt;Some text in a paragraph&lt;/p&gt;
    &lt;/div&gt;
    &lt;button id="b0" name="SomeButton"&gt;The Label for the Button&lt;/button&gt;
   &lt;/div&gt;
   &lt;hr/&gt;
   &lt;button id="b1" style="cursor: pointer;"&gt;Retrieve Collection&lt;/button&gt;
   &lt;br/&gt;&lt;br/&gt;
   &lt;table border="1" id="oTable" alt="Child Listing"&gt;
    &lt;tr&gt;
     &lt;th&gt;Array Index&lt;/th&gt;
     &lt;th&gt;Child Element&lt;/th&gt;
     &lt;th&gt;ID&lt;/th&gt;
     &lt;th&gt;Parent Object&lt;/th&gt;
    &lt;/tr&gt;
   &lt;/table&gt;
  &lt;/center&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/children.htm
}}
}}
{{Notes_Section
|Usage=Use this property to get a live collection of the child elements of an element.
|Notes=*Since this is a live collection, its '''length''', as well as its content, will always change whenever child elements are added, removed, or reordered.
*Similar to the objects contained in the [[dom/properties/all|'''all''']] collection, the objects contained in the '''children''' collection are undefined if the child elements are overlapping tags.
*The '''children''' collection can contain HTML elements.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=WHATWG DOM
|URL=http://dom.spec.whatwg.org/
|Status=Living Standard
|Relevant_changes=Section 5.8
}}{{Related Specification
|Name=DOM4
|URL=http://www.w3.org/TR/dom/
|Status=Working Draft
|Relevant_changes=Section 5.7
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