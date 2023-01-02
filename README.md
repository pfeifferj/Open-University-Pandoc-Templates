# About
**Unofficial** Pandoc Markdown/LaTeX Templates for Open University TMAs, EMAs, papers etc. 

Based on [eisvogel pandoc LaTeX templates](https://github.com/Wandmalfarbe/pandoc-latex-template)


# Usage
## Dependencies
* LaTeX
* Texlive LaTeX extra
* Texlive tilting
* Pandoc

## Install
Move the template eisvogel.latex to your pandoc templates folder. The location of the templates folder depends on your operating system:

* Unix, Linux, macOS: `$XDG_DATA_HOME/pandoc/templates`, `~/.pandoc/templates/` or `/usr/share/pandoc/data/templates/`
* Windows XP: `C:\Documents And Settings\USERNAME\Application Data\pandoc\templates`
* Windows Vista or later: `C:\Users\USERNAME\AppData\Roaming\pandoc\templates`

If there are no folders called templates or pandoc you need to create them and put the template eisvogel.latex inside.

## Writing
### Importing Presets
You can save settings such as author, module name, tutor etc. in a yaml file and use it to create new documents using [pandocomatic](https://github.com/htdebeer/pandocomatic).

### Count Words
`wordcount.lua` is included in the repo. The filter counts body text and ignores metadata, headings, references etc.

`pandoc --lua-filter wordcount.lua myfile.md`

### Spell Check
If you're using vim as your text editor, don't forget to [enable spell check](https://www.linux.com/learn/using-spell-checking-vim). 

### Referencing
1. Create a reference in references.bib 

Example:

```
@ARTICLE{smit54,
	AUTHOR = {J. G. Smith and H. K. Weston},
	TITLE = {Nothing Particular in this Year's History},
	YEAR = {1954},
	JOURNAL = {J. Geophys. Res.},
	VOLUME = {2},
	PAGES = {14-15}
}
```

2. Reference in text using `[@smit54]` 

#### Common OU specific questions
##### How do I cite online/module content?

Example:

```
@ONLINE{jj19,
	AUTHOR = {{Johnson {\&} Johnson}},
	TITLE = {Who we are},
	YEAR = {2019},
	URL = {http://www.jnj.ch/en/about-us/who-we-are.html},
	URLDATE = {2019-06-27}
```

Prints:

```
Johnson & Johnson (2019e) Who we are [Online]. Available at http://www.jnj.ch/en/aboutus/who-we-are.html (Accessed 27 June 2019).
```

##### How do I spell out the author name if it is a company or organisation?

Wrap the author in ``{{ }}``

##### Why are capitalisations lost in titles?

This is not a bug; it's a feature.

Wrap the title in ``{{ }}``

## Compiling

### PDF
`pandoc "template.md" -o "template.pdf" --from markdown --template "eisvogel.latex" --citeproc --bibliography "references.bib"`

### DOCX
`pandoc "template.md" -o "template.docx" --from markdown --template "eisvogel.latex" --citeproc --bibliography "references.bib"`

Note: Table of contents is not automatically displayed in text editors such as google docs and libre office
