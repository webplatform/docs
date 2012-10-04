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
|Return_value_description=C++

a variant value representing the expression of the property.

JavaScript

a variant value representing the expression of the property.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples demonstrate how to use the '''getExpression''' method to retrieve CSS properties.
|LiveURL=This example uses the '''getExpression''' method to retrieve the [[css/properties/width|'''width''']] property of a '''span''' object.
|Code=
&lt;body&gt;
&lt;span id{{=}}"trueBlueSpan" 
    style{{=}}"background-color:lightblue; width:100px"&gt;
    The width of this blue span is set inline at 100 pixels.
&lt;/span&gt;
&lt;span id{{=}}"oldYellowSpan" style{{=}}"background-color:lightyellow; 
    width:200px"&gt;
    The width of this yelllow span is set inline at 200 pixels.
&lt;/span&gt;
&lt;br&gt;
&lt;span id{{=}}"AlGreenSpan" style{{=}}"background-color:lightgreen; 
    width:expression(trueBlueSpan.style.pixelWidth + 
    oldYellowSpan.style.pixelWidth)"&gt;
    Click the button below to see the expression used to set 
    the width of this span.
&lt;/span&gt;
&lt;br&gt;
&lt;button onclick{{=}}alert(AlGreenSpan.style.getExpression("width"));&gt;
    See Expression&lt;/button&gt;
&lt;/body&gt;
}}
{{Single_Example
|Description=In the following example, the [[css/cssom/methods/setExpression|'''setExpression''']] method is used to set the [[css/properties/width|'''width''']] property of a blue '''input type{{=}}text''' object equal to the sum of the values in two other '''input type{{=}}text''' objects.  When the user clicks the '''input type{{=}}button''' element, the '''getExpression''' method is used to display the expression.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getExpression.htm
|Code=
&lt;html&gt;
&lt;head&gt;
&lt;script language{{=}}"JScript"&gt;
var s;
function fnInit() {
Box3.style.setExpression("width","eval(Box1.value) + eval(Box2.value)",
"jscript");
}
function getexp() {
s{{=}}Box3.style.getExpression("width");
alert("Expression for the width of the blue box is \n\n" + s + 
"\n\nThe width property has a value of " + Box3.style.width);
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}fnInit();&gt;
&lt;input type{{=}}text id{{=}}"Box1" value{{=}}40&gt;
&lt;br&gt;&lt;input type{{=}}text id{{=}}"Box2" value{{=}}40&gt;
&lt;br&gt;&lt;input type{{=}}text id{{=}}"Box3" style{{=}}"background-color:blue"&gt;
&lt;br&gt;&lt;input type{{=}}button id{{=}}"Button2" value{{=}}"Get expression" onclick{{=}}"getexp()"&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The following syntax sections show how to retrieve an expression from supported Cascading Style Sheets (CSS) and DHTML Properties.
*Use this syntax to retrieve an expression from a read/write property or from an [[dom/properties/expando|'''expando''']] property. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>var sExpression {{=}} object.getExpression(sPropertyName)</code></pre>
</div>
*Use this syntax to retrieve an expression from a CSS attribute. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>var sExpression {{=}} object.style.getExpression(sPropertyName)</code></pre>
</div>

|Import_Notes=
===Syntax===
===Parameters===
;''sPropertyName'' [in]:'''String''' that specifies the name of the property from which to retrieve the expression.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>IHTMLStyle2</code>
*<code>IHTMLElement2</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/recalc|recalc]]</code>
*<code>[[css/cssom/methods/removeExpression|removeExpression]]</code>
*<code>[[css/cssom/methods/setExpression|setExpression]]</code>
*<code>Conceptual</code>
*<code>CSS Attributes: Index</code>
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