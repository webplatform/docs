{{Page_Title}}
{{Flags}}
{{Summary_Section|You can use HTML tag methods to place HTML elements around text in a '''String''' object.
}}
==Syntax==
The following table lists the syntax for and a description of each HTML tag method.

In the Syntax column, string1 is a '''String''' object or literal.

The Standard column indicates [http://go.microsoft.com/fwlink/?LinkId=199553 World Wide Web Consortium (W3C)] recommendations for HTML 4. "Discouraged" indicates that the HTML element is discouraged in favor of style sheets.

{| class='wikitable'
|-
! Syntax
! Method description
! Parameter description
! Standard
|-
| string1.anchor( name )
| Places an HTML anchor that has a NAME attribute around the text.
| The name parameter is text to put in the NAME attribute of the HTML anchor.
|-
| string1.big()
| Places HTML &lt;BIG&gt; tags around the text.
| Discouraged
|-
| string1.blink()
| Places HTML &lt;BLINK&gt; tags around the text. The &lt;BLINK&gt; tag is not supported in Internet Explorer.
| Not in standard
|-
| string1.bold()
| Places HTML &lt;B&gt; tags around the text.
| Discouraged
|-
| string1.fixed()
| Places HTML &lt;TT&gt; tags around the text.
| Discouraged
|-
| string1.fontcolor( color )
| Places HTML &lt;FONT&gt; tags with a COLOR attribute around the text.
| The color parameter is a string value that contains the hexadecimal value or predefined name for a color. Valid predefined color names depend on the JavaScript host browser and its version.
| Deprecated
|-
| string1.fontsize( size )
| Places HTML &lt;FONT&gt; tags with a SIZE attribute around the text.
| The size parameter is an integer value that specifies the size of the text. Valid integer values depend on the JavaScript host browser and its version.
| Deprecated
|-
| string1.italics()
| Places HTML &lt;I&gt; tags around the text.
| Discouraged
|-
| string1.link( href )
| Places an HTML anchor that has an HREF attribute around the text.
| The href parameter is text to put in the HREF attribute of the HTML anchor.
|-
| string1.small()
| Places HTML &lt;SMALL&gt; tags around the text.
| Discouraged
|-
| string1.strike()
| Places HTML &lt;STRIKE&gt; tags around the text.
| Deprecated
|-
| string1.sub()
| Places HTML &lt;SUB&gt; tags around the text.
|-
| string1.sup()
| Places HTML &lt;SUP&gt; tags around the text.
|}
{{Remarks_Section
|Remarks=No checking is performed to determine whether the HTML tags have already been applied to the string.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following examples show how to use the HTML tag methods.

|Code= // anchor method.
 var strVariable = "This is an anchor.";
 document.write(strVariable.anchor("Anchor1"));
 // Output: &lt;A NAME="Anchor1"&gt;This is an anchor.&lt;/A&gt;
 
 // big method.
 var strVariable = "This is a string.";
 document.write(strVariable.big());
 // Output: &lt;BIG&gt;This is a string.&lt;/BIG&gt;
 
 //  blink method.
 var strVariable = "This is a string.";
 document.write(strVariable.blink());
 // Output: &lt;BLINK&gt;This is a string.&lt;/BLINK&gt;
 
 //  bold method.
 var strVariable = "This is a string.";
 document.write(strVariable.bold());
 // Output: &lt;B&gt;This is a string.&lt;/B&gt;
 
 //  fixed method.
 var strVariable = "This is a string.";
 document.write(strVariable.fixed());
 // Output: &lt;TT&gt;This is a string.&lt;/TT&gt;
 
 //  fontcolor method.
 var strVariable = "This is a string.";
 document.write(strVariable.fontcolor("red"));
 // Output: &lt;FONT COLOR="red"&gt;This is a string.&lt;/FONT&gt;
 
 //  fontsize method.
 var strVariable = "This is a string.";
 document.write(strVariable.fontsize(-1));
 // Output: &lt;FONT SIZE="-1"&gt;This is a string.&lt;/FONT&gt;
 
 //  italics method
 var strVariable = "This is a string.";
 document.write(strVariable.italics());
 // Output: &lt;I&gt;This is a string.&lt;/I&gt;
 
 //  link method.
 var strVariable = "This is a hyperlink.";
 document.write(strVariable.link("http://www.microsoft.com"));
 // Output: &lt;A HREF="http://www.microsoft.com"&gt;This is a hyperlink.&lt;/A&gt;
 
 //  small method.
 var strVariable = "This is a string.";
 document.write(strVariable.small());
 // Output: &lt;SMALL&gt;This is a string.&lt;/SMALL&gt;
 
 //  strike method.
 var strVariable = "This is a string.";
 document.write(strVariable.strike());
 // Output: &lt;STRIKE&gt;This is a string.&lt;/STRIKE&gt;
 
 //  sub method.
 var strVariable = "This is a string.";
 document.write(strVariable.sub());
 // Output: &lt;SUB&gt;This is a string.&lt;/SUB&gt;
 
 //  sup method.
 var strVariable = "This is a string.";
 document.write(strVariable.sup());
 // Output: &lt;SUP&gt;This is a string.&lt;/SUP&gt;
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/String{{!}}String Object]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ff806183(v=vs.94).aspx
|HTML5Rocks_link=
}}