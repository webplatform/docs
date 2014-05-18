{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Needs Review
|Content=Incomplete, Compatibility Incomplete, Examples Needed, Examples Best Practices, Needs Summary
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The '''sizes''' attribute is an extension of the [[html/elements/img|image element]]. It provides additional image related information to the browser to help decide the most appropriate image to load based on the viewport. Most commonly used for delivering the best image for responsive images. It can only be used in conjunction with '''[[html/attributes/srcset|scrset]]'''}}
{{Markup_Attribute
|Applies_to=dom/HTMLImageElement
|Property_applies_to=dom/HTMLImageElement
|Content='''sizes''' attribute is an extension of the of the [[html/elements/img|image element]] and is used to inform the browser which [[html/attributes/srcset|srcset]] image source to render based on the rules set out. '''sizes''' do not provide an instruction to the browser (''must'' use ''this'' image ''here'') but rather“''here is a viewport condition, use the best suited image based on your viewport, device pixel ration along with the width I said the image is going to be''”.



    sizes="[media query] [length], [media query] [length]"

Lengths can be declared using fixed widths (pixels) or relative units ('''vw''' or viewport width).  When declaring '''sizes''' it is recommended that the final '''vw''' unit be declared as 100vw to cover all of the '''sizes''' you do not consider.

    sizes="(min-width:30em) 300px, (min-width:60em) 500px, 100vw"
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Sizes attribute used in conjunction with SRCSET
|Code=http://codepen.io/justincavery/full/vjAgF/
|LiveURL=http://codepen.io/justincavery/full/vjAgF/
}}
}}
{{Notes_Section
|Usage='''sizes''' attribute is used along side '''[[html/attributes/srcset|scrset]]'''.
|Notes=It is recommended that the final sizes value is 
   sizes="[first sizes], [second to last sizes], 100vw"
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}