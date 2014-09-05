{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=PropertyName
|Data type=String
|Description='''String''' that specifies the name of the property to which ''expression'' is added.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=Expression
|Data type=String
|Description='''String''' that specifies any valid script (JScript, JavaScript, VBSCript) statement without quotations or semicolons. This string can include references to other properties on the current page. Array references are not allowed on object properties included in this script.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=Language
|Data type=String
|Description='''String''' that specifies one of the following values: 
*"JScript" -- Default. Language is JScript.
*"VBScript" --Language is VBScript.
*"JavaScript" -- Language is JavaScript.
|Optional=No
}}
|Method_applies_to=css/cssom/methods
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples use the '''setExpression''' method to change the width of a blue box. In each example, the width of the blue box is equal to the sum of the values of the first two text boxes. When a value in one of the text boxes changes, the width of the blue box recalculates.

This example shows the HTML implementation of '''setExpression'''.
|Code=&lt;INPUT TYPE{{=}}text ID{{=}}oBox1 value{{=}}40&gt;The sum of the values in 
    these two text boxes determines the width&lt;BR&gt;
&lt;INPUT TYPE{{=}}text ID{{=}}oBox2 value{{=}}40&gt;of the blue text box below.
&lt;BR&gt;&lt;INPUT TYPE{{=}}text ID{{=}}oBox3 
    STYLE{{=}}"width:expression(eval(oBox1.value) + 
    eval(oBox2.value));background-color:blue"&gt;
&lt;BR&gt;&lt;INPUT TYPE{{=}}button ID{{=}}Button 
    value{{=}}"Click to resize blue box above" 
    onclick{{=}}"recalc()"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/recalc_inline.htm
}}{{Single Example
|Language=JavaScript
|Description=This example uses the [[dom/HTMLElement/uniqueID|'''uniqueID''']] property and the '''setExpression''' method to update the [[dom/HTMLElement/innerText|'''innerText''']] property of a table row.
|Code=&lt;SCRIPT&gt;
window.onload{{=}}fnInit;
function fnInit(){
   var iLen{{=}}oSheet.rows.length-1;
   for(var i{{=}}1;i&lt;iLen;i++){
      var oRow{{=}}oSheet.rows[i];
      var oCells{{=}}oRow.cells;
      oCells(3).setExpression("innerText",
         "fnGetValue(" + oRow.uniqueID + ")");
   }
   var oGrand{{=}}oSheet.rows(iLen).cells(1);
   oGrand.setExpression("innerText","fnGetTotal()");
}
function fnGetTotal(){
   var iValue{{=}}0;
   var iLen{{=}}oSheet.rows.length-1;
   for(var i{{=}}1;i&lt;iLen;i++){
      iValue+{{=}}parseFloat(oSheet.rows(i).cells(3).innerText);
   }
   return iValue;
}
function fnGetValue(oRow){
   var oCells{{=}}oRow.cells;
   var oPrice{{=}}oCells(2);
   var oQuantity{{=}}oCells(1);
   var sPrice;
   var sQuantity;
   if(oPrice.childNodes[0].nodeName{{=}}{{=}}"#text"){
      sPrice{{=}}oPrice.innerText;
   }
   else{
      var vPrice{{=}}oPrice.childNodes[0].value;
      sPrice{{=}}(vPrice{{=}}{{=}}""?"0":vPrice);
   }
   if(oQuantity.childNodes[0].nodeName{{=}}{{=}}"#text"){
      sQuantity{{=}}oQuantity.innerText;
   }
   else{
      var vQuantity{{=}}oQuantity.childNodes[0].value;
      sQuantity{{=}}(vQuantity{{=}}{{=}}""?"0":vQuantity);
   }
   var vAlg1{{=}}parseFloat(sPrice) * parseFloat(sQuantity);
   return vAlg1;
}
&lt;/SCRIPT&gt;
&lt;TABLE ID{{=}}"oSheet"&gt;
&lt;TR&gt;&lt;TH&gt;Product&lt;/TH&gt;&lt;TH&gt;Quantity&lt;/TH&gt;
&lt;TH&gt;Price per #&lt;/TH&gt;&lt;TH&gt;Totals&lt;/TH&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TD&gt;Browser Putty&lt;/TD&gt;&lt;TD EDIT{{=}}"true"&gt;2&lt;/TD&gt;
&lt;TD EDIT{{=}}"true"&gt;4.99&lt;/TD&gt;&lt;TD&gt;&lt;/TD&gt;&lt;/TR&gt;
&lt;TR&gt;&lt;TH COLSPAN{{=}}3&gt;Grand Total&lt;/TH&gt;&lt;TH&gt;&lt;/TH&gt;&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setExpression.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Use the '''setExpression''' method to add expressions to supported [[css/cssom/methods/removeExpression|'''removeExpression''']] method.
The following syntax sections show how to set an expression on DHTML Properties and CSS attributes.
*Use this syntax to set an expression on a read/write property or on an '''expando''' property. 
<nowiki>
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.setExpression(sPropertyName, sExpression, sLanguage)</code></pre>
</div>
</nowiki>
*Use this syntax to set an expression on a CSS attribute. 
<nowiki>
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.style.setExpression(sPropertyName, sExpression, sLanguage)</code></pre>
</div>
</nowiki>
*Use the '''expression()''' syntax to set an expression on a CSS attribute in HTML. 
<nowiki>
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>&lt;ELEMENT STYLE{{=}}"sAttributeName:expression(sExpression)"&gt;</code></pre>
</div>
</nowiki>
The data type of the evaluated expression in the ''language'' parameter must match one of the possible values allowed for the ''expression'' parameter. If the property or attribute specified by the first parameter requires a string, the data type of the second parameter must be a string. Otherwise, the second parameter is evaluated prior to invoking '''setExpression''', causing the expression to be set to the result of the evaluation.
Use the [[dom/properties/uniqueID|'''uniqueID''']] property of an object in an expression to refer back to the object. Using '''uniqueID''' is an alternative to specifying an [[html/attributes/id|'''id''']] for expressions that use an object reference.
The [[css/cssom/styleSheet/cssText|'''cssText''']] property is a unique property that is not compatible with the dynamic properties implementation. Do not use '''cssText''' with any dynamic property methods.
The following examples illustrate common problems encountered with the ''expression'' parameter in '''setExpression'''.  The ''expression'' appears valid, but may not be.
*The provided ''expression'' is invalid because document.style.fontSize is "npx" and will not add to 13
<code>object.style.setExpression("height","document.style.fontSize + 13"); </code>
*The provided ''expression'' is invalid when document.body.style.fontSize is previously unspecified
<code>object.style.setExpression("width","document.body.style.fontSize"); </code>
|Import_Notes=
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
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>IHTMLElement2</code>
*<code>IHTMLStyle2</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/getExpression|getExpression]]</code>
*<code>[[css/cssom/methods/removeExpression|removeExpression]]</code>
*<code>[[css/cssom/methods/recalc|recalc]]</code>
*<code>Conceptual</code>
*<code>About Dynamic Properties</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}