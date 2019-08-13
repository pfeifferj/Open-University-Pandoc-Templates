# About
Pandoc Markdoen/LaTeX Templates for Open University TMAs, EMAs, papers etc. 

Based on [eisvogel pandoc LaTeX templates](https://github.com/Wandmalfarbe/pandoc-latex-template)

# TODO
Add tutor name on title page.

Nicer demo content

# Dependencies
* LaTeX

* Texlive LaTeX extra

* Texlive tilting

* Pandoc

# Compile

## PDF
`pandoc "template.md" -o "template.pdf" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

## DOCX
`pandoc "template.md" -o "template.docx" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

Note: Table of contents is not automatically displayed in some text editors such as google docs and libre office
