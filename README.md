# orm_book_samples

This directory contains skeleton/boilerplate book files for use with the O'Reilly Media, Inc. internal publishing tools.

----
NOTE: If you update any boilerplate in this repo, please update each filetype (HTMLBook, AsciiDoc, DocBook) as necessary and then deploy to the Atlas templates with the following:

Script Man File:

Usage
$ [options] v2sample_template_update

Examples
$ peripheral=true v2sample_template_update
$ format_specific=true asc=true v2sample_template_update

Variables

peripheral
   =true  - Specifies that peripheral files should be updated (this updates to every template) 

format_specific
   =all    - (NOTE ADDED YET) Pushes updates to each atlas template's format specific files
   =true   - Use in conjunction with a asc/db/html variables to specify which main content files
             should be updated.    
   asc
      =true  - Specifies that the asciidoc template repo's format specific files will be updated
   db
      =true  - Specifies that the docbook template repo's format specific files will be updated
   html
      =true  - Specifies that the htmlbook template repo's format specific files will be updated

eso
    =true   - (NOT ADDED YET) used for pushing esoteric files (in case we want this)

----

## File Organization

* root - standard files
  * book files for use with all Atlas projects regardless of content format
  * pdf.css (common theme overrides)
  * layout.html (use to specify EPUB/MOBI metadata)
  * README.md (this file)
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
