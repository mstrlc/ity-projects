# @file Makefile
# @brief FIT VUT -- ITY -- project 4
# @author Matyas Strelec <xstrel03@stud.fit.vutbr.cz>
# @date 2023-02-28

PROJ=4
PROJNAME=proj$(PROJ)

.PHONY: all clean

$(PROJNAME).pdf: $(PROJNAME).ps
	ps2pdf $(PROJNAME).ps

$(PROJNAME).ps: $(PROJNAME).dvi
	dvips -sPAPERSIZE=a4 $(PROJNAME).dvi

$(PROJNAME).dvi: $(PROJNAME).tex
	latex $(PROJNAME).tex
	make bibtex
	latex $(PROJNAME).tex
	latex $(PROJNAME).tex

bibtex: $(PROJNAME).bib
	bibtex $(PROJNAME)

all: $(PROJNAME).pdf

clean:
	rm -f *.aux *.log *.dvi *.ps *.out *.blg *.bbl $(PROJNAME).pdf 