---
title: configuring mimetypes on the server
tags:
  - Tutorials
readiness: 'In Progress'
notes:
  - 'Initial creation. Needs content/links review'
summary: 'How to set up media  or mime types for your your server and why you should always make sure they are set correctly.'
uri: 'tutorials/configuring mimetypes on the server'

---
# Setting up Mime Types on your server

**By [Carlos Araya](http://rivendellweb.net/work)**
Originally published 4/5/2013

## Summary

How to set up media or mime types for your your server and why you should always make sure they are set correctly.

After creating your content and setting up the proper content with text tracks and all the bells and whistles only to have your users report that it doesn't play for them. You wreck your head for a few days and then discover that your server is not set up to properly handle the new video (or audio or any other type of content) media types (also known as mime types.)

The media types help both servers and browsers to identify the kind of resource being asked for by the browser and served by the server. Take for example:

    video/mp4

represents an MP4 (sub type) video (type)

while

    application/font-woff

indicates a woff font (sub type) application (type).

With the sheer number of formats, specifications and sub types (if you're really curious you can check the [[Media Type Registry](http://www.iana.org/assignments/media-types%7CIANA)]j), it would be unrealistic to expect a server configuration to handle all the formats that we will use in our web sites and applications.

Fortunately for our system administrators, most if not all, the available servers have a way for you to add new mime types to the server arsenal. The exact process will depend on the server you're using and some of the servers (Apache) have more than one way to add the media type(s).

I have not listed all the possible servers. Only the ones I've directly worked with. If you have more servers to add, feel free to do so.

## Apache HTTPD server - httpd.conf

An administrator (with root access ideally) should edit the global configuration file (/etc/httpd.d/httpd.conf for example) and add the new types at the end of the media type listing, the lass line that starts with **AddType**. The format is illustrated below.

    AddType video/ogg .ogv
    AddType video/mp4 .mp4
    AddType video/webm .webm

## Apache HTTPD server - .htaccess

There may be times when you don't have access to edit the global configuration file or may want to make an exception by changing the global settings. In this instances Apache will allow you to create a special file (.htaccess) in the directory and add configuration directives that will apply only to that directory tree.

The sample below is a part of the [[Boilerplate](https://raw.github.com/h5bp/html5-boilerplate/%7CHTML5)]

    Sample Apache .htaccess mime type section, taken from the HTML5 Boilerplate

      # Audio
        AddType audio/mp4                                   m4a f4a f4b
        AddType audio/ogg                                   oga ogg

      # JavaScript
        # Normalize to standard type (it's sniffed in IE anyways):
        # http://tools.ietf.org/html/rfc4329#section-7.2
        AddType application/javascript                      js jsonp
        AddType application/json                            json

      # Video
        AddType video/mp4                                   mp4 m4v f4v f4p
        AddType video/ogg                                   ogv
        AddType video/webm                                  webm
        AddType video/x-flv                                 flv

      # Web fonts
        AddType application/font-woff                       woff
        AddType application/vnd.ms-fontobject               eot

        # Browsers usually ignore the font MIME types and sniff the content,
        # however, Chrome shows a warning if other MIME types are used for the
        # following fonts.
        AddType application/x-font-ttf                      ttc ttf
        AddType font/opentype                               otf

        # Make SVGZ fonts work on iPad:
        # https://twitter.com/FontSquirrel/status/14855840545
        AddType     image/svg+xml                           svg svgz
        AddEncoding gzip                                    svgz

## NGINX

To change this, you need to update the mime.types file in the conf directory. Depending on how you set up NGINX it could be located under /etc/nginx or /opt/nginx.

After opening the file, you should see something like this:

 types {

     text/html      html htm shtml;
     text/css      css;
     text/xml      xml;
     ...

}

## IIS

    <pre><configuration>
      <system.webServer>
        <staticContent>
          <!-- Video -->
          <mimeMap fileExtension=".mp4" mimeType="video/mp4"/>
          <mimeMap fileExtension=".webm" mimeType="video/webm"/>
        </staticContent>
      </system.webServer>
        <system.web>
            <compilation debug="true" targetFramework="4.0" />
        </system.web>
    </configuration>

## Google App Engine

    - url: /(.*\.ogv)
      static_files: videos_folder/
      mime_type: video/ogg
      upload: videos_folder/(.*\.ogv)

