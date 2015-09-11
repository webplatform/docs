---
title: HTML Tag Methods
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff806183(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'You can use HTML tag methods to place HTML elements around text in a String object.'
tags:
  - JS
  - Basic
uri: 'javascript/String/HTML Tag Methods'

---
## <span>Summary</span>

You can use HTML tag methods to place HTML elements around text in a String object.

## <span>Syntax</span>

## <span>Examples</span>

The following examples show how to use the HTML tag methods.

``` js
// anchor method.
 var strVariable = "This is an anchor.";
 document.write(strVariable.anchor("Anchor1"));
 // Output: <A NAME="Anchor1">This is an anchor.</A>

 // big method.
 var strVariable = "This is a string.";
 document.write(strVariable.big());
 // Output: <BIG>This is a string.</BIG>

 //  blink method.
 var strVariable = "This is a string.";
 document.write(strVariable.blink());
 // Output: <BLINK>This is a string.</BLINK>

 //  bold method.
 var strVariable = "This is a string.";
 document.write(strVariable.bold());
 // Output: <B>This is a string.</B>

 //  fixed method.
 var strVariable = "This is a string.";
 document.write(strVariable.fixed());
 // Output: <TT>This is a string.</TT>

 //  fontcolor method.
 var strVariable = "This is a string.";
 document.write(strVariable.fontcolor("red"));
 // Output: <FONT COLOR="red">This is a string.</FONT>

 //  fontsize method.
 var strVariable = "This is a string.";
 document.write(strVariable.fontsize(-1));
 // Output: <FONT SIZE="-1">This is a string.</FONT>

 //  italics method
 var strVariable = "This is a string.";
 document.write(strVariable.italics());
 // Output: <I>This is a string.</I>

 //  link method.
 var strVariable = "This is a hyperlink.";
 document.write(strVariable.link("http://www.microsoft.com"));
 // Output: <A HREF="http://www.microsoft.com">This is a hyperlink.</A>

 //  small method.
 var strVariable = "This is a string.";
 document.write(strVariable.small());
 // Output: <SMALL>This is a string.</SMALL>

 //  strike method.
 var strVariable = "This is a string.";
 document.write(strVariable.strike());
 // Output: <STRIKE>This is a string.</STRIKE>

 //  sub method.
 var strVariable = "This is a string.";
 document.write(strVariable.sub());
 // Output: <SUB>This is a string.</SUB>

 //  sup method.
 var strVariable = "This is a string.";
 document.write(strVariable.sup());
 // Output: <SUP>This is a string.</SUP>
```

## <span>Remarks</span>

No checking is performed to determine whether the HTML tags have already been applied to the string.

## <span>Syntax</span>

The following table lists the syntax for and a description of each HTML tag method.

In the Syntax column, string1 is a **String** object or literal.

The Standard column indicates [World Wide Web Consortium (W3C)](http://go.microsoft.com/fwlink/?LinkId=199553) recommendations for HTML 4. "Discouraged" indicates that the HTML element is discouraged in favor of style sheets.

<table class="wikitable">
<tr>
<th>
Syntax

</th>
<th>
Method description

</th>
<th>
Parameter description

</th>
<th>
Standard

</th>
</tr>
<tr>
<td>
string1.anchor( name )

</td>
<td>
Places an HTML anchor that has a NAME attribute around the text.

</td>
<td>
The name parameter is text to put in the NAME attribute of the HTML anchor.

</td>
</tr>
<tr>
<td>
string1.big()

</td>
<td>
Places HTML \<BIG\> tags around the text.

</td>
<td>
Discouraged

</td>
</tr>
<tr>
<td>
string1.blink()

</td>
<td>
Places HTML \<BLINK\> tags around the text. The \<BLINK\> tag is not supported in Internet Explorer.

</td>
<td>
Not in standard

</td>
</tr>
<tr>
<td>
string1.bold()

</td>
<td>
Places HTML \<B\> tags around the text.

</td>
<td>
Discouraged

</td>
</tr>
<tr>
<td>
string1.fixed()

</td>
<td>
Places HTML \<TT\> tags around the text.

</td>
<td>
Discouraged

</td>
</tr>
<tr>
<td>
string1.fontcolor( color )

</td>
<td>
Places HTML \<FONT\> tags with a COLOR attribute around the text.

</td>
<td>
The color parameter is a string value that contains the hexadecimal value or predefined name for a color. Valid predefined color names depend on the JavaScript host browser and its version.

</td>
<td>
Deprecated

</td>
</tr>
<tr>
<td>
string1.fontsize( size )

</td>
<td>
Places HTML \<FONT\> tags with a SIZE attribute around the text.

</td>
<td>
The size parameter is an integer value that specifies the size of the text. Valid integer values depend on the JavaScript host browser and its version.

</td>
<td>
Deprecated

</td>
</tr>
<tr>
<td>
string1.italics()

</td>
<td>
Places HTML \<I\> tags around the text.

</td>
<td>
Discouraged

</td>
</tr>
<tr>
<td>
string1.link( href )

</td>
<td>
Places an HTML anchor that has an HREF attribute around the text.

</td>
<td>
The href parameter is text to put in the HREF attribute of the HTML anchor.

</td>
</tr>
<tr>
<td>
string1.small()

</td>
<td>
Places HTML \<SMALL\> tags around the text.

</td>
<td>
Discouraged

</td>
</tr>
<tr>
<td>
string1.strike()

</td>
<td>
Places HTML \<STRIKE\> tags around the text.

</td>
<td>
Deprecated

</td>
</tr>
<tr>
<td>
string1.sub()

</td>
<td>
Places HTML \<SUB\> tags around the text.

</td>
</tr>
<tr>
<td>
string1.sup()

</td>
<td>
Places HTML \<SUP\> tags around the text.

</td>
</tr>
</table>
## <span>See also</span>

### <span>Other articles</span>

-   [String Object](/javascript/String)

