# About
**Unofficial** Pandoc Markdown/LaTeX Templates for Open University TMAs, EMAs, papers etc. 

Based on [eisvogel pandoc LaTeX templates](https://github.com/Wandmalfarbe/pandoc-latex-template)

# TODO
- [ ] Nicer demo content
- [ ] Write command-line tool to:
* Generate reusable profiles ie. for modules
* Create documents using saved profiles
* Import TMA questions & guidance notes into document from OU pdfs

# Using
## Dependencies
* LaTeX
* Texlive LaTeX extra
* Texlive tilting
* Pandoc

## Installing
Move the template eisvogel.latex to your pandoc templates folder. The location of the templates folder depends on your operating system:

* Unix, Linux, macOS: `$XDG_DATA_HOME/pandoc/templates`, `~/.pandoc/templates/` or `/usr/share/pandoc/data/templates/`
* Windows XP: `C:\Documents And Settings\USERNAME\Application Data\pandoc\templates`
* Windows Vista or later: `C:\Users\USERNAME\AppData\Roaming\pandoc\templates`

If there are no folders called templates or pandoc you need to create them and put the template eisvogel.latex inside.

## Writing
## Spell Check
If you're using vim as your text editor, don't forget to [enable spell check](https://www.linux.com/learn/using-spell-checking-vim). 

## Referencing
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

## Compiling

### PDF
`pandoc "template.md" -o "template.pdf" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

### DOCX
`pandoc "template.md" -o "template.docx" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

Note: Table of contents is not automatically displayed in some text editors such as google docs and libre office
