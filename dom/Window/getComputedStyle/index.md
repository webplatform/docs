{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets the computed style declaration of an element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=element
|Data type=DOM Node
|Description=The element that contains the desired style settings.
|Optional=No
}}{{Method Parameter
|Name=pseudoElementName
|Data type=String
|Description=The name of a CSS pseudo-element or a null value.
Optional in WebKit based browsers.
|Optional=No
}}
|Method_applies_to=dom/window
|Example_object_name=window
|Return_value_name=declaration
|Javascript_data_type=DOM Node
|Return_value_description=A [[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']] object that contains the CSS settings applied to the desired object.

The settings in the returned object account for all applicable style rules and represent the final values for the various CSS properties applied to the specified object.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=When the ''pseudoElementName'' is set to a value other than null, the value is interpreted as a CSS pseudo-element with respect to the object specified in the ''element'' parameter.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html
|Status=Recommendation
|Relevant_changes=Section 2.2.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/window|window]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|HTML5Rocks_link=
}}