{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add specification and compatibility.
'''As of time of writing, this property is not yet implemented in most browsers.'''
|Checked_Out=No
|Content=Examples Needed
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Defines whether the content of the <mask> element is treated as as luminance mask or an alpha mask.}}
{{CSS Property
|Initial value=luminance
|Applies to=<mask> elements.
|Inherited=No
|Media=visual
|Computed value=the unique non-ambiguous order defined by the formal grammar
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=luminance
|Description=Indicates that the luminance values of the mask should be used.
}}{{CSS Property Value
|Data Type=alpha
|Description=Indicates that the alpha values of the mask should be used.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Alpha mask type
|Code=<!-- alpha -->
<mask style="mask-type: alpha">
        <circle cx="50%" cy="50%" r="50%"/>
</mask>
}}{{Single Example
|Language=CSS
|Description=Luminance mask type
|Code=<!-- luminance -->
<mask style="mask-type: luminance">
        <circle cx="50%" cy="50%" r="50%" fill="white"/>
</mask>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Masking Level 1
|URL=http://www.w3.org/TR/css-masking-1/
|Status=W3C Last Call Working Draft
}}{{Related Specification
|Name=CSS Masking Level 1
|URL=http://dev.w3.org/fxtf/css-masking-1/
|Status=W3C Editor’s Draft
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
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}