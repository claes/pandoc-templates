# Pandoc-templates

Markdown is the best markup language, and [Pandoc](http://johnmacfarlane.net/pandoc/) is the best markdown
converter. Pandoc 1.4 has a new template system and since it also supports
[XeTeX](http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&item_id=xetex),
it is now possible to _easily_ create really good-looking pdf files from
Markdown, using system fonts. 

This project simply wraps Pandoc and its `markdown2pdf` program in a way that
makes it slightly simpler to customize the output. Feel free to customize and
clone and let's see how good looking pdf files we can create!

Requires:

- Pandoc 1.4 or later
- XeTeX

This pdf file was created as follows:

    ./md2pdf README.markdown.txt

`md2pdf` is a simple shell script wrapper that contains variables to set
font, font size, paper size, language (for hyphenation), margins and a few
more things.

For fonts, on Linux, first run `fc-list` to see what fonts you have available
on your system, then make your choice, edit `md2pdf` and set them. For
example, if you have installed [Microsoft Core Fonts for the Web](http://en.wikipedia.org/wiki/Core_fonts_for_the_Web), you can set

    mainfont=Georgia
    sansfont=Verdana
    monofont="Courier New"

as was done for this document.
