# babel-hungarian

Hungarian language support for the babel multilingual package in LaTeX.

The babel-hungarian on the CTAN website:
[https://ctan.org/pkg/babel-hungarian](https://ctan.org/pkg/babel-hungarian)

Hungarian typography in LaTeX in this TUG 2004 article:
[http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf](http://www.math.bme.hu/latex/dl/pts_tug2004_magyarldf2.pdf)

There is a longer user manual in Hungarian:
[http://math.bme.hu/latex/magyarldf-doc.pdf](http://math.bme.hu/latex/magyarldf-doc.pdf)

## Usage

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

## Changelog

### v1.5e (unreleased)

- Remove support for `\input magyar.ldf`. This is a bad practice, it is better if the compilation fails.
- `\ProvidesLanguage` and `\LdfInit` without unnecessary `\expandafters`.
- Delete `\magyar@do@option@low`.
- Fix: The `defaults=safest` option generates bad `\today` command.
- Fix: `babelmarkfix=yes` option generates test characters in the header of empty pages with newer babel versions. It lost its original function with newer babel versions anyway, so the option has been removed, with a warning about it.
- Fix: `\DocumentMetadata{lang=hu}` crashed with `\@@magyar@mathbins@tabularfix` in some cases.
- Remove the deprecated `captionfix` and `showfix` options, with a warning about them.
- New option handling using `\DeclareKeys`.
- Redefining `\hungarianDumpHuMin` due to new option handling.
- Using `\magyar@deprecatedopt` for deprecated option group.

### v1.5d (2025/05/02)

- Fix: `magyar.ldf` interferes with the anchors `hyperref` creates for theorem-like environments, so cross-references jump to the wrong location. When `amsthm` is also loaded, the interaction produces duplicate PDF destination names.
- Instead of `t1enc`, we recommend the `fontenc` package with the `T1` option.
- Remove recommendation for `latin2` input encoding.

---

This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3 of this license or (at your option) any later version.
The latest version of this license is in http://www.latex-project.org/lppl.txt and version 1.3 or later is part of all distributions of LaTeX version 2005/12/01 or later.

---