# orm_book_samples

This directory contains skeleton/boilerplate book files for use with the O'Reilly Media, Inc. internal publishing tools.

----
NOTE: If you update any boilerplate in this repo, please update each filetype (HTMLBook, AsciiDoc, DocBook) as necessary and then deploy to the Atlas templates with the following:

SCRIPT DETAILS TO COME

----

## File Organization

* root - standard files
  * book files for use with all Atlas projects regardless of content format
  * pdf.css (common theme overrides)
  * layout.html (use to specify EPUB/MOBI metadata)
* asciidoc_only/
  * book files for use in AsciiDoc projects only
  * v1_only/
    * book files for use with AsciiDoc projects in Atlas v1 (deprecated)
* docbook_only/
  * book files for use in DocBook projects only
  * v1_only/
    * book files for use with DocBook projects in Atlas v1 (deprecated)
* htmlbook_only/
  * book files for use in HTMLBook projects only