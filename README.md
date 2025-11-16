# babel-hungarian
Hungarian language support for the babel multilingual package in LaTeX.

The babel-hungarian on the CTAN website:
[https://ctan.org/pkg/babel-hungarian](https://ctan.org/pkg/babel-hungarian)

Hungarian typography in LaTeX in this TUG 2004 article:
[http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf](http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf)

There is a longer user manual in Hungarian:
[http://math.bme.hu/latex/magyarldf-doc.pdf](http://math.bme.hu/latex/magyarldf-doc.pdf)

Usage:

    \usepackage[T1]{fontenc}% when using pdflatex
    \PassOptionsToPackage{defaults=hu-min}{hungarian.ldf}
    \usepackage[hungarian]{babel}

or

    \usepackage[T1]{fontenc}% when using pdflatex
    \PassOptionsToPackage{defaults=hu-min}{magyar.ldf}
    \usepackage[magyar]{babel}

or

    \DocumentMetadata{lang=hu}
    \usepackage[T1]{fontenc}% when using pdflatex
    \PassOptionsToPackage{defaults=hu-min}{hungarian.ldf}
    \usepackage{babel}