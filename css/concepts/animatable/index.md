Properties that are ''animatable'' specify [[css/units/numeric|numeric
values]] or other values such as [[css/data_types/color|colors]] and
various [[css/functions|functions]] that compute to numeric values.
Keyword values accepted by many properties may also animate.  For
example, you may use
[[css/properties/background-position|'''background-position''']] to
animate an image from the '''left''' edge of an element to the
''right'''. However, you may not animate an element's
[[css/properties/text-align|'''text-align''']] property between
'''left''' and '''right''', because these represent entirely different
behaviors with no intervening states.  Some integer-only property
values also do not animate, such as
[[css/properties/z-index|'''z-index''']] and
[[css/properties/column-count|'''column-count''']].