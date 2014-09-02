{{Page_Title}}
{{Flags
|State=
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/cssom/properties
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The content of the primary document is shown in the code snippet below. In the following sample a '''div''' tag contains a custom element that has an element behavior attached to it. The '''div''' tag that is located in the primary document sets a number of CSS attributes, specifically the following:

<li>
[[html/attributes/color|'''color''']] is set to red.</li>
<li>
[[css/properties/font-size|'''fontSize''']] is set to 12 pt.</li>
<li>
[[css/properties/font-style|'''fontStyle''']] is set to italic. </li>
<li>
[[css/properties/border|'''border''']] is set to 2px solid blue. </li>
|Code=&lt;HTML xmlns:myns&gt;
&lt;HEAD&gt;
&lt;?import namespace{{=}}"myns" implementation{{=}}"viewInheritStyle.htc"&gt; 
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;DIV style{{=}} "color:red;font-size:12pt;font-Style:italic;border:2px solid blue"&gt;
This text is inside a DIV element in the primary document.
&lt;BR&gt;
&lt;!-- this is a custom element --&gt;
&lt;myns:abc&gt;&lt;/myns:abc&gt;
&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=The next code snippet shows the content of the HTC file,  <code>viewInheritStyle.htc</code>.

The HTC file contains a simple document fragment, which also includes a '''div''' tag that uses the following CSS styles.

<li>
[[css/properties/font-size|'''fontSize''']] is set to 20 pt.</li>
<li>
[[css/properties/border|'''border''']] is set to 2px solid green.</li>

Because the content in the primary document has CSS styles set on a '''div''' tag that contains the custom element, the '''div''' tag in the document fragment  inherits the inheritable CSS Styles when the '''viewInheritStyle''' property is true.
|Code=&lt;public:component tagName{{=}}"abc"&gt;
&lt;attach event{{=}}"oncontentready" onevent{{=}}init() /&gt;
&lt;/public:component&gt;
&lt;script&gt; 
function init(){
defaults.viewLink{{=}}document;
defaults.viewInheritStyle {{=}} false;
docFragCaption.innerText {{=}} "viewInheritStyle is now set to false";
}

function btnChangeInheritance_onClick(){
boolInherit {{=}} defaults.viewInheritStyle;

	if (boolInherit {{=}}{{=}} true) {
	defaults.viewInheritStyle {{=}} false;
	docFragCaption.innerText {{=}} "viewInheritStyle is now set to false";
	}
	else
	{
	defaults.viewInheritStyle {{=}} true;
	docFragCaption.innerText {{=}} "viewInheritStyle is now set to true";
	}
}
&lt;/script&gt;
&lt;BODY&gt;
&lt;DIV id{{=}}"docFragCaption" style{{=}} "font-size:20pt;border:2px solid green"&gt;&lt;/DIV&gt;
&lt;BR&gt;
&lt;INPUT id{{=}}btnChangeInheritance type{{=}}button value{{=}}"Toggle viewInheritStyle property" onclick{{=}}"btnChangeInheritance_onClick()"&gt;
&lt;/BODY&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
For more information on the CSS styles that can be inherited when '''viewInheritStyle''' is set to true, see About Viewlink CSS Inheritance. Inheritable CSS styles are only applied to elements in the document fragment that do not already have the corresponding CSS styles defined.
|Import_Notes====Syntax===
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
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>Conceptual</code>
*<code>Introduction to Viewlink</code>
*<code>About Viewlink CSS Inheritance</code>
*<code>About Element Behaviors</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}