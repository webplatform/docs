{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
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
|Description=''String''' that specifies the name of the property from which to remove an expression. Returns '''true''' if the expression was successfully removed, '''false''' otherwise.
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
|Description=This example uses the '''removeExpression''' method to remove an expression from the [[css/properties/width|'''width''']] property of a blue box.
|Code=&lt;INPUT TYPE{{=}}text ID{{=}}oBox1 value{{=}}40&gt;The sum of the values in these two text boxes determines the width &lt;BR&gt;&lt;INPUT TYPE{{=}}text ID{{=}}oBox2 value{{=}}40&gt;of the blue text box below.
&lt;BR&gt;&lt;INPUT TYPE{{=}}text ID{{=}}oBox3 STYLE{{=}}"background-color:blue"&gt;
&lt;BR&gt;&lt;BR&gt;&lt;INPUT TYPE{{=}}button ID{{=}}Button1 
    value{{=}}"Step 1: Get expression" onclick{{=}}"getexp()"&gt;
&lt;INPUT TYPE{{=}}button ID{{=}}Button2 value{{=}}"Step 2: Remove expression" 
    onclick{{=}}"remexp()"&gt;
&lt;INPUT TYPE{{=}}button ID{{=}}Button3 value{{=}}"Step 3: Get expression again" 
    onclick{{=}}"getexp()"&gt;
&lt;BR&gt;
&lt;HR&gt;
&lt;BR&gt;
Right-click anywhere on this page to view the source code.
 
&lt;SCRIPT&gt;
var s;
var b;
oBox3.style.setExpression("width","eval(oBox1.value) + 
    eval(oBox2.value)","jscript");
function getexp()
{
    s{{=}}oBox3.style.getExpression("width");
    alert("Expression for the width of the blue box is \n\n" + s + 
    "\n\nThe width property has a value of " + oBox3.style.width);
}
function remexp()
{
    b {{=}} oBox3.style.removeExpression("width");
    alert("Expression removed successfully? \n" + b);
}
&lt;/SCRIPT&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeExpression.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
After the expression is removed from the specified property, the value of the property equals the last computed value of the expression. To remove expressions set by the [[css/cssom/methods/setExpression|'''setExpression''']] method, use '''removeExpression'''.
The following syntax sections show how to remove an expression from supported Cascading Style Sheets (CSS) attributes and DHTML Properties.
*Use this syntax to remove an expression from a read/write property or from an [[dom/properties/expando|'''expando''']] property. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.removeExpression(sPropertyName)</code></pre>
</div>
*Use this syntax to remove an expression from a CSS attribute. <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>object.style.removeExpression(sPropertyName)</code></pre>
</div>
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
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/cssom/methods/getExpression|getExpression]]</code>
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