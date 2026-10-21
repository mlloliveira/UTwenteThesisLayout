# University of Twente thesis layout

A customizable LaTeX thesis template based on `memoir`, with a guide built into the example thesis. Each chapter demonstrates how to write, organize and personalize the document using the layout itself.

## Features

- Separate chapter folders, with figures stored alongside their chapter.
- University of Twente front matter, English and Dutch summaries, and a separate propositions insert.
- Global lists of mathematical symbols and abbreviations, with hyperlinks and first-use page references.
- Separate bibliographies for consulted literature and the author's publications.
- Chapter colours, edge markers, running headings, and circular page numbers.
- Editable covers and examples of figures, tables, equations, theorem boxes and algorithms.
- A 170 × 240 mm book format with 3 mm bleed, configurable for other page sizes.

## Getting started

Use a recent TeX Live or MiKTeX installation with the packages listed in [Configuration.tex](Configuration.tex). The template uses **pdfLaTeX** and **BibTeX**.

1. Clone or download this repository.
2. Edit [ThesisDetails.tex](ThesisDetails.tex) to set your titles, name, defence date, supervisors, identifiers and cover paths. These details are shared by the thesis and propositions insert.
3. Set `main.tex` as the main document and build from the repository root:

```sh
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Alternatively, use `latexmk -pdf main.tex`. Repeat pdfLaTeX if the log requests another pass; acronyms, symbol pages and cross-references depend on auxiliary files.

For Overleaf or another online LaTeX editor, upload the repository contents, select `main.tex` as the main document, and choose pdfLaTeX.

Build the propositions insert separately:

```sh
pdflatex propositions.tex
```

## Using the template

Replace the example chapter text with your research and keep each chapter's figures in its own `fig` directory. Update the front matter, summaries and acknowledgements in `Chapters/Chapter_0/`.

| File or directory | Purpose |
| --- | --- |
| [ThesisDetails.tex](ThesisDetails.tex) | Shared personal and publication details |
| [main.tex](main.tex) | Chapter order and document structure |
| [Configuration.tex](Configuration.tex) | Packages, page geometry, colours and styles |
| [DeclareSymbols.tex](DeclareSymbols.tex) | Symbol declarations and the global symbol registry |
| [MathOperators.tex](MathOperators.tex) | Mathematical operators and delimiter helpers |
| `Chapters/Chapter_0/` | Front matter and front cover |
| `Chapters/Chapter_1/` through `Chapter_8/` | Chapter content and local figure folders |
| `Chapters/Chapter_Appendix/` | Acronyms, symbols, notation and back cover |
| [References/references.bib](References/references.bib) | Consulted literature |
| [References/publications.bib](References/publications.bib) | Your publications; use `keywords={mypub}` |
| [propositions.tex](propositions.tex) | Standalone propositions insert |

Declare symbols in `DeclareSymbols.tex` and acronyms in `Chapters/Chapter_Appendix/Acronyms.tex`. Customize colours, typography and page styles in `Configuration.tex`; small personal overrides can go at the end of `ThesisDetails.tex`.

## Built-in guide

Compile `main.tex` to read the guide alongside its rendered examples.

| Chapter | Topic |
| --- | --- |
| 1 | Setup, file structure and compilation |
| 2 | Metadata, university pages, summaries and propositions |
| 3 | Figures, subfigures, tables, TikZ and algorithms |
| 4 | Symbols, equations, acronyms and theorem boxes |
| 5 | References, publications, citations and publication notes |
| 6 | Colours, fonts, margins, covers, edge markers and page numbers |
| 7 | Section files, appendices, partial builds and package responsibilities |
| 8 | Preparing your thesis and sharing its source |

The notation appendix provides a command reference.

## University requirements

The front matter is based on the [University of Twente Doctoral Regulations effective 1 January 2026](https://www.utwente.nl/en/education/tgs/downloads-forms/phd-downloads/ut-doctoral-regulations.pdf), including the title-page model in Annex 3. Submit your final title pages for approval through the [UT graduation workflow](https://www.utwente.nl/en/service-portal/research-support/phd-engd-programmes-tgs/doctorate-phdengd-monitoring-system).

The chapter palette, typography, covers and book dimensions can be personalized independently of the required front-matter content.


## Authorship

The original thesis layout and design are by **Marcio L. Lima de Oliveira**, with contributions credited to **V. el Hakim**.

The explanatory guide was written by **AI (OpenAI Codex)**. This attribution concerns the guide, not the authorship of the original layout.

## License and assets

The template source and documentation are licensed under the [LaTeX Project Public License version 1.3c](LICENSE). Copyright © 2026 Márcio Luiz Lima de Oliveira and V. el Hakim. The project is author-maintained by Márcio Luiz Lima de Oliveira.

The NASA/Apollo 17 photograph and University of Twente logo have separate attribution and reuse information: [photograph credits](Chapters/Chapter_3/fig/ATTRIBUTION.txt) and [logo notice](Chapters/Chapter_0/fig/ATTRIBUTION.txt). See [LICENSING.txt](LICENSING.txt) and [MANIFEST.txt](MANIFEST.txt) for license scope and the source-file list.
