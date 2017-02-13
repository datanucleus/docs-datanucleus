# docs-datanucleus

Project providing the documentation for the http://www.datanucleus.org site.
In versions up to and including v5.0 this made use of Maven "site" plugin and the "docs-datanucleus-skin" for theming of the site.
In version 5.1 and later it utilises AsciiDoc and the Maven asciidoctor plugin; this is an on-going process to migrate all docs so use v5.0 if you require complete docs.

You generate the http://www.datanucleus.org website by invoking Maven "asciidoctor" plugin like this
'mvn clean compile' which generates the website under _target/site_
