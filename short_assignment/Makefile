TEX = xelatex -interaction nonstopmode
BIB = bibtex

PAPER = lab_report
BIBFILE = lab_bib.bib

TARGETS = $(PAPER).pdf view

all: $(TARGETS)

view:
	open $(PAPER).pdf

$(PAPER).pdf: $(PAPER).tex $(PAPER).bbl
	$(TEX) $(PAPER).tex
	$(TEX) $(PAPER).tex

$(PAPER).bbl: $(PAPER).tex $(BIBFILE)
	$(TEX) $(PAPER).tex
	$(BIB) $(PAPER).aux


.PHONY: clean all view

clean:
	rm -rf *.fls *.vrb *.fdb_latexmk *.aux *.log *.bbl *.blg *.xml *.bcf *.toc *.out *.lot *.lof $(PAPER).pdf
