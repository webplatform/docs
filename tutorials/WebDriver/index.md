---
title: 'WebDriver'
readiness: 'Ready to Use'
summary: 'Basic tutorial on how to use WebDriver to test web documents without using a service or 3rd party software'
tags:
  - Tutorials
uri: tutorials/WebDriver

---
## Summary

Basic tutorial on how to use WebDriver to test web documents without using a service or 3rd party software

## WebDriver in a nutshell

WebDriver is a [W3C editors draft](https://dvcs.w3.org/hg/webdriver/raw-file/default/webdriver-spec.html) for writing automated tests of websites. It aims to mimic the behaviour of a real user, and as such interacts with the HTML of the application.

All implementations of WebDriver that communicate with the browser use the [JSON WireProtocol](https://code.google.com/p/selenium/wiki/JsonWireProtocol). This wire protocol defines a RESTful web service using JSON over HTTP.

## Real world support

All browser vendors except of Apple are committed to the WebDriver standard. Although not all browsers provide out of the box support for it, or implement the [JSON WireProtocol](https://code.google.com/p/selenium/wiki/JsonWireProtocol) as documented.

### Microsoft Internet Explorer

Microsoft has Support for WebDriver via an external binary, the so called [Internet Explorer Driver](https://code.google.com/p/selenium/wiki/InternetExplorerDriver) acts as a RESTful web server and instruments the browser using the non public debug API. The driver is compatible with the Internet Explorer versions 6 to 10, for IE 12 there are rumors that the WebDriver API will be brought natively to the browsers, without the need of an external binary.

### Google Chrome

Google provides support for WebDriver in the same manor as Microsoft does, using an external library called [Chromedriver](https://code.google.com/p/selenium/wiki/ChromeDriver), and like the Internet Explorer Driver, it acts as "man in the middle" to translate RESTful requests into something the browser understands. Due to the fast update path of the Chrome browser, the browser compatibility is in constant flux, but it's fairly save to say that the past three browser versions are support by the current driver binary.

### Mozilla Firefox

Unfortunately Mozilla does not adhere to the WebDriver standard, but instead supports a homegrown [raw TCP socket](http://en.wikipedia.org/wiki/Transmission_Control_Protocol) based testing Framework called [Marionette](https://developer.mozilla.org/en-US/docs/Mozilla/QA/Marionette), which fortunately is designed to be pretty close the the WebDriver spec. It was shipped in the stable builds beginning with Firefox version 24, but itself isn't stable & the API is in constant flux.

### PhantomJS

PhantomJS, the [headless](http://blog.arhg.net/2009/10/what-is-headless-browser.html) browser based on the WebKit rendering engine & JavaScriptCore javascript engine contains a WebDriver implementation named [Ghostdriver](https://github.com/detro/ghostdriver) that is nearly spec compliant. Ghostdriver is shipped bundled with PhantomJS since version 1.8.

### Mobile Browsers

Mobile browsers and operation systems do not contain an native WebDriver implementation (with the exception of the FirefoxOS debug builds containing Marionette); the [Appium](http://appium.io/) project tries to fill the gap by acting as a WebDriver server for Mobile Chrome, Mobile Safari & Firefox OS.

## Setup

For our basic test setup, we use [PhantomJS](http://phantomjs.org/) as the system we want to test & Chrome as our host system which will control PhantomJS remotely. The installation of PhantomJS is straight forward, just download it from [here](http://phantomjs.org/download.html) & you should have the `phantomjs` binary (or the `phantomjs.exe` if you're on windows) ready.

To start the remote WebDriver server,

On \*nix compatible systems:

`` $ `./phantomjs --webdriver=8080 ``

On windows:

`> phantomjs.exe --webdriver=8080`

The output should be something like this:

`PhantomJS is launching GhostDriver... [INFO  - 2014-05-18T12:53:19.120Z] GhostDriver - Main - running on port 8080`

Now that our WebDriver server is up & running, we need to start our client. Lets use Google Chrome for that (we could use anything here that speaks & understands HTTP as a client Node.js, PHP, other browsers etc.). Because of the `same origin policy` that all browser adhere to, we need to start Chrome with a special flag, that disables this policy for our tests, as our webdriver server runs on a different port/domain, than the page we open up in our browser.

You can disable the `same origin policy` by starting chrome with a special flag from the CMD or terminal:

On \*Nix systems:

`open -a Google\ Chrome --args -disable-web-security -allow-file-access-from-files`

On Windows:

`chrome.exe  –allow-file-access-from-files -disable-web-security`

To finally check if our setup is up & running, navigate to `localhost:8080`, you should see some output similar to this:

` Unknown Command - Request => {"headers":{"Accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,/;q=0.8","Accept-Encoding":"gzip,deflate,sdch","Accept-Language":"en-US,en;q=0.8,de;q=0.6","Connection":"keep-alive","Host":"localhost:8080","User-Agent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 1092) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/34.0.1847.137 Safari/537.36"},...]`

## Connecting to the remote browser

Next step is to connect our PhantomJS based server with the JavaScript code we will run in our Chrome client instance. Lets start by creating a simple webpage that will be the host of our tests:

    <!doctype html>
    <html>
      <head>
        <meta charset="utf-8">
        <title> WebDiver testpage</title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
      </head>
      <body>
        <h1>This is a WebDiver testpage</h1>
        <script>
          request = new XMLHttpRequest();
          request.open('GET', 'http://localhost:8080/status', true);

          request.onload = function() {
            var el = document.createElement('div');
            var contents = document.createTextNode(request.responseText);
              el.appendChild(contents);
              document.getElementsByTagName('body')[0].appendChild(el);
            };

           request.onerror = function() {
             // There was a connection error of some sort
               console.error('err:', arguments);
           };

           request.send();
        </script>
      </body>
    </html>

This sample page uses the `status` method defined in the [JSON WireProtocol](https://code.google.com/p/selenium/wiki/JsonWireProtocol), it queries the WebDriver servers status; We take that & display the contents of the request on our webpage.

The output should be something like this:

`{"sessionId":null,"status":0,"value":{"build":{"version":"1.0.4"},"os":{"name":"mac","version":"unknown","arch":"64bit"}}}`

We now connected Chrome & PhantomJS, time to extend our basic HTML page to obtain a WebDriver session, open up a webpage we want to test & read out the title of that one.

## Browser, I command you

If we want to grab the title of the Webplatform Wiki main page located at `/Main_Page`, we need to take three steps to make that happen:

-   First, we need to get a session from the remote Webdriver (in our case, PhantomJS)
-   Second, we need to tell the remote Webdriver which URL we want to navigate to
-   Third and last, we need to tell the remote Webdriver which data we want, in our case, that we want the `title`

### Obtain a session

As said, first we need to ask the remote Webdriver instance to start a new session for us, this is needed because a remote Webdriver instance can be requested from different clients at the same time & we it needs to hold some state like which URL we are currently on for example.

To obtain a session, we need to make a `POST` request to the [/session](https://code.google.com/p/selenium/wiki/JsonWireProtocol#/session) method. This method expects us to send some JSON data, the so called `desiredCapabilities`, with the request. The desired capabilities were invented to tell the remote WebDriver what we want in this run, most probably if we were running against a large browser array, which browser on which operating system we want to control. In our case, as we only want to talk directly to the browser, we can go with the default data:

    {
        desiredCapabilities: {
            browserName: 'phantomjs',
            version: '',
            platform: 'ANY'}
    }

A function that would do this request would look like this:

    var getSession = function (cb) {
      var request = new XMLHttpRequest();
      request.open('POST', 'http://localhost:8080/session', true);
      request.setRequestHeader('Content-Type', 'application/json');

      request.onload = function() {
            cb(null, JSON.parse(request.responseText));
      };

      request.onerror = function() {
            cb(arguments, null);
      };

      request.send(JSON.stringify({desiredCapabilities: {browserName: 'phantomjs', version: '', platform: 'ANY'}}));
    };

### Open the URL

After we obtained the session, we need to tell remote browser which URL we want to open. We can do this by issuing another `POST` request to the [/url](https://code.google.com/p/selenium/wiki/JsonWireProtocol#/session/:sessionId/url) method. The pattern here is always the same, if we want the remote browser to do something, like navigating to a page, clicking an element, etc., we make a `POST` request, if we want to retrieve data, we make a `GET` request.

If we transform the request into code, it looks like this:

    var openUrl = function (url, session, cb) {
        var request = new XMLHttpRequest();
        request.open('POST', 'http://localhost:8080/session/' + session + '/url', true);
        request.setRequestHeader('Content-Type', 'application/json');

        request.onload = function() {
          cb(null, JSON.parse(request.responseText));
        };

        request.onerror = function() {
          cb(arguments, null);
        };

      request.send(JSON.stringify({url: url}));
    };

Note that we need to send the sessionId, we received in the last request, with the request as a part of the URL. The address of the page we want to open needs to be transferred as a part of the request body.

### Grab the title

Now that we know how we can control the remote browser instance, lets see how we can receive some data. As said, we want to know the title of the Webplatform.org main wiki page. In order to do so, we need to request the [/title](https://code.google.com/p/selenium/wiki/JsonWireProtocol#/session/:sessionId/title) method, and as we want to receive some data, it is a `GET` request this time.

We also need to send the session with us (which makes sense, otherwise the Webdriver would not know from which URL it should fetch the title), and so the function looks quite similar to the ones we used before:

    var getPageTitle = function (session, cb) {
        var request = new XMLHttpRequest();
        request.open('GET', 'http://localhost:8080/session/' + session + '/title', true);
        request.setRequestHeader('Content-Type', 'application/json');

        request.onload = function() {
            cb(null, JSON.parse(request.responseText));
        };

        request.onerror = function() {
            cb(arguments, null);
        };

        request.send();
    };

### Display title & close the session

So, as we have coded our three functions to get a session, open an URL & request the page title, it is time to glue them all together and have some fun. I hope you noticed that every of our functions above takes an argument called `cb`. `cb` is short for `callback` & describes a function that should be invoked after the work in the previously called function is done, in our case, if the request is finished.

All of our callbacks take to arguments, the first argument `err` normally is `null` and will only change its value, if an error happens, in doing so we can be sure to always add at least some code to handle an error that occurs. The second arguments is the `data` that we receive from our request if it succeeds.

A typical response for a `GET` looks like this:

    {
        sessionId: "d8916520-e40a-11e3-84ea-b7d1dad7eee9",
        status: 0,
        value: "WebPlatform Docs · WebPlatform Docs · WPD · WebPlatform.org"
    }

The response contains the `sessionId` we send with the request, a `status` that indicates if an error was risen (0 indicates success) & the `value` attribute, which carries the answer to our question, in this case to: “What is the title?”. Responses for `POST` requests look similar, they only lack the `value` attribute.

Armoured with this knowledge we can glue our functions together & execute them:

    // load the session data
    getSession(function (err, data) {
        // check for an error & report
        if (err) console.error(err);

        // store the sessionId for later use
        var session = data.sessionId;

        // open the webplatform url
        openUrl('http://docs.webplatform.org/wiki/Main_Page', session, function (err, data) {
            // check for an error & report
            if (err) console.error(err);

            // get the page title
            getPageTitle(session, function (err, data) {
                // again check for an error & report
                if (err) console.error(err);

                // take the title response and display it
                var el = document.createElement('div');
            var contents = document.createTextNode('Title: ' + data.value);
            el.appendChild(contents);
            document.getElementsByTagName('body')[0].appendChild(el);

                // close the session
                closeSession(session);
            });
        });
    });

You might wondered what the `closeSession` method does, that is actually a function we haven’t added yet. The `closeSession` method makes a `DELETE` request to the [/session](https://code.google.com/p/selenium/wiki/JsonWireProtocol#DELETE_/session/:sessionId) method, which terminates the session (otherwise it would be open for a long time before it times out).

The function to do this, looks like so:

    var closeSession = function (session) {
      var request = new XMLHttpRequest();
      request.open('DELETE', 'http://localhost:8080/session/' + session, true);
      request.setRequestHeader('Content-Type', 'application/json');
      request.send();
    };

## Summary

To sum it up, the complete code looks like this:

    <!doctype html>
    <html>
      <head>
        <meta charset="utf-8">
        <title> WebDiver testpage</title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
      </head>
      <body>
        <h1>This is a WebDiver testpage</h1>
            <script>
                var getSession = function (cb) {
                  var request = new XMLHttpRequest();
                  request.open('POST', 'http://localhost:8080/session', true);
                  request.setRequestHeader('Content-Type', 'application/json');

                  request.onload = function() {
                        cb(null, JSON.parse(request.responseText));
                  };

                  request.onerror = function() {
                        cb(arguments, null);
                  };

                  request.send(JSON.stringify({desiredCapabilities: {browserName: 'phantomjs', version: '', platform: 'ANY'}}));
                };

                var openUrl = function (url, session, cb) {
                    var request = new XMLHttpRequest();
                    request.open('POST', 'http://localhost:8080/session/' + session + '/url', true);
                    request.setRequestHeader('Content-Type', 'application/json');

                    request.onload = function() {
                      cb(null, JSON.parse(request.responseText));
                    };

                    request.onerror = function() {
                      cb(arguments, null);
                    };

                  request.send(JSON.stringify({url: url}));
                };

                var getPageTitle = function (session, cb) {
                    var request = new XMLHttpRequest();
                    request.open('GET', 'http://localhost:8080/session/' + session + '/title', true);
                    request.setRequestHeader('Content-Type', 'application/json');

                    request.onload = function() {
                        cb(null, JSON.parse(request.responseText));
                    };

                    request.onerror = function() {
                        cb(arguments, null);
                    };

                    request.send();
                };

                var closeSession = function (session) {
                  var request = new XMLHttpRequest();
                  request.open('DELETE', 'http://localhost:8080/session/' + session, true);
                  request.setRequestHeader('Content-Type', 'application/json');
                  request.send();
                };

                // the fun part
                getSession(function (err, data) {
                    if (err) console.error(err);

                    var session = data.sessionId;
                    openUrl('http://docs.webplatform.org/wiki/Main_Page', session, function (err, data) {
                        if (err) console.error(err);

                        getPageTitle(session, function (err, data) {
                            if (err) console.error(err);

                            var el = document.createElement('div');
                        var contents = document.createTextNode('Title: ' + data.value);
                        el.appendChild(contents);
                        document.getElementsByTagName('body')[0].appendChild(el);

                            closeSession(session);
                        });
                    });
                });
            </script>
      </body>
    </html>

I encourage you to take this as a foundation, to play around with & to gain even more and deeper knowledge on how Webdriver works.

## Further reading & tooling

-   [W3C editors draft](https://dvcs.w3.org/hg/webdriver/raw-file/default/webdriver-spec.html) - The W3Cs specification document on Webdriver
-   [JSON WireProtocol](https://code.google.com/p/selenium/wiki/JsonWireProtocol) - The JSON WireProtocol specification
-   [Selenium](http://docs.seleniumhq.org/) - A Java based Framework to interface with different browsers
-   [Appium](http://appium.io/) - A Node.js based framework to interface with mobile applications & browsers
-   [WD.js](https://github.com/admc/wd) - A Node.js framework to interface with different browsers
-   [Dalek.js](http://dalekjs.com/) - A Node.js framework designed to test websites in different browsers

