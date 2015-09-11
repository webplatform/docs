---
title: word-wrap
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5888667'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`wordWrap`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'An alias of css/properties/overflow-wrap, word-wrap defines whether to break words when the content exceeds the boundaries of its container.'
tags:
  - CSS
  - Properties
uri: css/properties/word-wrap

---
## <span>Summary</span>

An alias of css/properties/overflow-wrap, word-wrap defines whether to break words when the content exceeds the boundaries of its container.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `wordWrap`

## <span>Syntax</span>

-   `word-wrap: break-word`
-   `word-wrap: normal`

## <span>Values</span>

normal
:   Default. Lines can only be broken at normal break points (spaces, non-alphanumeric characters, etc.).

break-word
:   Words that exceed the width of the container will be arbitrarily broken to fit within the container's bounds.

## <span>Examples</span>

This is the style rule that applies to the example.

``` css
.NormalValue        { word-wrap:normal;     background-color:lightgray; }
.WithBreaks         { word-wrap:break-word; background-color:lightgray; }
.NormalValueNarrow  { word-wrap:normal;     background-color:lightgray; width:10px }
.WithBreaksNarrow   { word-wrap:break-word; background-color:lightgray; width:10px }
.WithBreaksNoWrap    { word-wrap:break-word; background-color:lightgray; width:10px; white-space:nowrap; }
.clsLiteral          { font-family: Courier New, Courier, monospace; }
```

[View live example](http://code.webplatform.org/gist/5888667)

The following examples show how the **css/properties/word-wrap** property can be used to break one long word into multiple words on multiple lines. The *break-word* value avoids horizontal scrolling and can be useful for printing.

``` html
<!doctype html>
<html>
<head>
<title>wordWrap property</title>
</head>

<body>
<div class="body">

<h1>wordWrap property</h1>
<p>
<strong>Note</strong> that the <strong>"p"</strong> elements in the examples have layout because their widths are set.
</p>

<hr />

<p>
These examples shows the <span class="clsLiteral">break-word</span> value of the <strong>wordWrap</strong> property.
</p>

<p class="WithBreaks">
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
</p>

<p class="WithBreaksNarrow">
blonde
</p>

<hr />
<p>
These examples show the <span class="clsLiteral">normal</span> value of the <strong>wordWrap</strong> property.
In quirks mode (transitional DOCTYPE), the field width is extended to fit the word.
</p>

<p class="NormalValue">
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
</p>

<p class="NormalValueNarrow">
blonde
</p>

<hr />

<p>
These examples show the <span class="clsLiteral">break-word</span> value of the
<strong>wordWrap</strong> property with <span class="clsLiteral">white-space:nowrap</span>.
</p>

<p class="WithBreaksNoWrap">
Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word Long Word
</p>

<p class="WithBreaksNoWrap">
blonde
</p>

<hr />

<p>
To clip unwrapped text to the space provided, you can use <span class="clsLiteral">overflow:hidden</span>
and <span class="clsLiteral">text-overflow:ellipsis</span>.
</p>

<p class="NormalValue" style="overflow:hidden">
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
</p>

<p class="NormalValue" style="overflow:hidden;text-overflow:ellipsis">
LongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWordLongWord
</p>

<hr/>
</div>

</body>
</html>
```

[View live example](http://code.webplatform.org/gist/5888667)

## <span>Notes</span>

### <span>Remarks</span>

The **word-wrap** property was originally a proprietary property developed for Internet Explorer, and is used as a synonym for the standardized [**overflow-wrap**](/css/properties/overflow-wrap) property. This property to enables the browser to break up otherwise unbreakable strings (words). This differs from the [**white-space**](/css/properties/white-space) property, which turns wrapping of the text on and off. The **word-wrap** property specifies only whether wrapping can occur at a place in the word that is not otherwise allowed by the language rules in effect.

### <span>Standards information</span>

-   [CSS Text Level 3](http://www.w3.org/TR/css3-text/#overflow-wrap), Section 6.2

## <span>Related specifications</span>

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#overflow-wrap)
:   W3C Recommendation
