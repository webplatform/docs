{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Complete compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>font-weight</code> property specifies the weight or boldness of the font (their degree of blackness or stroke thickness). Note that some fonts are not available in all weights; some are available only on '''normal''' and '''bold'''.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=The keyword or the numerical value as specified, with bolder and lighter transformed to the real value.
|Animatable=Yes
|CSS object model property=fontWeight
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Normal font weight. Same as '''400'''.
}}{{CSS Property Value
|Data Type=bold
|Description=Bold font weight. Same as '''700'''.
}}{{CSS Property Value
|Data Type=lighter
|Description=One font weight lighter than the parent element (among the available weights of the font).
}}{{CSS Property Value
|Data Type=bolder
|Description=One font weight darker than the parent element (among the available weights of the font).
}}{{CSS Property Value
|Data Type=100, 200, 300, 400, 500, 600, 700, 800, 900
|Description=Numeric font weights for fonts that provide more than just normal and bold. If the exact weight given is unavailable, a face with a nearby weight is used.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A selection of examples showing some typical uses of the font-weight property. In practise, you most probably won't see much difference when using any  values except for <code>normal</code> and <code>bold</code>.
|Code=&lt;p class="example-one"&gt;Set text to be bold.&lt;/p&gt;
&lt;p class="example-two"&gt;Set text to two step darker than normal but less than a standard bold.&lt;/p&gt;
&lt;p class="example-three"&gt;Sets text to be one step lighter than the parent.&lt;/p&gt;
}}{{Single Example
|Language=CSS
|Code=p { font-size: 150%; }

p.example-one { font-weight: bold; }
p.example-two { font-weight: 600; }
p.example-three { font-weight: lighter; }
|LiveURL=http://code.webplatform.org/gist/5628518
}}
}}
{{Notes_Section
|Usage=Quite often there are only a few weights available for a particular font family. When a weight is specified for which no face exists, a face with a nearby weight is used:<br />
'''600-900''' use the closest available darker weight (or, if there is none, the closest available lighter weight).<br />
'''100-500''' use the closest available lighter weight (or, if there is none, the closest available darker weight).<br />
This means that for fonts that provide only normal and bold, '''100-500''' are normal, and '''600-900''' are bold.

Although the practice — also called “Faux bold” — is not well-loved by typographers, bold faces are often synthesized by user agents for faces that lack actual bold faces.

'''100''' to '''900'''<br />
These values form an ordered sequence, where each number indicates a weight that is at least as dark as its predecessor. These roughly correspond to the commonly used weight names below:

* '''100''' - Thin
* '''200''' - Extra Light (Ultra Light)
* '''300''' - Light
* '''400''' - Normal
* '''500''' - Medium
* '''600''' - Semi Bold (Demi Bold)
* '''700''' - Bold
* '''800''' - Extra Bold (Ultra Bold)
* '''900''' - Black (Heavy)
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/#font-weight-prop
|Status=W3C Working Draft
|Relevant_changes=No change.
}}{{Related Specification
|Name=CSS Transitions
|URL=http://www.w3.org/TR/css3-transitions/#animatable-css
|Status=W3C Working Draft
|Relevant_changes=Defines font-weight as animatable.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=2.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.3
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.1
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts, Text
|External_links=* A List Apart: [http://alistapart.com/article/say-no-to-faux-bold Say No to Faux Bold]
* Mozilla: [http://mxr.mozilla.org/mozilla/source/layout/style/html.css default style sheet]
* WebKit: [http://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css default style sheet]
* IECSS: [http://www.iecss.com/ Internet Explorer User Agent Style Sheets]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/font-weight
|MSDN_link=
|HTML5Rocks_link=
}}