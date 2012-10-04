{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''-ms-accelerator''' attribute in a '''u''' element to specify that the <code>N</code> in the '''label''' element is a keyboard shortcut.  When the option to "Hide keyboard navigation indicators until I use the Alt key" is enabled in the user's Display Properties, the <code>N</code> is not underlined until the user presses the ALT key. When ALT+N is pressed, the '''input''' element that defines an [[html/attributes/accessKey|'''accessKey''']] attribute value of 'N' receives the focus.
|LiveURL=
|Code=
&lt;LABEL FOR{{=}}"oName"&gt;&lt;U STYLE{{=}}"ACCELERATOR:true"&gt;N&lt;/U&gt;ame: &lt;/LABEL&gt;
&lt;INPUT TYPE{{=}}"text" 	
    ID{{=}}"oName" 
    SIZE{{=}}"25"
    ACCESSKEY{{=}}"N" 
    VALUE{{=}}"Your name here"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property is supported by Windows 2000 and later, which enables users to hide navigation indicators for menu items and controls until the ALT key is pressed.
An access key is a single character used as a keyboard shortcut for selecting an object. Press and hold the ALT key followed by the character to move input focus and invoke the default event associated with an object.
Windows Internet Explorer 8. The '''-ms-accelerator''' attribute is an extension to CSS, and can be used as a synonym for '''accelerator''' in IE8 Standards mode.
|Import_Notes=
===Syntax===
<code>'''-ms-accelerator: '''false '''{{!}}''' true</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[html/attributes/accessKey|accessKey]]</code>
|Topic_clusters=Media Queries
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}