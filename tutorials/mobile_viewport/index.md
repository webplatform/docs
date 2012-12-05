{{Page_Title|The Mobile Viewport}}
{{Flags
|High-level issues=Stub
}}
{{Byline}}
{{Summary_Section|All about the viewport meta tag.}}
{{Tutorial
|Content=Applying a ''viewport'' is the first and most important step to make
web pages presentable on mobile browsers.

Touch-based smartphone browsers are capable of presenting web pages
designed for desktop browsers, but the experience needs improvement.
When loading full-sized pages, mobile browsers display the entire page
at reduced magnification. Users must double-tap or pinch the screen to
magnify individual columns of content. Even then, text sized for
full-sized browsers is often difficult to read. The following shows
how a typical web page layout displays:

[[Image:viewport_fail.png]]

Users are obliged to go through several steps before text becomes
legible, in this case including tipping the handset to increase the
column's magnification. When users reach the end of the column, they
often experience difficulty reorienting themselves within the page.

The fixed rectangular area within which touch-based smartphone
browsers display larger web pages is called the ''viewport''.
Applying a viewport '''meta''' tag allows you to control how mobile
browsers render content within this rectangle, and whether users can
use magnification controls.

The following shows a sample screen layout without a viewport. The
initially loaded page is zoomed out too far to be legible, while
zooming in makes content extending off the right edge of the screen
relatively image:

[[Image:view_off.png]]

This reflects the browser's default assumption that content should
extend 980 pixels wide.

Note: This sample layout displays a flexibly positioned element that
adapts to the full width of the screen, along with a fixed-size
background image.

To correct this behavior, place the following line within the HTML's
'''head''' region:

 &lt;meta name="viewport" content="width=device-width" />

The following shows the screen layout after the above viewport is
applied:

[[Image:view_on.png]]

Setting the '''width''' to '''device-width''' recalculates flexible
CSS measurements (such as '''width:100%''') within the width of the
handset's screen rather than the default page width. (Tipping the
handset maintains the overall width of the content within the wider
window.)

On most touch-based mobile browsers, the '''device-width''' is 320
pixels. Make sure images and other fixed-dimension elements are sized
accordingly. The screen height varies significantly among devices, and
often increases in full-screen web applications that suppress the
browser's native screen controls.

Note: Applying a viewport has no effect on desktop browsers. It is
interpreted only once when the page loads, and cannot be modified
thereafter.

___

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