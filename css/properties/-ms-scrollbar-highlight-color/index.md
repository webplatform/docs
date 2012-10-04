{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to create a style rule that sets the '''-ms-scrollbar-highlight-color''' property for a '''textArea''' element.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollbarColor.htm
|Code=
&lt;HTML&gt;
  &lt;HEAD&gt;
    &lt;STYLE&gt;
        TEXTAREA.BlueHighlight  { scrollbar-highlight-color:blue }
    &lt;/STYLE&gt;
  &lt;/HEAD&gt;
  &lt;BODY&gt;
    &lt;TEXTAREA CLASS{{=}}"BlueHighlight"&gt;The scroll bar face for this 
    element will turn blue when a scroll bar button is pressed.
  &lt;/TEXTAREA&gt;
  &lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-scrollbar-highlight-color''' attribute is an extension to CSS, and can be used as a synonym for '''scrollbar-highlight-color''' in IE8 Standards mode.
The scroll box is the square box within a scroll bar that can be moved either up and down or left and right on a track to change the position of the content on the screen. The scroll arrows, located at each end of a scroll bar, are the square buttons containing the arrows that move the content on the screen in small increments, either up and down or left and right.
This property applies to elements that display a scroll bar.  Cascading Style Sheets (CSS) enable scrolling on all objects through the [[css/properties/overflow|'''overflow''']] property.  These objects are not listed in the Applies To list for this property.
|Import_Notes=
===Syntax===
<code>'''-ms-scrollbar-highlight-color: '''variant</code>
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/selectors/-ms-scrollbar-3d-light-color|-ms-scrollbar-3dlight-color]]</code>
*<code>[[css/selectors/-ms-scrollbar-arrow-color|-ms-scrollbar-arrow-color]]</code>
*<code>[[css/selectors/-ms-scrollbar-base-color|-ms-scrollbar-base-color]]</code>
*<code>[[css/selectors/-ms-scrollbar-darkshadow-color|-ms-scrollbar-darkshadow-color]]</code>
*<code>[[css/selectors/-ms-scrollbar-face-color|-ms-scrollbar-face-color]]</code>
*<code>[[css/selectors/-ms-scrollbar-shadow-color|-ms-scrollbar-shadow-color]]</code>
*<code>[[css/selectors/-ms-scrollbar-track-color|-ms-scrollbar-track-color]]</code>
|Topic_clusters=Scrollbar
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}