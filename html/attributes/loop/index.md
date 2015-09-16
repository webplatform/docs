---
title: 'loop'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/loop.htm'
compatibility:
  feature: loop
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the number of times a sound or video clip will loop when activated.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/loop

---
## Summary

Sets or retrieves the number of times a sound or video clip will loop when activated.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

This example uses the **loop** property and the [**src**](/html/attributes/src) property to change the number of times a background sound loops.

``` html
<SCRIPT>
function loopOnce() {
    oBGSound.loop = 1;
    oBGSound.src = oBGSound.src; // reload sound
}
function loopContinuously() {
    oBGSound.loop = -1;
    oBGSound.src = oBGSound.src; // reload sound
}
</SCRIPT>
:
<BGSOUND id="oBGSound" src="sound.wav">
<BUTTON onclick="loopOnce()">Loop Sound Once</BUTTON>
<BUTTON onclick="loopContinuously()">Loop Sound Continuously</BUTTON>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/loop.htm)

## Notes

### Remarks

To restart a sound or video clip after changing its **loop** property, set the [**src**](/html/attributes/src) property or **dynsrc** property to itself. For example:

    oBGSound.src = oBGSound.src

The following are descriptions of how the **loop** property works for some boundary cases. {

### Syntax

## See also

### Related pages

-   `bgSound`
-   `img`
-   `input`
-   `input type=image`
