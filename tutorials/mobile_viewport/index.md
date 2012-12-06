{{Page_Title|The Mobile Viewport and Orientation}}
{{Flags
}}
{{Byline|Mike Sierra}}
{{Summary_Section|Here you'll learn how the mobile viewport works, and
how it affects what appears on the screen when tipping the handset.}}
{{Tutorial |Content=Applying a ''viewport'' is the first and most
important step to make web pages presentable on mobile browsers.

Touch-based smartphone browsers are capable of presenting web pages
designed for desktop browsers, but the experience needs improvement.
When loading full-sized pages, mobile browsers display the entire page
at reduced magnification. Users must double-tap or pinch the screen to
magnify individual columns of content. Even then, text targeted for
full-sized browsers often features long line lengths that make it more
difficult to read on smaller mobile screens. This shows how a typical
web page layout displays on a mobile screen:

[[Image:viewport_fail.png]]

Users are obliged to go through several steps before text becomes
legible, in this case including tipping the handset to increase the
column's magnification. When users reach the end of the column, they
often experience difficulty re-orienting themselves within the page.

The fixed rectangular area within which touch-based smartphone
browsers display larger web pages is called the ''viewport''.
Applying a viewport '''meta''' tag allows you to control how mobile
browsers render content within this rectangle, and whether users can
use magnification controls.

The following shows a sample screen layout without a viewport. (For
the sake of illustration, it displays a flexibly positioned text
element that adapts to the full width of the screen, along with a
fixed-size background image.)  The initially loaded page is zoomed out
much too far to be legible, while zooming in makes content extending
off the right edge of the screen difficult to access:

[[Image:view_off.png]]

This reflects the browser's default assumption that content should
extend 980 pixels wide. Mobile browsers must make that assumption in
order to render pages that are ''not'' optimized for display on mobile
screens.

To override the browser's default behavior, place this line within the
HTML's '''head''' region:

 &lt;meta name="viewport" content="width=device-width" />

Here's how the screen layout looks after you apply the viewport:

[[Image:view_on.png]]

Setting the '''width''' to '''device-width''' recalculates flexible
CSS measurements (such as '''width:100%''') within the width of the
handset's screen rather than the default page width. (Tipping the
handset maintains the overall width of the content within the wider
window.)

On most touch-based mobile browsers, the '''device-width''' is 320
pixels. Make sure images and other fixed-dimension elements are sized
accordingly. The screen height varies significantly among handsets,
and often increases in full-screen web applications that suppress the
browser's native screen controls.

Applying a viewport has no effect on desktop browsers. It is
interpreted only once when the page loads, and cannot be modified
thereafter.

==Constraining Touch Response==

Applying the above viewport forces content to scroll downward, though
it can still extend horizontally or be positioned outside the screen.
By default, horizontal panning is disabled when the content fits
within the viewport. (A similar '''height=device-height''' property
may also resize content, but does not disable vertical panning to
navigate to overflowing content.)

Use CSS's '''translate()''' transform function if you want to stage
hidden interface elements off the edge of the screen, since it is a
more superficial visual effect that doesn't modify the dimensions of
the overall content within the page.

Once content is well-adapted and accessible for presentation on mobile
browsers, there may no longer be any need to use zoom controls to
access different portions of the page. To disable the browser's
default double-tap and pinch-zoom gestures and ensure that content
appears at the proper magnification level, apply this viewport:

 &lt;meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />

As an alternative to disabling scaling, you can apply decimal
'''minimum-scale''' and '''maximum-scale''' values to control the
potential ''range'' of magnification.  See below for details on how
these viewport options and related CSS affects the appearance of
landscape-oriented content.

The '''user-scalable''' property only affects access to the overall
page.  Touch-enabled web content within that page (such as map
interfaces) may still respond independently to pinch-zoom and
drag-scroll gestures.

To disable vertical scrolling, you need to make sure there is not so
much content on each page that it would overflow the screen. Screen
layouts may also explicitly disable vertical scrolling, but they do so
simply by making any overflowing content inaccessible. This
viewport-enabled example presents a full-screen '''section''' element
whose dimensions align with each edge of the screen:

 &lt;head>
 &lt;meta name="viewport" content="width=device-width" />
 &lt;style>
 section {
     position: absolute; top:0; bottom:0; left:0; right:0;
     overflow: hidden;
 }
 &lt;/style>
 &lt;/head>
 &lt;body>
   &lt;section>
   ...
   &lt;/section>
 &lt;/body>

Even if content overflows the screen without being hidden, setting the
following CSS renders it inaccessible:

 body { overflow: hidden }

Increasingly, mobile browsers allow users to navigate scrollable areas
content that appear within a page, but these should be used with care.
Users may become confused when the scrolling gestures they expect to
scroll the entire page instead scrolls within a narrow region of that
page.

==Tipping the Handset==

When you view browser pages or web apps and tip the device from
portrait to landscape orientation, the browser re-orients content
accordingly.

Web pages and web apps can modify their appearance when the device is
tipped in 90&deg; increments. The '''orientation''' CSS media query
allows you to assign different interface features depending on
'''portrait''' or '''landscape''' orientation. In this case,
landscaped pages use a two-column layout:

 @media all and (orientation: landscape) {
     article {
         -webkit-column-count : 2;
         column-count         : 2;
     }
     h1 {
         -webkit-column-span  : all;
         column-span          : all;
     }
 }

The result can be seen in this example, by resizing the browser window
so that it is alternately taller or wider:

[[Image:orient.png]]

Be careful, though, when presenting a much different landscape
interface. Changes to column layout may disorient users who expect
much the same layout as in portrait ortientation.

JavaScript can respond similarly to '''orientationchange''' events that
fire on the window, checking the state of the '''window.orientation'''
property for '''portrait''' or '''landscape''' values:

 window.addEventListener('orientationchange', function(e){
     var isUpright = (window.orientation == 'portrait');
 });

When you apply a mobile viewport, flexible layout elements conform to
the width of the device's window. Ordinarily, tipping the device to
landscape orientation magnifies the content, keeping the overall width
constant. To illustrate the range of available options, this example
shows a flexible layout against a fixed-size background element. In
landscape view, the page simply magnifies:

[[Image:view_on.png]]

To disable magnification and make flexible elements expand to the
wider screen, set the '''user-scalable=no''' viewport property:

 &lt;meta name="viewport" content="width=device-width, user-scalable=no"/>

Doing so disables pinch and double-tap gestures that otherwise allow
users to magnify content. The following shows how the same page
appears with scaling disabled. The layout element changes dimensions,
but the background element shows that the magnification remains
constant:

[[Image:view_on_noscale.png]]

As shown above, the browser independently magnifies text when shifting
to landscape orientation.  To keep the text size from changing,
disable the '''text-size-adjust''' CSS property. This fixes the entire
page:

 html {
     -webkit-text-size-adjust : none;
     text-size-adjust         : none;
 }

Here is the resulting page, with text appearing at the same size:

[[Image:view_on_noscale_noadjust.png]]

Be careful. Applying the CSS above within a ''desktop''-oriented
interface interferes with the browser's zoom feature, which is not
controlled by mobile '''viewport''' settings. In that case, when users
zoom in, the dimensions of screen elements change, but the size of
the text does not. If you are deploying a hybrid mobile interface
adapted for desktop or tablet browsers, use media queries to narrow
the scope of the above CSS:

 @media only screen and (max-device-width: 400px) {
     html {
         -webkit-text-size-adjust : none;
         text-size-adjust         : none;
     }
     /* rest of mobile interface */
 }

==Review==

Here's what we've learned:

* For cross-device compatability, apply flexible layout elements that adapt to available dimensions.

* Set the viewport's '''width=device-width''' to fit this content to the screen dimensions.

* Set the viewport's '''user-scalable=no''' to widen flexible content in landscape view.

* Set the '''text-size-adjust:none''' CSS property to keep text from zooming in landscape view.

* Optionally, use '''orientation''' media queries to change layout, and '''orientationchange''' handlers to respond in other ways when tipping the handset.

The behavior described above is supported not only by the iPhone, but
by Android and comparable smartphone browsers. While the viewport meta
tag is itself not a formal standard, it is now being folded into CSS
as the [[css/atrules/@viewport|'''@viewport''']] rule, a change not
yet reflected in mobile browsers on the market.

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
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
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}