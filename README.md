# docs-datanucleus

Project providing the documentation for the http://www.datanucleus.org site.
In versions up to and including v5.0 this made use of Maven "site" plugin and the "docs-datanucleus-skin" for theming of the site.
In version 5.1 and later it utilises AsciiDoc and the Maven asciidoctor plugin.
The site uses Bootstrap v3.3, Bootstrap-TOC plugin, Font Awesome, and AsciiDoc foundation CSS.

You generate the http://www.datanucleus.org website by invoking Maven "asciidoctor" plugin like this
'mvn clean compile' which generates the website under _target/site_


The generated web-site is suitable to go on a web server such as [Apache](https://httpd.apache.org).
The simplest form of set up would be what we use for the DataNucleus project. 
This involves a [Raspberry PI](https://www.raspberrypi.org) with attached SSD, running Raspberry Pi OS, with Apache 2 webserver.