==Enabling experimental features==

Cutting-edge features that you can't ordinarily use in your browser
may be available in experimental implementations.  One way to use them
is to download and launch standalone browser builds, which are
typically generated each day to reflect the latest set of committed
code.  Here are few places where you can get these builds:

* [http://nightly.webkit.org Webkit Nightly] (Safari)

* [https://www.google.com/intl/en/chrome/browser/canary.html Chrome Canary]

* [http://nightly.mozilla.org Firefox Nightly]

* [http://my.opera.com/desktopteam/blog/ Opera snapshots and release candidates]

Careful: these builds may be unstable, and may feature unexpected
security holes.

Otherwise, some commercial browser releases include latent features
that you can toggle on and off.  In Google Chrome, navigate to this
address:

 about:flags

You'll see a long list of often esoteric features. If you don't see
the feature you want to evaluate in that list, it may be included in a
broader ''experimental WebKit features'' item:

[[Image:chrome_flags.png]]

Enable the item you want, but pay careful attention to the wording,
since you may actually be choosing to ''disable'' a feature that is
enabled by default.  Usually you need to restart the browser for the
feature to work.

'''Note:''' Even after downloading a standalone Canary build, you may
need to change its flags to enable the set of experimental features
you want.

Apple Safari has a more limited ability to enable WebGL for complex 3D
rendering. Under the '''Advanced''' preferences menu, choose '''Show
Develop menu in menu bar''':

[[Image:safari_advanced_pref.png]]

The newly available '''Develop''' menu allows you to turn on WebGL:

[[Image:safari_develop_menu.png]]