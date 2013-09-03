{{Page_Title|Font related properties}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets font-style, font-variant, font-weight, font-size/line-height, font-family properties in one declaration. 

The order is obligatory, not all options must be set.

''font-size'' and ''font-family'' are required options.
}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=<code>
  p {
  font: italic 1.2em/1.5 Georgia;
  }
</code>

<code>
  font: italic small-caps 1.2em/14px "Times New Roman";</code>

  font: bold 1.2em/2ex Arial;
|Import_Notes====In this section===
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[css/properties/font|'''font''']]
{{!}}Sets or retrieves a combination of separate [[css/properties/font|'''font''']] properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.Sets or retrieves a combination of separate '''font''' properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.
{{!}}-
{{!}}[[css/properties/font-family|'''font-family''']]
{{!}}Sets or retrieves  the name of the font used for text in the object.
{{!}}-
{{!}}[[css/properties/font-feature-settings|'''font-feature-settings''']]
{{!}}Gets or sets one or more values that specify glyph substitution and positioning in fonts that include OpenType layout features.
{{!}}-
{{!}}[[css/properties/font-size|'''font-size''']]
{{!}}Sets or retrieves  a value that indicates the font size used for text in the object.
{{!}}-
{{!}}[[css/properties/font-size-adjust|'''font-size-adjust''']]
{{!}}Sets or retrieves a value that specifies an aspect value for an element that will effectively preserve the x-height of the first choice font, whether it is substituted or not.
{{!}}-
{{!}}[[css/properties/font-stretch|'''font-stretch''']]
{{!}}Sets or retrieves a value that indicates a normal, condensed, or expanded face of a font family.
{{!}}-
{{!}}[[css/properties/font-style|'''font-style''']]
{{!}}Sets or retrieves  the font style of the object as '''italic''', '''normal''', or '''oblique'''.
{{!}}-
{{!}}[[css/fonts/font-variant|'''font-variant''']]
{{!}}Gets or sets  whether the text of the object is in small capital letters.
{{!}}-
{{!}}[[css/properties/font-weight|'''font-weight''']]
{{!}}Gets of sets  the weight of the font of the object.
{{!}}}
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
|Topic_clusters=Fonts
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}