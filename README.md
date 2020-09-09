# Hot Sauce Labels

This repository hosts the hot sauce labels and materials used
for bottling and sharing hot sauce.


## About

The materials hosted in this repository are LaTeX based.

The code is split in to two distinct versions:
1. Labels (Used for bottles)
2. Leaflet (Used for pamphlet/handout materials)


### Labels
The labels are hosted and managed via the `labels/` directory.

The main `labels/labels.tex` file defines the layout and formatting
for the printable label sheet. This can be modified to fit individual
makes/models of label sheets.
Using `pdfpages` package, it's possible to define a variety of labels
per sheet.

Other files included in this directory define the individual labels
and layout. For example, `labels/scorpionpom.tex` defines the individual
label formatting.


### Leaflet

The leaflet material is stored in the root of the repository.

This uses a custom `leaflet` class to define the layout and page formatting to
ensure that the printed material can be folded into threes.

## Making Labels and Leaflets

A simple `pdflatex $filename.tex` should build the individual materials.

**Note regarding the labels-**
For labels, the individual label materials need to be generated into PDFs
before the label sheet is created.
This is to say, the PDFs of the individual labels are dependant build artifacts
of the label sheet.

e.g.:
```sh
pdflatex scorpionpom.tex
pdflatex other-label.tex
pdflatex labels.tex
```
