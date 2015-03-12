# orm_book_samples

This directory contains skeleton/boilerplate book files for use with the O'Reilly Media, Inc. internal publishing tools.

Steps for updating Atlas template repos.

<ol>
<li>
<p>Log on to Touchstone</p>
</p>This script can be run anywhere on Touchstone.</p>
</li>

<li> <p>Decide what you want to update.</p>
<ul>
  <li><p>Peripheral files that are common to each repo can be updated.</p>
  <p><b>NOTE</b>: Updating peripheral files will always update all the Atlas template repos</p>
  
  </li>
 <li><p>Format specific files that are specific to each template can be updated.</p>
  <p><b>NOTE</b>: You need to explicitly state which formats you want to update.</p>
  </li>
</ul>
</li>

<li>
<p>Run the script</p>
<p><code>$ [variables] v2sample_template_update</code></p>
<p>Here's a list of the variables to specify when you run the command:</p>

   <ul>
    <li>
     <p>To update format specific files</p>
     <pre>
     format_specific=true asc=true # Specifies to update asciidoc template repo
     format_specific=true db=true # Specifies to update db template repo
     format_specific=true html=true # Specifies to update html template repo</code></pre>
    </li>
   <li>
     <p>To update peripheral files</p>
     <pre>peripheral=true # Specifies to update every template repo's common files (like, titlepage.html, 
                                                                           toc.html, and so on) </pre>
    </li>
   </ul>

</li>
</ol>

<p>TIPs:</p>
<ol>
<li>
<p>You can update format specific files for more than one sample repo at a time.<p>
<pre>
#Examples
$ format_specific=true asc=true db=true v2sample_template_update
$ format_specific=true asc=true db=true html=true v2sample_template_update
</pre>
</li>
<li>
<p>You can update format specific files and peripheral files at the same time. (Peripheral file updates will be pushed to every template repo, but the format specific updates only apply to the repo specified):<p>
<pre>#Examples
$ peripheral=true format_specific=true asc=true v2sample_template_update
$ peripheral=true format_specific=true asc=true db=true html=true v2sample_template_update
</pre>
</li>

</ol>

----
NOTE: If you update any boilerplate in this repo, please update each filetype (HTMLBook, AsciiDoc, DocBook) as necessary and then deploy to the Atlas templates with the following:

Script Man File:
```
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
```
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
