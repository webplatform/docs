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



    sizes="[media query] [length], [media query] [length] ... etc"
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
|Usage='''sizes''' attribute is used along side '''[[html/attributes/srcset]]'''. The
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