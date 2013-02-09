{{Page_Title|Proprietary Internet Explorer Techniques}}
{{Flags}}
{{API_Name}}
{{Summary_Section|Back at the times of the browser wars between Microsoft and Netscape both vendors built all sorts of proprietary technology into their browsers. This had different reasons:

* W3C was in its infancy, so this was how new features were "proposed" back then
* Each of the two wanted to have the technological edge
* Other business divisions of the same vendor requested certain features (e.g. the Microsoft Outlook Web Access team)

So came that Microsoft's Internet Explorers learned a lot of techniques that admittedly were non-standard but that could still be very helpful in certain situations. Here we'll have a look at them.
}}
{{Concept_Page
|Content==Filters=

Filters present a way to apply certain visual effects either to page elements or to the page as a whole. They have nothing to do with the recently specified CSS Filter Effects although they both aim into the same direction. IE Filters are a lot older. 

A filter affecting the whole page might be a page or site enter or exit transition effect:

<syntaxHighlight lang="html5">
<meta http-equiv="Page-Enter" content="blendTrans(Duration=0.3)">
<meta http-equiv="Page-Exit" content="blendTrans(Duration=0.3)">
</syntaxHighlight>

Effects for page elements could be for example a blur:

<syntaxHighlight lang="css">
filter: Blur(direction=235,strength=6);
</syntaxHighlight>

A handful of these filters are not just statically applied, but they also need to be initialized via JavaScript afterwards, e.g. the Light filter:

<syntaxHighlight lang="html5">
<!DOCTYPE HTML>
<html>
<head>
    <meta charset="utf-8">
    <title>Light Filter</title>
    <style>
    #filtered {
        filter: light();
    }
    </style>
</head>
    <body>
        <img id="filtered" src="picture.jpg">
        <script>
            /*****************************************************
            At first, without assigning a light, element is black.
            
            Now Lighten the element with an ambient type of light, 
            in a red color RGB(255,0,0), 
            with medium brightness (100) 
            *****************************************************/
            document
            .getElementById('filtered')
            .filters
            .item('light')
            .addAmbient(255, 0, 0, 100);	
        </script>
    </body>
</html>
</syntaxHighlight>

Multiple filters can be chained into one property by separating them with spaces:

<syntaxHighlight lang="css">
/* Gray and blur filters applied at the same time */
filter: Gray() Blur(direction=235,strength=6);
</syntaxHighlight>

To make element filters work on Internet Explorers lower than IE 8 there was one further measure to take: You had to trigger the so called "hasLayout" mode on the filtered element. "hasLayout" is an internal concept of the older IE render engines and it got activated on an element when that had one of the following properties assigned:

* position: absolute
* float
* display: inline-block
* width: any value other than 'auto'
* height: any value other than 'auto'
* zoom: any value other than 'normal' (e.g. zoom: 1)

Best practice is to assign <code>zoom: 1</code> since that does not have any side effects apart from triggering hasLAyout. So this means that in most cases when you wanted to apply a filter to IE < 8 you would do this:
 
<syntaxHighlight lang="css">
filter: Blur(direction=235,strength=6);
zoom: 1;
</syntaxHighlight>

With the release of IE 5.5 Microsoft introduced a second generation of filters with a new value syntax. Whereas old filters were declared like this:

<syntaxHighlight lang="css">
/* IE 4+ filters */
filter: filtername(properties)
</syntaxHighlight>

the new generation is declared this way:

<syntaxHighlight lang="css">
/* IE 5.5+ filters */
filter: progid:DXImageTransform.Microsoft.filtername(properties)
</syntaxHighlight>

Most of the old filters got translated over into a new generation filter, but almost all got a little modified along the way. Take the old "Blur" filter for example. Since it always blurred into a certain direction it got renamed into "MotionBlur":

<syntaxHighlight lang="css">
filter: progid:DXImageTransform.Microsoft.MotionBlur(strength=13, direction=310);
</syntaxHighlight>

And a new "Blur" filter was installed that did a blurring in place:
 
<syntaxHighlight lang="css">
filter: progid:DXImageTransform.Microsoft.Blur(pixelradius=2); 
</syntaxHighlight>

For compatibility reasons, both generations and syntaxes are still supported by the later IEs.

With IE 8 came another modification to the syntax. Microsoft introduced the vendor prefixed <code>-ms-filter</code> property which apart from its name was identical to the former <code>filter</code> property. On top of that the value needed to be put into a string. The following two declarations are identical:

<syntaxHighlight lang="css">
/* IE < 8 syntax */
filter: progid:DXImageTransform.Microsoft.Blur(pixelradius=2); 

/* IE 8+ syntax */
-ms-filter: "progid:DXImageTransform.Microsoft.Blur(pixelradius=2)"; 
</syntaxHighlight>

The reason for this change was that W3C's CSS validator was flagging the former filter snytax as invalid whereas it accepted the new one without moaning. If validation is not your top concern you shoulkd still stay with the old syntax since it doesn't break anything and can also be understood by IE 7 or less (whatever advantage that might be).

One thing to note is that up until IE 8, font antialiasing is being disabled for all text inside a filtered element that is smaller than 18px. IE 9 does not face this problem as font rendering has been improved there. For IE 8 there is a trick for restoring font antialiasing: Wrap your text into another container which has <code>position: relative</code>, like so:

<syntaxHighlight lang="html5">
<div style="filter:progid:DXImageTransform.Microsoft.gradient(startColorstr=#26ffffff,endColorstr=#26ffffff)">
    <div style="position: relative">Lorem ipsum dolor sit amet.</div>
</div>
</syntaxHighlight>

Filters are supported from IE 4 - 9 and were removed from IE 10. They were also removed from all legacy modes inside IE 10.

=DHTML Behaviors=

In IE you can attach so-called "behaviors" to elements via CSS. Behaviors are scripts that can watch and modify the element. One handy advantage over using traditional page scripting is that when you attach new elements to the document tree those will automatically get a script treatment, too. A good use case is the dynamic light filter that we talked about. Assigning the filter property on its own is not enough - you always need to have a script run afterwards. Instead of doing this manually, you could put the script into a behavior file and attach that along with the filter in CSS: 

<syntaxHighlight lang="css">
filter: progid:DXImageTransform.Microsoft.Light();
behavior: url(/scripts/redcoloredlight.htc);
</syntaxHighlight>

It is important to know that the path referenced in <code>url()</code> is not relative to the CSS file as one would think. Instead it is relative to the HTML file. The best solution to counter any problems is to use an absolute URL as shown above.

That said, this would be how the referenced <code>redcoloredlight.htc</code> would look like:

<syntaxHighlight lang="javascript">
<component>
<script type="text/javascript">
element.filters.item('DXImageTransform.Microsoft.Light').addAmbient(255, 0, 0, 100);
</script>
</component>
</syntaxHighlight>

Within a behavior script the HTML element it is attached to can be accessed via <code>element</code>. And if you want to access <code>document</code> you need to address <code>element.document</code>.

Notice: Sometimes IE refuses to run a behavior script if the correct MIME type is not set. The correct type would be <code>text/x-component</code>. If you are on Apache you can set the MIME type yourself by adding this line to your <code>.htaccess</code>:

<syntaxHighlight>
AddType text/x-component .htc
</syntaxHighlight>

Behaviors are supported from IE 4 - 9 and were removed from IE 10. They were also removed from all legacy modes inside IE 10.

=Expressions=

Expressions allow you to dynamically calculate the value of a property. So for example you could do the following to teach older IEs to inherit the parent'S color:

<syntaxHighlight lang="css">
color: expression(this.parentNode.currentStyle.color);
</syntaxHighlight>

The main caveat with expressions is that they get evaluated very often, like after every event or change of the document. Since mousemove is such an event, too, expressions get evaluated a gazillion times when the user moves the mouse.

But this only applies for when expressions are done wrong. A better way is to write an expression that replaces itself with a static value at its first run. This can be achieved be assigning a static value to <code>this.runtimeStyle.property</code> - <code>property</code> being the one where the expression is assigned to initially. Taking the example from above that's how you can do it better:

<syntaxHighlight lang="css">
color: expression(this.runtimeStyle.color = this.parentNode.currentStyle.color);
</syntaxHighlight>

The only drawback now is that if you change the parent's color, this will not be reflected on its child.

Expressions are supported from IE 4 - 7 and were removed from IE 8.

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|External_links=* [http://www.satzansatz.de/cssd/onhavinglayout.html www.satzansatz.de - On Having Layout]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}