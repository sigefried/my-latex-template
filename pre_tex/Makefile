#
# Makefile
# sigefried, 2014-05-22 13:12
#

TARGET = my_presentation
TEX = pdflatex

all: $(TARGET).pdf

$(TARGET).pdf: $(TARGET).tex
	$(TEX) $(TARGET).tex
	$(TEX) $(TARGET).tex

.PHONY: clean all

clean:
	rm -rf *.fls *.vrb *.aux *.log *.out *.nav *.snm *.toc *.dvi *.pdf *.fdb_latexmk

# vim:ft=make

