
install latex for your OS

Build manually
```
pdflatex main.tex
```



















# maybe add this to workflows

```
name: LaTeX document CD

on:
  release:
    types: [created]

jobs:
  build-and-release:
    runs-on: ubuntu-latest
    steps:
      - name: Set up Git repository
        uses: actions/checkout@v2
      - name: Build and release LaTeX document
        uses: TemplatesHub/gh-action-latex-build-and-release@v2
        with:
          tex-entry-point: 'main'
          pdf-name: 'My_pdf_document'

```