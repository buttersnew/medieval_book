# The Saga of Hrōþigar

**Author:** Nero
**Publisher:** PILOS
**Edition:** 2026

## Overview

This repository contains the LaTeX source code for *The Saga of Hrōþigar*, an epic saga set in the Migration Era—a time of meadhalls and ancient feuds that laid the foundation for the Viking sagas to come. The story follows the journey of a warrior of Jutland blood, seeking glory and purpose in the shadow of Heorot.

## Structure

The work is divided into multiple books:
- **Book 1**
- **Book 2**
- **Book 3**
- **Book 4**
- **Book 5**
- **Book 6**
- **Book 7**

The project also includes prologues, epilogues, and appendices containing character registers and glossaries.

## Requirements

To compile this document, you need a standard LaTeX distribution (like TeX Live or MiKTeX) with `XeLaTeX` or `LuaLaTeX` (required for `fontspec`).

### Dependencies
The project relies on several LaTeX packages, including:
- `fontspec` (for font management)
- `microtype` (for typography enhancements)
- `glossaries` (for character and term management)
- `tikz` (for graphical elements)
- `csquotes`
- `lettrine`

### Fonts
The document uses specific fonts that must be installed on your system:
- **Main Font:** EB Garamond
- **Title/Display Font:** PfefferMediaeval

## Compilation

To build the PDF, run the following commands (or use your preferred LaTeX editor):

```bash
xelatex main.tex
makeglossaries main
xelatex main.tex
xelatex main.tex
```

*Note: `makeglossaries` is required to generate the character and term indices.*

## Project Layout

- `main.tex`: The master document file.
- `content/`: Contains the chapters organized by book.
- `frontmatter/`: Title page, copyright, and preface.
- `misc/`: Style definitions (`options.sty`).
- `prolog_epilog/`: Prologue and epilogue texts.
