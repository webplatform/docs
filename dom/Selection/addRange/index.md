{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Adds a Range to the current selection.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=range
|Data type=Range
|Description=Range to add.
|Optional=No
}}
|Method_applies_to=dom/Selection
|Example_object_name=selObj
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=/* Select all STRONG elements in an HTML document */

var strongs {{=}} document.getElementsByTagName('strong');
var selObj {{=}} window.getSelection();

if(selObj.rangeCount > 0) selObj.removeAllRanges();

for(var i = 0; i < strongs.length; i++) {
  var range {{=}} document.createRange();
  range.selectNode(strongs[i]);
  selObj.addRange(range);
}
}}{{Single Example
|Language=JavaScript
|Code=function selectElements(tagName){
var els {{=}} document.getElementsByTagName(tagName);
var selObj {{=}} window.getSelection();
if(selObj.rangeCount > 0) selObj.removeAllRanges();
		for(var i {{=}} 0; i < els.length; i++) {
		  var range {{=}} document.createRange();
		  range.selectNode(els[i]);
		  selObj.addRange(range);
		}   
   }

}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 9 and higher and Webkit browser do not currently support multiple or disjointed selections in standards mode. If '''addRange''' is applied to a selection that already contains a Range, the new Range is not added.
|Import_Notes====Syntax===
selObj.addRange(range)
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.6.1
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Selection.addRange Selection.addRange]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975172(v=vs.85).aspx addRange Method]
|HTML5Rocks_link=
}}