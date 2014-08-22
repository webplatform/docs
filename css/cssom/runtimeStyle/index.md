{{Page_Title|runtimeStyle}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets and retrieves the format and style of an object.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example sets a value on the '''runtimeStyle''' object to affect the [[css/cssom/currentStyle|'''currentStyle''']] object, but not the [[css/cssom/style|'''style''']] object.
|Code=&lt;SCRIPT&gt;
function fnChangeValue(sValue){
   if(oDIV.runtimeStyle.backgroundColor {{=}}{{=}} oDIV.style.backgroundColor){
      sValue{{=}}"";
   }
   oDIV.runtimeStyle.backgroundColor {{=}} sValue;
   console.log(oDIV.style.backgroundColor +
      "\n" + oDIV.currentStyle.backgroundColor +
      "\n" + oDIV.runtimeStyle.backgroundColor);
}
&lt;/SCRIPT&gt;
&lt;DIV ID {{=}} "oDIV"&gt;
This is a demonstration DIV.
&lt;/DIV&gt;
&lt;INPUT TYPE {{=}} "button" VALUE {{=}} "Change Color" onclick{{=}}"fnChangeValue('blue')"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/runtimeStyle.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''runtimeStyle''' object sets and retrieves the format and style of an object, and overrides existing formats and styles in the process. Other than having precedence over the [[css/cssom/style|'''style''']] object and not persisting, the '''runtimeStyle''' object is equivalent to the '''style''' object.
To change or clear multiple style properties simultaneously, use this object with the [[css/cssom/styleSheet/cssText|'''cssText''']] property. For example, to change the font color and background color of a '''DIV''' element, you could use the following code:
 <code>
 &lt;DIV onclick{{=}}"this.runtimeStyle.cssText {{=}} 'color:red;background-color:blue;border:5px solid black;'"&gt;
 Click this DIV to change style properties.&lt;/DIV&gt;
 </code>
Windows Internet Explorer 8 or later. The behavior of [[dom/Element/setAttribute|'''setAttribute''']] method depends on the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8.
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
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}