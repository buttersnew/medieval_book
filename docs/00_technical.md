### Requirements

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

### Compilation

To build the PDF, run the following commands (or use your preferred LaTeX editor):

```bash
xelatex main.tex
makeglossaries main
xelatex main.tex
xelatex main.tex
```

*Note: `makeglossaries` is required to generate the character and term indices.*

### Project Layout

- `main.tex`: The master document file.
- `content/`: Contains the chapters organized by book.
- `frontmatter/`: Title page, copyright, and preface.
- `misc/`: Style definitions (`options.sty`).
