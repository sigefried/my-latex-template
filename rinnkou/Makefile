TEX = platex -interaction nonstopmode
BIB = pbibtex
DVI = dvipdfmx

PAPER = dj_report
BIBFILE = dj_bib.bib

TARGETS = $(PAPER).pdf view

all: $(TARGETS)

view:

	okular $(PAPER).pdf


$(PAPER).pdf: $(PAPER).dvi
	$(DVI) $(PAPER).dvi


$(PAPER).dvi: $(PAPER).tex $(PAPER).bbl
	$(TEX) $(PAPER).tex
	$(TEX) $(PAPER).tex

$(PAPER).bbl: $(PAPER).tex $(BIBFILE)
	$(TEX) $(PAPER).tex
	$(BIB) $(PAPER).aux


.PHONY: clean all view

clean:
	rm -rf *.aux *.log *.bbl *.dvi *.blg *.xml *.bcf *.toc *.out *.lot *.lof $(PAPER).pdf
