---
title: 'zoom'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/zoom.htm'
compatibility:
  feature: zoom
  topic: css
notes:
  - 'Deletion Candidate:   zoom was originally only supported by Internet Explorer. It is now outdated and shouldn''t be recommended any more.'
readiness: 'Not Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies the magnification scale of the object.'
tags:
  - CSS_Selectors
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/mouseover
    - dom/events/mouseout
uri: css/properties/zoom

---
## Summary

Specifies the magnification scale of the object.

### Syntax

`zoom: normal number percentage`

### Remarks

Setting the value of the `zoom` property on a rendered object causes the content that surrounds the object to reflow. Even though the `zoom` property is not inherited, it affects its children. This effect is similar to the transformation caused by the [**background**](/html/attributes/background_(Body_element)) and [**-ms-filter**](/css/media_queries/filter) properties.

## Examples

The following examples use the **-ms-zoom** attribute and the **-ms-zoom** property to change the magnification scale of a **p** element.

``` html
<STYLE>
  .clsTeenyWeeny  { zoom: 0.10 }
</STYLE>
```

[This example uses a style rule in an embedded style sheet to set the **-ms-zoom** attribute to one-tenth of normal. View live example]

This example uses inline scripting to set the **-ms-zoom** property to 200% when an [**onmouseover**](/w/index.php?title=dom/events/mouseover&action=edit&redlink=1) event occurs. The magnification scale returns to normal when the [**onmouseout**](/w/index.php?title=dom/events/mouseout&action=edit&redlink=1) event occurs.

``` html
<P onmouseover="this.style.zoom='200%'"
   onmouseout="this.style.zoom='normal'">
```

This example provides controls that let the user adjust the **-ms-zoom** property.

``` html
<html xmlns:control="">
<head>
<title>Zoom Demo</title>
<script type="text/javascript">
function zoomIn() {
  newZoom= parseInt(oZoom.style.zoom)+10+'%'
      oZoom.style.zoom =newZoom;
      oCode.innerText='zoom: '+newZoom+'';
  }
function zoomOut() {
  newZoom= parseInt(oZoom.style.zoom)-10+'%'
      oZoom.style.zoom =newZoom;
      oCode.innerText='zoom: '+newZoom+'';
  }
function changeZoom() {
  newZoom= parseInt(oSlider.value)
        oZoom.style.zoom=newZoom+'%';
        oCode.innerText='zoom: '+newZoom+'%';
  }
function changeZoom2(oSel) {
  newZoom= oSel.options[oSel.selectedIndex].innerText
        oZoom.style.zoom=newZoom;
        oCode.innerText='zoom: '+newZoom+'';
  }
</script>
</head>
<body onload="oZoom.style.zoom='100%';
    oCode.innerText='zoom: 100%'; ">
<!-- Slider and + and - controls  -->
<div style="position: absolute; top: 15px; left: 20px;">
    <form>
<control:slider id="oSlider" style="sl--orientation:vertical;
    height:204px; width:28px; background-color:#336699;
    padding-left:5px; border-left:1px solid #6699CC" tickinterval="10"
    max="200" min="0" onchange="changeZoom()"> </control:slider>
    </form>
</div>
<div style="position: absolute; top: 15px; left: 48px; width: 28px; height: 200px; background-color: #336699;" align="center">
    <img src="/workshop/graphics/zoomscale.gif" alt="scale" border="0" usemap="#scaler">
</div>
<!-- The zoomable area container -->
<div style="position: absolute; top: 15px; left: 76px; width: 550px; height: 204px; background-color: black; vertical-align: middle; padding: 25px; font-family: arial; font-weight: bold; color: white; z-index: 3" align="center">
    <!-- The zoomable area -->
    <div id="oZoom" style="zoom: 100%" align="center">
        <h1>Welcome to Seattle!</h1>
        <img src="/workshop/graphics/seattlesmall.jpg" alt="Seattle skyline" align="left">
        <p align="center">A great city in the beautiful state of Washington.</p>
    </div>
</div>
<!-- Displayed code -->
<div style="overflow: hidden; border: 1px solid black; position: absolute; top: 219px; left: 20px; width: 606px; height: 90px; padding: 1px; padding-left: 25px; background-color: white; z-index: 3;">
    &lt;div style=&quot;
    <span style="font-weight: bold; font-family: verdana; color: red; font-size: 9pt" class="coder" id="oCode">
    </span>&quot;&gt;
    <div>
        &lt;h1&gt; Welcome to seattle!&lt;/h1&gt;</div>
    <div>
        &lt;img src=&quot;seattlesmall.jpg&quot;&gt;</div>
    <div>
        &lt;p&gt;A great city in the beautiful state of Washington.&lt;/p&gt;</div>
    <div class="coder">
        &lt;/div&gt;</div>
</div>
<div id="oControls" style="position: absolute; top: 308px; left: 20px; width: 606px; height: 100px; background-color: gray; color: white; font-family: verdana; font-size: 11pt; font-weight: normal; padding: 10px; z-index: 3; text-align: center; border: 1px solid black; text-align: left;">
    <div style="padding-left: 65px">
        The code used to generate the image is shown in the area above. <br>
        <br>
        Modify the image using the selections below or the <br>
        slider control above and to the left of this window. </div>
    <hr>
    <div align="center">
        <select id="percent" onchange="changeZoom2(percent); ">
        <option selected="">Use Percentage Value</option>
        <option>10%</option>
        <option>25%</option>
        <option>50%</option>
        <option>75%</option>
        <option>100%</option>
        <option>150%</option>
        <option>200%</option>
        </select> <select id="normal" onchange="changeZoom2(normal); ">
        <option selected="">Use Number Value</option>
        <option>.1</option>
        <option>0.25</option>
        <option>0.5</option>
        <option>0.75</option>
        <option>1.0</option>
        <option>1.5</option>
        <option>2.0</option>
        </select><hr></div>
</div>
<map name="scaler">
<area shape="rect" coords="0,182,19,199" alt="plus" href="#" onclick="zoomIn()" style="cursor: hand">
<area shape="rect" coords="1,1,18,15" alt="minus" href="#" onclick="zoomOut()">
</map>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/zoom.htm)

## See also

### Related articles

#### Visual Effects

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [clip](/css/properties/clip)

-   [cursor](/css/properties/cursor)

-   [opacity](/css/properties/opacity)

-   **zoom**

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   [filter](/svg/elements/filter)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Other articles

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
