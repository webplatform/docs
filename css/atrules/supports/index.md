{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The CSS <code>@supports</code> at-rule lets authors detect support of CSS features directly in CSS.}}
{{API_Listing
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=The CSS at-rule <code>@supports</code> is part of the [http://dev.w3.org/csswg/css3-conditional/ CSS Conditional Rules Module Level 3] Editor's Draft. It allows authors to condition rules based on whether particular property declarations are supported in CSS.

In other words <code>@supports</code> lets you detect browser support of CSS features directly in CSS. [http://modernizr.com/ Modernizr] is a well known library that detects features using JavaScript.

An abstract example with the detection of support for <code>display: flex</code> (known as [http://www.w3.org/TR/css3-flexbox/ CSS Flexible Box Layout Module]):

<syntaxhighlight lang="css">
@supports (display: flex) {
  div {
    display: flex;
  }
}
</syntaxhighlight>


It is also possible to chain the detection using the operator <code>and</code>:

<syntaxhighlight lang="css">
@supports (background: rgba(0,0,0,0.2)) and (opacity: 0.8) {
  body {
    background: rgba(0,0,0,0.2);
  }

  div {
    opacity: 0.8;
  }
}
</syntaxhighlight>


To detect if an experimental feature is supported with vendor-prefixes the <code>or</code> operator might be helpful:

(This example does not include <code>-o-</code> and <code>-ms-</code> prefixes as neither Opera nor Microsoft supported a prefixed version of <code>box-shadow</code>.)

<syntaxhighlight lang="css">
@supports (-webkit-box-shadow: 0 0 2px #000) or
          (   -moz-box-shadow: 0 0 2px #000) or
          (        box-shadow: 0 0 2px #000) {

  div {
    -webkit-box-shadow: 0 0 2px #000;
       -moz-box-shadow: 0 0 2px #000;
            box-shadow: 0 0 2px #000;
  }
}
</syntaxhighlight>

|Notes=Browser support for this feature is still pretty limited:

* Firefox in version 17 and up
* Opera in version 12.1

(None of these browsers is Stable as of the time of writing.)
}}
{{See_Also_Section
|External_links=* [https://developer.mozilla.org/en-US/docs/CSS/@supports MDN]
* [http://dabblet.com/gist/3895764 Test-case]
* [http://dev.w3.org/csswg/css3-conditional/#at-supports @supports in the CSS Conditional Rules Editor's Draft]
* [http://mcc.id.au/blog/2012/08/supports On Firefox' support in version 17]
* [http://my.opera.com/desktopteam/blog/2012/10/09/flexbox-and-supports Support in Opera 12.1 (still in beta)]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}