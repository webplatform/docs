{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script creates three new '''option''' objects and adds them to a '''select''' element. Because of the optional arguments, option "Two" is originally selected but option "Three" gains focus when the reset button is pressed.
|LiveURL=
|Code=
&lt;form action{{=}}"#"&gt;
&lt;select id{{=}}"oSelect"&gt;&lt;/select&gt;
&lt;button type{{=}}"reset"&gt;Reset to Defaults&lt;/button&gt;
&lt;/form&gt;
&lt;script type{{=}}"text/javascript"&gt;
var sel {{=}} document.getElementById('oSelect');
sel.options.add( new Option("One","1") );
sel.options.add( new Option("Two","2",false,true) );
sel.options.add( new Option("Three",3,1,0) );
&lt;/script&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use this object to instantiate new '''option''' elements before adding them to a '''select''' element. You can specify up to four optional arguments:
{| class="wikitable"
|-
|sText
|'''String''' that specifies the option text.
|-
|sValue
|'''String''' that specifies the option value.
|-
|bDefaultSelected
|'''Boolean''' that indicates whether the option is the default selection.
|-
|bSelected
|'''Boolean''' that indicates whether this option is selected when it is added to the collection.
|}
 
Numeric values are coerced into string and Boolean equivalents if possible.
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''Option''' object has these types of members:
*[#methods Methods]


====Methods====
The '''Option''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/create (option)|'''create''']]
|Initializes a new '''option''' element. This method cannot be called directly. See '''Option''' object.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/options|options]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}