{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eTag
|Data type=String
|Description=A '''String''' that specifies the name of an element.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElement'''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''createElement''' method to dynamically update the contents of a Web page by adding an element selected from a drop-down list box.
|Code=&lt;SCRIPT&gt;
function fnCreate(){
    oData.innerHTML{{=}}"";
    var oOption{{=}}oSel.options[oSel.selectedIndex];
    if(oOption.text.length&gt;0){
    var aElement{{=}}document.createElement(oOption.text);
    eval("aElement." + oOption.value + "{{=}}'" + oText.value + "'");
    if(oOption.text{{=}}{{=}}"A"){
        aElement.href{{=}}"http://www.bing.com";
   }
   }
    oData.appendChild(aElement);
}
&lt;/SCRIPT&gt;
&lt;SELECT ID{{=}}"oSel" onchange{{=}}"fnCreate()"&gt;
&lt;OPTION VALUE{{=}}"innerText"&gt;A
&lt;OPTION VALUE{{=}}"value"&gt;&amp;lt;INPUT TYPE{{=}}"button"&amp;gt;
&lt;/SELECT&gt;
&lt;SELECT ID{{=}}oText onchange{{=}}"fnCreate()"&gt;
&lt;OPTION&gt;
&lt;OPTION VALUE{{=}}"Text"&gt;Text
&lt;OPTION VALUE{{=}}"More and More Text"&gt;More and More Text
&lt;/SELECT&gt;
&lt;SPAN ID{{=}}"oData" &gt;&lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/createElement.htm
}}{{Single Example
|Description=In Internet Explorer, you can also specify all the attributes inside the '''createElement''' method by using an HTML string for the method argument. The following example demonstrates how to dynamically create two radio buttons utilizing this technique.
|Code=&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;

&lt;html xmlns{{=}}"http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
  &lt;title&gt;Radio Button DOM Insertion&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;
    function createRadioButton(){
      // Create radio button object with value{{=}}"First Choice" and then insert this element into the document hierarchy.
      var newRadioButton {{=}} document.createElement("&lt;input type{{=}}'radio' name{{=}}'radio1' value{{=}}'First Choice' /&gt;")
      document.body.insertBefore(newRadioButton); // Since the second argument is implicity null, this inserts the radio button at the end of this node's list of children ("this" node refers to the body element).
      
      // Create radio button object with value{{=}}"Second Choice" and then insert this element into the document hierarchy. 
      newRadioButton {{=}} document.createElement("&lt;input type{{=}}'radio' name{{=}}'radio2' value{{=}}'Second Choice' /&gt;")
      document.body.insertBefore(newRadioButton); // Insert the radio button at the end of this node's list of children (which is directly after the radio button we just inserted).
    }

    function displayHTML(htmlString) {
      var temp {{=}} document.createElement('div');
      temp.appendChild( document.createTextNode(htmlString) );
      document.getElementById('displayBox').innerHTML {{=}} "&lt;pre&gt;" + temp.innerHTML + "&lt;/pre&gt;";
    }
  &lt;/script&gt;
&lt;/head&gt;

&lt;body&gt;
  &lt;form&gt;
    &lt;input type{{=}}"button" onclick{{=}}"createRadioButton()" value{{=}}"Create two Radio Buttons" /&gt;
    &lt;br /&gt;
    &lt;input type{{=}}"button" onclick{{=}}"displayHTML(document.body.outerHTML)" value{{=}}"Click here to see HTML" /&gt;
  &lt;/form&gt;
  &lt;div id{{=}}"displayBox"&gt;&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
You must perform a second step when you use '''createElement''' to create the '''input''' element. The '''createElement''' method generates an input text box, because that is the default '''input''' [[html/attributes/type|'''type''']] property. To insert any other kind of '''input''' element, first invoke '''createElement''' for '''input''', and then set the '''type''' property to the appropriate value in the next line of code.
Attributes can be included with the ''eTag'' as long as the entire string is valid HTML. To include the [[html/attributes/name|'''NAME''']] attribute at run time on objects created with the '''createElement''' method, use the ''eTag''.
Use the ''eTag'' to include attributes when form elements are created that will be reset using the '''BUTTON''' with a [[html/attributes/type (button element)|'''TYPE''']] attribute value of <code>reset</code>.
In Microsoft Internet Explorer 4.0, the only new elements you can create are '''img''', '''area''', and '''option'''. As of Microsoft Internet Explorer 5, you can create all elements programmatically, 
except '''frame''' and '''iframe'''. The properties of these created elements are read/write and can be accessed programmatically. Before you use new objects, you must explicitly add them to their respective collections or to the document. To insert new elements into the current document, use the [[dom/methods/insertBefore|'''insertBefore''']] method or the [[dom/methods/appendChild|'''appendChild''']] method.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[dom/methods/cloneNode|cloneNode]]</code>
*<code>[[dom/methods/removeNode|removeNode]]</code>
*<code>Conceptual</code>
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}