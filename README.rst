=========================================
 Convert tool from Pukiwiki to MediaWiki
=========================================

Usage
======

Pukiwiki Format Text `~/Document.pukiwiki` is converted to `~/Document.mediawiki`. ::

    $ cat ~/Document.pukiwiki | sed -z -f pukiwiki-to-mediawiki.sed > ~/Document.mediawiki


Supported Items
===============

- Header
- List
- Preformatted Text
- Table (Only simple pattern. rowspan, colspan are not supported)
- Strings [#xxxxxxxx] in headers are removed
  
Unsupported Items
=================

- Table including rowspan or colspan

Test Environment
================

GNU sed 4.2.2

**Over 4.2.2 is needed, because -z option is used.**

