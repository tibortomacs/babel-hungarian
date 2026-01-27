# babel-hungarian

Hungarian language support for the babel multilingual package in LaTeX.

The babel-hungarian on the CTAN website:
[https://ctan.org/pkg/babel-hungarian](https://ctan.org/pkg/babel-hungarian)

Hungarian typography in LaTeX in this TUG 2004 article:
[http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf](http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf)

There is a longer user manual in Hungarian:
[http://math.bme.hu/latex/magyarldf-doc.pdf](http://math.bme.hu/latex/magyarldf-doc.pdf)

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

### v1.6a (unreleased)

- New option handling using `\DeclareKeys`.
This allows spaces before/after the `=` sign.
- Remove support for `\input magyar.ldf`. This is poor practice; it is better if the compilation fails.
- Remove deprecated options, with a warning about them:
`accents`, `amslevelfix`, `amsuppercasefix`,
`babelmarkfix`
(see [071d93b](https://github.com/tibortomacs/babel-hungarian/commit/071d93b),
[8849eb8](https://github.com/tibortomacs/babel-hungarian/commit/8849eb8)), 
`captionfix`, `cjhebrewfix`, `hyphenation`, and `showfix`.
- Fixed:
[116d69b](https://github.com/tibortomacs/babel-hungarian/commit/116d69b),
[8ff175f](https://github.com/tibortomacs/babel-hungarian/commit/8ff175f),
[issue #1](https://github.com/tibortomacs/babel-hungarian/issues/1),
[issue #2](https://github.com/tibortomacs/babel-hungarian/issues/2),
[issue #3](https://github.com/tibortomacs/babel-hungarian/issues/3),
[issue #4](https://github.com/tibortomacs/babel-hungarian/issues/4),
[issue #5](https://github.com/tibortomacs/babel-hungarian/issues/5),
[issue #6](https://github.com/tibortomacs/babel-hungarian/issues/6),
[issue #7](https://github.com/tibortomacs/babel-hungarian/issues/7),
[issue #8](https://github.com/tibortomacs/babel-hungarian/issues/8)
- Resolved:
[issue #9](https://github.com/tibortomacs/babel-hungarian/issues/9),
[issue #10](https://github.com/tibortomacs/babel-hungarian/issues/10)


### v1.5d (2025-05-02)

- Fix: `magyar.ldf` interferes with the anchors created by `hyperref` for theorem-like environments, causing cross-references to jump to the wrong location.
When the `amsthm` package is also loaded, duplicate PDF destination names are produced.
[f115d8a](https://github.com/tibortomacs/babel-hungarian/commit/f115d8a)
- Instead of `t1enc`, we recommend the `fontenc` package with the `T1` option.
- Remove the recommendation for the `latin2` input encoding.

## License

This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3 of this license or (at your option) any later version.
The latest version of this license is in http://www.latex-project.org/lppl.txt and version 1.3 or later is part of all distributions of LaTeX version 2005/12/01 or later.