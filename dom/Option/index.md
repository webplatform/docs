{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following script creates three new '''option''' objects and adds them to a '''select''' element. Because of the optional arguments, option "Two" is originally selected but option "Three" gains focus when the reset button is pressed.
|Code=&lt;form action{{=}}"#"&gt;
&lt;select id{{=}}"oSelect"&gt;&lt;/select&gt;
&lt;button type{{=}}"reset"&gt;Reset to Defaults&lt;/button&gt;
&lt;/form&gt;
&lt;script type{{=}}"text/javascript"&gt;
var sel {{=}} document.getElementById('oSelect');
sel.options.add( new Option("One","1") );
sel.options.add( new Option("Two","2",false,true) );
sel.options.add( new Option("Three",3,1,0) );
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Use this object to instantiate new '''option''' elements before adding them to a '''select''' element. You can specify up to four optional arguments:
{{{!}} class="wikitable"
{{!}}-
{{!}}sText
{{!}}'''String''' that specifies the option text.
{{!}}-
{{!}}sValue
{{!}}'''String''' that specifies the option value.
{{!}}-
{{!}}bDefaultSelected
{{!}}'''Boolean''' that indicates whether the option is the default selection.
{{!}}-
{{!}}bSelected
{{!}}'''Boolean''' that indicates whether this option is selected when it is added to the collection.
{{!}}}
 
Numeric values are coerced into string and Boolean equivalents if possible.
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}