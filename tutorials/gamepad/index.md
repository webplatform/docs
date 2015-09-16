---
title: 'Using the Gamepad API'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/API/Gamepad/Using_Gamepad_API)'
readiness: 'Ready to Use'
summary: 'How to access and use controllers for games in browser applications.'
tags:
  - Tutorials
  - Games
uri: tutorials/gamepad

---
## Summary

How to access and use controllers for games in browser applications.

HTML5 introduced many of the necessary components for rich, interactive game development. Technologies like \<canvas\>, WebGL, \<audio\>, and \<video\>, along with JavaScript implementations, have matured to the point where they can now support many tasks previously requiring native code.

The Web Gamepad API is a way for web and game developers, as well as interaction designers, to access and use gamepads and other controllers for games. The API introduces new events on the `window` object for reading gamepad and controller (hereby referred to as *gamepad*) state. In addition to these events, the API also adds a Gamepad object, which you can use to query the state of connected gamepads.

The Gamepad API is currently in [Editor's Draft status at the W3C](http://dvcs.w3.org/hg/webevents/raw-file/default/gamepad.html), and is subject to change.

## Connecting to a gamepad

When a new gamepad is connected to the computer, the focused page first receives a `MozGamepadConnected` event. If a gamepad is already connected when the page loaded, the `MozGamepadConnected` event is dispatched to the focused page when the user presses a button or moves an axis.

You can use `MozGamepadConnected` like this:

    <script>
    function gamepadConnected(e) {
      var gamepads = document.getElementById("gamepads"),
        gamepadId = e.gamepad.id;

      gamepads.innerHTML += " Gamepad Connected (id=" + gamepadId + ")";
    }

    window.addEventListener("MozGamepadConnected", gamepadConnected, false);
    </script>

Each gamepad has a unique ID associated with it, which is available on the event's `gamepad` property.

## Disconnecting a gamepad

When a gamepad is disconnected, and if a page has previously received data (e.g., MozGamepadConnected), a second event is dispatched to the focused window, **MozGamepadDisconnected**:

    <script>
    function gamepadDisconnected(e) {
      var gamepads = document.getElementById("gamepads"),
        gamepadId = e.gamepad.id;

      gamepads.innerHTML += " Gamepad Disconnected (id=" + gamepadId + ")";
    }

    window.addEventListener("MozGamepadDisconnected", gamepadDisconnected, false);
    </script>

The Gamepad's ID will be the same for **MozGamepadConnected** and **MozGamepadDisconnected** events, making it a suitable key for storing gamepad device information:

    var gamepads = {};

    function gamepadHandler(event, connecting) {
      var gamepad = event.gamepad;

      if (connecting) {
        gamepads[gamepad.id] = gamepad;
      } else {
        delete gamepads[gamepad.id];
      }
    }

    window.addEventListener("MozGamepadDisconnected", function(e) { gamepadHandler(e, true); }, false);
    window.addEventListener("MozGamepadDisconnected", function(e) { gamepadHandler(e, false); }, false);

This previous example also demonstrates how the **gamepad** property can be held after the event has completed--a technique we will use for device state querying later.

## Gamepad button events

Gamepads can have one or more buttons, and similar to a mouse button, this API provides events for buttons being pressed and released. When a gamepad button is pressed a **MozGamepadButtonDown** event is dispatched to the currently focused page. Similarly a **MozGamepadButtonUp** event is dispatched when it is released. Both events provide the same **gamepad**property, which indicates the gamepad (i.e., it's ID) that triggered the event. The button itself (i.e., whichever of the 2, 4, etc. buttons the gamepad has) is available on the event's **button** property.

    <script>
    function buttonHandler(event, pressed) {
      var gamepads = document.getElementById("gamepads"),
        gamepadId = event.gamepad.id,
        button = event.button,
        text = pressed ? " Gamepad button pressed" : " Gamepad button released";

      gamepads.innerHTML += text + " (id=" + gamepadId + ", button=" + button + )";
    }

    window.addEventListener("MozGamepadButtonDown", function(e) { buttonHandler(e, true); }, false);
    window.addEventListener("MozGamepadButtonUp", function(e) { buttonHandler(e, false); }, false);
    </script>

## Gamepad axis events

Similar to the button events, the axis events provide a way for developers to know when a user has moved one or more of a gamepad's axises (i.e., left-right or up-down). Just as a gamepad can have multiple buttons, so to can there be many axes. Each physical stick on a gamepad provides two axes for changes in X and Y positioning. The **MozGamepadAxisMove** event indicates that a gamepad's axis has changed, and its new value. The axis is numbered, and its value is given, which is a float between -1.0 (the lowest possible value) and 1.0 (the highest possible value):

    <script>
    function axisHandler(event, pressed) {
      var gamepads = document.getElementById("gamepads"),
        gamepadId = event.gamepad.id,
        axis = event.axis,
        value = event.value;

      gamepads.innerHTML += " Gamepad Axis Move (id=" + gamepadId +
                                                   ", axis=" + axis +
                                                   ", value=" + value + ")";
    }

    window.addEventListener("MozGamepadAxisMove", axisHandler, false);
    </script>

## Querying the gamepad object

All of the **MozGamepad\*** events discussed above included a **gamepad** property on the event object. We used this in order to determine which gamepad (i.e., it's ID) had caused the event, since multiple gamepads might be connected at once.

We can do much more with this Gamepad object, including holding a reference to it and querying it instead of using**MozGamepadButtonUp**, **MozGamepadButtonDown**, and **MozGamepadAxisMove** events. Doing so is often desirable for games or other interactive web pages that need to know the state of a gamepad now vs. the next time an event fires.

As we have seen, the Gamepad object for a given gamepad is available on the **MozGamepadConnected** event. For security reasons, it is not available as a property of the window object itself. Once we have a reference to it, we can query its properties for information about the current state of the gamepad. Behind the scenes, this object will be updated every time the gamepad's state changes.

The Gamepad object's properties include:

-   **id**: a unique id (string) for the gamepad.
-   **connected**: true if the gamepad is still connected to the system.
-   **buttons**: an array of the buttons present on the device. Each entry in the array is 0 if the button is not pressed, and non-zero (typically 1.0) if the button is pressed.
-   **axes**: an array of the axes present on the device. Each entry in the array is a float value in the range -1.0..1.0 representing the axis position from the lowest value (-1.0) to the highest value (1.0).
-   **index**: a unique auto-incrementing number for each gamepad connected to the system. A gamepad that is disconnected and reconnected will retain the same index.

The Gamepad object is often used in conjunction with an animation loop (e.g., requestAnimationFrame), where developers want to make decisions for the current frame based on the state of the gamepad or gamepads.

## Complete example: Displaying gamepad state

This example shows how to use the Gamepad object, as well as the **MozGamepadConnected** and**MozGamepadDisconnected** events in order to display the state of all gamepads connected to the system:

    <html>
    <head>
    <script type="text/javascript">
    var gamepads = {};

    function createDiv(gamepad) {
      var d = document.createElement("div");
      d.setAttribute("id", gamepad.id);
      var t = document.createElement("h1");
      t.appendChild(document.createTextNode("gamepad: " + gamepad.id));
      d.appendChild(t);
      var b = document.createElement("div");
      b.className = "buttons";
      for (var i=0; i<gamepad.buttons.length; i++) {
        var e = document.createElement("span");
        e.className = "button";
        e.innerHTML = i;
        b.appendChild(e);
      }
      d.appendChild(b);
      var a = document.createElement("div");
      a.className = "axes";
      for (var i=0; i<gamepad.axes.length; i++) {
        var e = document.createElement("progress");
        e.className = "axis";
        e.setAttribute("max", "2");
        e.setAttribute("value", "1");
        e.innerHTML = i;
        a.appendChild(e);
      }
      d.appendChild(a);
      document.getElementById("start").style.display = "none";

      return d;
    }

    function connectHandler(e) {
      var gamepad = e.gamepad;
      gamepads[e.gamepad.id] = gamepad;

      var div = createDiv(gamepad);
      document.body.appendChild(div);

      window.mozRequestAnimationFrame(updateStatus);
    }

    function disconnectHandler(e) {
      var d = document.getElementById(e.gamepad.id);
      document.body.removeChild(d);
      delete gamepads[e.gamepad.id];
    }

    function updateStatus() {
      for (j in gamepads) {
        var gamepad = gamepads[j],
          d = document.getElementById(j),
          buttons = d.getElementsByClassName("button"),
          axes = d.getElementsByClassName("axis");

        for (var i=0; i<gamepad.buttons.length; i++) {
          var b = buttons[i];
          if (gamepad.buttons[i]) {
            b.className = "button pressed";
          }
          else {
            b.className = "button";
          }
        }

        for (var i=0; i<gamepad.axes.length; i++) {
          var a = axes[i];
          a.innerHTML = i + ": " + gamepad.axes[i].toFixed(4);
          a.setAttribute("value", gamepad.axes[i] + 1);
        }
      }

      window.mozRequestAnimationFrame(updateStatus);
    }

    window.addEventListener("MozGamepadConnected", connectHandler);
    window.addEventListener("MozGamepadDisconnected", disconnectHandler);
    </script>
    <style>
    .buttons, .axes {
      padding: 1em;
    }

    .button {
      padding: 1em;
      border-radius: 20px;
      border: 1px solid black;
    }

    .pressed {
      background-color: green;
    }
    </style>
    </head>
    <body>

## Press a button on your controller to start

    </body>
    </html>

## DOM implementation

### nslDOMGamepad

All **MozGamepad\*** events include a **gamepad** property, which contains the state of the gamepad. This so-called Gamepad object is only available via **MozGamepad\*** events, and is not available on window. It has the following interface:

    interface nsIDOMGamepad : nsISupports {
      readonly attribute DOMString id;
      readonly attribute boolean connected;
      readonly attribute nsIVariant buttons;
      readonly attribute nsIVariant axes;
      readonly attribute unsigned long index;
    };

The **id** attribute is a string containing the USB vendor and product ID as well as a name. This string is unique per device type. Two gamepads of the same type will share the same string.

The **connected** attributed indicates whether or not the gamepad is connected to the system. After a**MozGamepadConnected** event, gamepad.connected will be true. It is false once **MozGamepadDisconnected** fires.

The **buttons** attribute is an array of all buttons on the gamepad and their state. The first button (e.g., buttons[0]) will be 0 (zero) if the button is not pressed, and non-zero if it is. The second button is buttons[1] and so on.

The **axe** attribute is an array of all the axes present on the device. Each entry in the array is a float value in the range -1.0 to 1.0, representing the axis position from the lowest value (-1.0) to the highest value (1.0). Each physical stick on a gamepad will expose two axes, one for changes in X (left-right), and the other for changes in Y (up-down) positioning.

The **index** attribute is a unique auto-incrementing number for each gamepad connected to the system. If a gamepad is disconnected and reconnected, it will retain the same index number.

The lifetime of an nsIDOMGamepad object is more than the lifetime of a **MozGamepad\*** event. Web content may save a reference to a **MozGamepad\*** event's **gamepad** property and refer to it at any time to determine the current state of the device. The state will not be updated while the content script is executing, only between script executions. For example, the state will not be updated during the course of a setTimeout callback, but it may be updated the next time the callback is called.

### nslDOMGamepadConnectionEvent

The **MozGamepadConnected** and **MozGamepadDisconnected** events use nsIDOMGamepadConnectionEvent:

    interface nsIDOMGamepadConnectionEvent : nsIDOMEvent
    {
      readonly attribute nsIDOMGamepad gamepad;
    };

The single **gamepad** attribute provides access to an associated nsIDOMGamepad object for this device. As was previously mentioned, this object can be held after the event callback has completed, and be used to query the state of the device at any point.

### nslDOMGamepadButtonEvent

Gamepad button state information is made available via nsIDOMGamepadButtonEvent:

    interface nsIDOMGamepadButtonEvent : nsIDOMEvent
    {
      readonly attribute unsigned long button;
      readonly attribute nsIDOMGamepad gamepad;
    };

The **button** attribute indicates the index of the button that was pressed or released.

The **gamepad** attribute provides access to the associated nsIDOMGamepad object, with full button state information available via **gamepad.buttons**.

### nslDOMGamepadAxisMoveEvent

Gamepad axes state information is made available via nsIDOMGamepadAxisMoveEvent:

    interface nsIDOMGamepadAxisMoveEvent : nsIDOMEvent
    {
      readonly attribute unsigned long axis;
      readonly attribute float value;
      readonly attribute nsIDOMGamepad gamepad;
    };

The **axis** attribute indicates the index of the axis that was moved.

The **value** attribute is a float indicating the position of the axis, between -1.0 and 1.0.

The **gamepad** attribute provides access to the associated nsIDOMGamepad object, with full axes state information available via**gamepad.axes**.

## Resources

Implementation and discussion on this API is happening in [bug 604039](https://bugzilla.mozilla.org/show_bug.cgi?id=604039). Feedback and suggestions are welcome.

### Obtaining builds

The latest information about custom builds for testing the API is in [bug 604039](https://bugzilla.mozilla.org/show_bug.cgi?id=604039). However, the most recent try-server builds are available at:

<http://people.mozilla.com/~tmielczarek/gamepad/>

### Demos, Libraries, Other Code

Examples of the Web Gamepad API should be added here. NOTE, the API is evolving, and some of the following examples may be based on earlier versions.

-   Simple API demo page - <https://bug604039.bugzilla.mozilla.org/attachment.cgi?id=549214>
-   Another API demo page - <https://bug604039.bugzilla.mozilla.org/attachment.cgi?id=550638>
-   Example of using MozGamepad\* listeners - <https://gist.github.com/58b0f9ed647f72da9173>
-   Gamepad API controlling \<video\> - <http://weblog.bocoup.com/javascript-firefox-nightly-introduces-dom-gamepad-events,http://jsfiddle.net/rwaldron/wPuGB/>
