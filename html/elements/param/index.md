{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add Category, Parent and Children information. Complete Compatibility table. Complete HTML information subsection.
Add history information.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This element defines parameters for plugins invoked by object elements.}}
{{Markup_Element
|DOM_interface=dom/HTMLParamElement
|Tag_omissions=No closing tag (self-closing)
|CSS_display=none
|Content=== Attributes ==

*<code>name</code> = name of the parameter<br />Gives the name of the parameter.<br />This attribute must be present.
*<code>value</code> = value of the parameter<br />Gives the value of the parameter.<br />This attribute must be present.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example displays the Internet Explorer Data Binding component's [[dom/properties/outerdom/outerHTML|'''outerHTML''']] so you can view the properties assigned by the '''PARAM''' elements.  You can perform this check to gather information when debugging an '''OBJECT''' element's properties.  You cannot edit the object's '''outerHTML''' property without reintializing the '''outerHTML''' object.
|Code=// The OBJECT CLASSID below is for the 
// Microsoft Internet Explorer Data Binding component
// Use just the following HTML and press the button
&lt;OBJECT                 
 ID{{=}}tdcContents
 CLASSID{{=}}"clsid:333C7BC4-460F-11D0-BC04-0080C7055A83"&gt;
  &lt;PARAM NAME{{=}}"DataURL" VALUE{{=}}"DataBinding.csv"&gt;								  
&lt;/OBJECT&gt;
&lt;BUTTON onclick{{=}}"oTxt.value{{=}}tdcContents.outerHTML"&gt;
Show Object outerHTML&lt;/BUTTON&gt;&lt;BR/&gt;
&lt;TEXTAREA ID{{=}}"oTxt"  STYLE{{=}}"height:400; width:450;padding:3; overflow{{=}}auto;"&gt; &lt;/TEXTAREA&gt;
//When the button is pressed the complete list of the object's
// PARAM elements display unformatted in the TEXTAREA as follows:
 
&lt;OBJECT id{{=}}tdcContents classid{{=}}clsid:333C7BC4-460F-11D0-BC04-0080C7055A83&gt;
&lt;PARAM NAME{{=}}"RowDelim" VALUE{{=}}"&amp;#10;"&gt;&lt;PARAM NAME{{=}}"FieldDelim" VALUE{{=}}","&gt;
&lt;PARAM NAME{{=}}"TextQualifier" VALUE{{=}}'"'&gt;&lt;PARAM NAME{{=}}"EscapeChar" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"UseHeader" VALUE{{=}}"0"&gt;&lt;PARAM NAME{{=}}"SortAscending" VALUE{{=}}"-1"&gt;
&lt;PARAM NAME{{=}}"SortColumn" VALUE{{=}}""&gt;&lt;PARAM NAME{{=}}"FilterValue" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"FilterCriterion" VALUE{{=}}"??"&gt;&lt;PARAM NAME{{=}}"FilterColumn" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"CharSet" VALUE{{=}}""&gt;&lt;PARAM NAME{{=}}"Language" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"CaseSensitive" VALUE{{=}}"-1"&gt;&lt;PARAM NAME{{=}}"Sort" VALUE{{=}}""&gt;
&lt;PARAM NAME{{=}}"Filter" VALUE{{=}}""&gt;&lt;PARAM NAME{{=}}"AppendData" VALUE{{=}}"0"&gt;
&lt;PARAM NAME{{=}}"DataURL" VALUE{{=}}"DataBinding.csv"&gt;
&lt;PARAM NAME{{=}}"ReadyState" VALUE{{=}}"4"&gt;
&lt;/OBJECT&gt;
}}{{Single Example
|Language=HTML
|Description=The following example shows how the param element can be used to pass a parameter to a plugin, in this case the O3D plugin
|Code=<nowiki>
<!DOCTYPE HTML>
<html lang="en">
  <head>
   <title>O3D Utah Teapot</title>
  </head>
  <body>
   <p>
    <object type="application/vnd.o3d.auto">
     <param name="o3d_features" value="FloatingPointTextures">
     <img src="o3d-teapot.png"
          title="3D Utah Teapot illustration rendered using O3D."
          alt="When O3D renders the Utah Teapot, it appears as a squat
          teapot with a shiny metallic finish on which the
          surroundings are reflected, with a faint shadow caused by
          the lighting.">
     <p>To see the teapot actually rendered by O3D on your
     computer, please download and install the <a href="http://code.google.com/apis/o3d/docs/gettingstarted.html#install">O3D plugin</a>.</p>
    </object>
    <script src="o3d-teapot.js"></script>
   </p>
  </body>
</html></nowiki>
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''PARAM''' element is valid within the '''APPLET''', '''EMBED''', and '''OBJECT''' elements.
'''Note'''  Properties set by a '''PARAM''' element cannot be altered by changing the '''PARAM''' object.
After the '''APPLET''', '''EMBED''', or '''OBJECT''' element is instantiated, the property set by the '''PARAM''' element cannot be changed with the '''param''' object.  To change the object's properties, use the script properties exposed by the object.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-param-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-param-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/objects.html#edef-PARAM
|Status=W3C Recommendation
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}