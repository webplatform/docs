---
title: 'SVGPreserveAspectRatio'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /svg/objects/SVGElement
standardization_status: Unknown
tags:
  - API
  - Objects
  - DOM
uri: svg/objects/SVGPreserveAspectRatio

---
Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from SVGElement

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

## Examples

``` html


<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"
[ <!ENTITY Smile "
<rect x='.5' y='.5' width='29' height='39' fill='black' stroke='red'/>
<g transform='translate(0, 5)'>
<circle cx='15' cy='15' r='10' fill='yellow'/>
<circle cx='12' cy='12' r='1.5' fill='black'/>
<circle cx='17' cy='12' r='1.5' fill='black'/>
<path d='M 10 19 A 8 8 0 0 0 20 19' stroke='black' stroke-width='2'/>
</g>
">
<!ENTITY Viewport1 "<rect x='.5' y='.5' width='49' height='29'
fill{{=}}'none' stroke{{=}}'blue'/>">
<!ENTITY Viewport2 "<rect x='.5' y='.5' width='29' height='59'
fill{{=}}'none' stroke{{=}}'blue'/>">
]>
<svg width="450px" height="300px" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <desc>Example PreserveAspectRatio - illustrates preserveAspectRatio attribute</desc>
  <rect x="1" y="1" width="448" height="298" fill="none" stroke="blue"/>
  <g font-size="9">
    <text x="10" y="30">SVG to fit</text>
    <g transform="translate(20,40)">&amp;Smile;</g>
    <text x="10" y="110">Viewport 1</text>
    <g transform="translate(10,120)">&amp;Viewport1;</g>
    <text x="10" y="180">Viewport 2</text>
    <g transform="translate(20,190)">&amp;Viewport2;</g>
    <g id="meet-group-1" transform="translate(100, 60)">
      <text x="0" y="-30">--------------- meet ---------------</text>
      <g><text y="-10">xMin*</text>&amp;Viewport1;
        <svg preserveAspectRatio="xMinYMin meet" viewBox="0 0 30 40" width="50" height="30">&amp;Smile;</svg></g>
      <g transform="translate(70,0)"><text y="-10">xMid*</text>&amp;Viewport1;
        <svg preserveAspectRatio="xMidYMid meet" viewBox="0 0 30 40" width="50" height="30">&amp;Smile;</svg></g>
      <g transform="translate(0,70)"><text y="-10">xMax*</text>&amp;Viewport1;
        <svg preserveAspectRatio="xMaxYMax meet" viewBox="0 0 30 40" width="50" height="30">&amp;Smile;</svg></g>
    </g>
    <g id="meet-group-2" transform="translate(250, 60)">
      <text x="0" y="-30">---------- meet ----------</text>
      <g><text y="-10">*YMin</text>&amp;Viewport2;
        <svg preserveAspectRatio="xMinYMin meet" viewBox="0 0 30 40" width="30" height="60">&amp;Smile;</svg></g>
      <g transform="translate(50, 0)"><text y="-10">*YMid</text>&amp;Viewport2;
        <svg preserveAspectRatio="xMidYMid meet" viewBox="0 0 30 40" width="30" height="60">&amp;Smile;</svg></g>
      <g transform="translate(100, 0)"><text y="-10">*YMax</text>&amp;Viewport2;
        <svg preserveAspectRatio="xMaxYMax meet" viewBox="0 0 30 40" width="30" height="60">&amp;Smile;</svg></g>
    </g>
    <g id="slice-group-1" transform="translate(100, 220)">
      <text x="0" y="-30">---------- slice ----------</text>
      <g><text y="-10">xMin*</text>&amp;Viewport2;
        <svg preserveAspectRatio="xMinYMin slice" viewBox="0 0 30 40" width="30" height="60">&amp;Smile;</svg></g>
      <g transform="translate(50,0)"><text y="-10">xMid*</text>&amp;Viewport2;
        <svg preserveAspectRatio="xMidYMid slice" viewBox="0 0 30 40" width="30" height="60">&amp;Smile;</svg></g>
      <g transform="translate(100,0)"><text y="-10">xMax*</text>&amp;Viewport2;
        <svg preserveAspectRatio="xMaxYMax slice" viewBox="0 0 30 40" width="30" height="60">&amp;Smile;</svg></g>
    </g>
    <g id="slice-group-2" transform="translate(250, 220)">
      <text x="0" y="-30">--------------- slice ---------------</text>
      <g><text y="-10">*YMin</text>&amp;Viewport1;
        <svg preserveAspectRatio="xMinYMin slice" viewBox="0 0 30 40" width="50" height="30">&amp;Smile;</svg></g>
      <g transform="translate(70,0)"><text y="-10">*YMid</text>&amp;Viewport1;
        <svg preserveAspectRatio="xMidYMid slice" viewBox="0 0 30 40" width="50" height="30">&amp;Smile;</svg></g>
      <g transform="translate(140,0)"><text y="-10">*YMax</text>&amp;Viewport1;
        <svg preserveAspectRatio="xMaxYMax slice" viewBox="0 0 30 40" width="50" height="30">&amp;Smile;</svg></g>
    </g>
  </g>
</svg>
```

</pre>
[Scalable Vector Graphics (SVG) 1.0 Specification View live example]

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

In some cases, typically when you are using the [**viewBox**](/svg/properties/viewBox) attribute, you want the graphics to stretch to non-uniformly fill the entire viewport. In other cases, you want to use uniform scaling to preserve the aspect ratio of the graphics. The [**preserveAspectRatio**](/svg/properties/preserveAspectRatio) attribute indicates whether to force uniform scaling.

### Standards information

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.7

### Members

The **SVGPreserveAspectRatio** object has these properties:

-   [**align**](/svg/properties/align): Gets or sets the type of alignment value.
-   [**meetOrSlice**](/svg/properties/meetOrSlice): Gets or sets the type of meet-or-slice value.
