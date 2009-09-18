# Skim.app Templates #

This is a collection of templates for exporting notes from [Skim.app](http://skim-app.sourceforge.net/) the open source PDF reader and note-taker for Mac OS X.

## Templates ##

### Notes as HTML ###

This template exports all annotations into a single HTML file to create a kind of summary of the text. The notes are color-coded; highlights are yellow, free-text and anchored notes are green, and everything else (circles, boxes, strike-outs, underlines, lines and freehand drawings) are red, to indicate they won't necessarily make much sense, unless you have annotated them with descriptive text. 

Each note is displayed in a `blockquote` element with a `cite` element containing its page number (or page index). Each `blockquote` element has a `title`-attribute containing the name of the note type, which is displayed as a tooltip on hover in most browsers.

The title of the original PDF-file in the heading is a link, so provided you haven't moved the original file, you can click this link to open the file.

## How to use ##

Install a template by placing it in `~/Library/Application Support/Skim/Templates` (where `~` is your home folder), creating this last folder if it does not yet exist.

From within Skim.app you can then select `File > Export...` and the template(s) will then be available from the `File Format` dropdown menu.

## How to edit ##

If you want to edit any of the templates or create your own, you will find [the templating language documented on the Skim wiki](http://sourceforge.net/apps/mediawiki/skim-app/index.php?title=Templates).

Any plain text formatted templates can be edited directly, and if you are comfortable editing raw HTML and CSS, you can edit the .html-templates directly as well. For easier editing, however, I recommend working with the included .haml source files.

Check out the [Haml](http://haml-lang.com/) and [Sass documentation](http://sass-lang.com/) and you will quickly be able to grok the structure of the file. Haml and Sass significantly simplify HTML and CSS markup, respectively, and especially Haml's auto-closing of tags makes editing HTML much easier and less error-prone.

To convert your edited .haml-file to HTML, first install the Haml gem if you haven't already by running this command on the command-line (in Terminal.app if you are on Mac OS X), typing your password when prompted:

    sudo gem install haml

Then navigate to the folder containing your .haml-file on the command-line (if you are on Mac OS X, optionally install [cdto](http://code.google.com/p/cdto/) to quickly open a Finder folder in Terminal.app) and convert it via the `haml` command-line utility:

    haml input.haml output.html

So for instance:

    haml "Notes as HTML.haml" "Notes as HTML.html"

(Note the added quotation marks because the filenames contain spaces).

## License ##

These templates are released under the MIT License, so hack away, sailor!

    Copyright (c) 2009 Dan Andrew Brendstrup

    Permission is hereby granted, free of charge, to any person obtaining a
    copy of this software and associated documentation files (the "Software"),
    to deal in the Software without restriction, including without limitation
    the rights to use, copy, modify, merge, publish, distribute, sublicense,
    and/or sell copies of the Software, and to permit persons to whom the
    Software is furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included
    in all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
    OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
    MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN
    NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
    DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
    OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE
    USE OR OTHER DEALINGS IN THE SOFTWARE.