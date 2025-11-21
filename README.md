# babel-hungarian
Hungarian language support for the babel multilingual package in LaTeX.

The babel-hungarian on the CTAN website:
[https://ctan.org/pkg/babel-hungarian](https://ctan.org/pkg/babel-hungarian)

Hungarian typography in LaTeX in this TUG 2004 article:
[http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf](http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf)

There is a longer user manual in Hungarian:
[http://math.bme.hu/latex/magyarldf-doc.pdf](http://math.bme.hu/latex/magyarldf-doc.pdf)

To typeset text in Hungarian, please in the preamble, use

    \usepackage[T1]{fontenc}% only needed for latex/pdflatex
    \PassOptionsToPackage{defaults=hu-min}{hungarian.ldf}% or \def\hungarianOptions{defaults=hu-min}
    \usepackage[hungarian]{babel}

or

    \usepackage[T1]{fontenc}% only needed for latex/pdflatex
    \PassOptionsToPackage{defaults=hu-min}{magyar.ldf}% or \def\magyarOptions{defaults=hu-min}
    \usepackage[magyar]{babel}

or

    \DocumentMetadata{lang=hu}
    \documentclass{...}
    \usepackage[T1]{fontenc}% only needed for latex/pdflatex
    \PassOptionsToPackage{defaults=hu-min}{hungarian.ldf}% or \def\hungarianOptions{defaults=hu-min}
    \usepackage{babel}