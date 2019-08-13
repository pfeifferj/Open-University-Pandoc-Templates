#Compile

## PDF
`pandoc "template.md" -o "template.pdf" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

## DOCX
`pandoc "template.md" -o "template.docx" --from markdown --template "eisvogel.latex" --filter pandoc-citeproc --bibliography "references.bib"`

Note: Table of contents is not automatically displayed in some text editors such as google docs and libre office
