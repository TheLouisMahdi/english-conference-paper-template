# English Conference Paper Template

A four-page example for writing an English engineering conference paper in a two-column IEEEtran layout. It includes a short abstract, a numbered equation, an editable diagram, results tables, and references. The example uses an analytical model with stated inputs.

## Examples

[View the four-page PDF](examples/conference-paper-example.pdf) · [Download the editable Word sample](examples/conference-paper-example.docx?raw=true)

## Start a paper

1. Select **Use this template** on GitHub, or download the source from **Code → Download ZIP**.
2. Edit the title, author, affiliation, abstract, and keywords in [frontmatter.tex](frontmatter.tex).
3. Replace the text in [sections/](sections/), update [references.bib](references.bib), and adapt the diagram in [figures/](figures/).
4. Build [paper.tex](paper.tex). The manuscript flows across pages as it grows. [example.tex](example.tex) reproduces the four-page sample with section breaks.

## Build the PDF

Use XeLaTeX and BibTeX with a recent TeX Live or MiKTeX installation and the IEEEtran, fontspec, etoolbox, and PGF/TikZ packages. The source uses **Times New Roman**. Install that font or set `\PaperFont` to `TeX Gyre Termes` in `frontmatter.tex` for an open substitute supplied by the `tex-gyre` package.

```sh
xelatex paper.tex
bibtex paper
xelatex paper.tex
xelatex paper.tex
```

The same commands with `example` in place of `paper` build the sample. In Overleaf, choose **XeLaTeX** and set **Main document** to `paper.tex`.

The [IEEEtran class](https://ctan.org/pkg/ieeetran) supplies the conference layout. This starter is an independent example. Each venue sets its own page limits and submission format.
