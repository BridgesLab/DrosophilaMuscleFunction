The latex input files were generated mostly automatically from the word document files using this command

`textutil -convert html ../Manuscript.docx -stdout | pandoc -s -f html -t latex -o Manuscript.tex`

They were then manually adjusted for the footnotes, section headers and the figure/table placement
