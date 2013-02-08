{{Page_Title|border-image-slice}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=100%
|Applies to=all elements, except internal table elements when <code>border-collapse</code> is set to <code>collapse</code>.
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=slice
|Description=Is a <code><number></code> or a <code><percentage></code> of the offset for the four slicing lines. Note that a <code><length></code> value is not allowed, and therefore invalid. The <code><number></code> represents pixels for raster images and coordinates for vector images. Also, <percentage> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to 100%.
}}{{CSS Property Value
|Data Type=horizontal
|Description=Is a <code><number></code> or a <code><percentage></code> of the offset for the two horizontal slicing lines, the top and the bottom ones. Note that a <code><length></code> value is not allowed, and therefore invalid. The <code><number></code> represents pixels for raster images and coordinates for vector images. Also, <percentage> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to <code>100%</code>.

}}{{CSS Property Value
|Data Type=vertical
|Description=Is a <code><number></code> or a <code><percentage></code> of the offset for the two vertical slicing lines, the right and the left ones. Note that a <length> value is not allowed, and therefore invalid. The <code><number></code> represents pixels for raster images and coordinates for vector images. Also, <code><percentage></code> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to <code>100%</code>.
}}{{CSS Property Value
|Data Type=top
|Description=Is a <number> or a <percentage> of the offset for the top slicing line. Note that a <length> value is not allowed, and therefore invalid. The <number> represents pixels for raster images and coordinates for vector images. Also, <percentage> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to 100%.
}}{{CSS Property Value
|Data Type=bottom
|Description=Is a <number> or a <percentage> of the offset for the bottom slicing line. Note that a <length> value is not allowed, and therefore invalid. The <number> represents pixels for raster images and coordinates for vector images. Also, <percentage> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to 100%.
}}{{CSS Property Value
|Data Type=right
|Description=Is a <number> or a <percentage> of the offset for the right slicing line. Note that a <length> value is not allowed, and therefore invalid. The <number> represents pixels for raster images and coordinates for vector images. Also, <percentage> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to 100%.
}}{{CSS Property Value
|Data Type=left
|Description=Is a <number> or a <percentage> of the offset for the left slicing line. Note that a <length> value is not allowed, and therefore invalid. The <number> represents pixels for raster images and coordinates for vector images. Also, <percentage> values are relative to the height or width of the image, whichever is adequate. Negative values are invalid and values greater than the relevant size, height or width, are clamped to 100%.
}}{{CSS Property Value
|Data Type=fill
|Description=Is a keyword whose presence forces the use of the middle image slice to be displayed over the background image, its size and height are resized like those of the top and left image slices, respectively.
}}{{CSS Property Value
|Data Type=inherit
|Description=Is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
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
|Topic_clusters=Border
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/border-image-slice
|MSDN_link=
|HTML5Rocks_link=
}}