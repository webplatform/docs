{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=normal
|Applies to=All HTML elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=This is the default attribute which specifies no blending. The blending formula simply selects the source color.
}}{{CSS Property Value
|Data Type=multiply
|Description=The source color is multiplied by the destination color and replaces the destination.

The resultant color is always at least as dark as either the source or destination color. Multiplying any color with black results in black. Multiplying any color with white preserves the original color.
}}{{CSS Property Value
|Data Type=screen
|Description=Multiplies the complements of the backdrop and source color values, then complements the result.

The result color is always at least as light as either of the two constituent colors. Screening any color with white produces white; screening with black leaves the original color unchanged. The effect is similar to projecting multiple photographic slides simultaneously onto a single screen.
}}{{CSS Property Value
|Data Type=overlay
|Description=Multiplies or screens the colors, depending on the backdrop color value.

Source colors overlay the backdrop while preserving its highlights and shadows. The backdrop color is not replaced but is mixed with the source color to reflect the lightness or darkness of the backdrop.
}}{{CSS Property Value
|Data Type=darken
|Description=The backdrop is replaced with the source where the source is darker; otherwise, it is left unchanged.
}}{{CSS Property Value
|Data Type=lighten
|Description=Selects the lighter of the backdrop and source colors.

The backdrop is replaced with the source where the source is lighter; otherwise, it is left unchanged.
}}{{CSS Property Value
|Data Type=color-dodge
|Description=Brightens the backdrop color to reflect the source color. Painting with black produces no changes.
}}{{CSS Property Value
|Data Type=color-burn
|Description=Darkens the backdrop color to reflect the source color. Painting with white produces no change.
}}{{CSS Property Value
|Data Type=hard-light
|Description=Multiplies or screens the colors, depending on the source color value. The effect is similar to shining a harsh spotlight on the backdrop.
}}{{CSS Property Value
|Data Type=soft-light
|Description=Darkens or lightens the colors, depending on the source color value. The effect is similar to shining a diffused spotlight on the backdrop.
}}{{CSS Property Value
|Data Type=difference
|Description=Subtracts the darker of the two constituent colors from the lighter color.

Painting with white inverts the backdrop color; painting with black produces no change.
}}{{CSS Property Value
|Data Type=exclusion
|Description=Produces an effect similar to that of the Difference mode but lower in contrast. Painting with white inverts the backdrop color; painting with black produces no change.
}}{{CSS Property Value
|Data Type=hue
|Description=Creates a color with the hue of the source color and the saturation and luminosity of the backdrop color.
}}{{CSS Property Value
|Data Type=saturation
|Description=Creates a color with the saturation of the source color and the hue and luminosity of the backdrop color. Painting with this mode in an area of the backdrop that is a pure gray (no saturation) produces no change.
}}{{CSS Property Value
|Data Type=color
|Description=Creates a color with the hue and saturation of the source color and the luminosity of the backdrop color. This preserves the gray levels of the backdrop and is useful for coloring monochrome images or tinting color images.
}}{{CSS Property Value
|Data Type=luminosity
|Description=Creates a color with the luminosity of the source color and the hue and saturation of the backdrop color. This produces an inverse effect to that of the Color mode.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The ‘background-blend-mode’ list must be applied in the same order as ‘background-image’. This means that the first element in the list will apply to the layer that is on top. If a property doesn't have enough comma-separated values to match the number of layers, the UA must calculate its used value by repeating the list of values until there are enough.

If the ‘background’ shorthand is used, the ‘background-blend-mode’ property for that element must be reset to its initial value.
|Notes=**Separable blend modes**
*(normal, multiply, screen, overlay, darken, lighten, color-dodge, color-burn, hard-light, soft-light, difference, exclusion)*

A blend mode is termed separable if each component of the result color is completely determined by the corresponding components of the constituent backdrop and source colors — that is, if the mixing formula is applied separately to each set of corresponding components.

**Non-separable blend modes**
*(hue, saturation, color, luminosity)*

Nonseparable blend modes consider all color components in combination as opposed to the seperable ones that look at each component individually.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Compositing and Blending Level 1
|URL=http://www.w3.org/TR/compositing/#blending
|Status=Working Draft
}}
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