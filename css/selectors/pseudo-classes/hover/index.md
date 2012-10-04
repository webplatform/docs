{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example sets the hover style of an anchor. When the user hovers the mouse pointer over a link, the text appears in bold red, over a beige background.
|LiveURL=Click to view sample.
|Code=
&lt;style&gt;
    a:hover { color:red; background-color:beige; font-weight:bolder; }
&lt;/style&gt;
&lt;a href{{=}}"#below"&gt;Click here to move to the bottom of this page.&lt;/a&gt;
&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;
&lt;a name{{=}}"below"&gt;&lt;/a&gt; 
}}
{{Single_Example
|Description=The following example demonstrates the type of effects you can achieve without script by using the ''':hover''' pseudo-class in Internet Explorer 7.
|LiveURL=Click to view sample.
|Code=
&lt;!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Strict//EN"&gt;
&lt;html&gt;
&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
    body:hover { background: url("wlbigielogo.gif") no-repeat center center; }
    h1:hover   { color: red; }
    img        { vertical-align: middle; }
    .zoom img  { zoom: 0.5; }
    img:hover  { zoom: 1.0; cursor: hand; }
    img.spacer { width: 0px; height: 30px; }
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;h1&gt;Hover Here&lt;/h1&gt;
&lt;img class{{=}}"spacer" src{{=}}"blank.gif"&gt;
&lt;span class{{=}}"zoom"&gt;
&lt;img src{{=}}"A.gif"&gt;
&lt;img src{{=}}"B.gif"&gt;
&lt;img src{{=}}"C.gif"&gt;
. . .
&lt;img src{{=}}"X.gif"&gt;
&lt;img src{{=}}"Y.gif"&gt;
&lt;img src{{=}}"Z.gif"&gt;
&lt;/span&gt;
&lt;/body&gt;&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
Hover means that the user has positioned the mouse pointer over the element but has not clicked, or otherwise activated the element. If the user simply passes the mouse pointer over a link, for example, the style reverts to its usual state when the mouse pointer is removed. The ''':hover''' pseudo-class is often used with [[css/selectors/pseudo-classes/:active|''':active''']], [[css/selectors/pseudo-classes/:link|''':link''']], and [[css/selectors/pseudo-classes/:visited|''':visited''']]; which are the pseudo-classes that affect the other states of a link.
'''Note'''   The order of pseudo-classes is important. For example, the style rule for ''':hover''' must occur after any [[css/selectors/pseudo-classes/:link|''':link''']] rule or any [[css/selectors/pseudo-classes/:visited|''':visited''']] rule to prevent the pseudo-classes from hiding each other.
Starting with
Windows Internet Explorer 7, when the browser is in standards-compliant mode (strict [[html/elements/!DOCTYPE|!DOCTYPE]]), you can apply the ''':hover''' pseudo-class to any element, not only links. If the pseudo-class is not applied specifically to an element in the selector, such as the [[html/elements/a|'''a''']] tag, the [[css/selectors/Universal|Universal (*) Selector]] is assumed. Indiscriminate use of the ''':hover''' pseudo-class can negatively impact page performance.
|Import_Notes=
===Syntax===

selector
:hover
===Parameters===
;''selector'':A CSS simple selector
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.11.3


}}
{{See_Also_Section
|Topic_clusters=Selectors, Pseudo-Classes
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}