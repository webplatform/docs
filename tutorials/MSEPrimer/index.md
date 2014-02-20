{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This guide gives you a basic look at Media Source Extensions, what they are, and how to use them to do add-on free video streaming. An example is presented that uses MSE and MPEG-DASH file to stream content from a single video file as source and used XMLHttpRequest to get segments. This is just one of several ways to stream content. }}
{{Tutorial
|Content=Introduction
Media Source Extensions (MSE) as adds buffer-based source options to HTML5 media for streaming support. Previously, you had to download a complete video file to play, or use an add-on like Silverlight or Adobe Flash to stream media. With MSE, no client add-ons are required for streaming. Additionally, you can stream video from a standard HTTP server. A special media server is not required. 
The example described here uses un-prefixed APIs, and runs in IE11. It loads in the latest Chrome, but won't load because the source video is MP4. 

MSE Overview
The primary addition to HTML5 media is the MediaSource object. The MediaSource object takes the place of a file URL as the src on a video object. 
      
      mediaSource = new window.MediaSource();  // Create a new object
      var url = URL.createObjectURL(mediaSource); // Make a URL from it
      videoElement.src = url; // Video is now pointing at the mediaSource object

Source buffers are added to the MediaSource object and filled with media data from segmented files. The HTML5 audio or video element does not know whether it's playing a file or a buffer.
 
    mediaSource.addEventListener('sourceopen', function (e) {
     var videoSource = mediaSource.addSourceBuffer('video/mp4');
     videoSource.appendBuffer(new Uint8Array([video content]));

Once the sourceBuffer is added, media content can be appended into the buffer. Content can be from a single source, or several sources or files. You can store files of different quality or resolution on different servers to provide load balancing or better connections. 

With the MediaSource object connected to the video object, you can append data to the buffers using any number of file request schemes. The example shown here uses a single video file, with a segment list defined in a Media Presentation Description (mpd) file. The buffer can be loaded using separate files. The only requirement is that when video starts, you must "prime the pump" so to speak by loading an initialization segment. The video initialization segment sets up codec, bitrate, resolution, and other parameters. 

If you're serving from a single video file like the example here, or all of your individual file segments have the exact same codec, bitrate, etc, then you just need to initialize once. If you change bitrates, or insert a commercial with different parameters, you'll need to load the initialization segment for the new stream. When you return to your regular content, you'll also have to re-initialize the video object. 

Using MSE on your page

The MSE API itself is a simple concept and basically follows these steps:
1.	Define an HTML5 video element in the HTML section of a page. 
2.	Create a MediaSource object in JavaScript. 
3.	Create a virtual URL using createObjectURL with the MediaSource object as the source. 
4.	Assign the virtual URL to the video element's src property. 
5.	Create a SourceBuffer using addSourceBuffer with the mime type of the video you're adding. 
6.	Get the video initialization segment from the media file online and add it to the SourceBuffer with appendBuffer.
7.	Get the segments of video data from the media file, append them to the SourceBuffer with appendBuffer.
8.	Call the play method on the video element. 
9.	Repeat step 7 until done. 
10.	Clean up.

These are the basic list of steps for using MSE. However your player needs to know where files are located, what kind of video file is coming (MP4 or 
WebM), and what the segments are. If it's a single segmented file, what the segments are, usually in a byte range.

For the example here, we're going to use a single file that's segmented, and uses a Media Presentation Description file for the list of segments. We'll go through how to setup the demo, and then discuss how the MPD file is built later. 

Since MSE is fairly basic, the majority of the example here is about getting video segments and handling the UI of the page. This example could be simplified by creating a segment list array, and hard-coding the file names and ranges. 

The HTML5 video element

The HTML that you need to use with MSE is very simple. It consists of a video element with any associated fall back code. The snippet below includes an Input Element field to define an MPD file, a play button, and some <div> areas to display results we get from the MPD file. The video element has the autoplay attribute set, but no src or controls attributes. The source for the video element is set in the script code by the information we'll get from the MPD file, and the play/pause control is done with the Play button. The Play button's click event is later handled in the JavaScript code with an addEventListener() rather than using the onclick() event on the element itself. In the online example, you can also click the video control to play or pause.

<div id="grid">
  <div id="col1">
   <label>Enter .mpd file: 
      <input type="text" id="filename" value="di_dash.mpd" />
    </label>
    <button id="load">Play</button>
    <!-- some areas to display info and content -->
    <div id="mydiv"></div>
    <div id="videoInfo"></div>
    <div id="dispIndexes" >Current index: <span id="curIndex"></span> of <span id="numIndexes"></span> </div> 
    <div id="DispSegs" >Current segment length: <span id="segLength"></span> </div> 
      <div id="curVidTime" >Current video time: <span id="curTime"></span></div>
  </div>
  <div id="col2">
    <video id="myVideo" autoplay="autoplay" >No video available</video>
  </div>
</div>

The architecture of the page puts the <script> tags below the HTML code in the <body> of the page. This adds efficiency by ensuring that the HTML elements have finished loading before the script starts. 

Handling play and pause

In the example, to play a DASH file click the Play button. Because the intrinsic controls are turned off on the video element, the play button code event handler plays or pauses the current video. The play button's behavior is conditional: 

•	If the video element is paused (its initial state), and the MPD file hasn't been loaded before, the getData() function is called to load and parse the MPD file. 
•	If the video is paused, but the file was loaded and hasn't changed, only the play method is called. 
•	If the file name in the input field has changed, and the video is paused, the new file is loaded and then played. 
•	If the video is playing, the pause method is called so the user can stop and start the video. 

    playButton.addEventListener("click", function () {
      //  If video is paused then check for file change
      if (videoElement.paused == true) {
        // Retrieve mpd file, and set up video
        var curMpd = document.getElementById("filename").value;
        //  If current mpd file is different then last mpd file, load it.
        if (curMpd != lastMpd) {
          //  Cancel display of current video position
          window.cancelAnimationFrame(requestId);
          lastMpd = curMpd;
          getData(curMpd);
        } else {
          //  No change, just play
          videoElement.play();
        }
      } else {
        //  Video was playing, now pause it
        videoElement.pause();
      }
    }, false);

To keep the button labels in sync with the state of the video element, the paused and playing events are used to handle switching the button's label between Play and Pause. 

// handler to switch button text to Play
videoElement.addEventListener("pause", function () {
  playButton.innerText = "Play";
}, false);

// handler to switch button text to pause
videoElement.addEventListener("playing", function () {
  playButton.innerText = "Pause";
}, false);

Getting the .mpd file and DASH parameters

The Media Presentation Description is an XML file that describes how the media is segmented, the type and codec (MP4 here), the bit rate, length, and basic segment size of the video. Some MPD files include audio info, and you can split content into separate streams for the video and audio players. The example shown here only uses a single buffer for both video and audio. 

// gets the mpd file and parses it    
function getData(url) {
  if (url !== "") {
    var xhr = new XMLHttpRequest(); // Set up xhr request
    xhr.open("GET", url, true); // Open the request          
    xhr.responseType = "text"; // Set the type of response expected
    xhr.send();

    //  Asynchronously wait for the data to return
    xhr.onreadystatechange = function () {
      if (xhr.readyState == xhr.DONE) {
        var tempoutput = xhr.response;
        var parser = new DOMParser(); //  create a parser object 

        //  create an xml doc from .mpd file for searching
        var xmlData = parser.parseFromString(tempoutput, "text/xml", 0);
        log("parsing mpd file");

        // Get and display the parameters of the .mpd file
        getFileType(xmlData);

        // set up video object, buffers, etc  
        setupVideo();

        // initialize a few variables on reload
        clearVars();
      }
    }

    //  Report errors if they happen during xhr
    xhr.addEventListener("error", function (e) {
      log("Error: " + e + " Could not load url.");
    }, false);
  }
}

This example uses the XMLHttpRequest object to retrieve the MPD file into the response attribute, tempoutput. We create a DOMParser object and parse the MPD file data into an XML document. We want an XML document (xmlData) to use querySelectorAll and getAttribute methods to extract the value of the XML nodes in the file. 

The following code queries our new XML document and pulls out the individual data points we want to display. The byte range segments are loaded into an array called segments. With the help of an index, we'll use the segments[] array to download the video segments. 

// retrieve parameters from our stored .mpd file
function getFileType(data) {
  try {
    adaptationSet = data.querySelectorAll("AdaptationSet");

    bitSwitch = data.querySelectorAll("bitstreamSwitching"); //adaptationSet[0].getAttribute("bitstreamSwitching");


    file = data.querySelectorAll("BaseURL")[0].textContent.toString();
    var rep = data.querySelectorAll("Representation");
    type = rep[0].getAttribute("mimeType");
    codecs = rep[0].getAttribute("codecs");
    width = rep[0].getAttribute("width");
    height = rep[0].getAttribute("height");
    bandwidth = rep[0].getAttribute("bandwidth");

    var ini = data.querySelectorAll("Initialization"); // get the initialization 
    initialization = ini[0].getAttribute("range");
    segments = data.querySelectorAll("SegmentURL");
   
    // get the length of the video per the .mpd file
    //   since the video.duration will always say infinity
    var period = data.querySelectorAll("Period");
    var vidTempDuration = period[0].getAttribute("duration");
    parseDuration(vidTempDuration); // display length

    var segList = data.querySelectorAll("SegmentList");
    segDuration = segList[0].getAttribute("duration");
  } catch (er) {
    log(er);
    return;
  }
  showTypes();  // Display parameters 
}

// Display parameters from the .mpd file
function showTypes() {
  var display = document.getElementById("mydiv");
  display.innerHTML = ""; // clear display first
  display.innerHTML += "<br/>Media file: " + file + "<br/>";
  display.innerHTML += "Type: " + type + "<br/>";
  display.innerHTML += "Codecs: " + codecs + "<br/>";
  display.innerHTML += "Width: " + width + " -- ";
  display.innerHTML += "Height: " + height + "<br/>";
  display.innerHTML += "Bandwidth: " + bandwidth + "<br/>";
  display.innerHTML += "Initialization Range: " + initialization + "<br/>";
  display.innerHTML += "Segment length: " + segDuration / 1000 + " seconds";
  document.getElementById("numIndexes").innerText = segments.length;
 
}

The getData() function calls getFileType() function fills global variables with the information from the MPD file. We then call the showTypes() function to display the parameters to the screen.

Setting up video and buffers

After the MPD file has been parsed, the media content pointed to in the MPD file is retrieved and played. When getting and playing video data, timing is very important. In an app that only plays a single resolution, the number of segments in the buffer isn't a big concern; however, you don't want to use up too much memory. If you're playing low resolution because of a slow network, you'll want to be ready to download a higher resolution video segment the next time the network speeds increases. In this case, you might not want to get too far ahead of the current playing segment. 

The play process goes like this:
1.	Download the video's initialization segment to the buffer and play it. 
2.	Download a segment of video to the buffer, and play it. 
3.	Repeat step 2 until all segments have been played. 

DASH media segments are downloaded and appended to the buffer, which is then played by the HTML5 video element. The MediaSource buffer takes the place of a file URL for the src of these elements. The addSourceBuffer method creates and adds a buffer to the MediaSource object. The removeSourceBuffer removes an existing SourceBuffer from the MediaSource object. The appendBuffer method adds media data to a SourceBuffer. 


      //  Create the media source 
      if (window.MediaSource) {
        mediaSource = new window.MediaSource();
       } else {
        log("mediasource or syntax not supported");
        return;
      }
      var url = URL.createObjectURL(mediaSource);
      videoElement.pause();
      videoElement.src = url;
      videoElement.width = width;
      videoElement.height = height;

      // Wait for event that tells us that our media source object is 
      //   ready for a buffer to be added.
      mediaSource.addEventListener('sourceopen', function (e) {
        try {
          videoSource = mediaSource.addSourceBuffer('video/mp4');
          initVideo(initialization, file);           
        } catch (e) {
          log('Exception calling addSourceBuffer for video', e);
          return;
        }
      });

To get individual segments from a single video file, we use setRequestHeader to specify a byte range for each segment in the file. These byte ranges are specified in the segment list we get from the MPD file. The XHR response property is typecast to a Uint8Array and appended to the source buffer. 

The initVideo() function in the example downloads the initialization segment from the video file and puts it into the SourceBuffer. 
The XHR request are asynchronous. To ensure functions are called at the right time, the readystatechange event is used. When readystatechange fires, the readyState property is checked. If it's equal to xhr.DONE, the response attribute (media data) is added to the source buffer as a Uint8Array.

    //  Load video's initialization segment 
    function initVideo(range, url) {
      var xhr = new XMLHttpRequest();
      if (range || url) { // make sure we've got incoming params

        // Set the desired range of bytes we want from the mp4 video file
        xhr.open('GET', url);
        xhr.setRequestHeader("Range", "bytes=" + range);
        segCheck = (timeToDownload(range) * .8).toFixed(3); // use .8 as fudge factor
        xhr.send();
        xhr.responseType = 'arraybuffer';
        try {
          xhr.addEventListener("readystatechange", function () {
             if (xhr.readyState == xhr.DONE) { // wait for video to load
              // Add response to buffer
              try {
                videoSource.appendBuffer(new Uint8Array(xhr.response));
                // Wait for the update complete event before continuing
                videoSource.addEventListener("update",updateFunct, false);

              } catch (e) {
                log('Exception while appending initialization content', e);
              }
            }
          }, false);
        } catch (e) {
          log(e);
        }
      } else {
        return // No value for range or url
      }
    }
    
The sourceBuffer's update event is used to see when the data has finished loading. When the media has finished loading into the SourceBuffer, the bufferUpdated flag is set. This flag is used later to check that the initialization content from the MP4 file is actually completed first. 

Feeding the buffer

After the initialization data is loaded, the media segments start to load and play. In this example, the first segment of data is loaded outside of the regular play loop. This is a small hack to get the video started because the main loop that drives the segment request and buffer maintenance is based on the video playing, and at initialization, the video is paused. After the first segment is loaded and is playing, the video update method is called and the loop starts. 

function updateFunct() {
      //  This is a one shot function, when init segment finishes loading, 
      //    update the buffer flag, call getStarted, and then remove this event.
      bufferUpdated = true;
      getStarted(file); // Get video playback started
      //  Now that video has started, remove the event listener      videoSource.removeEventListener("update", updateFunct);
    }

    //  Play our file segments
    function getStarted(url) {

      //  Start by loading the first segment of media
      playSegment(segments[index].getAttribute("mediaRange").toString(), url);

      // Start showing video time
      requestId = window.requestAnimationFrame(render);

      // Display current index
      curIndex.textContent = index + 1;
      index++;

      //  Continue in a loop where approximately every x seconds reload the buffer
      videoElement.addEventListener("timeupdate", fileChecks, false);

    }


To keep the video element playing, media segments are requested based on the time length of the current segment. The example uses a 20% fudge factor to ensure the content gets downloaded in time. If the current segment has 10 seconds of video, the next segment is requested after 8 seconds, or 80% of the segment total. This gives a small amount of extra time to request the segment, but doesn't eat up memory so quickly. This example gets the length of the segment (timeToDownload(range)) and multiplies it by .8, or 80%. The result is stored in the segCheck global variable used to calculate when to get the next segment. 

          xhr.addEventListener("readystatechange", function () {
            if (xhr.readyState == xhr.DONE) { //wait for video to load
              //  Calculate when to get next segment based on time of current one
                segCheck = (timeToDownload(range) * .8).toFixed(3); // Use .8 as fudge factor
                segLength.textContent = segCheck;
              // Add received content to the buffer
              try {
                videoSource.appendBuffer(new Uint8Array(xhr.response));
              } catch (e) {
                log('Exception while appending', e);
              }
            }
          }, false);


To calculate the time length of the current segment, we use the formula: time = (size * 8) / bitrate. The byte range is stored in the MPD file as xxxx-yyyy, or start-end. The example splits the string and subtracts the start from the end to get the size in bytes of the current segment. That value is multiplied by 8 to convert bytes to bits, and then divided by the bitrate. The bitrate of the media file is specified by the MPD file as bandwidth. The result is the time in seconds that the current segment takes to play. 

function timeToDownload(range) {
  var vidDur = range.split("-");
  // time = size * 8 / bitrate
  return (((vidDur[1] - vidDur[0]) * 8) / bandwidth)
}

It might seem like overkill to calculate the length in time of each segment when the MPD file gives us the duration of the segments as a parameter. Unfortunately, the duration parameter seems to be only a suggestion. In practice, the segments are often shorter or longer than the stated duration. The actual value depends on how the DASH MP4 file was segmented. The DASH tool tries to make segment breaks on keyframes, so the time depends on how often the video compression sets a keyframe. In a compressed video codec like MP4, a keyframe is a fully rendered frame, and is followed by a series of frames that contain only the changes for movement in the frame. The frequency of keyframes vary based on the amount of change, either action within a frame, or a scene change. 

The playback loop uses the video element's timeupdate event to drive when to get the next segment. When the event fires, it calls the fileChecks() function. fileChecks() first compares the current index with the total elements of the array of segments and continues if there are still segments left. Next, fileChecks() calculates the amount of time that the current segment has been playing. If this value is greater or equal to the total time we calculated for the segment, then the next segment of media data is requested. 

This loop continues until all the segments have been loaded and played. When the index matches the number of segments, the removeEventListener method is called to stop the timeupdate event. 

//  get video segments 
function fileChecks() {
  if (bufferUpdated == true) {
    if (index < segments.length) {
      //  loads next segment when time is close to the end of the last loaded segment 
      if ((videoElement.currentTime - lastTime) >= segCheck) {
        playSegment(segments[index].getAttribute("mediaRange").toString(), file);
        lastTime = videoElement.currentTime;
        curIndex.textContent = index + 1;// display current index    
        index++;
      }
    } else {
      videoElement.removeEventListener("timeupdate", fileChecks, false);
    }
  }
}

The PlaySegment() function downloads the media data and puts it into the source buffer. The function is called with a media byte range for the segment and the URL of the MP4 file. 

//  Play segment plays a byte range (format nnnn-nnnnn) of a media file    
function playSegment(range, url) {
  var xhr = new XMLHttpRequest();
  if (range || url) { // make sure we've got incoming params
    xhr.open('GET', url);
    xhr.setRequestHeader("Range", "bytes=" + range);
    xhr.send();
    xhr.responseType = 'arraybuffer';
    try {
      xhr.addEventListener("readystatechange", function () {
        if (xhr.readyState == xhr.DONE) { // wait for video to load
          //  Calculate when to get next segment based on time of current one
          //    Use .8 as fudge factor
            segCheck = (timeToDownload(range) * .8).toFixed(3); 
            segLength.textContent = segCheck;
          // add response to buffer
          try {
            videoSource.appendBuffer(new Uint8Array(xhr.response));
            videoSource.onreadystatechange = function () {
              if (videoSource.readyState == videoSource.done) {
                videoElement.play();
              }
            };
          } catch (e) {
            log('Exception while appending', e);
          }
        }
      }, false);
    } catch (e) {
      log(e);
      return // no value for range
    }
  }
}

To sum up, after the initialization process is complete, the timeupdate event drives the download and playback of segments. When the current segment has played approximately 90% of the way through, another segment is downloaded and added to the buffer and the play method is called. 
Making DASH and Media presentation description (MPD) files
The MPEG-DASH spec describes a how media files are segmented, and is relatively agnostic on codecs. MPEG-DASH is a container which can contain WebM or MP4 files. Segmented files can consist of a series of small single files, or a large file with indexed sections that are downloaded and played sequentially. When you use short segments of video, rather than long pieces, it's easier to do other tasks like inserting ads or changing quality. 
The W3C spec on MSE doesn't state a specific codec, but in general, video file support can be WebM or ISO BMFF (segmented MP4) and can vary with browser.
The MPEG-DASH MPD is an XML file that contains a description of all the info you'll need to play a video file. To get started, you need the video mime type, the list of segment urls, or the list of segment offsets (in bytes) if in a single file. Depending on what you're showing, you might want 
One way to make an MPD file is with the MP4box command line utility. MP4Box is an open source multimedia packaging tool by GPAC that can create a DASH segmented MP4 and associated MPD file. For more info about MP4Box and to download binaries, see GPAC MP4Box or view documentation. 
To create a single segmented MP4 and associated MPD file, start by installing MP4Box. Then, call MP4Box on the command line with this syntax: 
mp4box -dash 10000 -frag 1000 -rap path\yourfile.mp4

MP4Box creates two files with _dash appended to the name, an MP4 and an MPD file. In this example, it creates yourfile_dash.mp4 and yourfile_dashs.mpd with 10 second segments and 1 second fragments. The -rap flag tells MP4Box to try to make segments break on a keyframe or start of a decoding sequence. While we're asking for 10 second segments, the actual duration of each segment may vary. For more info about MPD files, see MPEG-DASH Tutorial.

Where to go from here
The example presented here shows how to create and attach buffers to the HTML5 video element and read one type of MPD file to get segments of video from a single file. As we've said, you can also use an MPD file to describe a number of small video files rather than segments in a single larger file. To work with that type of MPD setup, you can modify the code that reads the segment section of the MPD file to get individual URLs. This eliminates the need to use setRequestHeader because you'd be getting the whole file with XHR. 
The code here uses only Media Source Extensions and HTML5 video elements. You might want to provide a fallback such as Adobe Flash or Silverlight for browsers that don't support HTML5 video and MSE. 
Rather than writing all this code yourself, take a look at the dash.js library and reference player. Dash.js is an opensource library and player that is supported by many industry media companies, including Microsoft. Dash.js is a modular library with components that can be replaced or rewritten as needed. For large companies, this gives the flexibility of creating modules that handle special needs. For more info see dash.js on GitHub. 

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
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