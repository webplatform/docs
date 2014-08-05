{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Cancels the interval previously started using the setInterval method. }}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=timerID
|Data type=Number
|Description='''Integer''' that specifies the interval to cancel. This value must have been previously returned by the [[dom/Window/setInterval|'''setInterval''']] method.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;meta charset{{=}}"UTF-8"&gt;
&lt;title&gt;setInterval/clearInterval example&lt;/title&gt;
&lt;script&gt;
var nIntervId;
 
function changeColor() {
  nIntervId {{=}} setInterval(flashText, 500);
}
 
function flashText() {
  var oElem {{=}} document.getElementById("my_box");
  oElem.style.color {{=}} oElem.style.color {{=}}{{=}} "red" ? "blue" : "red";
}
 
function stopTextColor() {
  clearInterval(nIntervId);
}
&lt;/script&gt;
&lt;/head&gt;
 
&lt;body onload{{=}}"changeColor();"&gt;
&lt;div id{{=}}"my_box" style{{=}}"color: red;"&gt;
&lt;p&gt;Hello World&lt;/p&gt;
&lt;/div&gt;
&lt;button onclick{{=}}"stopTextColor();"&gt;Stop&lt;/button&gt;

&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section}}
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.clearInterval clearInterval]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536353(v=vs.85).aspx clearInterval Method]
|HTML5Rocks_link=
}}