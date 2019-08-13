# About
Pandoc Markdoen/LaTeX Templates for Open University TMAs, EMAs, papers etc. 

Based on [eisvogel pandoc LaTeX templates](https://github.com/Wandmalfarbe/pandoc-latex-template)

# TODO
Add tutor name on title page.

Nicer demo content

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

## Compile

### PDF
`pandoc "template.md" -o "template.pdf" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

### DOCX
`pandoc "template.md" -o "template.docx" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

Note: Table of contents is not automatically displayed in some text editors such as google docs and libre office
