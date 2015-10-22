# Report Template
Generic report template for the MultiMarkdown-LaTeX framework. This acts as a barebones framework for integrating a LaTeX  template into the MultiMarkdown system.

# Usage

In order to use this template, the [papers_base](https://github.com/trecvt-oss/papers_base) must be cloned and configured correctly. This repository would then be cloned to a folder inside the templates directory of papers_base, so that the directory structure would look akin to:
```
papers_base/templates/report
```

To create a paper utilizing this interface, the start of the MultiMarkdown paper would include the following two lines of metadata:
```
latex input: report/setup.tex
latex footer: report/footer.tex
```

which, if the `TEXINPUTS` environment variable is correctly defined as per the papers_base instructions, would create the paper by executing:
```
multimarkdown -t latex -o paper.tex paper.mmd
pdflatex paper.tex
```

as per normal LaTeX usage. The papers_base repository includes a script to create new papers from an example, which include a Makefile to execute these commands.
