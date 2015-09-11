---
title: experimental features
uri: 'concepts/experimental features'

---
## <span>Enabling experimental features</span>

Cutting-edge features that you can't ordinarily use in your browser may be available in experimental implementations. One way to use them is to download and launch standalone browser builds, which are typically generated each day to reflect the latest set of committed code. Here are few places where you can get these builds:

-   [Webkit Nightly](http://nightly.webkit.org) (Safari)

-   [Chrome Canary](https://www.google.com/intl/en/chrome/browser/canary.html)

-   [Firefox Nightly](http://nightly.mozilla.org)

-   [Opera snapshots and release candidates](http://my.opera.com/desktopteam/blog/)

Careful: these builds may be unstable, and may feature unexpected security holes.

Otherwise, some commercial browser releases include latent features that you can toggle on and off, as described below:

### <span>Chrome's about:flags</span>

In Google Chrome, navigate to this address:

    about:flags

You'll see a long list of often esoteric features, and the same warning holds: they may be unstable. If you don't see the feature you want to evaluate in that list, it may be included in a broader *experimental WebKit features* item:

![chrome flags.png](/assets/public/9/90/chrome_flags.png)

Enable the item you want, but pay careful attention to the wording, since you may actually be choosing to *disable* a feature that is enabled by default. Usually you need to restart the browser for the feature to work.

**Note:** Even after downloading a standalone Canary build, you may need to change its flags to enable the set of experimental features you want.

### <span>Mozilla's about:config</span>

In Firefox, navigate to the following address:

    about:config

Double-click any of the items listed to toggle them, again being very careful to leave items alone if you don't know what they're used for:

![mozilla about config.png](/assets/public/e/ee/mozilla_about_config.png)

Most of these options modify the browser application itself, such as how tabs and URL bars behave, but several allow you to try out emerging cross-browser web standards, especially those prefixed *dom*. For example, the **dom.event.clipboardevents.enabled** option allows an application to respond to **cut**, **copy**, and **paste** events. The **dom.battery.enabled** option allows you to test the [Battery Status API](/apis/battery_status) on mobile devices.

### <span>Safari Developer Menu</span>

Apple Safari has a more limited ability to enable WebGL for complex 3D rendering. Under the **Advanced** preferences menu, choose **Show** Develop menu in menu bar**:**

![safari advanced pref.png](/assets/public/e/e3/safari_advanced_pref.png)

The newly available **Develop** menu allows you to turn on WebGL:

![safari develop menu.png](/assets/public/8/8c/safari_develop_menu.png)