---
title: behavior
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/components/htc/toc/toc.htm'
notes:
  - 'Add values, syntax, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': ''
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
summary: 'Non standard. Sets or retrieves the location of the Dynamic HTML (DHTML) behavior.'
tags:
  - CSS
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/behavior

---
## Summary

Non standard. Sets or retrieves the location of the Dynamic HTML (DHTML) behavior.

## Overview table

[Initial value](/css/concepts/initial_value)
:

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

## Values

## Examples

The following examples demonstrate various ways of applying the **-ms-behavior** property on a page.

``` html
<ul>
  <li style="behavior:url(ul.htc) url(hilite.htc)">HTML</li>
  <ul>
      <li>Internet Explorer authoring tips</li>
      :
  </ul>
</ul>
```

[This example implements an expanding and collapsing table of contents by applying the behavior as an inline style to the **li** element. In this case, two behaviors implemented as HTC have been applied to the element to achieve a combination of mouseover highlighting and expanding/collapsing effect. View live example]

This example defines the **-ms-behavior** attribute in a separate **style** block.

``` html
<style>
   .CollapsingAndHiliting {behavior:url(ul.htc) url(hilite.htc)}
</style>
<ul>
  <li class="CollapsingAndHiliting">HTML</li>
  <ul>
      <li>Internet Explorer authoring tips</li>
      :
  </ul>
</ul>
```

This example sets the **-ms-behavior** property in script.

``` html
<script>
   function window.onload()
   {
      idTopic1.style.behavior = "url(ul.htc) url(hilite.htc)";
   }
</script>
 :
<ul>
  <li id=idTopic1>HTML Authoring</li>
  <ul>
      <li>Internet Explorer authoring tips</li>
      :
  </ul>
</ul>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/components/htc/toc/toc.htm)

If the expanding/collapsing example were to use a DHTML behavior implemented in C++ as an ActiveX control, the code would look slightly different. In this example, the **-ms-behavior** attribute points to the [**id**](/html/attributes/id) property of the object specified in the **object** element.

``` html
<style>
   .Collapsing { behavior:url(#myObject) }
</style>
<object id=myObject ... ></object>
<ul>
  <li class="Collapsing">HTML Authoring</li>
  <ul>
      <li>Internet Explorer authoring tips</li>
      :
  </ul>
</ul>
```

## Notes

### Remarks

You can apply multiple behaviors to an element by specifying a space-delimited list of URLs for the **-ms-behavior** attribute, as shown in the following syntax:

    <element style="behavior:url(a1.htc) url(a2.htc) ..." >

In the following section, one example demonstrates how you can apply two behaviors to an element to achieve a combination of effects. Conflicts resulting from applying multiple behaviors to an element are resolved based on the order in which the behavior is applied to the element. Each succeeding behavior takes precedence over the previous behavior. For example, if multiple behaviors set the element's color, the prevailing color is the one set by the behavior last applied to the element. The same rule applies in resolving name conflicts, such as with property, method, or event names exposed by multiple behaviors. Once the **-ms-behavior** property is defined for the element, the **addBehavior** method can be used to dynamically attach additional behaviors to the element. **Note**  A behavior attached to an element by using the **addBehavior** method or by applying the proposed Cascading Style Sheets (CSS) **-ms-behavior** attribute inline is not automatically detached from the element when the element is removed from the document hierarchy. However, a behavior attached using a style rule defined in the document is detached automatically as the element is removed from the document tree. Windows Internet Explorer 8. The **-ms-behavior** attribute is an extension to CSS, and can be used as a synonym for **behavior** in IE8 Standards mode.

### Syntax

`-ms-behavior: url(sLocation) | url(#objID) | url(#default#behaviorName)`

## See also

### Related articles

#### Media Queries

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [\<resolution\>](/css/data_types/resolution)

-   [accelerator](/css/media_queries/accelerator)

-   [MediaQueryList](/css/media_queries/apis/MediaQueryList)

-   [MediaQueryListListener](/css/media_queries/apis/MediaQueryListListener)

-   [StyleMedia](/css/media_queries/apis/StyleMedia)

-   [addListener](/css/media_queries/apis/addListener)

-   [handleChange](/css/media_queries/apis/handleChange)

-   [matchMedia](/css/media_queries/apis/matchMedia)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [matches](/css/media_queries/apis/matches)

-   [media](/css/media_queries/apis/media)

-   [type](/css/media_queries/apis/properties/type)

-   [removeListener](/css/media_queries/apis/removeListener)

-   [Colors by](/css/media_queries/colors_by)

-   [device-height](/css/media_queries/device-height)

-   [filter](/css/media_queries/filter)

-   [ms-interpolation-mode](/css/media_queries/ms-interpolation-mode)

-   **behavior**

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `Conceptual`
-   `Using DHTML Behaviors`
-   `Other Resources`
-   `Behavioral Extensions to CSS`
