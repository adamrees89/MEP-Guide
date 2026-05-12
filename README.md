# MEP Guide

A LaTeX source repository for a Building Services / Mechanical, Electrical and Plumbing (MEP) design reference guide. This project collects calculation methods, system design guidance, and technical notes for ventilation, heating, cooling, domestic water services, and drainage topics.

## Repository Contents

- `MEP_Guide.tex` - Main LaTeX document that assembles the guide.
- `MEP_Guide.pdf` - Current generated PDF output.
- `main.tdo` - To-do list for draft content and author notes.
- `chapters/` - Chapter source files for individual sections of the guide.
- `graphics/` - Supporting graphics and schematic drawings used in the document.
- `supportfiles/` - LaTeX support files including title page, glossary, and preamble setup.
- `texlive/` - Helper files for installing TeX Live and a package list for reproducible builds.
- `library.bib` - Bibliography file for references.

## What this repository is for

This repository provides the LaTeX source for an MEP educational guide. The document structure currently includes:

- Ventilation
- Heating and Cooling
- Domestic Water Services
- Drainage and Rainwater

*The project is in draft form and includes markup for glossary entries, acronyms, figures, and to-do notes.*

## Build Instructions

### Requirements

- A working LaTeX distribution such as TeX Live or MiKTeX.
- The packages listed in `texlive/texlive_packages`.
- `makeglossaries` for glossary generation.

### Recommended build steps

From the repository root:

```bash
pdflatex MEP_Guide.tex
makeglossaries MEP_Guide
pdflatex MEP_Guide.tex
pdflatex MEP_Guide.tex
```

If you use a LaTeX workflow tool such as `latexmk`:

```bash
latexmk -pdf MEP_Guide.tex
```

### Linux / macOS helper

For a reproducible TeX Live installation, use the included script:

```bash
bash texlive/texlive_install.sh
```

This script installs TeX Live 2026 into `/tmp/texlive`, configures the repository, and installs the packages listed in `texlive/texlive_packages`.

> On Windows, install TeX Live or MiKTeX through the normal installer and ensure the required packages are available.

## Project structure

### Top-level files

- `README.md` - This file.
- `LICENSE` - Repository license.
- `CODE_OF_CONDUCT.md` - Community guidelines.
- `CONTRIBUTING.md` - Contribution rules and workflow.
- `library.bib` - Bibliography referenced from the document.

### Source files

- `MEP_Guide.tex` - Root document that includes chapter files.
- `chapters/` - Modular chapter content for each section.
- `supportfiles/` - Setup, title, glossary, and formatting definitions.

### Output and support

- `MEP_Guide.pdf` - Built PDF document included as current output.
- `texlive/texlive_packages` - Required LaTeX package list.
- `texlive/texlive_install.sh` - Installation helper for TeX Live.

## Contributing

This repository already includes a `CONTRIBUTING.md` file. Use it for:

- proposing new chapter content
- suggesting edits or corrections
- adding figures, tables, and worked examples
- improving LaTeX build and formatting

If you are unsure where to contribute, start by opening an issue or pull request.

## Notes

- The document currently contains draft material and to-do notes.
- The LaTeX source is arranged so chapters can be edited independently in `chapters/`.
- `supportfiles/set-up.tex` contains the document preamble and package configuration.

## Useful commands

```bash
# Build the document
pdflatex MEP_Guide.tex
makeglossaries MEP_Guide
pdflatex MEP_Guide.tex

# Clean auxiliary files
rm *.aux *.log *.toc *.gls *.glo *.glg *.ist *.gz
```

## License and governance

This project is governed by the files already included in the repository:

- `LICENSE`
- `CODE_OF_CONDUCT.md`
- `CONTRIBUTING.md`

Please refer to those files before contributing.
