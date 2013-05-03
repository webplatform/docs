{{Page_Title|flex}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''flex''' CSS property specifies the ability of a flex item to alter its dimensions to fill the available space. '''flex''' is a shorthand property comprised of the [[css/properties/flex-grow|flex-grow]], [[css/properties/flex-shrink|flex-shrink]], and [[css/properties/flex-basis|flex-basis]] properties. A flex item can be stretched to use available space proportional to its flex grow factor, or reduced proportional to its flex shrink factor to prevent overflow.}}
{{CSS Property
|Initial value=0 1 auto
|Applies to=flex items
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=Yes
|Values={{CSS Property Value
|Data Type=none
|Description=Equivalent to '''0 0 auto'''
* The flex item does not adjust its size to fit the container.
* The flex item's initial main size is determined by the size of its contents.
}}{{CSS Property Value
|Data Type=auto
|Description=Equivalent to '''1 1 auto'''
* The flex item grows exactly proportional to all of the other flex items to fit a larger container.
* The flex item shrinks exactly proportional to all of the other flex items to fit a smaller container.
* The flex item's initial main size is determined by the size of its contents.
}}{{CSS Property Value
|Data Type=initial
|Description=Equivalent '''0 1 auto''''
* The flex item does not grow with the other flex items to fit a larger container.
* The flex item shrinks proportional to the other flex items to fit a smaller container.
* The flex item's initial main size is determined by the size of its contents.
}}{{CSS Property Value
|Data Type=3 1 60%
|Description=* The flex item grows three times as much as the other flex items to fit a larger container.
* The flex item shrinks just as much as the other flex items to fit a smaller container.
* The flex item's initial main size is 60% of its container.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The Holy Grail layout CSS: how to set up one layout that covers both desktop and mobile use cases.
|Code=body {
   font: 24px Helvetica;
   background: #999999;
  }
 
  #main {
   min-height: 800px;
   margin: 0px;
   padding: 0px;
   display: -webkit-flex;
   display:         flex;
   -webkit-flex-flow: row;
           flex-flow: row;
   }
  
  #main > article {
   margin: 4px;
   padding: 5px;
   border: 1px solid #cccc33;
   border-radius: 7pt;
   background: #dddd88;
   -webkit-flex: 3 1 60%;
           flex: 3 1 60%;
   -webkit-order: 2;
           order: 2;
   }
   
  #main > nav {
   margin: 4px;
   padding: 5px;
   border: 1px solid #8888bb;
   border-radius: 7pt;
   background: #ccccff;
   -webkit-flex: 1 6 20%;
           flex: 1 6 20%;
   -webkit-order: 1;
           order: 1;
   }
   
  #main > aside {
   margin: 4px;
   padding: 5px;
   border: 1px solid #8888bb;
   border-radius: 7pt;
   background: #ccccff;
   -webkit-flex: 1 6 20%;
           flex: 1 6 20%;
   -webkit-order: 3;
           order: 3;
   }
  
  header, footer {
   display: block;
   margin: 4px;
   padding: 5px;
   min-height: 100px;
   border: 1px solid #eebb55;
   border-radius: 7pt;
   background: #ffeebb;
   }
  
  /* Too narrow to support three columns */
  @media all and (max-width: 640px) {
   
   #main, #page {
    -webkit-flex-flow: column;
            flex-flow: column;
   }
 
   #main > article, #main > nav, #main > aside {
    /* Return them to document order */
    -webkit-order: 0;
            order: 0;
   }
   
   #main > nav, #main > aside, header, footer {
    min-height: 50px;
    max-height: 50px;
   }
  }
|LiveURL=http://code.webplatform.org/gist/5506026
}}{{Single Example
|Language=HTML
|Description=The Holy Grail layout HTML.
|Code=<!DOCTYPE html>
<html lang="en">
  <head>
    <style>
    </style>
  </head>
  <body>
 <header>header</header>
 <div id='main'>
    <article>article</article>
    <nav>nav</nav>
    <aside>aside</aside>
 </div>
 <footer>footer</footer>
  </body>
</html>
|LiveURL=http://code.webplatform.org/gist/5506026
}}
}}
{{Notes_Section
|Usage=* Best practice is to always specify a unit for the flex-basis value, i.e. 30em or 60%.
* The flex shrink factor is multiplied by the flex basis when distributing negative space.
|Notes=* The initial values of [[css/properties/flex-grow|flex-grow]] and  [[css/properties/flex-basis|flex-basis]] are different from their values when omitted in the '''flex''' shorthand.
** '''flex-grow''' value when omitted: '''1'''
** '''flex-basis''' value when omitted: '''0'''
* When specifying only the flex-basis, a unitless zero not preceded by two flex factor values, for example, '''&nbsp;&nbsp;0''' will be interpreted as a flex factor (probably flex-grow). If you wish to specify only the flex-basis, you must include a unit, for example, a percentage, as in '''0%'''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://dev.w3.org/csswg/css-flexbox/#flex
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=25
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21
|Firefox_supported=Yes
|Firefox_version=20
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=18
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=25
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Mozilla
|Version=18, 19
|Note=Firefox supports only single-line flexbox. To activate flexbox support, for Firefox 18 and 19, the user has to change the about:config preference "layout.css.flexbox.enabled" to true.
}}
}}
{{See_Also_Section
|Topic_clusters=Flexbox
|External_links=Also, check out the following live demo sites:
* [http://demo.agektmr.com/flexbox/ Flexbox Playground]
* [http://the-echoplex.net/flexyboxes Flexy Boxes]
}}
{{Topics|Flexbox}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Tutorials/Using_CSS_flexible_boxes
|MSDN_link=
|HTML5Rocks_link=
}}