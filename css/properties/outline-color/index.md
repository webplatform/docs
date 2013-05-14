{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The outline-color CSS property sets the color of the [[css/properties/outline|outline]] of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.}}
{{CSS Property
|Initial value=Invert
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=The computed value for ‘invert’ is ‘invert’. For <color> values, the computed value is as defined for the ‘color’ property.
|Animatable=No
|CSS object model property=outlineColor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<color>
|Description=Specify the color to use on all outlines. This can be anywhere from one to four values representing the top, right, bottom, and left outline respectively.
}}{{CSS Property Value
|Data Type=inherit
|Description=This is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}{{CSS Property Value
|Data Type=Invert
|Description=This is expected to perform a color inversion on the pixels on the screen.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=An example of using outline color
|Code=&lt;div class=&quot;outline&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt; 
&lt;div class=&quot;outline outline--blue&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt;
&lt;div class=&quot;outline outline--green&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt; 
&lt;div class=&quot;outline outline--invert&quot;&gt;I &hearts; WebPlatform.org!&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5566688
}}{{Single Example
|Language=CSS
|Description=Multiple classes that change the original outline color
|Code=/*
  outline color example
*/

.outline--green {
  /* make the outline red */
  outline-color: #00ff00;
}

.outline--blue {
  /* make the outline blue */
  outline-color: #0000ff;
}

.outline--invert {
	/* outline invert */
	outline-color: invert;
}
|LiveURL=http://code.webplatform.org/gist/5566688
}}
}}
{{Notes_Section
|Notes====Remarks===
A value of '''invert''' ensures that the outline
is visible regardless of the background color.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''outline-color: '''''
&lt;color&gt;
'' '''{{!}}''' invert</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 18.4
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
|Topic_clusters=Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/selectors/outline|outline]]</code>
*<code>[[css/selectors/outline-style|outline-style]]</code>
*<code>[[css/selectors/outline-width|outline-width]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/outline-color
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}