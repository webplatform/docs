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
|Content==x=Filters=x=

Filters present a way to apply certain visual effects either to page elements or to the page as a whole. They have nothing to do with the recently specified CSS Filter Effects although they both aim into the same direction. IE Filters are a lot older. 

A filter affecting the whole page might be a page or site enter or exit transition effect:

<syntaxHighlight lang="html">
&lt;meta http-equiv="Page-Enter" content="blendTrans(Duration=0.3)"&gt;
&lt;meta http-equiv="Page-Exit" content="blendTrans(Duration=0.3)"&gt;
</syntaxHighlight>

Effects for page elements could be for example drop-shadow or blur:

<syntaxHighlight lang="css">
filter: Blur(direction=235,strength=6);
</syntaxHighlight>

A handful of these filters are not just statically applied, but they also need to be initialized via JavaScript afterwards, e.g. the Light filter.

Multiple filters could be chained into one property by separating them with spaces:

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

Best practice is to assign <code>zoom: 1</code> since that did not have any side effects. So this means that in most cases when you wanted to apply a filter to IE < 8 you would do this:
 
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

With IE 8 came another modification to the syntax. Microsoft introduced the vendor prefixed <code>-ms-filter</code> property which apart from its name was identical to the former <code>filter</code> property. On top of that the value needed to be put into a string. The following is exactly the same:

<syntaxHighlight lang="css">
/* IE < 8 syntax */
filter: progid:DXImageTransform.Microsoft.Blur(pixelradius=2); 
</syntaxHighlight>

<syntaxHighlight lang="css">
/* IE 8+ syntax */
-ms-filter: "progid:DXImageTransform.Microsoft.Blur(pixelradius=2)"; 
</syntaxHighlight>

The reason for this change was that W3C's CSS validator was flagging the former filter snytax as invalid whereas it accepted the new one without moaning. If validation is not your top concern you shoulkd still stay with the old syntax since it doesn't break anything and can also be understood by IE 7 or less (whatever advantage that might be).

Filters are supported from IE 4 - 9 and were removed from IE 10. They were also removed from all legacy modes inside IE 10.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|External_links=* [http://www.satzansatz.de/cssd/onhavinglayout.html On Having Layout]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}