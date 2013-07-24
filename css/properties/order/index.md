{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''order''' property controls the order in which flex items appear within their flex container, by assigning them to ordinal groups.}}
{{CSS Property
|Initial value=0
|Applies to=flex items and absolutely-positioned flex container children
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=Yes
|CSS object model property=order
|Values={{CSS Property Value
|Data Type=<integer>
|Description=The ordinal group for this flex item.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children in custom sequence
|Code=.list {
  display: flex;
}
.list div {
  flex: 1;
}
.list .first {
  order: 3;
}
.list .second {
  order: 1;
}
.list .third {
  order: 2;
}
|LiveURL=http://code.webplatform.org/gist/4741023
}}{{Single Example
|Language=CSS
|Description=The Holy Grail Layout example. Given a source order of article-nav-aside, use order to rearrange these elements as flex items into nav-article-aside
|Code=article { order: 2; }
nav { order: 1; }
aside { order: 3; }
}}
}}
{{Notes_Section
|Notes=This property was previously named '''flex-order''' in earlier drafts.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#order-property
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=http://caniuse.com/#flexbox
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Flexbox
}}
{{Topics|CSS, Flexbox}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}