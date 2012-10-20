{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Non standard. Sets or retrieves the location of the Dynamic HTML (DHTML) behavior.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples demonstrate various ways of applying the '''-ms-behavior''' property on a page.
|Code=&lt;ul&gt;
  &lt;li style{{=}}"behavior:url(ul.htc) url(hilite.htc)"&gt;HTML&lt;/li&gt;
  &lt;ul&gt;
      &lt;li&gt;Internet Explorer authoring tips&lt;/li&gt;
	  :
  &lt;/ul&gt;
&lt;/ul&gt;
|LiveURL=This example implements an expanding and collapsing table of contents by applying the behavior as an inline style to the '''li''' element. In this case, two behaviors implemented as HTC have been applied to the element to achieve a combination of mouseover highlighting and expanding/collapsing effect.
}}{{Single Example
|Language=HTML
|Description=This example defines the '''-ms-behavior''' attribute in a separate 					'''style''' block.
|Code=&lt;style&gt;
   .CollapsingAndHiliting {behavior:url(ul.htc) url(hilite.htc)} 
&lt;/style&gt;
&lt;ul&gt;
  &lt;li class{{=}}"CollapsingAndHiliting"&gt;HTML&lt;/li&gt;
  &lt;ul&gt;
      &lt;li&gt;Internet Explorer authoring tips&lt;/li&gt;
	  :
  &lt;/ul&gt;
&lt;/ul&gt;
}}{{Single Example
|Language=HTML
|Description=This example sets the '''-ms-behavior''' property in script.
|Code=&lt;script&gt;
   function window.onload()
   {
      idTopic1.style.behavior {{=}} "url(ul.htc) url(hilite.htc)";
   }
&lt;/script&gt;
 :
&lt;ul&gt;
  &lt;li id{{=}}idTopic1&gt;HTML Authoring&lt;/li&gt;
  &lt;ul&gt;
      &lt;li&gt;Internet Explorer authoring tips&lt;/li&gt;
	  :
  &lt;/ul&gt;
&lt;/ul&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/components/htc/toc/toc.htm
}}{{Single Example
|Language=HTML
|Description=If the expanding/collapsing example were to use a DHTML behavior implemented in C++ as an ActiveX control, the code would look slightly different. In this example, the '''-ms-behavior''' attribute points to the [[html/attributes/id|'''id''']] property of the object specified in the '''object''' element.
|Code=&lt;style&gt;
   .Collapsing { behavior:url(#myObject) }
&lt;/style&gt;
&lt;object id{{=}}myObject ... &gt;&lt;/object&gt;
&lt;ul&gt;
  &lt;li class{{=}}"Collapsing"&gt;HTML Authoring&lt;/li&gt;
  &lt;ul&gt;
      &lt;li&gt;Internet Explorer authoring tips&lt;/li&gt;
	  :
  &lt;/ul&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
You can apply multiple behaviors to an element by specifying a space-delimited list of URLs for the '''-ms-behavior''' attribute, as shown in the following syntax:
 <code>&lt;element style{{=}}"behavior:url(a1.htc) url(a2.htc) ..." &gt;</code>
In the following section, one example demonstrates how you can apply two behaviors to an element to achieve a combination of effects. Conflicts resulting from applying multiple behaviors to an element are resolved based on the order in which the behavior is applied to the element. Each succeeding behavior takes precedence over the previous behavior. For example, if multiple behaviors set the element's color, the prevailing color is the one set by the behavior last applied to the element. The same rule applies in resolving name conflicts, such as with property, method, or event names exposed by multiple behaviors.
Once the '''-ms-behavior''' property is defined for the element, the '''addBehavior''' method can be used to dynamically attach additional behaviors to the element.
'''Note'''  A behavior attached to an element by using the '''addBehavior''' method or by applying the proposed Cascading Style Sheets (CSS) '''-ms-behavior''' attribute inline is not automatically detached from the element when the element is removed from the document hierarchy. However, a behavior attached using a style rule defined in the document is detached automatically as the element is removed from the document tree.
Windows Internet Explorer 8. The '''-ms-behavior''' attribute is an extension to CSS, and can be used as a synonym for '''behavior''' in IE8 Standards mode.
|Import_Notes====Syntax===
<code>'''-ms-behavior: '''url(sLocation) '''{{!}}''' url(#objID) '''{{!}}''' url(#default#behaviorName)</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Media Queries
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>Using DHTML Behaviors</code>
*<code>Other Resources</code>
*<code>[http://go.microsoft.com/fwlink/p/?linkid{{=}}203734 Behavioral Extensions to CSS]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}