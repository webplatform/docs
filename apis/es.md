---
title: 'APIs'
lang: es
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/af
    - apis/ar
    - apis/ast
    - apis/az
    - apis/bcc
    - apis/bg
    - apis/br
    - apis/ca
    - apis/cs
    - apis/da
    - apis/de
    - apis/diq
    - apis/el
    - apis/eo
    - apis/fa
    - apis/fi
    - apis/fr
    - apis/gl
    - apis/gu
    - apis/he
    - apis/hu
    - apis/hy
    - apis/id
    - apis/it
    - apis/ja
    - apis/ka
    - apis/kk
    - apis/km
    - apis/ko
    - apis/ksh
    - apis/kw
    - apis/mk
    - apis/ml
    - apis/mr
    - apis/ms
    - apis/nl
    - apis/no
    - apis/oc
    - apis/pl
    - apis/pt
    - apis/pt-br
    - apis/ro
    - apis/ru
    - apis/si
    - apis/sk
    - apis/sl
    - apis/sq
    - apis/sr
    - apis/sv
    - apis/ta
    - apis/th
    - apis/tr
    - apis/uk
    - apis/vi
    - apis/yue
    - apis/zh
    - apis/zh-hans
    - apis/zh-hant
    - apis/zh-tw
uri: apis/es

---
## Resumen

Las APIs, o Interfaces de programación de aplicaciones, son objetos estándar de JavaScript que realizan una variedad de tareas. Encapsulan objetos, métodos, propiedades y eventos que puedes utilizar para crear aplicaciones que funcionarán a través de los diferentes navegadores.

## Antecedentes

Las APIs se hicieron populares en la Web hace varios años cuando los creadores de estándares abiertos y los desarroladores de aplicaciones se dieron cuenta de que era una excelente idea el hacer sus datos, servicios y tecnologías fácilmente accesibles y reutilizables mediante interfaces sencillas basadas en objetos estándar de JavaScript. En la actualidad puedes encontrar muchos ejemplos de APIs disponibles y en uso a través de toda la Internet, por ejemplo:

-   Sitios web/aplicaciones tan diversas como [Twitter](https://dev.twitter.com/docs), [Flickr](http://www.flickr.com/services/developer/), [Amazon](https://affiliate-program.amazon.com/gp/advertising/api/detail/main.html), [YouTube](http://code.google.com/apis/youtube/overview.html), [Drop Box](http://www.dropbox.com/developers) y [The Guardian](http://www.guardian.co.uk/open-platform).
-   Bibliotecas JavaScript como [Modernizr](http://modernizr.com/), [jQuery](http://jquery.com/) y [Raphaël](http://raphaeljs.com/).

Muchas bibliotecas incluyen funcionalidades de API, de manera que no tienes que utilizar la API cruda. Para APIs como [XHR](/apis/xhr) y [Web Socket](/apis/websocket), puedes usar la API a través de una biblioteca como jQuery en lugar de crear tu propia petición HTTP o construir tu propia capa de conexión.

Nota: Si eres completamente nuevo en el desarrollo web, puede que desees revisar [Desarrollo web para principiantes](/beginners/es).

Sin embargo, la mayoría de las APIs están diseñadas para ser utilizadas directamente en tu código. A continuación encontrarás una lista de todas las APIs documentadas actualmente aqui.

## Lista de todas las APIs

[Ambient Light API](/apis/ambient_light)
:   The Ambient Light API defines events that provide information about the ambient light level, as measured by a device's light sensor.

[appcache](/apis/appcache)
:   In order to enable users to continue interacting with Web applications and documents even when their network connection is unavailable — for instance, because they are traveling outside of their ISP's coverage area — authors can provide a manifest which lists the files that are needed for the Web application to work offline and which causes the user's browser to keep a copy of the files for use offline.

[audio-video](/apis/audio-video)
:   HTML5 audio-video elements used for enhancing the Web page experience with audio backgrounds, music, videos, presentations, etc. Also see "Related articles" below.

[Battery Status API](/apis/battery_status)
:   Provides information about the battery status of the hosting device.

[canvas](/apis/canvas)
:   Allows applications to render pixel-based graphics within a **canvas** element using a two-dimensional graphics *context*.

[CSS Regions API](/apis/css-regions)
:   Programmatic interface to [content that flows](/css/concepts/named_flow) through a series of [chained](/css/concepts/region_chain) [*region*](/css/concepts/region) elements.

[Device Orientation API](/apis/device_orientation)
:   The Device Orientation API defines several new DOM events which provide information about the physical orientation and motion of a hosting device.

[file](/apis/file)
:   The File API allows a developer to use javascript to access the contents and local path of a file uploaded from the input file widget. This enables the developer to build a javascript frontend that allows the website to show a preview of the file uploaded. By using the File API, the developer can also enable a user to upload files via drag-and-drop. Prior to the File API, functionalities like these can only be accomplished via Flash or other plugins.

[File System API](/apis/filesystem)
:   The File System API simulates a local file system that web apps can navigate around. You can develop apps that can read, write, and create files and directories in a virtual, sandboxed file system. The asynchronous API methods return without blocking the calling thread. The asynchronous API doesn't give you data by returning values; instead, you have to pass a callback function. The synchronous API is intended to be used with WebWorkers.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[gamepad](/apis/gamepad)
:   The Gamepad specification defines a low-level interface that represents gamepad devices.

[Geolocation API](/apis/geolocation)
:   The geolocation API lets you share your location with trusted web sites. The latitude and longitude are available to JavaScript on the page, which in turn can send it back to the remote web server and do fancy location-aware things like finding local businesses or showing your location on a map.

[Mediastream Image Capture](/apis/image_capture)
:   Allows users to take a photo via Javascript.

[Indexed Database API](/apis/indexeddb)
:   IndexedDB is a client side storage API that persists data in a user's browser. It is a transactional, non-relational storage mechanism that saves key-value pairs in Object Stores and allows searching data using indexes.

[Media Capture and Streams](/apis/media_capture_and_streams)
:   Enables access to local devices (video cameras, microphones, Web cams) that can generate multimedia stream data (video, audio, or both).

[MediaStream Recording](/apis/media_recorder)
:   Allows users to record camera/microphone's streams

[Media Source Extensions](/apis/media_source_extensions)
:   Provides a buffer based source for HTML5 Video elements to enable media streams for playback, for features like adaptive streaming and shifting live streams.

[navigation timing](/apis/navigation_timing)
:   An interface for web applications to access timing information related to navigation and elements.

[Network Information API](/apis/network_information)
:   Provides an interface for web applications to access the underlying connection information of the device.

[Pointer Lock API](/apis/pointer_lock)
:   The Pointer Lock API provides scripted access to raw mouse movement data while locking the target of mouse events to a single element and removing the cursor from view. This is an essential input mode for certain classes of applications, especially first person perspective 3D applications and 3D modelling software.

[quota management](/apis/quota_management)
:   Manages usage and availability of local storage resources, and defines a means by which a user agent may grant Web applications permission to use more local space, temporarily or persistently, via various storage APIs.

[resource timing](/apis/resource_timing)
:   An interface for web applications to access the complete timing information for resources in a document.

[Screen Orientation API](/apis/screen_orientation)
:   The Screen Orientation API provides the ability to read the screen orientation state, to be informed when this state changes, and to be able to lock the screen orientation to a specific state.

[Storage](/apis/storage)
:   The Storage APIs provide developers with JavaScript objects for storing temporary and permanent data on the client's device. These features range from simple key/value storage to a robust sandboxed filesystem.

[user timing](/apis/user_timing)
:   This API defines an interface to help web developers measure the performance of their applications by giving them access to high precision timestamps.

[Vibration API](/apis/vibration)
:   The Vibration API provides access to the vibration mechanism of the hosting device. Vibration is a form of tactile feedback, often used by mobile phones.

[Web Animations API](/apis/web_animations)
:   Javascript programming interface for modeling synchronizing and timing the changes to a web page's presentation.

[web-messaging API](/apis/web-messaging)
:   This API defines mechanisms for communicating between browsing contexts in HTML documents.

[web-storage API](/apis/web-storage)
:   The Web Storage API provides objects for storing [temporary (sessionStorage)](/apis/web-storage/Storage/sessionStorage) and [permanent (localStorage)](/apis/web-storage/Storage/localStorage) data on the client's device.

[Web Audio API](/apis/webaudio)
:   Describes a high-level JavaScript API for processing and synthesizing audio in web applications.

[WebRTC API](/apis/webrtc)
:   Enables real-time communication across the web.

[websocket API](/apis/websocket)
:   WebSocket is a JavaScript API and accompanying protocol that allows you to create "web sockets", capable of bi-directional full-duplex communication over a persistent TCP connection (socket).

[workers API](/apis/workers)
:   Workers (also commonly referred to as Web Workers) are scripts that run in the background independently of any user interface scripts. This allows for long-running scripts that are not interrupted by scripts that respond to clicks or other user interactions, and allows long tasks to be executed without yielding to keep the page responsive.

[XMLHttpRequest (XHR) API](/apis/xhr)
:   XMLHttpRequest (XHR) is a Javascript object that is used to send HTTP or HTTPS requests directly to a web server and load the server response data directly back into the script.

## Contribuir con la documentación de las APIs

Consulta la [página del Proyecto API](/WPD:Proposals/api_docs) para obtener una descripción sobre el trabajo que se está realizando con el fin de desarrollar la referencia de las APIs. Revisa [Crear páginas de API](/WPD:Creating_API_pages) para aprender a cómo documentar una API.

## Contribuir con la tecnología HTML

Para contribuir al desarrollo de APIs y proporcionar feedback, necesitas saber dónde está alojada la especificación y/o su código fuente. Por ejemplo, puedes encontrar la manera de publicar tus comentarios sobre las APIs de HTML5 visitando la [página principal de HTML del W3C](http://www.w3.org/html/), o sugerir correcciones a Modernizr en el [Repositorio de Github de Modernizr](https://github.com/Modernizr/Modernizr).
