---
title: param
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Add Category, Parent and Children information. Complete Compatibility table. Complete HTML information subsection.\nAdd history information."
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLParamElement](/dom/HTMLParamElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'This element defines parameters for plugins invoked by object elements.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/outerdom/outerHTML
uri: html/elements/param

---
## <span>Summary</span>

This element defines parameters for plugins invoked by object elements.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLParamElement](/dom/HTMLParamElement)

## <span>Attributes</span>

-   `name` = name of the parameter
    Gives the name of the parameter.
    This attribute must be present.
-   `value` = value of the parameter
    Gives the value of the parameter.
    This attribute must be present.

## <span>Examples</span>

This example displays the Internet Explorer Data Binding component's [**outerHTML**](/w/index.php?title=dom/properties/outerdom/outerHTML&action=edit&redlink=1) so you can view the properties assigned by the **PARAM** elements. You can perform this check to gather information when debugging an **OBJECT** element's properties. You cannot edit the object's **outerHTML** property without reintializing the **outerHTML** object.

``` html
// The OBJECT CLASSID below is for the
// Microsoft Internet Explorer Data Binding component
// Use just the following HTML and press the button
<OBJECT
 ID=tdcContents
 CLASSID="clsid:333C7BC4-460F-11D0-BC04-0080C7055A83">
  <PARAM NAME="DataURL" VALUE="DataBinding.csv">
</OBJECT>
<BUTTON onclick="oTxt.value=tdcContents.outerHTML">
Show Object outerHTML</BUTTON><BR/>
<TEXTAREA ID="oTxt"  STYLE="height:400; width:450;padding:3; overflow=auto;"> </TEXTAREA>
//When the button is pressed the complete list of the object's
// PARAM elements display unformatted in the TEXTAREA as follows:

<OBJECT id=tdcContents classid=clsid:333C7BC4-460F-11D0-BC04-0080C7055A83>
<PARAM NAME="RowDelim" VALUE="&#10;"><PARAM NAME="FieldDelim" VALUE=",">
<PARAM NAME="TextQualifier" VALUE='"'><PARAM NAME="EscapeChar" VALUE="">
<PARAM NAME="UseHeader" VALUE="0"><PARAM NAME="SortAscending" VALUE="-1">
<PARAM NAME="SortColumn" VALUE=""><PARAM NAME="FilterValue" VALUE="">
<PARAM NAME="FilterCriterion" VALUE="??"><PARAM NAME="FilterColumn" VALUE="">
<PARAM NAME="CharSet" VALUE=""><PARAM NAME="Language" VALUE="">
<PARAM NAME="CaseSensitive" VALUE="-1"><PARAM NAME="Sort" VALUE="">
<PARAM NAME="Filter" VALUE=""><PARAM NAME="AppendData" VALUE="0">
<PARAM NAME="DataURL" VALUE="DataBinding.csv">
<PARAM NAME="ReadyState" VALUE="4">
</OBJECT>
```

The following example shows how the param element can be used to pass a parameter to a plugin, in this case the O3D plugin

``` html

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
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

The **PARAM** element is valid within the **APPLET**, **EMBED**, and **OBJECT** elements. **Note**  Properties set by a **PARAM** element cannot be altered by changing the **PARAM** object. After the **APPLET**, **EMBED**, or **OBJECT** element is instantiated, the property set by the **PARAM** element cannot be changed with the **param** object. To change the object's properties, use the script properties exposed by the object.

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-param-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-param-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/objects.html#edef-PARAM)
:   W3C Recommendation
