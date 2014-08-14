{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add values/parameters, syntax, example, compatibility.
|Checked_Out=No
|High-level issues=Stub, Missing Relevant Sections
|Content=Incomplete
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Allows authors to reference the value of a custom property for cascading variables.}}
{{CSS_Function
|Content===Syntax==
* '''var ( <custom-property> )'''
* '''var ( <custom-property>, <default-value> )'''

==Parameters==
'''custom-property'''

''The name of the custom property to use.''

'''default-value'''

''A value to use when the custom property isn't defined.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.block .header {  
	/* use a variable for the text color of the header, with default 'blue' */
	color: var(--header-color, blue);
	
	/* use a variable for the background color of the header, with default 'blue' */
	background-color: var(--text-color, blue);
	
	padding: 1em;
}

.block .contents{  
	/* use a variable for the text color of the contents, with default 'red' */
	color: var(--text-color, red);
	padding: 1em;
}

.block{  
	/* only the --text-color variable is set, so the --header-color will show it's default 'blue' */
	--text-color: green;  
}
|LiveURL=http://code.webplatform.org/gist/a41474c974dfef4ec106
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Custom Properties for Cascading Variables Module Level 1
|URL=http://www.w3.org/TR/css-variables-1/
|Status=W3C Last Call Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table}}
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
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