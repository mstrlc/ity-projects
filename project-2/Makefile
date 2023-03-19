# @file Makefile
# @brief FIT VUT -- ITY -- project 2
# @author Matyas Strelec <xstrel03@stud.fit.vutbr.cz>
# @date 2023-02-22

PROJ=2
PROJNAME=proj$(PROJ)

.PHONY: all clean over

$(PROJNAME).pdf: $(PROJNAME).ps
	ps2pdf $(PROJNAME).ps

$(PROJNAME).ps: $(PROJNAME).dvi
	dvips -sPAPERSIZE=a4 $(PROJNAME).dvi

$(PROJNAME).dvi: $(PROJNAME).tex
	latex $(PROJNAME).tex
	latex $(PROJNAME).tex

all: $(PROJNAME).pdf

over: all
	pdftk vzor.pdf multibackground $(PROJNAME).pdf output overlay.pdf

clean:
	rm -f *.aux *.log *.dvi *.ps *.out $(PROJNAME).pdf 