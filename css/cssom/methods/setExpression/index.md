{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''setExpression''' method to change the width of a blue box. In each example, the width of the blue box is equal to the sum of the values of the first two text boxes. When a value in one of the text boxes changes, the width of the blue box recalculates.

This example shows the HTML implementation of '''setExpression'''.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/recalc_inline.htm
|Code=
&lt;INPUT TYPE{{=}}text ID{{=}}oBox1 value{{=}}40&gt;The sum of the values in 
    these two text boxes determines the width&lt;BR&gt;
&lt;INPUT TYPE{{=}}text ID{{=}}oBox2 value{{=}}40&gt;of the blue text box below.
&lt;BR&gt;&lt;INPUT TYPE{{=}}text ID{{=}}oBox3 
    STYLE{{=}}"width:expression(eval(oBox1.value) + 
    eval(oBox2.value));background-color:blue"&gt;
&lt;BR&gt;&lt;INPUT TYPE{{=}}button ID{{=}}Button 
    value{{=}}"Click to resize blue box above" 
    onclick{{=}}"recalc()"&gt;
}}
{{Single_Example
|Description=This example uses the [[dom/properties/uniqueID|'''uniqueID''']] property and the '''setExpression''' method to update the [[dom/properties/innerText|'''innerText''']] property of a table row.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setExpression.htm
|Code=
&lt;SCRIPT&gt;
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use the '''setExpression''' method to add expressions to supported [[css/cssom/methods/removeExpression|'''removeExpression''']] method.
The following syntax sections show how to set an expression on DHTML Properties and CSS attributes.
*Use this syntax to set an expression on a read/write property or on an [[dom/properties/expando|'''expando''']] property. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.setExpression(sPropertyName, sExpression, sLanguage)</code></pre>
</div>
*Use this syntax to set an expression on a CSS attribute. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.style.setExpression(sPropertyName, sExpression, sLanguage)</code></pre>
</div>
*Use the '''expression()''' syntax to set an expression on a CSS attribute in HTML. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>&lt;ELEMENT STYLE{{=}}"sAttributeName:expression(sExpression)"&gt;</code></pre>
</div>

The data type of the evaluated expression in the ''language'' parameter must match one of the possible values allowed for the ''expression'' parameter. If the property or attribute specified by the first parameter requires a string, the data type of the second parameter must be a string. Otherwise, the second parameter is evaluated prior to invoking '''setExpression''', causing the expression to be set to the result of the evaluation.
Use the [[dom/properties/uniqueID|'''uniqueID''']] property of an object in an expression to refer back to the object. Using '''uniqueID''' is an alternative to specifying an [[html/attributes/id|'''id''']] for expressions that use an object reference.
The [[css/cssom/styleSheet/cssText|'''cssText''']] property is a unique property that is not compatible with the dynamic properties implementation. Do not use '''cssText''' with any dynamic property methods.
The following examples illustrate common problems encountered with the ''expression'' parameter in '''setExpression'''.  The ''expression'' appears valid, but may not be.
*The provided ''expression'' is invalid because document.style.fontSize is "npx" and will not add to 13<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.style.setExpression("height","document.style.fontSize + 13"); </code></pre>
</div>
*The provided ''expression'' is invalid when document.body.style.fontSize is previously unspecified<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.style.setExpression("width","document.body.style.fontSize"); </code></pre>
</div>

|Import_Notes=
===Syntax===
===Parameters===
;''sPropertyName'' [in]:'''String''' that specifies the name of the property to which ''expression'' is added.
;''sExpression'' [in]:'''String''' that specifies any valid script(JScript, JavaScript, VBSCript) statement without quotations or semicolons. This string can include references to other properties on the current page. Array references are not allowed on object properties included in this script.
;''sLanguage'' [in, optional]:'''String''' that specifies one of the following values: <dl class{{=}}"indent"><dt><a id{{=}}"JScript"/><a id{{=}}"jscript"/><a id{{=}}"JSCRIPT"/>'''JScript'''</dt><dd>Default. Language is JScript.</dd><dt><a id{{=}}"VBScript"/><a id{{=}}"vbscript"/><a id{{=}}"VBSCRIPT"/>'''VBScript'''</dt><dd>Language is VBScript.</dd><dt><a id{{=}}"JavaScript"/><a id{{=}}"javascript"/><a id{{=}}"JAVASCRIPT"/>'''JavaScript'''</dt><dd>Language is JavaScript.</dd></dl>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
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
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}