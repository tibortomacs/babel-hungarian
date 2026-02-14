# babel-hungarian

Hungarian language support for the babel multilingual package in LaTeX.

The babel-hungarian on the CTAN website:
[https://ctan.org/pkg/babel-hungarian](https://ctan.org/pkg/babel-hungarian)

Hungarian typography in LaTeX in this TUG 2004 article:
[https://math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf](https://math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf)

There is a longer user manual in Hungarian:
[https://math.bme.hu/latex/magyarldf-doc.pdf](https://math.bme.hu/latex/magyarldf-doc.pdf)

Detailed instructions and learning materials on how to use LaTeX for Hungarian language documents can be found at the following link:
[https://tibortomacs.github.io/latex-tutorial-hu](https://tibortomacs.github.io/latex-tutorial-hu)

## Usage

To typeset text in Hungarian, please in the preamble, use
```
\usepackage[T1]{fontenc}% only needed for latex/pdflatex
\PassOptionsToPackage{defaults=hu-min}{hungarian.ldf}% or \def\hungarianOptions{defaults=hu-min}
\usepackage[hungarian]{babel}
```
or
```
\usepackage[T1]{fontenc}% only needed for latex/pdflatex
\PassOptionsToPackage{defaults=hu-min}{magyar.ldf}% or \def\magyarOptions{defaults=hu-min}
\usepackage[magyar]{babel}
```
or
```
\DocumentMetadata{lang=hu}
\documentclass{...}
\PassOptionsToPackage{defaults=hu-min}{hungarian.ldf}% or \def\hungarianOptions{defaults=hu-min}
\usepackage{babel}
```

## Changelog

### v1.6a (2026-02-03)

- Introduced new option handling using `\DeclareKeys`, allowing spaces before and after the `=` sign.
- Removed support for `\input magyar.ldf` (poor practice; compilation should fail instead).
- Removed deprecated options; their use now emits a warning:
`accents`, `amslevelfix`, `amsuppercasefix`,
`babelmarkfix`
(see [65458c4](https://github.com/tibortomacs/babel-hungarian/commit/65458c4)
and
[837305d](https://github.com/tibortomacs/babel-hungarian/commit/837305d)), 
`captionfix`, `cjhebrewfix`, `hyphenation`, and `showfix`.
- Fixed:
commits
[6a5d987](https://github.com/tibortomacs/babel-hungarian/commit/6a5d987)
[add944e](https://github.com/tibortomacs/babel-hungarian/commit/add944e),
[ef82fd4](https://github.com/tibortomacs/babel-hungarian/commit/ef82fd4),
issues
[#1](https://github.com/tibortomacs/babel-hungarian/issues/1),
[#2](https://github.com/tibortomacs/babel-hungarian/issues/2),
[#3](https://github.com/tibortomacs/babel-hungarian/issues/3),
[#4](https://github.com/tibortomacs/babel-hungarian/issues/4),
[#5](https://github.com/tibortomacs/babel-hungarian/issues/5),
[#6](https://github.com/tibortomacs/babel-hungarian/issues/6),
[#7](https://github.com/tibortomacs/babel-hungarian/issues/7),
and
[#8](https://github.com/tibortomacs/babel-hungarian/issues/8).
- Implemented:
issues
[#9](https://github.com/tibortomacs/babel-hungarian/issues/9)
and
[#10](https://github.com/tibortomacs/babel-hungarian/issues/10).

## License

This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3 of this license or (at your option) any later version.
The latest version of this license is in   [https://www.latex-project.org/lppl.txt](https://www.latex-project.org/lppl.txt) and version 1.3c or later is part of all distributions of LaTeX version 2008 or later.