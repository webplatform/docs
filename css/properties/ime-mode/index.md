{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. IME is not affected. This is the same as not specifying the '''-ms-ime-mode''' attribute.}}
{{CSS_Property_Value|Data Type=active |Description=All characters are entered through the IME. Users can still deactivate the IME.}}
{{CSS_Property_Value|Data Type=inactive |Description=All characters are entered without IME. Users can still activate the IME.}}
{{CSS_Property_Value|Data Type=disabled |Description=IME is completely disabled. Users cannot activate the IME if the control has focus.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''-ms-ime-mode''' attribute.
|LiveURL=
|Code=
&lt;INPUT TYPE {{=}} text STYLE {{=}} "ime-mode:active" &gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-ime-mode''' attribute is an extension to CSS, and can  be used as a synonym for '''ime-mode''' in IE8 Standards mode.
An IME allows users to enter and edit Chinese, Japanese, and Korean characters. The IME is an essential component for writing Chinese, Japanese, and Korean scripts. These writing systems have more characters than can be encoded for a regular keyboard. The IMEs for these languages use sequences of base characters that describe an individual character or group of characters to enter a larger set of characters. Base characters can be component letters from Hangul syllables, phonetic components for Japanese Kanji characters, or various combinations for Chinese characters.
To compose text with an IME, the user generally uses dictionary lookup and contextual analysis, especially in languages where homonyms are frequent, as in Japanese. A user typically starts by entering a few component characters, optionally selecting from various choices, and a confirmation command.
Input Method Editors have two principle states:
*Inactive mode. The keyboard acts like a regular keyboard and input is limited to a small set of characters.
*Active mode. The IME accepts component characters or processing commands.

HTML authors can provide users with some control by specifying an IME mode for a specific text entry. For example, if Japanese users enter information in a registration form, they might be required to enter their names in Kanji and Roman characters. By default, the users would have to make sure that the IME is inactive when entering their names in the Latin alphabet. The user would activate the IME to enter Kanji letters, then deactivate the IME to complete the form in the Latin alphabet. By controlling the IME mode, the HTML author prevents the user from having to activate and deactivate the IME.
|Import_Notes=
===Syntax===
<code>'''-ms-ime-mode: '''auto '''{{!}}''' active '''{{!}}''' inactive '''{{!}}''' disabled</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}